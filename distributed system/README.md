# 分布式系统
## 一、分布式缓存
### Memcached
  - Memcached 简介
  - Memcached的分布式算法简介
  - Memcached的数据清除算法
  - Memcacehd 的工作流程是怎么样的？
  - Memcached 和 Redis 有什么区别？
  - Memcached 适用的业务场景有哪些？
  - Memcached 不适用哪些业务场景？
  - 能够遍历 Memcached 中所有的 item 吗？
  - Memcached 集群是怎么工作的？
  - Memcached 最大的优势是什么？
  - Memcached 和 MySQL 的 query cache 相比，有什么优缺点？
  - Memcached 和服务器的 local cache（比如 PHP 的 APC、mmap 文件等）相比，有什么优缺点？
  - Memcached 的 cache 机制是怎样的？
  - Memcached 如何实现冗余机制？
  - Memcached 如何处理容错的？
  - 如何将 Memcached 中 item 批量导入导出？
  - 如果确实需要把 Memcached 中的 item 批量导出导入，怎么办？
  - Memcached 是如何做身份验证的？
  - Memcached 的多线程是什么？如何使用它们？
  - Memcached 能接受的 key 的最大长度是多少？
  - Memcached 对 item 的过期时间有什么限制？
  - Memcached 最大能存储多大的单个 item？
  - 为什么单个 item 的大小被限制在 1M byte 之内？
  - 可以在不同的 Memcached 节点上使用大小不等的缓存空间吗？如果这么做之后，Memcached 能够更有效地使用内存吗？
  - Memcached 的内存分配器是如何工作的？为什么不适用 malloc/free？为何要使用 slabs？
  - Memcached 是原子的吗？
  - 什么时候失效的数据项会从缓存中删除？
### Redis
#### 1、Redis 是什么？都有哪些使用场景？
  
1、Redis本质上是一个Key-Value类型的内存数据库，很像memcached，整个数据库统统加载在内存当中进行操作，定期通过异步操作把数据库数据flush到硬盘上进行保存。<br>
2、Redis最适合所有数据in-momory的场景，虽然Redis也提供持久化功能，但实际更多的是一个disk-backed的功能，跟传统意义上的持久化有比较大的差别。

那么可能大家就会有疑问，似乎Redis更像一个加强版的Memcached，那么何时使用Memcached，何时使用Redis呢?

如果简单地比较Redis与Memcached的区别，大多数都会得到以下观点：

Redis不仅仅支持简单的k/v类型的数据，同时还提供list，set，zset，hash等数据结构的存储。
Redis支持数据的备份，即master-slave模式的数据备份。
Redis支持数据的持久化，可以将内存中的数据保持在磁盘中，重启的时候可以再次加载进行使用。

（1）会话缓存（Session Cache）

最常用的一种使用Redis的情景是会话缓存（session cache）。

用Redis缓存会话比其他存储（如Memcached）的优势在于：Redis提供持久化。当维护一个不是严格要求一致性的缓存时，如果用户的购物车信息全部丢失，大部分人都会不高兴的，现在，他们还会这样吗？

幸运的是，随着 Redis 这些年的改进，很容易找到怎么恰当的使用Redis来缓存会话的文档。甚至广为人知的商业平台Magento也提供Redis的插件。

（2）全页缓存（FPC）

除基本的会话token之外，Redis还提供很简便的FPC平台。回到一致性问题，即使重启了Redis实例，因为有磁盘的持久化，用户也不会看到页面加载速度的下降，这是一个极大改进，类似PHP本地FPC。

再次以Magento为例，Magento提供一个插件来使用Redis作为全页缓存后端。

此外，对WordPress的用户来说，Pantheon有一个非常好的插件 wp-redis，这个插件能帮助你以最快速度加载你曾浏览过的页面。

（3）队列

Reids在内存存储引擎领域的一大优点是提供 list 和 set 操作，这使得Redis能作为一个很好的消息队列平台来使用。Redis作为队列使用的操作，就类似于本地程序语言（如Python）对 list 的 push/pop 操作。

如果你快速的在Google中搜索“Redis queues”，你马上就能找到大量的开源项目，这些项目的目的就是利用Redis创建非常好的后端工具，以满足各种队列需求。例如，Celery有一个后台就是使用Redis作为broker，你可以从这里去查看。

（4）排行榜/计数器

Redis在内存中对数字进行递增或递减的操作实现的非常好。集合（Set）和有序集合（Sorted Set）也使得我们在执行这些操作的时候变的非常简单，Redis只是正好提供了这两种数据结构。

所以，我们要从排序集合中获取到排名最靠前的10个用户–我们称之为“user_scores”。

当然，这是假定你是根据你用户的分数做递增的排序。如果你想返回用户及用户的分数，你需要这样执行：

```java
ZRANGE user_scores 0 10 WITHSCORES
```
Agora Games就是一个很好的例子，用Ruby实现的，它的排行榜就是使用Redis来存储数据的，你可以在这里看到。

