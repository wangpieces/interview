# interview
java面试题整理

1 Spring事物的传播属性和隔离级别

2 分布式锁实现方式

3 CAP简介

4 什么是幂等性

5 SQL语句的执行顺序

6 简述一下HTTP请求的在客户端和服务端的请求过程

7 线程的实现方式、什么是锁重入

8 简述一下生产者消费者模式。

9 JVM运行时划分

10 单体应用和微服务的区别和目前实现方式

11 谈谈dubbo

12 开发中Java用了比较多的数据结构有哪些

13 谈谈你对HashMap的理解，底层的基本实现。HashMap是怎么解决碰撞问题的？这些数据结构中是线程安全的吗？

14 简单说说类加载过程，里面执行了哪些操作？GC和内存管理，平时在tomcat里面有没有进行过相关的配置

15 get和post的基本区别？说说 tcp/ip协议，三次握手，窗口滑动机制

16 开发中用了哪些数据库？ mysql存储引擎有哪些？区别有哪些？悲观锁和乐观锁使用场景、分布式集群实现的原理？如何线上排查JVM的相关问题

17 springMVC和mybatis的工作原理，底层源码理解多少？

18 rdeis中的基本存储类型、事务、使用场景

19 如何保障请求的执行顺序

20 Dubbo的超时重试，Dubbo超时时间设置

21 分布式事务与分布式锁怎样保障扣款不出现负数？

22 分布式session如何设置的？

23 Zookeeper有哪些作用

24 JVM 内存模型，jvm加载原理

25 数据库垂直和水平拆分

26 MyBatis如何分页；如何设置缓存；MySQL分页

27 熟悉IO么？与NIO的区别，阻塞与非阻塞的区别

28 分布式session一致性

29 分布式接口的幂等性设计（不能重复扣款）

30 画一下项目技术架构图

31 JVM老年代和新生代的比例？

32 jstack,jmap,jutil分别的意义？如何线上排查JVM的相关问题？

33 线程池的构造类的方法的5个参数的具体意义？

34 Set的实现原理

35 单机上一个线程池正在处理服务如果忽然断电怎么办?(正在处理和阻塞队列里的请求怎么处理)

36 使用无界阻塞队列会出现什么问题？

37 接口如何处理重复请求

38  如何保证共享变量修改时的原子性？

39  设计一个对外服务的接口实现类，在1，2，3三个主机（不同ip）上实现负载均衡和顺序轮询机制（考虑并发）

40  concurrentMap,TreeMap的机制

41  volatile 关键字

42  简诉 快速排序

43  高并发下分布式的缓存一致性？

44 mysql大表优化方案

45  springAOP，IOC的实现原理，以及他的应用是实现

46 redis和memcached的区别

47  spring要把一个组件注入spring中应该怎么做？

48 spring 使用了哪些设计模式？

49 手机扫二维码登录的实现原理

50 结合内存说下多线程、进程、线程的区别

51 collection的理解，选择一种说下底层实现？

1）集合类：List和Set比较，各自的子类比较（ArrayList，Vector，LinkedList；HashSet，TreeSet）；

2）HashMap的底层实现，之后会问ConcurrentHashMap的底层实现；

3）如何实现HashMap顺序存储：可以参考LinkedHashMap的底层实现；

4）HashTable和ConcurrentHashMap的区别；

5）String,StringBuffer和StringBuilder的区别；

6）Object的方法有哪些：比如有wait方法，为什么会有；

7）wait和sleep的区别，必须理解；

8）JVM的内存结构，JVM的算法；

9）强引用，软引用和弱引用的区别；

10）数组在内存中如何分配；

11）用过哪些设计模式，手写一个（除单例）；

12）springmvc的核心是什么，请求的流程是怎么处理的，控制反转怎么实现的；

13）spring里面的aop的原理是什么；

14）mybatis如何处理结果集：反射，建议看看源码；

15）java的多态表现在哪里；

16）接口有什么用；

17）说说http,https协议；

18）tcp/ip协议簇；

19）osi五层网络协议；

20）tcp，udp区别；

21）用过哪些加密算法：对称加密，非对称加密算法；

22）说说tcp三次握手，四次挥手；

23）cookie和session的区别，分布式环境怎么保存用户状态；

24）git，svn区别；

25）请写一段栈溢出、堆溢出的代码；

26）ThreadLocal可以用来共享数据吗；


二. IO:

1）bio，nio，aio的区别；

2）nio框架：dubbo的实现原理；

3）京东内部的jsf是使用的什么协议通讯：可参见dubbo的协议；


三. 算法：

1）java中常说的堆和栈，分别是什么数据结构；另外，为什么要分为堆和栈来存储数据。

2）TreeMap如何插入数据：二叉树的左旋，右旋，双旋；

3）一个排序之后的数组，插入数据，可以使用什么方法？答：二分法；问：时间复杂度是多少？

4）平衡二叉树的时间复杂度；

5）Hash算法和二叉树算法分别什么时候用；

6）图的广度优先算法和深度优先算法：详见jvm中垃圾回收实现；


四. 多线程相关：

1）说说阻塞队列的实现：可以参考ArrayBlockingQueue的底层实现（锁和同步都行）；

2）进程通讯的方式：消息队列，共享内存，信号量，socket通讯等；

3）用过并发包的哪些类；

4）什么地方用了多线程；

5）Excutors可以产生哪些线程池；

6）为什么要用线程池；

7）volatile关键字的用法：使多线程中的变量可见；


五. 数据库相关（mysql）：

1）msyql优化经验：

2）mysql的语句优化，使用什么工具；

3）mysql的索引分类：B+，hash；什么情况用什么索引；

4）mysql的存储引擎有哪些，区别是什么；

5）说说事务的特性和隔离级别；

6）悲观锁和乐观锁的区别，怎么实现；


六. mq：

1）mq的原理是什么：有点大。。都可以说；

2）mq如何保证实时性；

3）mq的持久化是怎么做的；


七. nosql相关（主要是redis）:

1）redis和memcache的区别；

2）用redis做过什么；

3）redis是如何持久化的：rdb和aof；

4）redis集群如何同步；

5）redis的数据添加过程是怎样的：哈希槽；

6）redis的淘汰策略有哪些；

7）redis有哪些数据结构；


八. zookeeper:

1）zookeeper是什么；

2）zookeeper哪里用到；

3）zookeeper的选主过程；

4）zookeeper集群之间如何通讯；

5）你们的zookeeper的节点加密是用的什么方式；

6）分布式锁的实现过程；


九. linux相关：
1）linux常用的命令有哪些；

2）如何获取java进程的pid；

3）如何获取某个进程的网络端口号；

4）如何实时打印日志；

5）如何统计某个字符串行数；


十. 设计与思想：

1）重构过代码没有？说说经验；

2）一千万的用户实时排名如何实现；

3）五万人并发抢票怎么实现；












































