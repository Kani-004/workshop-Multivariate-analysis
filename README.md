workshop-Multivariate-analysis

Aim:

To Perform Multivarient Analysis

Algorithm

1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file PROGRAM:

Types of Bivariate Analysis:

(i) Numerical & Numerical

Scatter plot
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

Multivariate analysis

Categorical & Categorical Heatmap

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/FlightInformation.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

Output:

![image](https://user-images.githubusercontent.com/129577149/229983143-7c3f5af1-677f-4bc4-af5e-ada978dfeab0.png)


![image](https://user-images.githubusercontent.com/129577149/229983798-a1109ae5-f7d5-4acf-a2a3-1556af8276bc.png)



![image](https://user-images.githubusercontent.com/129577149/229983374-a1872774-b5da-4041-b168-d4ab58aea459.png)


![image](https://user-images.githubusercontent.com/129577149/229983400-6f55822f-2933-4048-88cc-3e1d67caf1ff.png)


![image](https://user-images.githubusercontent.com/129577149/229983538-af7ab981-1b5a-4fec-80d6-1c48f69f843b.png)



Result:

Thus, Bivariate/Multivariate Analysis is performed successfully