（5）发布/订阅

最后（但肯定不是最不重要的）是Redis的发布/订阅功能。

发布/订阅的使用场景确实非常多，我已看见人们在社交网络连接中使用，还可作为基于发布/订阅的脚本触发器，甚至用Redis的发布/订阅功能来建立聊天系统！（不，这是真的，你可以去核实）。
　　
Redis提供的所有特性中，我感觉这个是喜欢的人最少的一个，虽然它为用户提供如此多功能。
#### 2、Redis 有哪些功能？
  
#### 3、Redis 和 memecache 有什么区别？
  - Master写内存快照，save命令调度rdbSave函数，会阻塞主线程的工作，当快照比较大时对性能影响是非常大的，会间断性暂停服务，所以Master最好不要写内存快照。
  - Master AOF持久化，如果不重写AOF文件，这个持久化方式对性能的影响是最小的，但是AOF文件会不断增大，AOF文件过大会影响Master重启的恢复速度。
Master最好不要做任何持久化工作，包括内存快照和AOF日志文件，特别是不要启用内存快照做持久化，如果数据比较关键，某个Slave开启AOF备份数据，策略为每秒同步一次。
  - Master调用BGREWRITEAOF重写AOF文件，AOF在重写的时候会占大量的CPU和内存资源，导致服务load过高，出现短暂服务暂停现象。
  - Redis主从复制的性能问题，为了主从复制的速度和连接的稳定性，Slave和Master最好在同一个局域网内。
    
#### 4、Redis 为什么是单线程的？
#### 5、什么是缓存穿透？怎么解决？
#### 6、Redis 支持的数据类型有哪些？
  - String、List、Set、Sorted Set、hash。
#### 7、Redis 支持的 java 客户端都有哪些？
  - Redisson、Jedis、lettuce等等，官方推荐使用Redisson。
#### 8、Jedis 和 redisson 有哪些区别？
  - Jedis是Redis的Java实现的客户端，其API提供了比较全面的Redis命令的支持；
  - Redisson实现了分布式和可扩展的Java数据结构，和Jedis相比，功能较为简单，不支持字符串操作，不支持排序、事务、管道、分区等Redis特性；       - Redisson的宗旨是促进使用者对Redis的关注分离，从而让使用者能够将精力更集中地放在处理业务逻辑上。
#### 9、怎么保证缓存和数据库数据的一致性？
#### 10、Redis 持久化有几种方式？
  - 1、快照（snapshots）

缺省情况情况下，Redis把数据快照存放在磁盘上的二进制文件中，文件名为dump。rdb。你可以配置Redis的持久化策略，例如数据集中每N秒钟有超过M次更新，就将数据写入磁盘；或者你可以手工调用命令SAVE或BGSAVE。

**工作原理**

  - Redis forks。
  - 子进程开始将数据写到临时RDB文件中。
  - 当子进程完成写RDB文件，用新文件替换老文件。
  - 这种方式可以使Redis使用copy-on-write技术。
- 2、AOF

快照模式并不十分健壮，当系统停止，或者无意中Redis被kill掉，最后写入Redis的数据就会丢失。这对某些应用也许不是大问题，但对于要求高可靠性的应用来说，Redis就不是一个合适的选择。

Append-only文件模式是另一种选择。你可以在配置文件中打开AOF模式。

- 3、虚拟内存方式

当你的key很小而value很大时，使用VM的效果会比较好。因为这样节约的内存比较大。当你的key不小时，可以考虑使用一些非常方法将很大的key变成很大的value，比如你可以考虑将key，value组合成一个新的value。
　　
vm-max-threads这个参数，可以设置访问swap文件的线程数，设置最好不要超过机器的核数，如果设置为0，那么所有对swap文件的操作都是串行的。可能会造成比较长时间的延迟，但是对数据完整性有很好的保证。

自己测试的时候发现用虚拟内存性能也不错。如果数据量很大，可以考虑分布式或者其他数据库
#### 11、Redis 怎么实现分布式锁？
#### 12、Redis 分布式锁有什么缺陷？
#### 13、Redis 如何做内存优化？
#### 14、Redis 淘汰策略有哪些？
#### 15Redis 常见的性能问题有哪些？该如何解决？

> 整理来源：
1、https://mp.weixin.qq.com/s/HMHTEv9WGgTDPtd-iaiEOA
2、https://juejin.im/post/5cb13b4d6fb9a0687b7dd0bd#heading-42


## 二、分布式服务框架
### Dubbo
  - Dubbo简介
  - 待续

## 三、分布式协调服务
### Zookeeper
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
  
