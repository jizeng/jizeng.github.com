# 曾吉/Zeng Ji
--
> MAIL:　braveji8@gmail.com  
> TEL :　18210219928   
> Blog:　[https://github.com/jizeng](https://github.com/jizeng)

--

### 教育经历
>西安电子科技大学 　导航、制导控制　　　　　硕士　　　　　　　2013.09－2016.01  
>西安电子科技大学 　电子信息科学与技术　　　本科　　　　　　　2009.09－2013.06

--
### 工作经历
>####北京嘀嘀无限科技发展有限公司 　　　　　　　　　　　　　2016.02--至今
>**(一) 额度管控系统**   
>**简介**：员工额度、企业额度等各种额度的配置与扣减管理；  
>**特点**：存在**并发**请求，**准确性**及**幂等性**要求高；   
>**设计**：  
>　　1、使用Redis的**分布式锁setnx**从业务层保证并发的更新操作不会丢失更新；  
>　　2、使用Innodb的**排他锁（Record Lock算法）**作为兜底方案；  
>　　3、使用Innodb的**当前读（非MVCC）**确保日志中更新前后额度数据的准确性；   
>**职责**：模块owner  
>　　1、设计额度表结构；  
>　　2、设计各类锁防止丢失更新；  
>　　3、设计幂等操作实现，防止二次更新；   
>**效果**：保障了订单和账单数据的**一致性**，每月账单额度管控**正确无误**；保障了额度管理的**准确性**；基于此企业回款效率增加了**2d+**;
>
>**(二) 规则管控系统**   
>**简介**： 用车规则(如用车时间，上下车地点等)、敏感规则(附加费超出，预估里程超出)等各种规则的配置管理；  
>**特点**： **B端**后台管控业务；部分管控逻辑互相**依赖及耦合**，业务较为**复杂**；  
>**设计**：   
>　　1、以用车规则为基准核心；增加任意其他管控规则时，单独设计其实现并增加其与用车规则的映射关系；  
>　　2、基于 **binlog + kafka + es** 打造日志存储模块，实现部分业务日志与业务操作的分离；   
>**职责**：模块owner   
>　　1、抽象新增的管控规则模型，并设计与实现；  
>　　2、协助优化由于索引导致的慢查询；  
>**效果**：支持管控规则相关的产品能够**快速迭代**，**白名单快速试错**的效率提升至**60%+**；单条数据的历史操作记录**清晰明了**；删除了大批**冗余索引**，部分线上大查询切换至**离线库**或者ES，及相关**索引优化**，线上大查询**几乎降为0**；
>
>**(三) 用车鉴权系统**  
>**简介**：企业员工用车时，是否符合管理员给员工配合的各种管控限制；  
>**特点**：**C 端**用户产品，**QPS高**；**稳定性，可用性**要求高；  
>**设计**：  
>　　1、基于redis缓存的业务架构；  
>　　2、业务逻辑封装，组件化；  
>　　3、业务收敛，黑盒接口输出；  
>**职责**：模块owner  
>　　1、将之前过程式的写法重构，业务逻辑封装为一个个组件，并归纳分类；  
>　　2、熟悉APP企业用车的整个流程，故障时能够快速定位问题，并给出解决方案；   
>**效果**：实现了企业员工用车的**高可用**，及**稳定性**；组件化及配合app改版之后，企业支付相关的问题反馈**从42%下降至10%**。
>   

--
### 技术特长
> 1、熟悉MySQL；对Innodb的**索引、事务、MVCC、锁**等有一定的见解。   
> 2、熟悉Redis；对其**底层数据结构、持久化、阻塞、事件触发、集群**等有一定的见解。   
> 3、熟练使用PHP；对其内部**三层架构**有一定的见解。  
> 4、熟悉常用的中间件；如kafka，elasticsearch等。  
> 5、熟悉常见的高可用高并发策略；如负载均衡、限流、降级、缓存、异步、扩容等。  
> 6、扎实的基础知识；如数据结构；算法；Linux；OOP；设计模式。  
> 7、具备一定的项目管理知识，正在获取PMP认证。

--
### 个人评价
>1、热爱学习与分享。创办《九点读书会》兴趣小组；并在部门内部多次输出与分享，如mysql系列（innodb的索引，innodb的事务）、redis系列（数据结构、网络模型）、高可用系列（超时分析、高可用策略）等；   
>2、热爱沟通与交流。积极参加部门组织活动的主持人，以及内部talk show；非常喜欢参与运营、销售、产品的拜见客户活动，从而站在更深层次对研发的产品进行审视；  
>3、活泼与可爱。定期参与各种运动，羽毛球，桌球等；语言较为幽默得体。

--




