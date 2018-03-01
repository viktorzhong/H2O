# H2O
H2O是一个分布式的基于内存的，可扩展的机器学习，深度学习框架;
Sparkling water将h2o和spark相结合，让我们可以在spark平台上运行h2o服务。

安装
----------------
1. 下载对应版本的sparkling-water, 比如spark版本为2.2.1，则选择2.2.1的sparkling-water <br />
   http://h2o-release.s3.amazonaws.com/sparkling-water/rel-2.2/9/index.html
2. 解压并运行(以Spark local模式为例):
   export MASTER="local[*]"   <br />
   unzip sparkling-water-2.2.9.zip  <br />
   cd sparkling-water-2.2.9  <br />
   bin/sparkling-shell --conf "spark.executor.memory=1g"  <br />

3. 创建H2O服务，在shell中运行：
   >import org.apache.spark.h2o._  <br />
   >val h2oContext = H2OContext.getOrCreate(spark)  <br />
   使用浏览器访问54321端口可以查看sparkling water服务.
   
