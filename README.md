
## Java虚拟机相关知识点学习整理
    Java Virtual Machine


##### 1.JVM内存模型分哪几部分？
    程序计数器、Java虚拟机栈、本地方法栈、堆、方法区
##### 2.轻Minor GC是否会引起内存溢出？
    不会，发生OOM一般都发生在Major GC
##### 3.发生Minor GC，Eden会怎样？
    被清空
##### 4.Eden、Survivor0、Survivor1比例？
    一般8:1:1
##### 5.-Xms、-Xmx啥意思？作用范围？
    -Xms是堆初始内存分配大小，默认为物理内存1/64
    -Xmx是堆最大分配内存，默认为物理内存的1/4
    两者作用范围都是 Eden + Survivor0 + Survivor1 + Old memory
##### 6.分代收集算法？
    新生代内存一般发生复制算法
    老年代发生标记清除算法或标记整理算法
##### 7.你所知道的垃圾回收算法？
    引用计数法
    复制算法
    标记清除法
    标记整理法
    标记清除整理
##### 8.复制算法优缺点？
    没有内存碎片，但是浪费内存空间。
##### 9.标记清除算法优缺点？
    节约空间，但是会有空间碎片，且效率低。
##### 10.标记整理算法优缺点？
    没有内存碎片，但是效率低，有移动对象成本。    
##### 11.Minor GC与Full GC分别在什么时候发生？
    Minor GC发生在新生代 Eden + Survivor0 + Survivor1
    Full GC发生在老年代 Old memory