## 四、分布式消息队列
### RabbitMQ
  - 什么是RabbitMQ?
  - 为什么要使用RabbitMQ?
  - 消息队列的优缺点？
  - RabbitMQ 与 Kafka 有什么区别？
  - RabbitMQ 的使用场景有哪些？
  - RabbitMQ 有哪些重要的角色？
  - RabbitMQ 有哪些重要的组件？
  - RabbitMQ 中 vhost 的作用是什么？
  - RabbitMQ 的消息是怎么发送的？
  - RabbitMQ 怎么保证消息的稳定性？
  - RabbitMQ 怎么避免消息丢失？
  - 要保证消息持久化成功的条件有哪些？
  - RabbitMQ 持久化有什么缺点？
  - RabbitMQ 有几种广播类型？
  - RabbitMQ 怎么实现延迟消息队列？
  - RabbitMQ 集群有什么用？
  - RabbitMQ 节点的类型有哪些？
  - RabbitMQ 集群搭建需要注意哪些问题？
  - RabbitMQ 每个节点是其他节点的完整拷贝吗？为什么？
  - RabbitMQ 集群中唯一一个磁盘节点崩溃了会发生什么情况？
  - RabbitMQ 对集群节点停止顺序有要求吗？
### Kafka
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

## 五、分布式搜索引擎

### Elasticsearch
  - Elasticsearch简介

### Solr
![Solr](https://github.com/bigrotor187/awesome-java-interview/blob/master/img/Solr.png)
  - [1、Solr简介](https://github.com/bigrotor187/awesome-java-interview/blob/master/distributed%20system/README.md#1solr%E7%AE%80%E4%BB%8B)
  - [2、简述Solr的倒排索引](https://github.com/bigrotor187/awesome-java-interview/tree/master/distributed%20system#2%E7%AE%80%E8%BF%B0solr%E7%9A%84%E5%80%92%E6%8E%92%E7%B4%A2%E5%BC%95)
  - [3、为什么要使用Solr?](https://github.com/bigrotor187/awesome-java-interview/tree/master/distributed%20system#3%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E4%BD%BF%E7%94%A8solr)
  - [4、Solr和elasticsearch的区别？](https://github.com/bigrotor187/awesome-java-interview/tree/master/distributed%20system#4solr%E5%92%8Celasticsearch%E7%9A%84%E5%8C%BA%E5%88%AB)
  
#### 1、Solr简介
  - Solr 是一个 Java 开发的基于 Lucene 的`企业级`、`开源`、`全文搜索`平台。它采用的是`反向索引`，即从关键字到文档的映射过程。 
  - Solr 的资源`Document`为对象进行存储，每个文档由一系列的`Field`构成，每个`Field`表示资源的一个属性。 文档的`Field`可以被索引，以提供高性能的搜索效率。 一般情况下文档都包含一个能唯一表示该文档的id字段。
  
#### 2、简述Solr的倒排索引
  - 倒排索引就是从文档内容到文档序号的过程，将文档内容用solr自带分词器进行分词，然后作为索引，用二分法将关键字与排序号的索引进行匹配，进而查找到对应文档。
  
 > 【注】可参考：1、https://blog.csdn.net/chunlei_zhang/article/details/38520315<br>
 2、https://blog.csdn.net/hu948162999/article/details/42463043</font>
#### 3、为什么要使用Solr?
- Solr 是一个 Java 开发的基于 Lucene 的`企业级`、`开源`、`全文搜索`平台，严格来说，Lucene 负责数据存储，而 Solr 作为一个引擎提供搜索和插入功能，跟数据库的解释器是一样的。但是，如果数据库中有一个字段存了很长的文本，比如存了 1000 个汉字，现在想要从中搜一个词的时候，普通的数据库会使用 like 去查询，遍历整个文本去模糊匹配，效率很低。
- 所以，为了解决这个问题，自然而然地使用全文搜索工具是最好地。比如 lucene 所作的就是分词，然后去匹配分词的词中是否有想搜的词即可。而 Solr 正是基于 Lucene 实现的，使用 Solr 的检索功能可以大大提高检索效率。
#### 4、Solr和elasticsearch的区别？
- 共同点：
    - solr 和 elasticsearch 都是基于 Lucene 实现的。
- 不同点：
  - 1、solr 利用 zookeeper 进行分布式管理，而 elasticsearch 自身带有分布式协调管理功能；
  - 2、solr 比 elasticsearch 实现更加全面，solr 官方提供的功能更多，而 elasticsearch 本身更注 重于核心功能，高级功能多由第三方插件提供；
  - 3、solr 在传统的搜索应用中表现好于 elasticsearch，而 elasticsearch 在实时搜索应用方面比 solr 表现好。
- 最后有必要说明一下传统搜索和实时搜索：
  - 传统搜索是从静态数据库中筛选出符合条件的结果，这种结果往往是不可变得、静态的。而实时搜索则是说用户对于搜索的结果是实时变化的。
  - 传统搜索比如电商这种，实时搜索参考谷歌，百度，这种实时搜索。

## 六、分布式事务
- 刚性分布式事务
- 柔性分布式事务
- 两阶段提交协议&三阶段提交协议
- 一致性哈希算法
