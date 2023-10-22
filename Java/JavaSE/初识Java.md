# 初识Java

## 计算机部分

### 计算机核心硬件

- CPU：用来运算计算机中的程序，相当于人类的大脑
- 内存：临时存放数据的地方，其中的数据不是长期保存
- 硬盘：存放数据的地方，其中的数据永久保存
- 主板：每个硬件安装的地方，相当于人类的骨架
- 显卡：页面的帧率

### 计算机中的软件分类

- 系统软件：Windows、Mac、Linux等
- 应用软件：QQ、微信等

## Java起源

​		由**Sun**公司中的**詹姆斯·高斯林**（James Gosling）带领的团队所开发，原名为Oak（橡树）

## Java发展史

1. 1995年诞生
2. 1996年Java1开源
3. 1998年Java2，分为JavaSE、JavaME、JavaEE三大体系
4. 2004年Java5，新特征：自动拆箱/装箱、泛型、注解、枚举
5. **2010年**，Oracle收购Sun公司-->从此Java版本半年推出一版
6. **2014年Java8**，新特征：Lambda表达式、Stream流、新日期类型
7. **2018年Java11**，新特征：引入HTTPClient API
8. **2021年Java17**，新特征：Sealed类等

#### 三大体系

JavaSE：Java标准版，后续改为J2SE

JavaEE：Java企业版，在JavaSE之上，解决企业中问题（如：OA、银行等），后续改为J2EE

JavaME：Java微型版，在JavaSE之上取精髓，后续改为J2ME

## Java特征

- 简单性：相对于C/C++而言，Java中取消了指针等特征。
- 面向对象：完全面向对象
- **跨平台性**：每个系统都有对应的JVM，使得Java可以在不同的系统上运行（一次编译，到处运行）

`java源代码在Windows上编写，编译后的字节码文件可以在Windows系统执行，只要Windows上有JVM。如果想在Linux上执行这个字节码，只需要在Linux上安装JVM即可`

- 安全性：Java代码在运行时会检查字节码文件
- **自动垃圾回收机制**：Java中提供了GC，程序运行过程中会自动的回收垃圾，无需程序员手动操作。

`在C/C++中需要程序员手动释放`

## Java运行机制

- 编译阶段：javac.exe
  - 检查java源文件中的代码是否符合规范
  - 将java源文件编译生成class字节码文件
- 运行阶段：java.exe
  - 启动JVM，classLoader查找字节码文件
  - 将字节码文件加载到JVM中
  - JVM检查字节码文件是否安全，并给静态变量、静态方法等开辟空间，将符号引用转为直接引用（指向内存地址）
  - 执行静态变量、静态方法等进行初始化赋值
  - 执行主程序
  - 清理无用资源
  - 将字节码转换成所在系统识别的机器码，并与底层硬件交互

## 安装Java

### JDK、JRE、JVM

- JDK：java开发工具包：核心类库都在其中
- JRE：java运行环境：主要用来运行java程序
- JVM：java虚拟机：用来执行字节码文件和与操作系统交互

三者关系：JDK-->JRE-->JVM

官网下载地址：[Oracle官网](https://www.oracle.com/java/technologies/downloads)

## path与classpath

path：隶属于Windows操作系统上，主要用于在使用一些指令时给系统指路。

classpath：隶属于Java上，在执行字节码文件时，classLoader会去找对应的类。查找就是通过classpath配置的路径上查询，如果不配置classpath默认为当前路径

### 相对路径与绝对路径

- 绝对路径：带有磁盘的都是绝对路径。`c:\xxx;d:\xxx;/xxx/xxx`
- 相对路径：不带有磁盘的路径，在查找时默认从当前路径为起点然后拼接上相对路径

