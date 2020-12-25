# Apache-Skywalking

## 下载安装  
https://mirrors.tuna.tsinghua.edu.cn/apache/skywalking/8.3.0/apache-skywalking-apm-8.3.0.tar.gz

## 执行命令
tar -zxvf apache-skywalking-apm-8.3.0.tar.gz

## 启动
/apache-skywalking-apm-bin/bin目录下启动 ./startup.sh  

## skywalking端口
web监控dashboard:8080
如果不想用8080作为端口,可以修改目录/apache-skywalking-apm-bin/webapp/webapp.yml  
http数据收集:12800  
gRPC:11800  

## SpingBoot项目启动参数设置
-javaagent：解压apache-skywalking-apm-8.3.0.tar.gz后agent目录下skywalking-agent.jar绝对路径  
-Dskywalking.agent.service_name：你的SpringBoot Application Name  
-Dskywalking.collector.backend_service:部署skywalking的地址:11800

例如:  
IntelijIDEA 启动设置VM options设置:
-javaagent=D:\apache-skywalking-apm-bin\agent\skywalking-agent.jar  
-Dskywalking.agent.service_name=ApolloDemo  
-Dskywalking.collector.backend_service=XXX.XXX.XXX.XXX:11800  

