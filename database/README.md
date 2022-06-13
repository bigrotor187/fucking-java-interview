# MySQL 学习笔记

## 《MySQL是怎样运行的——从根儿上理解MySQL》

- [1、MySQL 概述]()
- [2、MySQL 查询请求执行过程]()
- [3、常用存储引擎]()
- [4、字符集和比较规则]()
- [5、InnoDB 是如何存储一条数据记录的？]()
- [6、InnoDB 数据页结构]()
- [7、快速查询的秘籍——B+ 树索引简介]()
- [8、B+ 树索引是如何使用的？]()
- [9、MySQL 的数据目录]()
- [10、存放页面的大池子——InnoDB 的表空间]()
- [11、MySQL 单表是如何访问的？]()
- [12、连接的原理及查询成本的优化]()
- [13、MySQL 基于规则的优化与子查询优化]()
- [14、EXPLAIN 详解]()
- [15、InnoDB 的 Buffer Pool——条件磁盘和 CPU 的矛盾]()
- [16、MySQL 事务简介]()
- [17、redo 日志]()
- [18、undo 日志]()
- [19、事务隔离级别和 MVCC]()
- [20、面试老大难——锁]()


# MySQL 实战案例
- [1、MySQL 加锁分析](http://www.fanyilun.me/2017/04/20/MySQL%E5%8A%A0%E9%94%81%E5%88%86%E6%9E%90/)
- [2、常见 MySQL 死锁案例](https://github.com/aneasystone/mysql-deadlocks)


# MySQL 面试问题

  - [1、数据库的三范式是什么？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#1%E6%95%B0%E6%8D%AE%E5%BA%93%E7%9A%84%E4%B8%89%E8%8C%83%E5%BC%8F%E6%98%AF%E4%BB%80%E4%B9%88)
  - [2、一张自增表里面总共有 7 条数据，删除了最后 2 条数据，重启 mysql 数据库，又插入了一条数据，此时 id 是几？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#2%E4%B8%80%E5%BC%A0%E8%87%AA%E5%A2%9E%E8%A1%A8%E9%87%8C%E9%9D%A2%E6%80%BB%E5%85%B1%E6%9C%89-7-%E6%9D%A1%E6%95%B0%E6%8D%AE%E5%88%A0%E9%99%A4%E4%BA%86%E6%9C%80%E5%90%8E-2-%E6%9D%A1%E6%95%B0%E6%8D%AE%E9%87%8D%E5%90%AF-mysql-%E6%95%B0%E6%8D%AE%E5%BA%93%E5%8F%88%E6%8F%92%E5%85%A5%E4%BA%86%E4%B8%80%E6%9D%A1%E6%95%B0%E6%8D%AE%E6%AD%A4%E6%97%B6-id-%E6%98%AF%E5%87%A0)
  - [3、如何获取当前数据库版本？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#3%E5%A6%82%E4%BD%95%E8%8E%B7%E5%8F%96%E5%BD%93%E5%89%8D%E6%95%B0%E6%8D%AE%E5%BA%93%E7%89%88%E6%9C%AC)
  - [4、说一下 ACID 是什么？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#4%E8%AF%B4%E4%B8%80%E4%B8%8B-acid-%E6%98%AF%E4%BB%80%E4%B9%88)
  - [5、char 和 varchar 的区别是什么？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#5char-%E5%92%8C-varchar-%E7%9A%84%E5%8C%BA%E5%88%AB%E6%98%AF%E4%BB%80%E4%B9%88)
  - [6、float 和 double 的区别是什么？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#6float-%E5%92%8C-double-%E7%9A%84%E5%8C%BA%E5%88%AB%E6%98%AF%E4%BB%80%E4%B9%88)
  - [7、mysql 的内连接、左连接、右连接有什么区别？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#7mysql-%E7%9A%84%E5%86%85%E8%BF%9E%E6%8E%A5%E5%B7%A6%E8%BF%9E%E6%8E%A5%E5%8F%B3%E8%BF%9E%E6%8E%A5%E6%9C%89%E4%BB%80%E4%B9%88%E5%8C%BA%E5%88%AB)
  - [8、mysql 索引是怎么实现的？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#8mysql-%E7%B4%A2%E5%BC%95%E6%98%AF%E6%80%8E%E4%B9%88%E5%AE%9E%E7%8E%B0%E7%9A%84)
  - [9、怎么验证 mysql 的索引是否满足需求？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#9%E6%80%8E%E4%B9%88%E9%AA%8C%E8%AF%81-mysql-%E7%9A%84%E7%B4%A2%E5%BC%95%E6%98%AF%E5%90%A6%E6%BB%A1%E8%B6%B3%E9%9C%80%E6%B1%82)
  - [10、说一下数据库的事务隔离？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#10%E8%AF%B4%E4%B8%80%E4%B8%8B%E6%95%B0%E6%8D%AE%E5%BA%93%E7%9A%84%E4%BA%8B%E5%8A%A1%E9%9A%94%E7%A6%BB)
  - [11、说一下 mysql 常用的引擎？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#11%E8%AF%B4%E4%B8%80%E4%B8%8B-mysql-%E5%B8%B8%E7%94%A8%E7%9A%84%E5%BC%95%E6%93%8E)
  - [12、说一下 mysql 的行锁和表锁？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#12%E8%AF%B4%E4%B8%80%E4%B8%8B-mysql-%E7%9A%84%E8%A1%8C%E9%94%81%E5%92%8C%E8%A1%A8%E9%94%81)
  - [13、说一下乐观锁和悲观锁？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#13%E8%AF%B4%E4%B8%80%E4%B8%8B%E4%B9%90%E8%A7%82%E9%94%81%E5%92%8C%E6%82%B2%E8%A7%82%E9%94%81)
  - [14、mysql 问题排查都有哪些手段？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#14mysql-%E9%97%AE%E9%A2%98%E6%8E%92%E6%9F%A5%E9%83%BD%E6%9C%89%E5%93%AA%E4%BA%9B%E6%89%8B%E6%AE%B5)
  - [15、如何做 mysql 的性能优化？](https://github.com/bigrotor187/awesome-java-interview/tree/master/database#15%E5%A6%82%E4%BD%95%E5%81%9A-mysql-%E7%9A%84%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96)
  
  ## 1、数据库的三范式是什么？
  - **第一范式:** 每个列都不可以再拆分。

- **第二范式:** 非主键列完全依赖于主键,而不能是依赖于主键的一部分.。

- **第三范式:** 非主键列只依赖于主键,不依赖于其他非主键。

在设计数据库结构的时候，要尽量遵守三范式，如果不遵守，必须有足够的理由，比如性能。事实上我们经常会为了性能而妥协数据库的设计。

  ## 2、一张自增表里面总共有 7 条数据，删除了最后 2 条数据，重启 mysql 数据库，又插入了一条数据，此时 id 是几？
  - 一般情况下，MySQL 中创建表的类型为 InnoDB，如果新增一条记录（在 MySQL 不重启的情况下），这条记录的 ID 为 8；但是，如果**重启 MySQL 的情况下**，那么这条记录的 ID 为
  6，因为 InnoDB 表只把自增主键的最大 ID 记录到内存中，所以重启数据库或者对表执行 OPTIMIZE 操作，都会使最大 ID 丢失。
  - 如果我们设置表的类型是 MyISAM，那么这条记录的 ID 就是 8。因为MylSAM表会把自增主键的最大ID记录到数据文件里面，重启MYSQL后，自增主键的最大ID也不会丢失。
  - 如果在这 7 条记录里面删除的是中间的几个记录（比如删除的是 3,4,5 三条记录），重启 MySQL 数据库后，insert 一条记录后，ID 都是 8。因为内存或者数据库文件存储的都是自增主键的最大 ID。

  ## 3、如何获取当前数据库版本？
  - 一、使用命令行模式进入mysql会看到最开始的提示符：
  
  ![](https://github.com/bigrotor187/awesome-java-interview/blob/master/img/MySQL%E5%91%BD%E4%BB%A4%E8%A1%8C%E6%9F%A5%E7%9C%8B%E7%89%88%E6%9C%AC%E5%8F%B7.jpg)
  
  - 二、命令行中使用 status 可以查看：
  
  ![](https://github.com/bigrotor187/awesome-java-interview/blob/master/img/status%E6%9F%A5%E7%9C%8B%E7%89%88%E6%9C%AC%E5%8F%B7.jpg)
  
  - 三、使用系统函数 version()：
  
  ![](https://github.com/bigrotor187/awesome-java-interview/blob/master/img/%E7%B3%BB%E7%BB%9F%E5%87%BD%E6%95%B0%E6%9F%A5%E7%9C%8B%E7%89%88%E6%9C%AC%E5%8F%B7.jpg)

## 4、说一下 ACID 是什么？
  
  - ACID 指的是事务 的四大特性，分别是`原子性（Atomicity）`、`一致性（Consistency）`、`隔离性（Isolation）`、`永久性（Durability）`。
    - **原子性：** 原子性是指事务是一个不可分割的工作单位，事务中的操作要么全部成功，要么全部失败。比如在同一个事务中的SQL语句，要么全部执行成功，要么全部执行失败。
    - **一致性：** 官网上事务一致性的概念是：事务必须使数据库从一个一致性状态变换到另外一个一致性状态。以转账为例子，A向B转账，假设转账之前这两个用户的钱加起来总共是2000，那么A向B转账之后，不管这两个账户怎么转，A用户的钱和B用户的钱加起来的总额还是2000，这个就是事务的一致性。
    - **隔离性：** 事务的隔离性是多个用户并发访问数据库时，数据库为每一个用户开启的事务，不能被其他事务的操作数据所干扰，多个并发事务之间要相互隔离。
    - **永久性：** 持久性是指一个事务一旦被提交，它对数据库中数据的改变就是永久性的，接下来即使数据库发生故障也不应该对其有任何影响。

## 5、char 和 varchar 的区别是什么？

  - **是否是定长的：** char 是一个定长字段，假如申请了char(10) 的空间，那么无论实际存储多少内容，该字段都占用 10 个字符。而 varchar 是变长的，也就是说申请的只是最大长度，占用的空间为实际字符长度 +1，最后一个字符存储使用了多长的空间。

- **从检索效率上来讲**，char > varchar，因此在使用中如果确定某个字段的值的长度，可以使用 char，否则应该尽量使用 varchar。例如存储用户MD5加密后的密码，则应该使用 char。

## 6、float 和 double 的区别是什么？

- float类型表示单精度浮点数值，double类型表示双精度浮点数值，float和double都是浮点型，而decimal是定点型；
- MySQL 浮点型和定点型可以用类型名称后加（M，D）来表示，M表示该值的总共长度，D表示小数点后面的长度，M和D又称为精度和标度，如float(5,2)的 可显示为999.99，MySQL保存值时会进行四舍五入，如果插入999.009，则结果为999.01。
- float和double在不指定精度时，默认会按照实际的精度来显示，而DECIMAL在不指定精度时，默认整数为10，小数为0。

> 具体可参考：https://blog.csdn.net/lihua5419/article/details/81316914

  ## 7、MySQL 的内连接、左连接、右连接有什么区别？
  
  - 左连接：左边有的，右边没有的为 null

  - 右连接：左边没有的，右边有的为 null

  - 内连接：显示左边右边共有的
  
  > 具体请移步: https://blog.csdn.net/wang0112233/article/details/78418698

  ## 8、MySQL 索引是如何实现的？
  
  - 索引的数据结构和具体的数据库存储引擎的实现有关，在 MySQL 中使用较多的索引有哈希索引、BTree索引等。其中，哈希索引底层数据结构使用的是哈希表，而BTree索引使用的是B树中的B+Tree。在 MySQL 中，经常使用的 InnoDB 存储引擎的默认索引实现为：BTree索引。
  - 创建索引时，建议对如下情况创建：
    - 出现在 SELECT、UPDATE、DELETE 语句的 WHERE 从句中的列
    - 包含在 ORDER BY、GROUP BY、DISTINCT 中的字段
    - 并不要将符合 1 和 2 中的字段的列都建立一个索引， 通常将 1、2 中的字段建立联合索引效果更好
    - 多表 join 的关联列
    
  常见的索引类型有：主键索引、唯一索引、普通索引、全文索引、组合索引

  1、主键索引：即主索引，根据主键pk_clolum（length）建立索引，不允许重复，不允许空值；
  `ALTER TABLE `table_name` ADD PRIMARY KEY (`column`);`

  2、唯一索引：用来建立索引的列的值必须是唯一的，允许空值
  `ALTER TABLE `table_name` ADD UNIQUE (`column`) ;`

  3、普通索引：用表中的普通列构建的索引，没有任何限制
   `ALTER TABLE `table_name` ADD INDEX index_name (`column`);`

  4、全文索引：用大文本对象的列构建的索引
  `ALTER TABLE `table_name` ADD FULLTEXT (`column`);`

  5、组合索引：用多个列组合构建的索引，这多个列中的值不允许有空值
  `ALTER TABLE `table_name` ADD INDEX index_name (`column1`, `column2`, `column3`);`

  ## 9、怎么验证 MySQL 的索引是否满足需求？或者换个说法，如何判断创建的索引有没有被使用到?或者说怎么才可以知道这条语句运行很慢的原因?
  
  需要根据查询需求来决定配置索引的类型，一旦确定索引类型之后，可以使用 EXPLAIN 查看 SQL 执行计划，确认索引是否满足需求。
  
  - MySQL提供了 EXPLAIN 命令来查看语句的执行计划，MySQL在执行某个语句之前，会将该语句过一遍查询优化器，之后会拿到对语句的分析,也就是执行计划，其中包含了许多信息。可以通过其中和索引有关的信息来分析是否命中了索引，例如 possilbe_key，key，key_len 等字段,分别说明了此语句可能会使用的索引，实际使用的索引以及使用的索引长度。具体过程如下:
  
    - 在 select 语句前加上 explain 就可以用来查看 sql 的执行计划，EXPLAIN 显示了 MySQL 如何使用索引来处理 select 语句以及连接表;

    - possible_keys：显示可能应用在这张表中的索引。如果为空，没有可能的索引。可以为相关的域从WHERE语句中选择一个合适的语句

    - key： 实际使用的索引。如果为 NULL，则没有使用索引。很少的情况下，MySQL 会选择优化不足的索引。这种情况下，可以在 SELECT 语句中使用 USE INDEX(indexname) 来强制使用一个索引或者用IGNORE INDEX(indexname)来强制MYSQL忽略索引
  
  最后,虽然 EXPLAIN 可以检查我们的 SQL 索引命中情况，但实际上线后，最好配合监控来看下接口的 RT。

  ## 10、说一下数据库的事务隔离？
  
多个线程开启各自事务操作数据库中数据时，数据库系统要负责隔离操作，以保证各个线程在获取数据时的准确性。

**1、事务不考虑隔离性可能会引发的问题**

如果事务不考虑隔离性，可能会引发如下问题：

- （1）脏读
脏读指一个事务读取了另外一个事务未提交的数据。

这是非常危险的，假设Ａ向Ｂ转帐100元，对应sql语句如下所示

```java
1.update account set money=money+100 where name='B';    
2.update account set money=money-100  where name='A';
```
当第1条 SQL 执行完，第2条还没执行(A 未提交时)，如果此时 Ｂ 查询自己的帐户，就会发现自己多了 100 元钱。如果 A 等 B 走后再回滚，B 就会损失 100 元。

- （2）不可重复读
不可重复读指在一个事务内读取表中的某一行数据，多次读取结果不同。

例如银行想查询 A 帐户余额，第一次查询A帐户为 200 元，此时A向帐户内存了 100 元并提交了，银行接着又进行了一次查询，此时 A 帐户为 300 元了。银行两次查询不一致，可能就会很困惑，不知道哪次查询是准的。

不可重复读和脏读的区别是，脏读是读取前一事务未提交的脏数据，不可重复读是重新读取了前一事务已提交的数据。

很多人认为这种情况就对了，无须困惑，当然是后面的为准。我们可以考虑这样一种情况，比如银行程序需要将查询结果分别输出到电脑屏幕和写到文件中，结果在一个事务中针对输出的目的地，进行的两次查询不一致，导致文件和屏幕中的结果不一致，银行工作人员就不知道以哪个为准了。

- （3）虚读(幻读)
虚读(幻读)是指在一个事务内读取到了别的事务插入的数据，导致前后读取不一致。

如丙存款 100 元未提交，这时银行做报表统计 account 表中所有用户的总额为 500 元，然后丙提交了，这时银行再统计发现帐户为 600 元了，造成虚读同样会使银行不知所措，到底以哪个为准。

注：以下为在原文的基础上补充的部分

- （4）丢失修改
丢失修改（Lost to modify）是指在一个事务读取一个数据时，另外一个事务也访问了该数据，那么在第一个事务中修改了这个数据后，第二个事务也修改了这个数据。这样第一个事务内的修改结果就被丢失，因此称为丢失修改。 

例如：事务 1 读取某表中的数据 A=20，事务 2 也读取 A=20，事务 1 修改 A=A-1，事务 2 也修改 A=A-1，最终结果 A=19，事务 1 的修改被丢失。

*不可重复读和幻读区别：*

不可重复读的重点是修改，比如多次读取一条记录发现其中某些列的值被修改；幻读的重点在于新增或者删除，比如多次读取一条记录发现记录增多或减少了。

  ## 11、说一下 MySQL 常用的引擎？
  
  MySQL 常用的引擎主要有`InnoDB`和`MyISQM`两种，其中，在 5.5 版本之前，`MyISAM`是 MySQL 默认的数据库引擎，而 5.5 版本之后默认的数据库引擎是`InnoDB`。`MyISAM`强调的是性能，性能极佳，并且提供了大量的特性，比如全文索引、压缩、空间函数等，但是`MyISAM`不支持事务和行级锁，最大的缺陷就是不支持崩溃后的安全恢复。两者的区别主要如下：
  - **是否支持行级锁** : MyISAM 只有表级锁(table-level locking)，而InnoDB 支持行级锁(row-level locking)和表级锁，默认为行级锁；
  - **是否支持外键**： MyISAM不支持，而InnoDB支持；
  - **是否支持事务和崩溃后的安全恢复**：MyISAM 强调的是性能，每次查询具有原子性,其执行速度比 InnoDB 类型更快，但是不提供事务支持。而 InnoDB 提供事务支持，外键等高级数据库功能。 具有事务(commit)、回滚(rollback)和崩溃修复能力(crash recovery capabilities)的事务安全(transaction-safe (ACID compliant))型表。
  - **是否支持MVCC**：仅 InnoDB 支持 MVCC。应对高并发事务，MVCC比单纯的加锁更高效；MVCC只在 READ COMMITTED 和 REPEATABLE READ 两个隔离级别下工作；MVCC可以使用`乐观(optimistic)锁`和`悲观(pessimistic)锁`来实现；各数据库中MVCC实现并不统一。
  
  **那么这两种数据库引擎要如何选择呢？**
  
  - 一般情况下选择 InnoDB 都是没有问题的，但是某些情况下如果并不在乎可扩展能力和并发能力，也不需要事务支持，也不在乎崩溃后的安全恢复问题的话，选择 MyISAM 也是一个不错的选择。但是一般情况下，我们都是需要考虑到这些问题的。

  ## 12、说一下 MySQL 的行级锁和表级锁？
  
  - MyISAM 默认采用的是表级锁（table-level locking），而 InnoDB 支持行级锁（row-level locking）和表级锁，但默认采用的是行级锁。
  - **表级锁：** MySQL 中锁定`粒度最大`的一种锁，对当前操作的整张表加锁，实现简单，资源消耗也比较少，加锁快，不会出现死锁。其锁定粒度最大，触发锁冲突的概率最高，并发度最低，MyISAM和 InnoDB引擎都支持表级锁。
  - **行级锁：** MySQL中锁定`粒度最小`的一种锁，只针对当前操作的行进行加锁。 行级锁能大大减少数据库操作的冲突。其加锁粒度最小，并发度高，但加锁的开销也最大，加锁慢，会出现死锁。
  
  **InnoDB 引擎中锁的算法有三种：**
  - Record lock：单个行记录上的锁
  - Gap lock：间隙锁，锁定一个范围，不包括记录本身
  - Next-key lock：record+gap 锁定一个范围，包含记录本身

  ## 13、说一下乐观锁和悲观锁？
  
**乐观锁**

- 乐观锁不是数据库自带的，需要我们自己去实现。乐观锁是指操作数据库时(更新操作)，想法很乐观，认为这次的操作不会导致冲突，在操作数据时，并不进行任何其他的特殊处理（也就是不加锁），而在进行更新后，再去判断是否有冲突了。

- 通常实现是这样的：在表中的数据进行操作时(更新)，先给数据表加一个版本(version)字段，每操作一次，将那条记录的版本号加1。也就是先查询出那条记录，获取出version字段,如果要对那条记录进行操作(更新),则先判断此刻version的值是否与刚刚查询出来时的version的值相等，如果相等，则说明这段期间，没有其他程序对其进行操作，则可以执行更新，将version字段的值加1；如果更新时发现此刻的version值与刚刚获取出来的version的值不相等，则说明这段期间已经有其他程序对其进行操作了，则不进行更新操作。

**悲观锁**

- 与乐观锁相对应的就是悲观锁了。悲观锁就是在操作数据时，认为此操作会出现数据冲突，所以在进行每次操作时都要通过获取锁才能进行对相同数据的操作，这点跟java中的synchronized很相似，所以悲观锁需要耗费较多的时间。另外与乐观锁相对应的，悲观锁是由数据库自己实现了的，要用的时候，我们直接调用数据库的相关语句就可以了。

- 说到这里，由悲观锁涉及到的另外两个锁概念就出来了，它们就是共享锁与排它锁。共享锁和排它锁是悲观锁的不同的实现，它俩都属于悲观锁的范畴。

> 引自: https://www.cnblogs.com/zousong/p/10513372.html

  ## 14、MySQL 问题排查都有哪些手段？
  
  详情可参考: https://juejin.im/post/5c8375bc5188257fdd0bd252#heading-14

  ## 15、如何做 MySQL 的性能优化？
  
  这个问题太大了,具体可以参考[Mysql高性能优化规范建议](https://www.cnblogs.com/huchong/p/10219318.html)，不过一般对于 MySQL 方面的优化问题,很多时候指的是 SQL 查询很慢之类的问题,对于这类问题怎么分析呢?
  
在业务系统中,除了使用主键进行的查询,其他的我都会在测试库上测试其耗时,慢查询的统计主要由运维在做,会定期将业务中的慢查询反馈给我们.

慢查询的优化首先要搞明白慢的原因是什么? 是查询条件没有命中索引?是 load 了不需要的数据列?还是数据量太大?

所以优化也是针对这三个方向来的:

- 首先分析语句,看看是否 load 了额外的数据,可能是查询了多余的行并且抛弃掉了,可能是加载了许多结果中并不需要的列,对语句进行分析以及重写.
- 分析语句的执行计划,然后获得其使用索引的情况,之后修改语句或者修改索引,使得语句可以尽可能的命中索引.
- 如果对语句的优化已经无法进行,可以考虑表中的数据量是否太大,如果是的话可以进行横向或者纵向的分表.

如果有时间,推荐看这篇更详细的文章分析 [一条SQL语句执行得很慢的原因有哪些？](https://mp.weixin.qq.com/s?__biz=Mzg2OTA0Njk0OA==&mid=2247485185&idx=1&sn=66ef08b4ab6af5757792223a83fc0d45&chksm=cea248caf9d5c1dc72ec8a281ec16aa3ec3e8066dbb252e27362438a26c33fbe842b0e0adf47&token=79317275&lang=zh_CN#rd)
  
  > 参考来源:https://mp.weixin.qq.com/s/l9up2dlPniOYO4usoe-dFA
