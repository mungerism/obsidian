---
aliases: [Concurrent Mark Sweep, CMS Garbage Collector]
---

平时多数时间采用[[标记-清除算法]]，直到内存空间的碎片化程序大到影响对象分配时，再采用[[标记-压缩算法]]收集一次。