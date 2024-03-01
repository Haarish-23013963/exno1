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

```py
# Developed By: Haarish V
# Register Number: 212223230067
```
<table>
  <tr>
    <td width=50%>


### 1) Read and display DataFrame
```Python
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
df
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 160851](https://github.com/Haarish-23013963/exno1/assets/147139700/ed6fdc23-4327-4401-9c65-1dbff58d6066
)
</td>
</tr>
<tr>
  <td width=50%>
              
### 2) Display head
```Python
df.head()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161039](https://github.com/Haarish-23013963/exno1/assets/147139700/08999790-3655-4ba3-8ecd-997da71d7f56)

</td>
</tr>
<tr>
  <td width=50%>

### 3) Display tail
```Python
df.tail()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161129](https://github.com/Haarish-23013963/exno1/assets/147139700/eb2150b3-8d47-482c-9f9d-0a4bc1b563a9)

</td>
</tr>
<tr>
  <td width=50%>

### 4) Info of datafram
```Python
df.info()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161213](https://github.com/Haarish-23013963/exno1/assets/147139700/0f350c7d-31e8-4bb8-9a8e-1956c61f3db1)

</td>
</tr>
<tr>
  <td width=50%>

### 5) Describe about the dataframe
```Python
df.describe()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161243](https://github.com/Haarish-23013963/exno1/assets/147139700/53141d5a-9a06-42ee-aa18-786406346d85)

</td>
</tr>
<tr>
  <td width=50%>

### 6) Shape of the datafram
```Python
df.shape
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161318](https://github.com/Haarish-23013963/exno1/assets/147139700/c62a35d3-0873-4b03-8981-8c5301d18f3b)

</td>
</tr>
<tr>
  <td width=50%>

### 7) Checking tha NUll values
```Python
df.isnull()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161403](https://github.com/Haarish-23013963/exno1/assets/147139700/c0ef159f-832d-460e-a8cb-57dc20c02f07)

</td>
</tr>
<tr>
  <td width=50%>

### 8) Drop the Null values
```Python
df.dropna(axis=0)
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161436](https://github.com/Haarish-23013963/exno1/assets/147139700/61b3d133-a7dc-4247-b3af-cdd8e98df867)

</td>
</tr>
<tr>
  <td width=50%>



### 9) Fill the Null values
```Python
df.fillna(0)
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-23 161539](https://github.com/Haarish-23013963/exno1/assets/147139700/8353f3c6-686a-485d-8316-71c2d645db72)

</td>
</tr>
<tr>
  <td width=50%>



# Result
The data cleaning has beeen done successfully.
