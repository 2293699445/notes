# Java 高级 

#### 一、面向对象基础&进阶 

#### 二、阶段项目一

#### 三、常用API

#### 四、常见算法

#### 五、集合进阶

#### 六、阶段项目二

#### 七、stream流

#### 八、方法引用

#### 九、异常

#### 十、File

#### 十一、IO流

#### 十二、多线程

#### 十三、网络编程

#### 十四、反射和动态代理 

#### 十五、面向对象

#### 十六、数组

1. 数组的概述与静态初始化 

   - 概念：存储同种数据类型的多个值

     - 隐式转换——向下兼容。比如double[ ]，int,short,byte,long,float都可以存 

   - **数组的定义**：

     - 格式一：数据类型[ ] 数组名。int[ ] arr1
     - 格式二：数据类型 数组名[ ]。int  arr1[ ]

   - **数组的初始化**：内存中为数组容器开辟空间，将数据存入容器的过程 

     - 静态初始化（开始就赋值，长度固定）

       - 原始格式：int[ ] arr1 = new int[ ]{num1,num2,num3};
       - 简化格式：int[ ] arr1 = {num1,num2,num3};

     - 动态初始化（后面才赋值，长度固定）

       - 格式：int[ ] arr1 = new int[length]; 

         开辟空间，给空间中填充默认值，后续可以给数组赋值覆盖空间中的默认值。

       - 默认值类型：

         - 字符类型：默认初始化值'\ u0000' ，显示为一个空格

2. 数组的地址值和元素访问

   - 地址值

     

     ``````java
     double[ ] arr = {n1,n2,n3};
     System.out.println(arr)
     //打印出[D@66h67fg
     ``````

     - [D@66h67fg是数组在内存中的地址值，其中“ [ ”表示是一个数组，“ D ”表示数组的数据类型为Double，“ @”表示间隔符，没有含义，“66h67fg”真正的地址值，十六进制。

   - 元素访问

     - 通过索引访问数组元素，索引从0开始。

3. 数组的遍历

   - 概念：遍历就是将所有的数据取出来。
   - 循环遍历 
     - idea快捷键，快速生成数组的遍历方式：数组名.fori

4. 练习 

   - 练习1

     <img src="C:\Users\19625\AppData\Roaming\Typora\typora-user-images\image-20250112231241296.png" alt="image-20250112231241296" style="zoom:50%;" />

   - 练习2

     <img src="C:\Users\19625\AppData\Roaming\Typora\typora-user-images\image-20250112231323320.png" alt="image-20250112231323320" style="zoom:50%;" />

   - 练习3

     <img src="C:\Users\19625\AppData\Roaming\Typora\typora-user-images\image-20250112231343212.png" alt="image-20250112231343212" style="zoom:50%;" />

   - 练习4

     <img src="C:\Users\19625\AppData\Roaming\Typora\typora-user-images\image-20250112231416035.png" alt="image-20250112231416035" style="zoom:67%;" />

#### 十七、字符串和ArrayList