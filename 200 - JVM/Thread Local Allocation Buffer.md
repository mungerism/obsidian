---
aliases: [TLAB]
---

每个[[Java 线程|线程]]可以在[[Java 堆]]中申请一段私有的连续内存，用于给对象分配内存空间。由于[[Java 堆|堆]]是线程共享的，这样可以避免出现分配内存时，两条线程争夺同一块内存的情况。

申请 [[Thread Local Allocation Buffer|TLAB]] 的操作需要加锁，线程需要维护两个指针，一个指向 [[Thread Local Allocation Buffer|TLAB]]中空余内存的起始位置，一个则指向 [[Thread Local Allocation Buffer|TLAB]] 末尾。