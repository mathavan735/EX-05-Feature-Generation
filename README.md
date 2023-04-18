### EX-05-Feature-Generation

## AIM

To read the given data and perform Feature Generation process and save the data to a file. 

### Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

### ALGORITHM

### STEP 1

Read the given Data

### STEP 2

Clean the Data Set using Data Cleaning Process

### STEP 3

Apply Feature Generation techniques to all the feature of the data set

### STEP 4

Save the data to the file

### CODE

NAME:S.MATHAVAN

REGISTER NUMBER:212221220031
```
import pandas as pd

df=pd.read_csv("/content/data[1].csv")

df.info()

df.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['Ord_2'] = le.fit_transform(df['Ord_2'])

sns.set(style ="darkgrid")

sns.countplot(df['Ord_2'])

from sklearn.preprocessing import OneHotEncoder

enc = OneHotEncoder()

enc = enc.fit_transform(df[['City']]).toarray()

encoded_colm = pd.DataFrame(enc)

df = pd.concat([df, encoded_colm], axis=1)

df = df.drop(['City'], axis=1)

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2'])

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1'])

df.head(10)
```

### OUPUT

![image](https://user-images.githubusercontent.com/120443233/231797352-0458f8b9-8635-477c-8107-37e8f6641471.png)

![image](https://user-images.githubusercontent.com/120443233/231797390-c9338fdd-f0a6-435f-9d43-929a0cd42c5c.png)

![image](https://user-images.githubusercontent.com/120443233/231797434-2dc5bfad-f851-45bf-bf72-33704a3c4ea6.png)

![image](https://user-images.githubusercontent.com/120443233/231797652-d8180e61-3b89-4172-85a6-e0d5e3c508f7.png)

![image](https://user-images.githubusercontent.com/120443233/231797707-99d6f365-7366-4555-b052-c99db36be69b.png)

### encoding dataset

![image](https://user-images.githubusercontent.com/120443233/231799161-eba55c94-a495-48ed-8cb8-20c1f61db775.png)

![image](https://user-images.githubusercontent.com/120443233/231799510-58b3611d-737f-45a2-9e02-d2bd57ea10b1.png)

![image](https://user-images.githubusercontent.com/120443233/231799571-6a53d605-6ea0-4de2-9138-9ab74aff9ccb.png)

![image](https://user-images.githubusercontent.com/120443233/231799604-7d120697-b37e-4a52-bd2e-c4f29e891b2c.png)

![image](https://user-images.githubusercontent.com/120443233/231799699-e32d6086-e65c-4b2c-a4ec-a7370024bd4e.png)

![image](https://user-images.githubusercontent.com/120443233/231799775-d1b8a731-4d5c-4d9f-88d4-a11bfaa63dd8.png)

![image](https://user-images.githubusercontent.com/120443233/231800205-6871a63a-1fa9-497b-b24a-b3c6d3c0bc27.png)

![image](https://user-images.githubusercontent.com/120443233/231800254-3ecff74e-2bc6-40de-a007-7f45477f41b5.png)

![image](https://user-images.githubusercontent.com/120443233/231800299-23ab9cfc-ae7f-4c65-9d82-48293ba6b2fb.png)

![image](https://user-images.githubusercontent.com/120443233/231800377-bcb30824-d8e4-4b96-a73f-bfcabc11e1b2.png)

![image](https://user-images.githubusercontent.com/120443233/231800435-98c28e09-353d-4ccf-9798-433bce06b95e.png)

### RESULT:

Hence Feature Generation process and Feature Scaling process is applied to the given data frames sucessfully.


