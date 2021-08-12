* `data.csv`使用了后一天的开盘价涨跌作为`label`
  * `testData.csv`和`trainData.csv`基于`data.csv`创建，其中使用了`MinMaxScaler`做为**归一化方式**
  * `testData3.csv`和`trainData3.csv`基于`data.csv`创建，其中使用了`RobustScaler`做为**归一化方式**
* `data2.csv`使用了后三天的开盘价涨跌作为`label`
  * `testData2.csv`和`trainData2.csv`基于`data2.csv`创建，其中使用了`MinMaxScaler`做为**归一化方式**
  * `testData4.csv`和`trainData4.csv`基于`data2.csv`创建，其中使用了`RobustScaler`做为**归一化方式**