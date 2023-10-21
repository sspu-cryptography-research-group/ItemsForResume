# ItemsForResume
可以用在简历上的项目
## 基础架构方面
1. CMU15-445(C++)   
   课程地址：https://15445.courses.cs.cmu.edu/fall2023/assignments.html   
   课程简介：实现一个simple的数据库，其中包含使用可扩展哈希、LRU-K、B+树、算子（Agg、Insert等）、加解锁、死锁检测   
   参考代码：   
   课程讲解：[moody老师PPT讲解](https://www.bilibili.com/video/BV1bQ4y1Y7iT/?spm_id_from=333.999.0.0&vd_source=794854cc093032754621b2943dbdb87e)  
   简历参考：
   ```
   主要工作：
   - 给予可扩展哈希表和lru-k设计了Buffer pool，实现了Buffer pool的页面调度功能；
   - 基于B+树实现了非聚簇索引和迭代器功能，并利用每个节点独立的读写锁兼顾了多线程并发访问的安全性和效率；
   - 采用火山模型，实现了多种语句的执行层事务，如SELECT、INSERT、GROUP BY、JOIN等；
   - 给予2PL设计了锁管理器，支持RR、RC、RU三种隔离级别和表、行锁两种粒度的五种意向锁，实现对死锁的检测和处理；
   ```
3. MIT6.824（Go）   
   课程地址：      
   课程简介：实现一个基于Go、Raft的分布式kv数据库     
   参考代码：      
   课程讲解：   
   简历参考：   
   ```
   主要工作：
   – 实现Multi-Raft架构，支持数据分片处理以及分片迁移处理；
   – Raft支持Leader选举、日志复制、Snapshot等基本功能。
   ```
5. MIT6.S081（C）   
6. rCore（Rust）
7. pingcap plan（Rust、Go）
   6.1 
8. simpleSearch（Go）
9. searchKV（GO）   
   课程地址：      
   课程简介：实现一个基于LSM-Tree的单机存储引擎，参考Wiskey论文实现KV分离的特性     
   参考代码：      
   课程讲解：   
   简历参考：   
   ```
   主要工作：
   – 使用跳表将新插入的数据进行有序管理，并通过内存池的方式减少频繁向系统申请存储的时间开销；
   – 实现W-TinyLFU缓存热点数据并能够应对突发稀疏流量、实现布隆过滤器加速磁盘查询过程；
   – 层级合并过程中，进行了并行处理的优化，对比Level DB，极大地提高了Compact模块的速度；
   – 基于Wisckey实现以vlog file和gc的为核心的KV分离特性，以此减少LSM-Tree存在的读写放大问题。
   ```
11. AsyncFlow（Rust）   
   课程地址：      
   课程简介：实现一个基于Rust开发的支持任务自动调度、自动续作、灵活任务配置的异步任务处理框架
   参考代码：      
   课程讲解：   
   简历参考：   
     ```
     主要工作：
     – 将框架设计为生产者-消费者模型，使用自定义排序和上下文加载逻辑满足通用性设计；
     – 抽象出orderTime对任务排序规则以及优先级进行解耦，设置为提前多少秒执行；
     – 使用Redis分布式锁减少多机竞争任务时发生冲突导致压力不稳定、CPU飚高、消耗剧烈等问题；
     ```
