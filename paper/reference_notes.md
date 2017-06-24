#### **2017.6.16**

- ***Temperature error correction based on bp neural network in meteorological WSN***

  > 对比了国家气象站的不足和传感网的优势

- ***predictive capacity of meteorological data will it rain tomorrow***

  > 对几种流行的机器学习算法做了测试，并比较准确率
  >
  > Naive Bayes, Random Forest, J48, IB1
  >
  > 分为两类：根据天气情况预测今天是周几
  >
  > ​                   根据天气情况预测未来时刻的天气情况    准确率   70-87%

#### **2017.6.17**

- ***A data driven approach to soil moisture collection and prediction***

  > 系统主要分为两部分：数据采集、数据预测
  >
  > 由于预测模型需要的数据量较大，所以实际用的并不是论文中提到的采集系统的数据，而是来自国家项目的数据集
  >
  > 数据精度为小时级别
  >
  > 一定要有特色和贡献点（和已有的工作相比）
  >
  > ​	1、可自动调整周期，当土壤水分值不怎么变化时，就增大观测周期，一旦检测到数据变化，立马密集观测，类似于我们的降雨量周期调整
  >
  > ​	2、预测模型：反馈环，t时刻的预测输出被用于t+1时刻预测的输入



#### **2017.6.19**

- ***The SMART approach to comprehensive quality assessment of site-based spatial-temporal data***

  > 从站点的角度来提高数据准确率
  >
  > 从一系列时空数据中，找出测量错误的站点，并不是比较数据的准确性

- ***validation of remote sensing retrived products using data from a wireless sensor-based online monitoring in antarctica***

  > 对比了WSN和气象站的数据，说明WSN的观测数据是可靠的
  >
  > 但并没有具体分析，为什么两者数据之间具有很高的相似性，然后说明数据是可靠的，只是给出了两张时间序列图（直观上看，趋势也差了挺多的）

- ***Anomaly detection algorithm for localized abnormal weather using low-cost wireless sensor nodes***

  > 通过处理大气压力时间序列数据，观察台风发生前气压的异常变化，定义了一个计算值val = 当前时间的气压值-五分钟前气压值的平方和，论文结果得出：在台风发生前，val值会明显变大，气压波动剧烈！（其实从结果图中，并看不出这一点）。


#### **2017.6.20**

- ***Experimental comparison of representation methods and similarity measures for time series data***

  > ​给出了9种相似性度量的方法和实验


#### **2017.6.24**

- **Time Series+Anomaly Detection+Algorithms+StatsBot**

  > 异常检测：找到偏离标准或通常信号的数据
  >
  > STL分解：Seasonal  trend loess decomposition，将数据分为季节性、趋势和残余三部分
  >
  > Classification and regression Tree、xgboost、ARIMA、Neural Network(LSTM)
  >
  > 另外三篇论文分别详细介绍了STL分解、ARIMA、CART
  >
  > 这篇文章主要还是介绍了异常点检测