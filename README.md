# 关于

- 本仓库将以面试题为导向，将 Java 后台开发面试中遇到的问题和解题思路或答案整理输出，一方面是为了方便自己复盘，另一方面也是希望对其他胖友能有所帮助；
- 由于水平有限，本仓库中部分题目来源于面试所遇，一部分源于网上；
- 短期来看，也许可以面向面试官编程，但长期来看，如果想在技术这条路上走得更远，不能只浮于面试题表面，而是要稳扎稳打，把基础打牢，勿在浮沙筑高台；
- 源码之中，了无秘密，即使现在没有太多源码阅读的经验，后续也一定要多多阅读源码。

# 前言

- 整理不易，如果觉得有帮助请点个 `star`

# 目录

## Java基础
## Java并发
## JVM
## 框架
- [Spring](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring)
  - [Spring Framework](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-framework)
  - [Spring Bean](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-bean)
  - [Spring IoC](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-ioc)
  - [Spring 注解](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-%E6%B3%A8%E8%A7%A3)
  - [Spring AOP](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-aop)
  - [Spring 事务](https://github.com/bigrotor187/awesome-java-interview/tree/master/framework#spring-%E4%BA%8B%E5%8A%A1)
## 分布式系统
### 分布式缓存
- Memcached

- Redis


### 分布式服务框架
- Dubbo
  - Dubbo简介
  - 待续

### 分布式协调服务
- Zookeeper
  - 简述Zookeeper
  - 简述ZAB协议
  - 简述Paxos算法
  - ZK如何保证数据的一致性？
  - Dubbo简介及以Zookeeper为注册中心
  - Zookeeper的leader选举过程
  - 2PC and 3PC
  - 简述Zookeeper的watcher
  - 简述ZAB集群数据同步的过程
  - 简述Zookeeper中的ACL
  - Zookeeper底层是如何实现数据一致性的？
  - Zookeeper在yarn框架中如何实现避免脑裂的?
  
### 分布式消息队列
- RabbitMQ
  - 什么是RabbitMQ?
  - 为什么要使用RabbitMQ?
  - 消息队列的优缺点？
  - RabbitMQ 与 Kafka 有什么区别？
- Kafka
  - Kafka 都有哪些特点？
  - 请简述下你在哪些场景下会选择 Kafka？
  - 简述Kafka 的设计架构
  - Kafka 分区的目的
  - Kafka 是如何做到消息的有序性的？
  - Kafka 的高可靠性是怎么实现的？
  - 请谈一谈 Kafka 数据一致性原理
  - ISR、OSR、AR 是什么？
  - LEO、HW、LSO、LW等分别代表什么
  - Kafka 在什么情况下会出现消息丢失？
  - 怎么尽可能保证 Kafka 的可靠性
  - 消费者和消费者组有什么关系？
  - Kafka 的每个分区只能被一个消费者线程，如何做到多个线程同时消费一个分区？
  - 数据传输的事务有几种？
  - Kafka 消费者是否可以消费指定分区消息？
  - Kafka消息是采用Pull模式，还是Push模式？
  - 如何为Kafka集群选择合适的Topics/Partitions数量
  - 待续

### 分布式搜索引擎

- Elasticsearch
  - Elasticsearch简介

- Solr
  - Solr简介
  - 简述Solr的倒排索引
  - 为什么要使用Solr?
  - Solr和elasticsearch的区别？

### 分布式事务
- 刚性分布式事务
- 柔性分布式事务
- 两阶段提交协议&三阶段提交协议
- 一致性哈希算法

## 数据库
## 设计模式
## 数据结构和算法
