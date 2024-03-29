# Amazon-sales-Report.
![](Salesandmarketing.jpg)

---

### INTRODUCTION.
In today's dynamic business landscape, understanding and leveraging sales data has become more critical than ever. A comprehensive sales analysis provides invaluable insights into consumer behavior, market trends, and the performance of your products or services. By delving deep into the wealth of information hidden within your sales data, you can unlock the key to optimizing your strategies, enhancing profitability, and achieving sustainable growth. In this report, we will embark on a journey to unravel the mysteries behind your sales figures, empowering you to make informed decisions that will propel your business forward. So, fasten your seatbelts as we embark on this exciting exploration into the realm of sales analysis!
stay tuned :😉

---
---

### PROBLEM STATEMENT.
A forensic detailed analysis was carried out on a company in Asia Continent, this company needed to build an headquarter in one of the countries big cities, My team and I Were entrusted with the task of predicting the best location(i.e city) for the headquarter. 

After critical thoughts, some questions needed an answer:
 - Where is The best Location to build an Headquarters?
 - What are the most bought Size?
 - Which city or cities should we invest in more?
 - How do we encourage sales generally?

---

### DATA SOURCES.
Data were extracted from the excel work sheet into the Jupyter note using the Python's pandas library.
Data was normalised; that is,the information were categorically separated into different colums.


---

### DATA CLEANING AND TRANSFORMATION
Data in its pure state is "Dirty", Data is not just a paramount aspect of data analysis but the bedrock upon which Great Results are built. The basic data cleaning process involves Remove Duplicates, Handling missing values,outlier detection and handling,data type conversion and normalisation standardisation. Data cleaning was performed per column. The Data set appeared to be clean. The quality of each column is 100% with no error or nulls. Below is a preview of the data set before and after the data cleaning opreations. These were done to ensure Data consistency and Data integrity.


Dirty Data sets|Clean Data Sets 
:---------------|---------------:
![](dirtydataset.png)|![](cleandataset.png)

---

### PYTHON CODES.
Python scripts were written as the needs arises to efficiently and effectively model the data set.

---


~~~python

# import neccessary libraries
import pandas as pd
import seaborn as sns 
import matplotlib.pyplot as plt
%matplotlib inline
import numpy as np

# load the csv file
df = pd.read_csv('Amazon Sale Report.csv', encoding='unicode_escape')

# check key informations about your data
df.shape
df.info()
df.head()
df.shape()

#check for missing values and drop if there is any
#NB: If you must drop Nan, use df.dropna(How='all')

#check for duplicates
df.duplicated()
#if any duplicates
df.drop_duplicates()

df.isna().sum()
df.dropna(inplace=True)

# drop empty columns
df.drop(['New','PendingS'],axis =1, inplace= True)

# convert dtypes to their appropiate dtypes
df['ship-postal-code'] = df['ship-postal-code'].astype(int)

# convert the date column to the date format
df['Date'] = pd.to_datetime(df['Date'])

~~~

### DATA ANALYSIS AND VISUALISATION.

Analysis were done using different analytical skills while Exploratory Data and Visualisation were carried with the Python's Seaborn and matplotlib libraries respectively.

---

      



![](amazonsales.png)

---
![](amazonshippingstatus.png)

---


![](top10Statewiththehighestsales.png)|![](pie.png)
:-------------------------------------|------------:

### CONCLUSION AND RECOMMENDATIONS.
 - The city of **MAHARASHTRA** is the best location to build the office Headquarters.
 - Varieties of **Colors** and  **Designs** on the **M**,  **L** and **XL** Sizes should be produce as these are the most sold out Sizes.
 - Discount/ Sales should be done on **M**, **L** and **XL** sizes respectively to encourage sales.
 - The cities of **MAHARASHTRA** And **KARNATAKA** should be consider first in terms of **New products** and **Discounts** as these are the  cities with the highest sales record.
 - Free shipping should be given to the cities with low shippment to encourage them to buy more.

---   


###### My goal is to provide value to the stakeholders and not just to build reports and dashboard.

# Thank You 🥰


