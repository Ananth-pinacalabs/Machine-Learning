<h1>Naive bayes</h1>

<a href = "https://www.youtube.com/watch?v=O2L2Uv9pdDA" > StatQuest Naive Bayes, Clearly Explained!!!</a>

Imagine you are building a spam filter to classify the mails  in your inbox. 
you have the a bunch of conditional probabilities of the  occurernce of words given that the mail is spam or not. This forms you knowledge base. 

You create the conditional probabilities by creating word histograms.

![image histogram](images/word_histograms.png)

![calculating likelihoods](images/calculating-likelihoods.png)

similarly  you do the same for the spam messages.


Normal message

p(Dear | Normal message )    = 0.47

p(Friend | Normal message )  = 0.29

p(Lunch | Normal message )   = 0.18

p(Money | Normal message )   = 0.06

Spam message

p(Dear | spam message )    = 0.29

p(Friend | spam  message )  = 0.14

p(Lunch | spam message )   = 0.00

p(Money | soam message )   = 0.57



since they represent individual words they are known as likelihoods not probability

We also take an initial estimate of the probabuility of message being a normal message. This inital guess is the prior probability. 

P(Normal message) =                4
   `(prior probability)`    _________________    =  0.5
                               4   +    4                   




to find the probability of dear friend occuring in a normal message you would


probability of
`Dear Friend`      
occuring in
Normal message.     =  P(Normal message) x P(Dear | N) x P(Friend | N)

                    =  0.5 x 0.47 x 0.29
                    
                    = 0.09


probability of
`Dear Friend`      
occuring in
Spam message.     =  P(Spam message) x P(Dear | S) x P(Friend | S)

                    =  0.33 x 0.29 x 0.14
                    
                    = 0.01


0.09 is the score the message  `Dear Friend` gets given that it is Normal. 
The actual probability that the message is Normal is propotional to 0.09. 

Similarly, the probability that the message `Dear Friend` is Spam is  propotional to 0.01

Therefore we assign that the message  is  `Not spam`. 


<h2>problem with naive bayes</h2>

if we were to find the probability of message `lunch money money money money` to be spam or not


you would find that the 

P(lunch money money money money | Normal)   = 0.18 x 0.06 ^ 4  = 0.00002

P(lunch money money money money | Spam)     = 0.00 x 0.57 ^ 4  = 0.0 


Here, P(lunch money money money money | Normal) > P(lunch money money money money | Spam), which is wrong. 


Just because the  P(lunch | spam ) is 0  the entire score becomes 0.
To avoid this pseaudo counts are added to all each word in histogram such that the conditional probability  any word is never 0. 

![pseudo counts text](images/pseudo-counts.png)

here we set the alpha to be 1.

This does  not change our initial guess of P(Normal message) which still remains to be. This does'nt change the number of messages in the inbox. 

Also we need to re-calculate the likelihoods of all the words and the prior probability of the message being spam or not.


![recalculating the probabilies for lunch money money money](images/recalculating-probabilities.png)


Now you can note that the problem is fixed. 




<h2>Why is naive bayes naive?</h2>

The naive bayes disregards the ordering in words and would treat the words as simple bag of words. It does'nt consider the relation between the words or their meaning. 

The naive bayes would give the same score for both 
            `Dear Friend`  and `Friend Dear` 


This still does a great job at spam filtering never the less as it is very difficult to capture all the different word sequences and ordering . 

