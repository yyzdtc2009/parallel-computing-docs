##Machine Learning with Spark
很多人看到用Spark进行机器学习，可能第一反应都会想到Mlib。由于Spark RDD的特性，使得Spark在进行迭代计算时，相对Hadoop Mapreduce来说有了一个质的提升，Mlib构建在Spark core之上，充分地利用了Spark的优势，集成了很多算法，减少数据分析业务的开发难度。

然而Mlib只是一个算法库，对于一个数据分析系统来说，仅有一个算法库是远远不够的。一个数据分析系统是一个完整的数据生态链，由很多组件组成，比如数据收集、数据存储、数据分析、结果输出、前端应用等。而对于一个用于分析处理大规模数据的学习系统来说，还必须保证系统具有易扩展性和容错能力。此外，如果可能的话，还应该能够提供批处理和流式处理两种方式。

![](https://github.com/yyzdtc2009/parallel-computing-docs/blob/master/resource/images/machine-learning-system.png)

上图展示了一个最简单机器学习流水线示意图，下面逐个来对此进行说明。


Spark对于建立一个机器学习系统来说的优势在于，它本身的平台性在机器学习系统各个组成部分上都有很好的解决方案，这种在同一个上下文中完成所有步骤的能力是其他平台所不具有的。
