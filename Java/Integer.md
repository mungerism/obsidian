Integer 创建以后，值就不会被修改，自增操作每次都会创建一个对象。

[[AtomicInteger]] 的 `getAndIncrement()` 不会创建对象。