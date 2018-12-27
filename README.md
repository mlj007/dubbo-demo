# dubbo 服务端和客户端使用栗子
下列模块的下载地址[Apache Dubbo(incubating)](https://github.com/mlj007/dubbo-demo):

* dubbo-demo-api
* dubbo-demo-consumer
* dubbo-demo-provider


## 提示  

这个例子来自官网[incubator-dubbo](https://github.com/apache/incubator-dubbo)，本用例无需修改可直接使用。


## 使用说明

一、修改配置：

1、dubbo-demo-provider.xml 文件中<dubbo:registry address="multicast://224.5.6.7:1234"/> 

改成<dubbo:registry address="zookeeper://10.0.23.115:2181"/> 

10.0.23.115是zookeeper注册中心的ip ，2181是zookeeper端口号。

2、dubbo-demo-consumer.xml 文件中<dubbo:registry address="multicast://224.5.6.7:1234"/> 

改成<dubbo:registry address="zookeeper://10.0.23.115:2181"/> 

10.0.23.115是zookeeper注册中心的ip ，2181是zookeeper端口号。

二、启动程序：

可以用你的IDE Terminal 

1、进入dubbo-demo 模块下 dubbo-demo-provider 的target文件下执行命令运行

命令：java -jar dubbo-demo-provider-2.6.6-SNAPSHOT.jar 运行服务端 

2、进入dubbo-admin模块下 dubbo-demo-consumer 的target文件下执行命令运行

命令 java -jar dubbo-demo-consumer-2.6.6-SNAPSHOT.jar 运行客户端.

3、后台查看服务使用情况

  [管理后台源码地址](https://github.com/mlj007/incubator-dubbo-ops) 





