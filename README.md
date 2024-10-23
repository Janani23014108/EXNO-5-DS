# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import matplotlib.pyplot as plt
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label="line 1")

x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line 2")

plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')

plt.legend()
```

![image](https://github.com/user-attachments/assets/4e039400-0c01-4816-a027-12bb41ec0fdd)

```
import matplotlib.pyplot as plt
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('some cool!')
```

![image](https://github.com/user-attachments/assets/d25d24d6-5557-47ef-83ce-720feb458d65)

```
import matplotlib.pyplot as plt
x_values=[1,2,3,4,5]
y_values=[1,5,10,16,20]
plt.scatter(x_values,y_values,s=20,color="purple")
plt.show()
```

![image](https://github.com/user-attachments/assets/f93ffdfb-64c0-4228-8a2a-3c11ecbfa64c)

```
x=[1,2,3,4,5,6,7,8,10]
y=[0,2,3,5,10,11,12,13,15]
plt.scatter(x,y,s=20,color="black",label="stars",marker="*")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My scatter plot!')
plt.legend()
plt.show()
```

![image](https://github.com/user-attachments/assets/09215ca0-d061-4a70-a8bb-0860d4c48244)

```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='yellow')
plt.legend(['y1','y2'])
plt.show()
```

![image](https://github.com/user-attachments/assets/e5e69c04-e172-49c3-a463-3dc4c7127622)

```
import matplotlib.pyplot as plt
values=[5,6,3,7,2]
names=["A","B","C","D","E"]

plt.barh(names,values,color="yellowgreen")
plt.show()
```

![image](https://github.com/user-attachments/assets/d5c3f15f-d66b-4be4-8bf9-7936084cb52b)

```
height=[10,24,36,40,5]
names=['one','two','three','four','five']
c1=['red','green']
c2=['b','g']
plt.bar(names,height,color=c1,width=0.8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My bar plot!')
plt.show()
```

![image](https://github.com/user-attachments/assets/2c5fd5b4-e77b-43cd-957d-2cdd78c17786)

```
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x2,y2,color='g')
plt.title('Bar graph')
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
```

![image](https://github.com/user-attachments/assets/533be14f-cc5c-40da-9d39-b9fae4b25176)

```
import matplotlib.pyplot as plt
ages=[2,5,70,40,30,45,50,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('No.of people')
plt.title('My histogram')
plt.show()
```

![image](https://github.com/user-attachments/assets/e039d84f-3332-4583-a331-0aeaf2f78bc6)

```
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```

![image](https://github.com/user-attachments/assets/6db805b7-d15e-460f-8919-b3312f16cbf2)

```
import matplotlib.pyplot as plt
x=[2,1,6,2,4,8,9,4,2,4,10,6,4,5,7,7,3,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='blue',alpha=0.5)
plt.show()
```

![image](https://github.com/user-attachments/assets/97296b8f-a6e4-494c-88d8-ac327be1e0e9)

```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Values')
ax.set_title('Box plot')
```

![image](https://github.com/user-attachments/assets/802ea7d9-3fd2-4dbc-944e-deb11df02cf9)

```
import matplotlib.pyplot as plt
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
c=['r','y','g','b']

plt.pie(slices,labels=activities,colors=c,startangle=90,shadow=True,explode=(0,0.1,0,0),autopct='%1.1f%%')
plt.show()
```

![image](https://github.com/user-attachments/assets/36d13138-0e36-4c23-b5b2-7b27f309f78f)

```
#Data to plot
labels ='Python', 'C++', 'Ruby', 'Java'
sizes =[215, 138, 245, 210]
colors= ['gold', 'yellowgreen', 'lightcoral', 'lightskyblue']
explode = (0, 0.4, 0, 0.5)
#Plot
plt.pie(sizes, explode=explode, labels =labels, colors=colors, autopct='%1.1f%%', shadow=True)
plt.axis('equal')
plt.show()
```

![image](https://github.com/user-attachments/assets/db2c9c6f-c7f5-452e-ba0e-219e741d9965)






# Result:
Thus the program to Perform Data Visualization using matplot python library for the given datas is been implemented.
