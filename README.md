模型选择与建立：
在本项目中，选用了SARIMA（季节性自回归移动平均）模型作为数据挖掘模型。原因是交通流量的周期性强，白天流量大晚上流量小，周期为24小时。SARIMA模型是一种用于时间序列分析和预测的经典模型，特别适用于具有季节性和趋势性特征的数据。
SARIMA模型是对ARIMA模型的扩展，它考虑了数据中的季节性变化。ARIMA模型由自回归（AR）、差分（I）和移动平均（MA）三个部分组成，而SARIMA模型除了这些部分外，还包括季节性自回归（SAR）、季节性差分（SI）和季节性移动平均（SMA）。

模型评估与调优： 
本项目使用了各种方法来对模型进行了评估和调优。下面是项目中SARIMA模型的评估和调优操作：
1.	网格搜索：使用嵌套循环遍历不同的参数组合。通过尝试不同的AR、差分和MA阶数以及季节性AR、季节性差分和季节性MA阶数的组合，来创建和拟合多个SARIMA模型。
2.	模型拟合和预测：对每个参数组合，使用训练数据拟合SARIMA模型，并使用该模型进行未来交通流量的预测。
3.	均方根误差（RMSE）计算：使用预测结果和测试数据，计算均方根误差作为模型性能的评估指标。
4.	最佳模型参数选择：通过比较不同参数组合的RMSE，更新记录最小RMSE和对应的最佳参数组合。
5.	输出最佳参数和最小RMSE：打印出最佳参数组合和对应的最小RMSE。
