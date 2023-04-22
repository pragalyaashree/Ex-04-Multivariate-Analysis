# Ex-04-Multivariate-Analysis
## AIM :
To perform Multivariate EDA on the given data set.

## EXPLANATION :
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM :
## STEP1:
Import the built libraries required to perform EDA and outlier removal.

## STEP2
Read the given csv file.

## STEP3
Convert the file into a dataframe and get information of the data.

## STEP4
Return the objects containing counts of unique values using (value_counts()).

## STEP5
Plot the counts in the form of Histogram or Bar Graph.

## STEP6
Use seaborn the bar graph comparison of data can be viewed.

## STEP7
Find the pairwise correlation of all columns in the dataframe.corr() .

## STEP8
Save the final data set into the file.

## PROGRAM:

Developed by : R.K PRAGALYAA SHREE

Register no : 212221040125
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

data=pd.read_csv("SuperStore.csv")
data

data.head()

data.info()

data.describe()

data.isnull().sum()

data.dtypes

sns.scatterplot(data['Postal Code'],data['Sales'])

states=data.loc[:,["State","Sales"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES")
plt.ylabel=("SALES") 
plt.show()

states=data.loc[:,["State","Postal Code"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Postal Code",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES") 
plt.ylabel=("Postal Code") 
plt.show()

states=data.loc[:,["Segment","Sales"]] 
states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(10,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("SEGMENT") 
plt.ylabel=("SALES") 
plt.show()

sns.barplot(data['Postal Code'],data['Ship Mode'],hue=data['Region'])

data.corr()

sns.heatmap(data.corr(),annot=True)
```
## OUTPUT :
## DATASET
![001](https://user-images.githubusercontent.com/128135934/233773562-b21a6899-9ce1-4a04-8bc7-f5b22679ffe9.png)

## HEAD DATA
![002](https://user-images.githubusercontent.com/128135934/233773621-c63258ba-0410-417a-ac5b-09b18699a25d.png)

## INFORMATION
![003](https://user-images.githubusercontent.com/128135934/233773644-8584a7ce-fede-4a58-94ce-1e50f963bc26.png)

## DESCRIPTION
![004](https://user-images.githubusercontent.com/128135934/233773671-982cfedd-c11d-40d1-a96f-4578ac29d189.png)

## DATATYPE
![005](https://user-images.githubusercontent.com/128135934/233773695-b5558113-56aa-439a-84d5-df5d7a2a4e04.png)

## NULL DATA
![006](https://user-images.githubusercontent.com/128135934/233773709-022968ab-90bd-4a57-8be9-3774a616649d.png)

## SCATTER PLOT
![007](https://user-images.githubusercontent.com/128135934/233773732-3995c2ca-22f3-4692-8da0-944cdabd5869.png)

## BAR PLOT - State and Sales
![008](https://user-images.githubusercontent.com/128135934/233773767-1aadbc55-2efd-400a-90aa-faa21c70620e.png)

## BAR PLOT - State and Postal code
![009](https://user-images.githubusercontent.com/128135934/233773818-7c1b8368-7c74-4dcf-aa84-165a58358885.png)

## BAR PLOT- Segment and Sales
![0010](https://user-images.githubusercontent.com/128135934/233773833-7e99656d-bfee-4e15-aacf-0c949acbfdd6.png)

## BAR PLOT - Postal code and Ship mode
![0011](https://user-images.githubusercontent.com/128135934/233773897-28d0c049-6e41-412d-99a3-8b38b59d6d28.png)

## CORRELATION COEFFICIENT
![0012](https://user-images.githubusercontent.com/128135934/233773965-a5e90fac-3a0b-4539-840c-73a5e1390199.png)

## HEATMAP
![0013](https://user-images.githubusercontent.com/128135934/233773990-ebc3a1fb-ebfe-42c8-8ea2-0cc5c2fc6a3c.png)

## RESULT:
Thus the program to perform Multivariate EDA on the given data set is successfully executed.




 
