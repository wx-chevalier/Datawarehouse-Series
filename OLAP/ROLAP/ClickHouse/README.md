# ClickHouse

数据处理现在还是分为 OLTP 和 OLAP。OLTP（在线事务处理）优化的方向是高并发、高可用，是精确，是各种增删改查。所以面临和解决的问题都是怎么解决高并发下的增删改查，怎么解决脏读、脏写，保证数据一致性等问题。

OLAP（在线分析处理）的优化方向则是高速数据处理能力、高速读取能力。一般又分为两个优化方向，一个是预先计算好各个维度的数据，存成 CUBE，分析的时候直接查询结果就行，这是 MOLAP（Multidimensional OLAP，多维在线分析处理），典型代表的是 Kylin。一个是结构化存好，然后用尽各种方法优化，分析的时候拼命计算，这是 ROLAP（Relational OLAP，关系型在线分析处理），典型代表就是 ClickHouse 了。
