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
import pandas as pd
df=pd.read_csv('/content/Data_set (5).csv')
<img width="1854" height="552" alt="image" src="https://github.com/user-attachments/assets/cc75f525-d7f0-4ed3-9db3-fad224e120c2" />
df.describe()
<img width="1856" height="451" alt="image" src="https://github.com/user-attachments/assets/038498ff-a50e-41dc-a623-2d05c90c7b9d" />
df.head(16)
<img width="1842" height="653" alt="image" src="https://github.com/user-attachments/assets/44a93454-c172-472c-bd55-6c89bb09eca7" />
df.tail(5)
<img width="1649" height="352" alt="image" src="https://github.com/user-attachments/assets/d5ff3e87-4901-47a1-95e4-e9b400ed9c5c" />
df.shape
<img width="1854" height="132" alt="image" src="https://github.com/user-attachments/assets/379309f9-dfd3-4483-9fd2-9d6a59b6e408" />
df.isnull()
<img width="1509" height="576" alt="image" src="https://github.com/user-attachments/assets/7a68172a-64dc-499b-a055-d159de6400dd" />
df.notnull()
<img width="1548" height="560" alt="image" src="https://github.com/user-attachments/assets/9fed736f-5df0-47f5-8e99-f9ecab947348" />
df.isnull().sum() /len(df)*100
<img width="1436" height="515" alt="image" src="https://github.com/user-attachments/assets/7d71a9bc-fdd1-4d26-8d17-a8cc3e702f0b" />
df.dropna(axis=0)
<img width="1698" height="594" alt="image" src="https://github.com/user-attachments/assets/4273bddb-701f-4e44-bd67-98dcae90d102" />
df.dropna(axis=1)
<img width="1807" height="569" alt="image" src="https://github.com/user-attachments/assets/9a719bb2-8d44-46fb-9bf7-8d547d52e6bd" />
dfs=df[df['current_overall_rank']>50]
dfs
<img width="1727" height="646" alt="image" src="https://github.com/user-attachments/assets/d7184c10-126f-461b-89df-1e5afb24c6a4" />
df.fillna(0)
df
<img width="1706" height="614" alt="image" src="https://github.com/user-attachments/assets/34d91bf3-efc1-4b17-a899-3db79a45e1ac" />
dfs=df[df['show_name'].astype('str').str.upper().str.startswith('A','B')]
dfs
<img width="1749" height="396" alt="image" src="https://github.com/user-attachments/assets/6422743f-a3e7-47e1-b38a-3cf2961089e1" />
df.iloc[:4]
<img width="1672" height="297" alt="image" src="https://github.com/user-attachments/assets/8be51326-2260-412e-a142-e1cc589bb6e6" />
df.iloc[[1,3,5],[1,3,5]]
<img width="1467" height="221" alt="image" src="https://github.com/user-attachments/assets/047850d1-9bed-4e5c-871f-54b59d3f18b4" />
df.fillna('sample value')
<img width="1664" height="596" alt="image" src="https://github.com/user-attachments/assets/28e192cb-724b-4196-ae2d-283b4d076bfd" />
ffil=df.fillna(method='ffill') #fflill=forward fill
ffil
<img width="1648" height="662" alt="image" src="https://github.com/user-attachments/assets/9b957a63-29bd-4226-bc5b-442a25230c91" />
bfil=df.fillna(method='bfill')
bfil
<img width="1804" height="650" alt="image" src="https://github.com/user-attachments/assets/fd14e883-cf16-4732-8dc2-3f275c85564c" />
m=df.num_episodes.mean()
m
<img width="1727" height="113" alt="image" src="https://github.com/user-attachments/assets/9daab05e-6e75-4415-a15a-8a94a4dc5e31" />
n=df.fillna(df['num_episodes'].mean())
n
<img width="1666" height="608" alt="image" src="https://github.com/user-attachments/assets/a304f101-ee35-4e65-abb1-557d7770c25f" />
fmean=df['lifetime_popularity_rank'].fillna(value=df['lifetime_popularity_rank'].mean())
fmean
<img width="1468" height="645" alt="image" src="https://github.com/user-attachments/assets/7e824fc8-1a93-4fa6-91c3-1b91011cf14b" />
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS (2).csv')
df
<img width="1512" height="753" alt="image" src="https://github.com/user-attachments/assets/4504262a-e27e-4612-bfc4-78399761d196" />
df.shape
<img width="1601" height="112" alt="image" src="https://github.com/user-attachments/assets/c6991f90-c87c-4ea9-ae9a-b1ca8506ae30" />
df.describe()
<img width="1412" height="448" alt="image" src="https://github.com/user-attachments/assets/744661e3-1368-42bc-aebf-ac4194505f6c" />
df.info()
<img width="1328" height="513" alt="image" src="https://github.com/user-attachments/assets/53805c6e-ca29-49d0-ac96-5952d51816ba" />
df['GENDER'].value_counts()
<img width="1614" height="283" alt="image" src="https://github.com/user-attachments/assets/4551857b-8c9a-48cc-977a-f3ddc0ca6f68" />
df.dropna(how='any').shape
<img width="1574" height="116" alt="image" src="https://github.com/user-attachments/assets/4103e8cd-8e0e-4532-b8e9-3d161c577d0e" />
x1=df.dropna(how='any')
x1
<img width="1328" height="643" alt="image" src="https://github.com/user-attachments/assets/9a8aa13d-e133-4394-bb0a-0f7b625e3afd" />
res=df.dropna(subset=['M1','M2','M3','M4'],how='any')
res
<img width="1442" height="626" alt="image" src="https://github.com/user-attachments/assets/11ff1bf0-90e2-40ac-8173-7f9c1d3f2d2c" />
m2=df.TOTAL.mean()
m2
<img width="1573" height="140" alt="image" src="https://github.com/user-attachments/assets/b4a71825-b001-4eac-a719-168a7e85f168" />
df.TOTAL.fillna(m2,inplace=False)
df
<img width="1342" height="731" alt="image" src="https://github.com/user-attachments/assets/947cadca-e5c2-4a2f-b7c9-d53db8e0c943" />
df.isnull()
<img width="1505" height="741" alt="image" src="https://github.com/user-attachments/assets/a6075dd6-a419-4c74-9c15-694ea8ae43f0" />
import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
<img width="1307" height="695" alt="image" src="https://github.com/user-attachments/assets/71ba85a3-80c7-40ba-a5f2-12dfa2483dd8" />
sns.heatmap(df.isnull(),yticklabels=True,annot=True)
<img width="1289" height="682" alt="image" src="https://github.com/user-attachments/assets/a5703e73-d295-4d4b-9d96-353a8e054eab" />
df.dropna(inplace=True)
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
<img width="1291" height="701" alt="image" src="https://github.com/user-attachments/assets/e9702d59-1014-4595-9033-bd43c9ae89c8" />
df=pd.read_csv('/content/heights (1).csv')
df
<img width="1464" height="686" alt="image" src="https://github.com/user-attachments/assets/b5b699c7-f6b6-402f-acb1-97d55ee2fb8e" />
sns.boxplot(data=df)
<img width="1175" height="638" alt="image" src="https://github.com/user-attachments/assets/d08bfb33-ae27-4444-b80c-8afc7d2ba18a" />
sns.scatterplot(data=df)
<img width="1404" height="639" alt="image" src="https://github.com/user-attachments/assets/3dee140e-858b-4b4e-a6ed-426eadd59995" />
max=df['height'].quantile(0.75)
min=df['height'].quantile(0.25)
iqr=max-min
iqr
<img width="1569" height="187" alt="image" src="https://github.com/user-attachments/assets/80d32c4e-94ee-486d-8ca9-b9f2528e81a6" />
lb=min-1.5*iqr
ub=max+1.5*iqr
outliers=df[(df['height']<lb)|(df['height']>ub)]
print("Lower bound",lb)
print("Upper bound",ub)
print("outliers",outliers)
<img width="1594" height="309" alt="image" src="https://github.com/user-attachments/assets/7b780b2a-6be3-4a4a-b458-d425ebba8246" />
no_outliers=df[~((df['height']<lb)|(df['height']>ub))]
no_outliers
<img width="1553" height="602" alt="image" src="https://github.com/user-attachments/assets/adb20848-f951-4c85-9a80-632b09421e72" />
sns.boxplot(data=no_outliers)
<img width="1647" height="620" alt="image" src="https://github.com/user-attachments/assets/b618f29a-843a-4f9d-97cd-5b4562bf4930" />
sns.scatterplot(data=no_outliers)
<img width="1556" height="632" alt="image" src="https://github.com/user-attachments/assets/99c62488-b53c-447d-a351-12e1e183b6b1" />
import matplotlib.pyplot as plt
df
<img width="1626" height="694" alt="image" src="https://github.com/user-attachments/assets/fa4d6f0d-8858-4e4e-aeaf-8c95d2b91db2" />
max=df['height'].quantile(0.75)
q2=df['height'].quantile(0.5)
min=df['height'].quantile(0.25)
iqr=max-min
lb=min-1.5*iqr
ub=max+1.5*iqr
dfs=df[(df['height']>=lb)&(df['height']<=ub)]
dfs
<img width="1554" height="734" alt="image" src="https://github.com/user-attachments/assets/4e7d2418-266d-4314-a3be-78bb41e94757" />
import numpy as np  
from scipy import stats
z= np.abs(stats.zscore(df['height']))
z
<img width="1572" height="244" alt="image" src="https://github.com/user-attachments/assets/056f0272-fd21-4266-b280-18b23de55c1b" />
df1=df[z<3]
df1
<img width="1670" height="655" alt="image" src="https://github.com/user-attachments/assets/123f27ef-a595-4fa4-9797-a8a12188cd90" />
val=df['height']
val
<img width="1611" height="699" alt="image" src="https://github.com/user-attachments/assets/a0fb8d5f-dc40-446a-b670-2f2b706a7118" />
out=[]
def d_o(val):
  ts=3
  m=np.mean(val)
  sd=np.std(val)
  for i in val:
    z=(i-m)/sd
    if np.abs(z)>ts:
      out.append(i)
      return out
<img width="1782" height="303" alt="image" src="https://github.com/user-attachments/assets/0d4b96e7-6e07-49e7-bbba-af20a1c986cf" />
op=d_o(val)
op
<img width="1681" height="150" alt="image" src="https://github.com/user-attachments/assets/c7e5617f-f181-4dc8-8ccf-fda68484a555" />








![Uploading image.png…]()



# Result
          Thus we have cleaned the data and removed the outliers by detection using IQR and Z-score method.
