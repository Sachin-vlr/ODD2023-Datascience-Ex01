# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 

# Loan Data csv
```python
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# DATA SET CSV

```python
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```

# OUTPUT

#DATA

```python
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```

![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/d91190d7-6d3b-4030-9366-565b2f5c89f8)

# NON NULL BEFORE

```python
df.info()
```
![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/fb3cc145-326d-4b02-80b7-9f9abc7b4def)

#MODE

```python
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/f13e602f-5d24-41f1-8916-e4e04819c56a)

# MEAN

```python
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```

![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/9bcb2046-f550-4b64-8afd-456489d6057b)

# MEDIAN

```python
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```

![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/1ffb0c4c-64cc-4858-a01b-c6cb5d99d978)

# NON NULL AFTER

```python
df.info()
```

![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/d8745d3f-9c53-44d6-92fa-d3824a99dddc)

```python
df.isnull().sum()
```

![image](https://github.com/Sachin-vlr/ODD2023-Datascience-Ex01/assets/113497666/ceee5f3e-4769-41d8-8632-b0e70453e186)

# FOR DATASET

# DATA

```python
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
```
![Uploading image.png…]()

![Uploading image.png…]()
