# workshop-Multivariate-analysis
Aim:

To perform Multivariate EDA on the given data set.

##Explanation Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

Algorithm:


Step1:

Import the built libraries required to perform EDA and outlier removal.

Step2:

Read the given csv file.

Step3:

Convert the file into a dataframe and get information of the data.

Step4:

Return the objects containing counts of unique values using (value_counts()).

Step5:

Plot the counts in the form of Histogram or Bar Graph.

Step6:

Use seaborn the bar graph comparison of data can be viewed.

Step7:

Find the pairwise correlation of all columns in the dataframe.corr()

Step8:

Save the final data set into the file.

Types of bivariate analyis

1)Numerical & Numerical(Scatter plot)

2)Numerical & Categorical(Bar plot,Box plot,Dist plot)

Code

Developed by : Shakthi Kumar S

Registration Number : 212222110043

import pandas as pd

import seaborn as sns

df=pd.read_excel("/content/FlightInformation.xlsx")

printf(df)



df.info()


sns.scatterplot(x=df['Dep_Time'],y=df['Duration'])


sns.barplot(x=df['Duration'],y=df['Price'])


sns.barplot(x=df['Dep_Time'],y=df['Price'])


import matplotlib.pyplot as pl

states=df.loc[:,["Duration","Price]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

sns.barplot(x=states.index,y="Price",data=states)

pl.xticks(rotation=90)

pl.xlabel=("Duration")

pl.ylabel=("Price")

pl.show()


df.corr()

import numpy as np

data=np.random.randint(low=5,high=110,size=(10,10))

print("The datas to be plotted:\n")

print(data)

h=sns.heatmap(data=data)

pl.show




Output:

Data set

![WORK-1](https://user-images.githubusercontent.com/120207509/229767732-f76f2cef-e354-4455-8088-92129480ad8f.png)


Data Information

![WORK-2](https://user-images.githubusercontent.com/120207509/229767811-136df2f3-3025-4172-bc9d-c1bd8de34696.png)

Numerical & Numerical (Scatter Plot)

![WORK-3](https://user-images.githubusercontent.com/120207509/229767842-dcf28652-3aba-4878-b710-a07e3b677162.png)


Numerical & Categorical (Bar Plot)

![WORK-4](https://user-images.githubusercontent.com/120207509/229767944-d4ef2918-fcbe-470e-8676-d4ef56045823.png)
![WORK-5](https://user-images.githubusercontent.com/120207509/229769441-63095475-3532-4e48-8f91-f17a177b7d05.png)
![WORK-6](https://user-images.githubusercontent.com/120207509/229769014-3a79b05b-6cdd-4410-b571-3a3d20f38842.png)

Non-Graphical method(correlation)

![WORK-7](https://user-images.githubusercontent.com/120207509/229769069-104381cd-d529-4b88-ac4c-5b3e6219547d.png)


Result:

Thus we have performed Multivariate EDA on the given data set.
