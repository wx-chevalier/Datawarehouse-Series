# OLAP 引擎

数仓构建包括模型定义和预计算两部分，数据工程师根据业务分析需要，使用星型或雪花模型设计数据仓库结构，利用数据仓库中间件完成模型构建和更新。一个普遍的共识是，没有一个 OLAP 引擎能同时在数据量，灵活性和性能这三个方面做到完美，用户需要基于自己的需求进行取舍和选型。预计算模式的 OLAP 引擎在查询响应时间上相较于 MPP 引擎（Impala、SparkSQL、Presto 等）有一定优势，但相对限制了灵活性。
