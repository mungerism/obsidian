---
aliases: [Ordinary Object Pointer Map]
---

## 1. 什么是 OopMap
[[OopMap]] 是记录了[[虚拟机栈]]中哪些位置是[[Java 引用]]的数据结构。

## 2. 作用
用于查找[[虚拟机栈]] 上的 [[GC Roots]] 作[[可达性分析算法|可达性分析]]。


## 3. OopMap 类型
> 1.  OopMaps for **interpreted methods**. They are computed lazily, i.e. when GC happens, by analyzing bytecode flow. The best reference is the source code (with lots of comments), see [generateOopMap.cpp](http://hg.openjdk.java.net/jdk8u/jdk8u/hotspot/file/80ee2541504e/src/share/vm/oops/generateOopMap.cpp#l37). InterpreterOopMaps are stored in [OopMapCache](http://hg.openjdk.java.net/jdk8u/jdk8u/hotspot/file/80ee2541504e/src/share/vm/interpreter/oopMapCache.hpp#l31).
2.  OopMaps for **JIT-compiled methods**. They are generated during JIT-compilation and kept along with the compiled code so that VM can quickly find by instruction address the stack locations and the registers where the object references are held.
3.  OopMaps for generated **shared runtime stubs**. These maps are constructed manually by the developers - authors of these runtime stubs.
