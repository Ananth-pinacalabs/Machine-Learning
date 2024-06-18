<h1 align = "center">Descriptive Statistics</h1>


<p  align = "center"> A field of statistics that deals with  organising, describing and presenting the data, without making any inferences/ prediction about the data.</p>

  *Deals with finding some sample parameters: refered to as sample `statistics`, that best describes the data*
<h3 align = "center">Measures of central tendency</h3>

The following are some measures that descibe the center of the data/ points around which the data is centered.


###  **Mean** - 
The average of all the values.Found by  diving the sum of all the values in the data the number of ovbservations. 


*formula for finding mean -*

$$

\text{Mean} = \frac{\text{Sum of all the observations in the data}}{\text{Count of observations in the data}}

$$
<br>
<br>

$$
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
\
$$



#### **Pros & cons** - 
*  This is very easy to interpret and in the same units as the data. 
*  This heavily affected by  outliers, in which case it  will not be representing the centrality of the data. 


You need to mindful wether you are finding the mean for population or a sample. They may be very different in many scinarios. 

**population mean -**
$$\
\bar{X} = \frac{1}{N} \sum_{i=1}^{N} x_i
\
$$

**sample mean-**

$$\
\mu = \frac{1}{N} \sum_{i=1}^{N} x_i
\
$$


### **Median-**
The `middle most value` when you sort all the values in a acsending order. This is unaffected by outliers. *More reliable representation of the cemtrality of data than mean.*

### **Mode** - 
The most frequent value in the  dataset. This is more commonly used for `discrete` variables or `categorical` variables.

*Does not make sence when it comes to continuous variables.*


### **Weighted Mean** - Each data observation is multiplied by  before computing the mean. 

$$\
\text{Weighted mean} = \frac{1}{N} \sum_{i=1}^{N} x_i * w_i
\
$$



<h2><b>Measure of dispersion</b></h2>

A statistical measure that represent the spred / variability off the dataset. 

To tell how the data is distributed around the central tendency of the dataset. 

### **Range** -
The difference between the max and min value in the data. *This is heavily affected by outliers* 

$$
 \text{range} = x_{max} - x_{min} 
$$


### **Varience**
The average squared difference between each  data point and mean of the observation.*This is prone to outliers.*

**Population varience**

$$
\sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2
$$
<br>
<br>

**Sample varience**

$$
s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$
<br>
<br>


One downside is that this is in squared units.

### **Mean Absolute Difference**


### **Standard Deviation**
This brings gives the squred root of varience. It present the measure of spread in the same units as the data point. 


**Population Standard Deviation**
$$
\sigma = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2}
$$
<br>
<br>
**Sample Standard Deviation**
<br>

$$
s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2}
$$

<br>
<br>

### **Coeffecient of  Varience**
It is difficult to compare the standard deviations of two different variables as they  might be in different units.


example you can not compare the std of say the salary and years of experience. 


$$
 \text{cv} = \frac{\text{standard deviation}} {\text{mean}} * 100 
$$


This is a unit less value that is represented as a percentage, that tells  you close the  std is to your mean.

 















