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


# Outlier Detection and Removal 
## Coding and Output
```Python
import pandas as pd
import seaborn as sns
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
dff=pd.DataFrame(age)
dff
```
              
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/28a59ebe-bdcc-4f04-93be-c29c353cdcb0)

### 15) Boxplot
```Python
dsf=sns.boxplot(dff)
```
     
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/9876bce8-ef7f-49b2-8a97-114162113c71)


### 16) Scatterplot
```Python
dsf=sns.scatterplot(dff)
```
   
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/8144b619-8a24-44fd-a670-d317c88e81f9)



### 17) IQR
```Python
q1=dff.quantile(0.25)
q2=dff.quantile(0.5)
q3=dff.quantile(0.75)
iqr=q3-q1
iqr
```

              
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/5ce6b72c-20d6-4542-a6ef-f607de82fc3d)

    
### 18) Checking the high and low value
```Python
low=q1-1.5*iqr
low
high=q3+1.5*iqr
high
```

              
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/23185839-8632-43ee-bd1c-33da6ec53f9c)

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/aef8585c-4c27-4d68-a0cb-653026339b45)


    
### 19) Filtering outlier value
```Python
dff=dff[((dff>=low)&(dff<=high))]
dff
```
     
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/a350867b-a6c0-4d3a-94fa-7e13b6874499)

    
### 20) Dropping the null value
```Python
dff.dropna()
```

              
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/e89a47bf-418b-4d60-9c75-f4e150bde470)


    
### 21) Box plotting after filtering outlier
```Python
sns.boxplot(data=dff)
```
     
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/b26c5fa9-3286-4299-a3e0-462659b72e6d)

  
### 22) Z Score
```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
data={'weight':[12,15,18,21, 24, 27, 30, 33, 36, 39, 42, 45, 48, 51, 54, 57,60,63,66,69,202,72, 75, 78, 81, 84, 232, 87, 90, 93,96,99,258]}
ds=pd.DataFrame(data)
ds
```
 
#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/c81cd121-42a2-4608-892b-33755423d018)

### 23) Z Score
```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
data={'weight':[12,15,18,21, 24, 27, 30, 33, 36, 39, 42, 45, 48, 51, 54, 57,60,63,66,69,202,72, 75, 78, 81, 84, 232, 87, 90, 93,96,99,258]}
ds=pd.DataFrame(data)
ds
```

#### OUTPUT:

![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/c81cd121-42a2-4608-892b-33755423d018)

    
### 24) Z Score
```Python
sns.boxplot(data=ds)
```

              
#### OUTPUT:
![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/a1afb418-e531-4eaa-9f0f-db5be7b0c20c)

    
 ### 25) Z Score
```Python
z=np.abs(stats.zscore(ds))
z
```
   
#### OUTPUT:
![image](https://github.com/LATHIKESHWARAN/exno1/assets/119393556/f52c84e7-00eb-4c8e-b5a7-653ea094ed1f)





# Result
The data cleaning has beeen done successfully.
