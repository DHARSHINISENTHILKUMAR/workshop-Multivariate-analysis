# workshop-Multivariate-analysis
# Aim:
  To Perform Multivarient Analysis
# Algorithm
1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file PROGRAM:
# Types of Bivariate Analysis:
(i) Numerical & Numerical
# Scatter plot
~~~
import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib as plt

df = pd.read_csv("/content/FlightInformation.csv")

sns.scatterplot (df['Price'],df['Arrival_Time'])
Bar Plot

import pandas as pd

import seaborn as sns

sns.barplot (x=df['Duration'],y=df['Price']) 
sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df) 
states=df.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

import matplotlib.pyplot as plt

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()
~~~
# Multivariate analysis
# Categorical & Categorical Heatmap
~~~
import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/FlightInformation.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()
~~~
# Output:
![image](https://user-images.githubusercontent.com/113699377/229267310-5743bb6e-be35-4094-bda9-d39a82c32a3a.png)
![image](https://user-images.githubusercontent.com/113699377/229267318-1c427bb0-2f0d-41c1-84bf-6771566d92d8.png)
![image](https://user-images.githubusercontent.com/113699377/229267340-7e8e9c69-86f5-4065-88f8-1e260f2c4c7f.png)
![image](https://user-images.githubusercontent.com/113699377/229267398-5f5b10ef-1753-416a-b2f1-ce83bc03c85f.png)
![image](https://user-images.githubusercontent.com/113699377/229267414-a20ac298-de09-45fe-9eea-6057eab2e26f.png)
# Result:
Thus, Bivariate/Multivariate Analysis is performed successfully.

