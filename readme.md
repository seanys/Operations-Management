## Operations Management - Tongji MS&E 

This repository includes examples and slides in Prof. Qiu Chanhua's OM class. My notes for the examples are as follows.

[TOC]

### LP Problem

#### Simple LP problem

We use the LP model of excel to solve the LP problem. Our preliminary work is to convert the LP problem into a standard format. 

```
Max     Z=2X+4Y
s.t.    4X+6Y<=120
        2X+6Y<=72
        Y<=10
        X,Y>=0
```

![image-20200607143021015](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607143021015.png)

Then input the target cells, variable cells, and constraints into the scheduling model. Click scheduling and we can get the computing results.

![img](img/image-20200607143240027.png)

#### Transportation Problem

Transportation Problem is a special LP problem. The core methodology is the same as beyond, which builds a linear programming problem and uses the LP scheduling model to solve it.

![img](img/image-20200607142350303.png)

The first table contains the costs from factories to warehouses. The second table contains all variables that are transportation quantities. The third table computes the total cost which is also the basis of the objective function. Input these items input the scheduling model of excel and we can simply get the final result.

![img](img/image-20200607142301300.png)

### Scheduling

#### Production planning examples



#### Scheduling issues



#### Production planning-cumulative curve method



#### Total production planning technology

In order to compute 





![image-20200607155256874](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607155256874.png)



### Inventory Management 

In this part, we take Newsvendor Model for example.





### Forecasting

#### Moving Averages

Moving average is the most simple way for forecasting demand. We only need to calculate the average of the demand in the previous few weeks.

![image-20200607160622779](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607160622779.png)

#### Forecast Error Measures

To measure the forecasting error, we need to take some values as indicators. 

**RSFE**: the running sum of forecast errors

**MAD**: Mean Absolute Deviation

**TS**: Time series

![image-20200607161048451](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607161048451.png)

#### Causal Relationships/Linear Regression

In order to forecast the demand or the sales, we can also find the casusal relationships between them and other variable.

For example, the number of housing start permits have casusal relationships with the carpet sales.

![image-20200607162110603](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607162110603.png)

In some cases, x and y may not have linear correlations. We need to replace y with different power-law index and compute the linear regression again.

#### Exponential Smoothing 

Exponential smoothing method is another forecasting method. 

![image-20200607162710198](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607162710198.png)

#### Second Exponential Smoothing Method



#### Time Series Method



### Supply chain management - Problem

Source:  ([Riskpool-example.xls](5.Supply-chain-management))

![image-20200607164335982](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607164335982.png)

![image-20200607171212156](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607171212156.png)

EOQ: Economic order quantity

We can use the same way to compute the average inventory of decentralized system and centralized system to maintain a 97% service level. Just compute the safty stock, ROP, and EOQ according to the leading time and history demand, the average inventory is easy to compute.

![image-20200607171240035](/Users/sean/Documents/Projects/My Github/Operations-Management/img/image-20200607171240035.png)

### Simulation

#### Simulation Principle



#### Machine Maintenance Simulation-Example



#### Tennessee Wagon Simulation-Example



### MRP







