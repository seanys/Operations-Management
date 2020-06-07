## Operations Management - Tongji MS&E 

This repository includes examples and slides in [Prof. Qiu Canhua's](https://sem.tongji.edu.cn/semch/15130.html) OM class. Notes for the examples are as follows.

- [LP Problem](#lp-problem)
  * [Simple LP problem](#simple-lp-problem)
  * [Transportation Problem](#transportation-problem)
- [Scheduling](#scheduling)
  * [Production planning examples](#production-planning-examples)
  * [Scheduling issues](#scheduling-issues)
  * [Production planning-cumulative curve method](#production-planning-cumulative-curve-method)
  * [Total production planning technology](#total-production-planning-technology)
- [Inventory Management - Problem](#inventory-management---problem)
- [Forecasting](#forecasting)
  * [Moving Averages](#moving-averages)
  * [Forecast Error Measures](#forecast-error-measures)
  * [Causal Relationships/Linear Regression](#causal-relationships-linear-regression)
  * [Time series decomposition](#time-series-decomposition)
  * [Exponential Smoothing](#exponential-smoothing)
  * [Second Exponential Smoothing Method](#second-exponential-smoothing-method)
- [Supply chain management - Problem](#supply-chain-management---problem)
- [Simulation](#simulation)
  * [Simulation Principle](#simulation-principle)
  * [Machine Maintenance Simulation-Example](#machine-maintenance-simulation-example)
- [MRP](#mrp)
  * [One Products Planning](#one-products-planning)

  * [Total Planning](#total-planning)



### LP Problem

#### Simple LP problem

Source:[Use Excel to solve the linear programming problem.xls](Line-programing)

We use the LP model of excel to solve the LP problem. Our preliminary work is to convert the LP problem into a standard format. 

```
Max     Z=2X+4Y
s.t.    4X+6Y<=120
        2X+6Y<=72
        Y<=10
        X,Y>=0
```

<img src="img/image-20200607143021015.png" alt="image-20200607143021015" height="350px" />

Then input the target cells, variable cells, and constraints into the scheduling model. Click scheduling and we can get the computing results.

<img src="img/image-20200607143240027.png" alt="img" height="300px" />

#### Transportation Problem

Source:[Use Excel to solve the transportation problem.xls](Line-programing)

Transportation Problem is a special LP problem. The core methodology is the same as beyond, which builds a linear programming problem and uses the LP scheduling model to solve it.

<img src="img/image-20200607142350303.png" alt="img" height="150px" />

The first table contains the costs from factories to warehouses. The second table contains all variables that are transportation quantities. The third table computes the total cost which is also the basis of the objective function. Input these items input the scheduling model of excel and we can simply get the final result.

<img src="img/image-20200607142301300.png" alt="img" height="350px" />

### Scheduling

#### Production planning examples

Source: [Production planning examples and scheduling issues.xls](Scheduling)

<img src="img/image-20200608011424776.png" alt="image-20200608011424776" height="300px" />

#### Scheduling issues

Source: [Production planning examples and scheduling issues.xls](Scheduling)

Excel can schedule directly, so we need to schedule one by one. We can ultimately get the schedule below.

<img src="img/image-20200607233622733.png" alt="image-20200607233622733" height="350px" />

<img src="img/image-20200608010408977.png" alt="image-20200608010408977" height="300px" />

#### Production planning-cumulative curve method

Source: [Production planning-cumulative curve method.xls](Scheduling)

<img src="img/image-20200608000424715.png" alt="image-20200608000424715" height="350px" />

In this production planning problem, we assume average daily output is a constant to simplify this problem. 

To minimize total inventory cost, we can calculate the average daily output which can make the ending inventory of this year zero. Then we can calculate the first table. 

```
3460 ton /242 day=14.30 Ton/day
```

However, we can see the ending inventory will lower than zero during Sep. to Nov. So, we need to adjust daily output. 

It's obvious ending inventory is the lowest in October. If we make it zero, ending inventory every month will be greater than zero.

```
3150 ton /203 day=15.517 Ton/day
```

Cumulative production equals to cumulative demand in October and cumulative production is always greater than cumulative demand during this year after adjustment.

<img src="img/image-20200608002635882.png" alt="image-20200608002635882" height="350px" />

#### Total production planning technology

Source: [Total production planning technology.xls](Scheduling)

In order to compute the number of workers which can maintain the lowest cost, we can simply convert it into a linear programming problem. The total cost is the objective function. However, this method can only handle when demand is fixed. 

<img src="img/image-20200608011832741.png" alt="image-20200608011832741" height="500px" />

<img src="img/image-20200607155256874.png" alt="image-20200607155256874" height="350px" />

### Inventory Management - Problem

Source: [Newsvendor Model example.xls](Inventory)

In this part, we take Newsvendor Model for example. As for this problem, we only need to compute the expected marginal income and the expected marginal loss. Net income = MP\*Probability-ML\*Probability

We can see from below that if the number of requirements is greater than 37, net income is cheaper than 0. So we should stock 37 pieces of products. 

<img src="img/image-20200607190151009.png" alt="image-20200607190151009" height="300px" />

<img src="img/image-20200607190754807.png" alt="image-20200607190754807" height="250px" />

### Forecasting

#### Moving Averages

Source: [Forecasting examples to students.xls](Forecasting)

Moving average is the most easy way for forecasting demand. We only need to calculate the average of the demand in the previous few weeks. This method is called the simple moving average method.

We can also take endow history demands different weight to calculate the weighted average. This method is called the weighted moving average method.

<img src="img/image-20200607160622779.png" alt="image-20200607160622779" height="600px" />

#### Forecast Error Measures

Source: [Forecasting examples to students.xls](Forecasting)

To measure the forecasting error, we need to take some values as indicators. 

**RSFE**: the running sum of forecast errors

**MAD**: Mean Absolute Deviation

**TS**: Time series

<img src="img/image-20200607161048451.png" alt="image-20200607161048451" height="200px" />

#### Causal Relationships/Linear Regression

Source: [Forecasting examples to students.xls](Forecasting)

In order to forecast the demand or the sales, we can also find the casusal relationships between them and other variable.

For example, the number of housing start permits have casusal relationships with the carpet sales.

<img src="img/image-20200607162110603.png" alt="image-20200607162110603" height="500px" />

In some cases, x and y may not have linear correlations. We need to replace y with different power-law index and compute the linear regression again.

#### Time series decomposition

Source: [Time Series.xls](Forecasting)

Demands consist of average demand, trend, seasonal element, cyclical element, rand variation, autocorrelation. 

Time series can be defined as a series arranged in chronological order, which contains one or more influence factors of demand. 

Take the seasonal element as an example, we need to use seasonal coefficient to adjust sales. Sales may have linear correlations with time after adjustment.

<img src="img/image-20200607202904176.png" alt="image-20200607202904176" height="350px" />

#### Exponential Smoothing 

Source: [Forecasting examples to students.xls](Forecasting)

The recent data is more accurate than the earlier data in predicting the future, so the weight of the most recent data is more important than the weight of the previous data. So the exponential smoothing method is proposed. 

The next week’s forecast demand is equal to this week’s forecast demand minus this week’s actual demand times the smoothing parameter(0.1/0.6). 

Next week's forecast demand = This week's forecast demand + The deviation between forecast and actual demand this week * smooth parameter

<img src="img/image-20200607202443921.png" alt="image-20200607202443921" height="100px" />

<img src="img/image-20200607162710198.png" alt="image-20200607162710198" height="500px" />

#### Second Exponential Smoothing Method

Source: [Second exponential smoothing method.xls](Forecasting)

In the case of a trend, the exponential smoothing method will lag, so the second exponential smoothing method can be used for prediction.
For the situation after the trend and seasonal fluctuations, it is necessary to use the three-exponential smoothing method to predict. We only introduce the secondary exponential smoothing method here.

<img src="img/image-20200607202753043.png" alt="image-20200607202753043" height="80px" />

<img src="img/image-20200607200500332.png" alt="image-20200607200500332" height="300px" />

### Supply chain management - Problem

Source:  [Riskpool-example.xls](Supply-chain-management)

<img src="img/image-20200607164335982.png" alt="image-20200607164335982" height="300px" />

<img src="img/image-20200607171212156.png" alt="image-20200607171212156" height="280px" />

EOQ: Economic order quantity

We can use the same way to compute the average inventory of decentralized system and centralized system to maintain a 97% service level. Just compute the safty stock, ROP, and EOQ according to the leading time and history demand, the average inventory is easy to compute.

<img src="img/image-20200607171240035.png" alt="image-20200607171240035" height="600px" />

### Simulation

#### Random Number Generation

Sourcing: [Simulation Principle.xls](Simulation)

In excel, most of the distributions used in our assignments can be directly applied to generate a random number. If not, the inverse transform method can generate a random number from a certain distribution based on a uniform distribution.

For example, use VLOOKUP to find the interval to which the random number belongs and the time interval will be generated from that distribution.

<img src="img/image-20200608022116350.png" alt="image-20200608022116350" height="450px" />

#### Machine Maintenance Simulation-Examples

Sourcing: [Machine Maintenance Simulation-Examples.xls](Simulation)

Generate random numver from distribution and repeat this experiment. Obtain the statistical characteristics of the test results, and then compare them.

<img src="img/image-20200608022847777.png" alt="image-20200608022847777" height="400px" />

<img src="img/image-20200608022758698.png" alt="image-20200608022758698" height="450px" />

### MRP

#### One Products Planning

Sourcing: [MRP Example.xls](MRP)

<img src="img/image-20200608020259297.png" alt="image-20200608020259297" height="400px" />

#### Total Planning 

Sourcing: [Moran.xls](MRP)

<img src="img/image-20200608020357359.png" alt="image-20200608020357359" height="550px" />



