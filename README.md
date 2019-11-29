# Fundamentals-of-Data-Analysis_Assessment-2019

__Name:__ Martina Crkonova<br/>
__Instructions:__ The assesment concerns the Tips dataset and the Python packages seaborn and jupyter.<br/>
__Date:__ November 2019

### About the dataset

Food servers’ tips in restaurants may be influenced by many factors, including the nature of the restaurant, size of the party, and table locations in the restaurant. Restaurant managers need to know which factors matter when they assign tables to food servers. For the sake of staff morale, they usually want to avoid either the substance or the appearance of unfair treatment of the servers, for whom tips (at least in restaurants in the United States) are a major component of pay. In one restaurant, a food server recorded the following data on all cus- tomers they served during an interval of two and a half months in early 1990. The restaurant, located in a suburban shopping mall, was part of a national chain and served a varied menu. In observance of local law, the restaurant offered to seat in a non-smoking section to patrons who requested it. Each record includes a day and time, and taken together, they show the server’s work schedule.

* source: https://www.kaggle.com/ranjeetjain3/seaborn-tips-dataset


The analysis is divided into 3 sections:
* Descriptive analysis of the dataset
* Regression analysis 
* Detailed analysis of selected variable



### Used libraries and applications:
* NumPy
>a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. 
* Seaborn
>Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
* Jupyter notebook 
>an open-source web application that allows to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more.

* source:<br/>
>https://jupyter.org/ <br/>
>https://seaborn.pydata.org/<br/>
>https://en.wikipedia.org/wiki/NumPy<br/>

### 1, Descriptive analysis of the dataset

The dataset is converted to dataframe using Pandas.The quick revision if all data are loaded and check on the last couple of rows of the dataframe. The function describe() used to summarise and provide the calculations of basics statistical calculations. For visualisation of the dataframe the Pairplot and Histograms are used.

The basic overview of each variable in the dataframe completed as per below:

#### Variable "Sex"

The pairplot used to visualise relationship between variables and distribution of data, distinguished by the Female and Mlae subcategory.Pivot tables used in order to provide different angles on the data, split by differnet subcategories. 

#### Variable "Day"

The pairplot used to get first visuale understanding of the relationships of variables and distribution of data , split by days. The boxplot is used to get a good indication of how the values in the data are spread out. The pivot tables is providing the information on mean, minimum , maximum ,median and standard deviation displayed by days .

#### Variable "Smoker"

The same approach used, the pairplot used to ilustrate the relationship between variables size, tip and total bill split by if in the group was a smoker or not. Two sub-datasets prepared to illustrate the data for group with and without the smoker. Pivot table used to display different calculations. The Boxplot for each of the sub-group prepared.

#### Variable "Time"

The scatter plots used to display the relationships on the two variables , split by dinner and lunch in the specific day. 


#### Variable "Size"

The size variable is measuring the size of the group paying for the served food. Again, pivot tables are used to look on the data from different perspective.


### 2, Regression analysis 

Regression analysis is a statistical method that allows to examine the relationship between two or more variables of interest.In this analysis the relationship between total bill paid and tips is investigated. I assumed that the tip is dependent variable and total bill is independent (or predictor) variable.<br/>
<br/>
Scatter plot ilustrate the relationship between the paid bill and tips.<br/>
<br/>
The Pearson's correlation is used to evaluate how strong two variables are related.<br/>
<br/>
Linear regression analysis is used to to understand the association between one independent variable (total bill) and one continuous dependent (tip) variable. The best values for slope and y intercept.They are mathematically calculated  and also obtained from using the np.polyfit function.

### 3, Detailed analysis of selected variable "Sex"

The selected variable sex is investigated from different perspectives-by variable time, day, size and smoker. The dataframe is splitted into two datasets-Female and Males. Pivot tables and various plotes are used to ilustrate the analysis. In the last section is the linear regression analysis used to calculate the best fit model for Female and Males variables total bill and tips.




### Definitions:

#### Difference between mean and median

* source: https://statistics.laerd.com/statistical-guides/measures-central-tendency-mean-mode-median.php

The mean is equal to the sum of all the values in the data set divided by the number of values in the data set.<br/>
The median is the middle score for a set of data that has been arranged in order of magnitude. The median is less affected by outliers and skewed data.

#### Standard deviation

* source: https://en.wikipedia.org/wiki/Standard_deviation

In statistics, the standard deviation is a measure of the amount of variation or dispersion of a set of values. A low standard deviation indicates that the values tend to be close to the mean (also called the expected value) of the set, while a high standard deviation indicates that the values are spread out over a wider range

#### Corelation and Covariance

* source: https://towardsdatascience.com/let-us-understand-the-correlation-matrix-and-covariance-matrix-d42e6b643c22

“Covariance” indicates the direction of the linear relationship between variables. “Correlation” on the other hand measures both the strength and direction of the linear relationship between two variables. Correlation is a function of the covariance. What sets them apart is the fact that correlation values are standardized whereas, covariance values are not. 


#### Regression analysis

* source:
>https://en.wikipedia.org/wiki/Regression_analysis<br/>
>https://www.statisticshowto.datasciencecentral.com/probability-and-statistics/regression-analysis/

Regression analysis is a statistical method that allows to examine the relationship between two or more varaibles of interest. While there are many types of regression analysis, at their core they all examine the influence of one or more independent variables on a dependent variable. 

#### Boxplot

* source:
>https://support.minitab.com/en-us/minitab-express/1/help-and-how-to/graphs/boxplot/interpret-the-results/key-results/
>https://www.wellbeingatschool.org.nz/information-sheet/understanding-and-interpreting-box-plots
>https://towardsdatascience.com/analyze-the-data-through-data-visualization-using-seaborn-255e1cd3948e

Boxplots are a standardized way of displaying the distribution of data based on a five number summary (“minimum”, first quartile (Q1), median, third quartile (Q3), and “maximum”).<br/>
>median (Q2/50th Percentile): the middle value of the dataset.<br/>
>first quartile (Q1/25th Percentile): the middle number between the smallest number (not the “minimum”) and the median of the dataset.<br/>
>third quartile (Q3/75th Percentile): the middle value between the median and the highest value (not the “maximum”) of the dataset.<br/>
>interquartile range (IQR): 25th to the 75th percentile.<br/>
>whiskers (shown in blue)<br/>
>outliers (shown as green circles)<br/>
>“maximum”: Q3 + 1.5*IQR<br/>
>“minimum”: Q1 -1.5*IQR<br/>

![Boxplot](https://user-images.githubusercontent.com/47481671/69892800-4f076080-1301-11ea-8e8d-02a45a4f39ad.PNG)

#### Histogram

* source:
>https://www.ck12.org/book/CK-12-Probability-and-Statistics-Concepts/section/4.6/<br/>
>https://datavizcatalogue.com/methods/histogram.html

A Histogram visualises the distribution of data over a continuous interval or certain time period. Each bar in a histogram represents the tabulated frequency at each interval/bin.

Histograms help give an estimate as to where values are concentrated, what the extremes are and whether there are any gaps or unusual values. They are also useful for giving a rough view of the probability distribution.
