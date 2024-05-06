# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.


STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![Screenshot 2024-05-05 223127](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/f25431da-c22c-4fad-9f3e-68881e874253)

```
df = sns.load_dataset("tips")
df

```
![Screenshot 2024-05-05 223230](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/37823e17-f809-4a81-90dd-53db859c9060)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```


![Screenshot 2024-05-05 223309](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/b474e79a-47db-42b2-9ba6-35cb068062b0)

```

x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")

```
![Screenshot 2024-05-05 223347](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/7f5405cb-9743-482a-a154-6cdcd98b3976)

```

tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()

```
![Screenshot 2024-05-05 223421](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/0a33b345-d7f2-4dfd-b5e7-fd1f85a3a278)

```

avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

```

![Screenshot 2024-05-05 223502](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/89ae1b62-f42c-4bf3-a2ab-e7e5eb87e0fc)

``` 

years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)


```



![Screenshot 2024-05-05 223541](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/7be5ffdd-93d8-4536-aa9a-9c446d401c10)


```

import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')

 ```
![Screenshot 2024-05-05 223614](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/13d2bdcb-0701-4d44-ba68-52f1bd3ccdd2)

```

tit=pd.read_csv("titanic_dataset.csv")
tit


```



![Screenshot 2024-05-05 223655](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/4c25bd4e-5e18-45e0-9b26-a684ba6b7c2a)

```

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")

```


![Screenshot 2024-05-05 223722](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/9f6a0bed-5e90-4823-87b2-35012e8af184)


```

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![Screenshot 2024-05-05 223815](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/08580b45-c06f-4e2d-891f-53bf472ecb02)


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')

```



![Screenshot 2024-05-05 223850](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/2590117d-721a-4af3-86e7-fc5b51925246)


```

num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var

```

![Screenshot 2024-05-05 223934](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/b054a6a9-1a7b-4d9b-919f-f9a2af07f2db)

```

sns.histplot(data = num_var, kde = True)


```

![Screenshot 2024-05-05 224010](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/a09fff3d-fd22-41ea-910a-b7edfc64d0cd)


```

df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```


![Screenshot 2024-05-05 224051](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/08ca57df-e78e-4de8-b6ee-8b9419e16e4d)


```c
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```


![Screenshot 2024-05-05 224133](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/e691d8d0-b5fa-4d67-8224-3af1595f0359)


```c


sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

```

![Screenshot 2024-05-05 224215](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/08e4920e-30cd-421f-9c28-97bbff28205c)

```c

sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")

```

![Screenshot 2024-05-05 224300](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/0f12c201-de2a-4d9c-a1c2-d933b4a8526f)

```

mart=pd.read_csv("titanic_dataset.csv")
mart

```
![Screenshot 2024-05-05 224332](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/3fafba0b-e58b-4d91-857f-bdd67e6e3d5d)


```

mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)

```
![Screenshot 2024-05-05 224411](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/ba585050-0b03-4c38-9b4a-fbc90a7191e0)


```
sns.kdeplot(data=mart,x='PassengerId')
```

![Screenshot 2024-05-05 224459](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/9f082e14-b7d5-4ea1-b9b2-3f0376b5fbbe)


```

sns.kdeplot(data=mart,x='Age')

```
![Screenshot 2024-05-05 224530](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/fc442de9-504e-416e-88e4-1c1605a3cd25)

```

sns.kdeplot(data=mart)

```
![Screenshot 2024-05-05 224616](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/2f57607b-16e8-4dbb-9f76-43723dbbd7ba)


```

sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

```


![Screenshot 2024-05-05 224703](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/7ed56cbc-2425-44d5-81c6-528d8ec1e4c6)

```

sns.kdeplot(data=mart,x='PassengerId',y='Survived')

```
![Screenshot 2024-05-05 224755](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/960f9422-ca4d-4084-b9c4-ed1ef7af7319)

```

data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)

```

![Screenshot 2024-05-05 224837](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/7605b3a7-48b4-4d5e-9113-10ff29d8cc2e)



```
hm=sns.heatmap(data=data)

```

![Screenshot 2024-05-05 224910](https://github.com/SubhashriRavichandran10/EXNO-6-DS/assets/145743413/1a441978-004f-4c01-9b11-a0aa038bfd7b)





# Result:
 Thus, all the data visualization techniques of seaborn has been implemented
