# Ex:05 Feature Generation

## AIM:

To read the given data and perform Feature Generation process and save the data to a file.

## Explanation:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM:

## STEP 1:
Read the given Data

## STEP 2:
Clean the Data Set using Data Cleaning Process

## STEP 3:
Apply Feature Generation techniques to all the feature of the data set

## STEP 4:
Save the data to the file

## PROGRAM:
```
Developed by : PAVITHRA R
Register Number: 212222230106
```
## DATA.CSV
```
import pandas as pd
df1 = pd.read_csv("/content/data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1


```
## ENCODING.CSV
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df

```
## BMI.CSV:
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2

```


## OUTPUT:
## DATA.CSV:

## INITIAL DATA:

![data 1](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/ea7e987e-998e-44bd-a255-2888ac3aa692)


## HEAD:

![data 2](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/c2798eb2-dab7-4f0b-b3f3-c854099f6fb9)



## UNQIUE:

![data 3](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/37e02693-37f6-4037-a9ed-271cf03e6269)


## ORDINAL ENCODER:

![data 4](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/18516b1f-72df-4f02-8e17-ac2857cbb343)


![data 5](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/8e112d10-f7cf-409c-82f9-4fe2ed8b27c5)


## LABEL ENCODER:

![data 6](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/dac22896-d68d-4bba-849c-9cd36b901dbb)


## BINARY ENCODER:

![data 7](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/56a53fbc-d356-45fa-bb14-4353ac6d754c)

![data 8](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/3a6afbdb-b32a-46bd-8099-d8fc1c25990f)


## ENCODING DATA:

## INITIAL DATA:

![encoding 1](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/fadd064c-1f64-4b2e-8bb4-f6b27ecf364c)


## HEAD:

![encoding 2](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/32fb9fdc-575c-474d-8bc4-bad7b06acc70)


## ORIGINAL ENCODER:
![encoding 3](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/28305cf7-2ea7-4741-8f26-ca63104cd0ac)



## LABEL ENCODER:

![encoding 4](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/8bb5e0cd-a910-4b26-b376-a4614005cef1)



## BINARY ENCODER:


![encoding 5](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/5e51e214-40cf-4d67-82c8-86c969464053)


![encoding 6](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/6544be72-2350-434a-9f31-221fab4d2bd8)


## BMI.CSV:


## INITIAL DATA:

![bsmi 1](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/3c40b958-2a82-46f8-8da1-8582ac8ac189)



## HEAD:


![bsmi 2](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/5887f506-a4e4-458f-8d9e-546c2e7aa841)



## BINARY ENCODER:

![bsmi 3](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/4c89ac1d-7cdc-4185-b2d7-0c5069147653)


![bsmi 5](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-05/assets/118596964/e2767911-8cea-4e37-b348-d8b260a28d9a)


## RESULT:
 Thus the program has been executed successfully.


