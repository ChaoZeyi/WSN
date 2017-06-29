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

  > 给出了8种表示方式和9种相似性度量的方法和实验
  >
  > 对于大规模数据的表示，常用的还是DFT、DWT、PAA，很少用到SVD
  >
  > one to one mapping
  >
  > 1.  L1：（曼哈顿距离）
  > 2.  L2：（欧式距离）数据量较大时，相比于更复杂的方法，也有很好的效果；但对噪声很敏感，无法处理局部值突变的情况
  >
  > one to many mapping
  >
  > 1.  DTW
  > 2.  LCSS
  >
  > 感觉整篇看下来，没什么重点，只是介绍了几种名词解释。


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

#### 2017.6.27

- **A review of the application of data mining techniques for decision making in agriculture（可参考）**

  > 这篇文章主要是一个综述，介绍了一系列的数据挖掘技术在农业上的应用：人工神经网络、贝叶斯网络、支持向量机，比如：农作物生长情况、杀虫剂和营养物流失、土壤水分估计等
  >
  > **这篇文章给出了很多数据挖掘的定义和名词解释，在写Introduction时可能会用到**
  >
  > 数据挖掘就是从大量复杂数据中，找出隐藏的模式特征


#### 2017.6.28

- **Least squares support vector machine for short-term prediction of meteorological time series（可参考）**

  > **K-S检验**：经验分布和理想分布是否一致
  >
  > ​相比于传统的统计方法，神经网络用于时间序列预测的优势
  >
  > 最重要的，**传统方法不能处理非线性、非平稳的输入，而神经网络可以**
  >
  > 劣势：局部最优、过拟合
  >
  > SVM可以解决神经网络局部最优的问题，达到全局最优
  >
  > **混合模型**
  >
  > **文章给出了很多使用神经网络或者混合模型对气象时间序列进行预测的例子，可以参考**
  >
  > 评价模型时，不仅要比较精度，还要看模型的泛化能力
  >
  > Ls-SVM是一种改进的SVM算法（介绍）
  >
  > 太阳辐射（G）温度（T）相对湿度（RH）气压（P）风速（WS）风向（WD)
  >
  > ​调参算法：grid search网格搜索，找到所有的参数组合一一实验，得到最优的参数