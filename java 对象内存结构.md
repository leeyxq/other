java 对象内存结构
====

1、头

  8个字节（数组除外头8个字节+4个数组长度字节）

2、基本类型

  1 bytes：byte、boolean
  2 bytes：char、short
  4 bytes：int、float
  8 bytes：double、long
  
3、引用类型 4bytes

4、8的倍数不够，补充

@see http://www.javamex.com/tutorials/memory/object_memory_usage.shtml
