# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

## Data Cleaning

```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS (1).csv")
df
```
![Screenshot 2025-04-17 093217](https://github.com/user-attachments/assets/7de83fb3-eb99-4e49-b9d9-367f96e41e32)
![Screenshot 2025-04-17 093228](https://github.com/user-attachments/assets/b29a5fc7-0ed4-4f39-92f9-b61d9a06e510)
```
df.shape
```
![Screenshot 2025-04-17 093330](https://github.com/user-attachments/assets/26c645a7-4021-4d2d-b2b0-21a64c074d62)
```
df.isnull()
```
![Screenshot 2025-04-17 093407](https://github.com/user-attachments/assets/1d7e33cb-0c24-4355-8fad-2f1aa89e280d)
![Screenshot 2025-04-17 093414](https://github.com/user-attachments/assets/ff7910ca-0654-4381-a5ca-bfd0a439f2c4)
```
df.isnull().sum()
```
![Screenshot 2025-04-17 093454](https://github.com/user-attachments/assets/9457dae8-efcd-4366-8eb4-709b0ae3eeca)
```
import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
```
![Screenshot 2025-04-17 093530](https://github.com/user-attachments/assets/9c2886a6-6933-40fd-8098-4b8fca4e8054)
```
df.dropna(how='any').shape
```
![Screenshot 2025-04-17 093604](https://github.com/user-attachments/assets/0aa94015-071b-469c-a872-66bc20cd6ab8)
```
df.fillna(method='ffill')
```
![Screenshot 2025-04-17 093737](https://github.com/user-attachments/assets/f5cac4de-c6c0-4077-81b7-4608bed1cd03)
```
df.fillna(method='bfill')
```
![Screenshot 2025-04-17 094451](https://github.com/user-attachments/assets/ce92baa1-aafd-4651-905c-788a8bd084d2)
```
  mean=df.TOTAL.mean()
  mean
```
![Screenshot 2025-04-17 094518](https://github.com/user-attachments/assets/c33d8288-bc27-4b9c-9846-38d87b3af4e5)
```
df['DOB']=pd.to_datetime(df['DOB'], format='mixed', errors='coerce')
df['DOB']
```
![Screenshot 2025-04-17 094553](https://github.com/user-attachments/assets/76e96adf-647c-490f-9db7-d692cce86d8f)
```
df.dropna(inplace=True)
df
```
![Screenshot 2025-04-17 094612](https://github.com/user-attachments/assets/d4c6be21-8cbd-4449-8fd4-811ee479d53b)
```
sns.heatmap(df.isnull(), yticklabels=False, annot=True)
```
![Screenshot 2025-04-17 094656](https://github.com/user-attachments/assets/81b626fe-f702-477d-aabf-f5af7ca06930)


## Oulier Detection & Removal

# Result
          <<include your Result here>>
