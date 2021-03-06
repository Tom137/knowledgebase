# 事务
## 目录
#### 1. 传统事务
##### 1.1 特性
##### 1.2 隔离级别
##### 1.3 事务日志
##### 1.4 事务模式
##### 1.5 用法

#### 2. 分布式事务
##### 2.1 CAP理论
##### 2.2 强一致性 - 两阶段提交
##### 2.3 最终一致性 - BASE

## 1. 传统事务
### 1.1 特性
+ 原子性（Atomicity）
+ 一致性（Consistency）
+ 隔离性（Isolation）
+ 持久性（Durability）

### 1.2 隔离级别
+ Read uncommitted
+ Read committed
+ Repeatable read
+ Serializable

### 1.3 事务日志

### 1.4 事务模式
+ auto commit
+ 显式事务
+ 隐藏式事务
### 1.5 用法
+ begin tran
+ commit tran
+ save tran
+ rollback tran

## 2. 分布式事务

### 2.1 CAP理论

+ 一致性（C）：在分布式系统中的所有数据备份，在同一时刻是否同样的值。（等同于所有节点访问同一份最新的数据副本）  
+ 可用性（A）：在集群中一部分节点故障后，集群整体是否还能响应客户端的读写请求。（对数据更新具备高可用性）  
+ 分区容忍性（P）：以实际效果而言，分区相当于对通信的时限要求。系统如果不能在时限内达成数据一致性，就意味着发生了分区的情况，必须就当前操作在C和A之间做出选择。

##### 2.2 # 强一致性 - 两阶段提交（XA规范）
###### 2.2.1 阶段
+ prepare
+ commit

###### 2.2.2 实现
+ 关系型数据库
+ JTA

##### 2.3 最终一致性 - BASE
###### 2.3.1 特点
+ 异步协调事务
+ 不保证何时能达到数据一致

###### 2.3.2 实现
基于消息的分布式事务
https://segmentfault.com/a/1190000011479826


