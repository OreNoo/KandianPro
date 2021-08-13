`data_复权.csv`为初始数据

1. `data_复权.csv`经过`DataClean.ipynb`的以下处理生成生成`data.csv`

   * 去除"指数"数据

   * 筛取当前在市的股票

   * 删除含有NaN的行

   * 删除`volume==0`的数据

   * 保存数据
2. `data.csv`经过`OutlierProcess.ipynb`的以下处理生成生成`data2.csv`

   * 异常值处理 删除异常值

   * 删除数据量过少的股票的数据
3. `data2.csv`通过`DataProcess.ipynb`生成以下文件：
   * 使用了后一天的开盘价涨跌作为`label`
     * `testData.csv`和`trainData.csv`基于`data2.csv`创建，其中使用了`MinMaxScaler`做为**归一化方式**
     * `testData3.csv`和`trainData3.csv`基于`data2.csv`创建，其中使用了`RobustScaler`做为**归一化方式**
   * 使用了后三天的开盘价涨跌作为`label`
     * `testData2.csv`和`trainData2.csv`基于`data2.csv`创建，其中使用了`MinMaxScaler`做为**归一化方式**
     * `testData4.csv`和`trainData4.csv`基于`data2.csv`创建，其中使用了`RobustScaler`做为**归一化方式**