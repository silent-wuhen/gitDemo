# 前言

视频：[黑马程序员](https://www.bilibili.com/video/BV17F411T7Ao/?spm_id_from=333.337.search-card.all.click&vd_source=bd0b10b1a89eeb70aae017bf4b5233c3)





# 1.`Java`入门

## 1.人机交互

- 什么是cmd？

  在windows操作系统中，利用命令行的方式操作计算机。如：打开文件，打开文件夹，创建文件夹等。

- 常用CMD命令

  | 操作               | 说明                            |
  | ------------------ | ------------------------------- |
  | 盘符名称:          | 盘符切换。E:，表示切换到E盘。   |
  | dir                | 查看当前路径下的内容。          |
  | cd 目录            | 进入单级目录。cd itheima        |
  | cd ..              | 回退到上一级目录。              |
  | cd 目录1\目录2\... | 进入多级目录。cd itheima\JavaSE |
  | cd \               | 回退到盘符目录。                |
  | cls                | 清屏。                          |
  | exit               | 退出命令提示符窗口。            |
  
- 环境变量




## 2. `Java`概述

- Java是什么？

  >计算机语言：人与计算机之间进行信息交流沟通的一种特殊语言

- JDK下载，安装与介绍（17版本）

  1. 下载：[官方网站获取](http://www.oracle.com/)

  2. 安装：改路径即可

  3. 介绍

     | 目录名称 | 说明                                                         |
     | -------- | ------------------------------------------------------------ |
     | bin      | 该路径下存放了JDK的各种工具命令。javac和java就放在这个目录。 |
     | conf     | 该路径下存放了JDK的相关配置文件。                            |
     | include  | 该路径下存放了一些平台特定的头文件。                         |
     | jmods    | 该路径下存放了JDK的各种模块。                                |
     | legal    | 该路径下存放了JDK各模块的授权文档。                          |
     | lib      | 该路径下存放了JDK工具的一些补充JAR包。                       |

- 入门HelloWorld

  1. Java程序开发运行流程

     需要三个步骤：编写程序，编译程序，运行程序。

  2. HelloWorld案例的编写（修改为.java后缀）

     >javac + 文件名 + 后缀名 （就是编译java文件）
     >
     >java + 文件名（无后缀，运行编译之后的class文件）

     >java文件：程序员自己编写的代码。
     >
     >class文件：交给计算机执行的文件。

      ```java
     public class HelloWorld {
     	public static void main(String[] args) {
     		System.out.println("HelloWorld");
     	}
     }
      ```

  3. System.out.printf（）；该输出语句支持%s占位符

     ```java
     public class Test {
         public static void main(String[] args) {
             //两部分参数：
             //第一部分参数：要输出的内容%s（占位）
             //第二部分参数：填充的数据
             
             System.out.printf("你好啊%s","张三");//用张三填充第一个%s
             System.out.println();//换行
             System.out.printf("%s你好啊%s","张三","李四");//用张三填充第一个%s，李四填充第二个%s
         }
     }
     ```

- 环境变量

  1. **JAVA_HOME**
  2. **Path**：

- Java语言的发展

  1. Java5.0：这是Java的第一个大版本更新。
  2. Java8.0：这个是目前绝大数公司正在使用的版本。因为这个版本最为稳定。
  3. Java17.0：这个是我们课程中学习的版本。

  >向下兼容，新的版本只是在原有的基础上添加了一些新的功能。

- Java的三大平台

  1. JavaSE(标准版)：是其他两个版本的基础。

  2. JavaME（微型版）：Java语言的小型版，用于嵌入式消费类电子设备或者小型移动设备的开发。

  3. JavaEE（企业版）：用于Web方向的网站开发。（主要从事后台服务器的开发）

- Java的主要特性

  1. 面向对象
  2. 安全性
  3. 多线程
  4. 简单易用
  5. 开源
  6. 跨平台
  7. 分布式

  > 跨平台原理:
  >
  > ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/002.png?raw=true)
  >
  > - 操作系统本身其实是不认识Java语言的。
  > - 但是针对于不同的操作系统，Java提供了不同的虚拟机。虚拟机会把Java语言翻译成操作系统能看得懂的语言。

- JRE和JDK

  ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/001.png?raw=true)

  1. JVM（Java Virtual Machine），Java虚拟机,java程序运行的地方。
  2. 核心类库：Java提前定义好的，如：println
  3. JRE（Java Runtime Environment），Java运行环境，包含了JVM和Java的核心类库（Java API）
  4. JDK（Java Development Kit）称为Java开发工具包(javac,java，jdb调试工具)，包含了JRE和开发工具

- Java8的安装与配置

  >1. 官网下载JDK安装
  >
  >2. 环境变量：
  >
  >  CLASSPATH：没设置的话，会自动设置为当前目录（不要设置）
  >

  



# 2.`Java`基础概念



## 1.注释

> 注释是对代码的解释和说明文字。

* 单行注释：

  ```java
  // 这是单行注释文字
  ```

* 多行注释：

  ```java
  /*
  这是多行注释文字
  这是多行注释文字
  这是多行注释文字
  */
  注意：多行注释不能嵌套使用。
  ```

* 文档注释（暂时用不到）：

  ```java
  /**
  这是多行注释文字
  这是多行注释文字
  这是多行注释文字
  */
  ```



## 2. 关键字

- 概念：被Java赋予了特定含义的英文单词。

  | **abstract**   | **assert**       | **boolean**   | **break**      | **byte**   |
  | -------------- | ---------------- | ------------- | -------------- | ---------- |
  | **case**       | **catch**        | **char**      | **class**      | **const**  |
  | **continue**   | **default**      | **do**        | **double**     | **else**   |
  | **enum**       | **extends**      | **final**     | **finally**    | **float**  |
  | **for**        | **goto**         | **if**        | **implements** | **import** |
  | **instanceof** | **int**          | **interface** | **long**       | **native** |
  | **new**        | **package**      | **private**   | **protected**  | **public** |
  | **return**     | **strictfp**     | **short**     | **static**     | **super**  |
  | **switch**     | **synchronized** | **this**      | **throw**      | **throws** |
  | **transient**  | **try**          | **void**      | **volatile**   | **while**  |

- 第一个关键字class

  > 表示定义一个类。创建一个类。

  1. 类：Java项目最基本的组成单元，一个完整的Java项目有可能会有成千上万个类来组成的。

  2. 类名：class后面跟随的就是这个类的名字。

  3. 在类名后面会有一对大括号，表示这个类的内容。

     ```java
     public class HelloWorld{
         
        
     }
     /*
     解释：
     class表示定义类。
     类名：HelloWorld
     HelloWorld后面的大括号表示这个类的范围。
     */
     ```




## 3. 字面量

> **作用：数据在程序中的书写格式。**

| **字面量类型** | **说明**                                                 | **程序中的写法**           |
| -------------- | -------------------------------------------------------- | -------------------------- |
| 整数           | 不带小数的数字                                           | 666，-88                   |
| 小数           | 带小数的数字                                             | 13.14，-5.21               |
| 字符           | 必须使用单引号，有且仅能一个字符（可中文,中文是2个字节） | ‘A’，‘0’，   ‘我’          |
| 字符串         | 必须使用双引号，内容可有可无                             | “HelloWorld”，“黑马程序员” |
| 布尔值         | 布尔值，表示真假，只有两个值：true，false                | true 、false               |
| 空值           | 一个特殊的值，空值                                       | 值是：null                 |

特殊字符（串）：

```java
'\t':打印时把前面的字符串补齐到8，或8的整数，最少一个空格，最多8个空格
```



~~~java
public class Demo {
    public static void main(String[] args) {
        System.out.println(10); // 输出一个整数
        System.out.println(5.5); // 输出一个小数
        System.out.println('a'); // 输出一个字符
        System.out.println(true); // 输出boolean值true
        // System.out.println(null); 不能直接打印
        System.out.println("欢迎来到黑马程序员"); // 输出字符串
    }
}
~~~

**区分技巧：**

1. 用双引号引起来的，是字符串类型的字面量。
2. 字符类型的字面量，用单引号引起来，有且只能有一个。
3. 布尔类型的字面量只有两个值：true、false。
4. 空类型的字面量只有一个值：null。



## 4. 变量

> 变量：在程序中临时存储数据的容器，但是这个容器中只能存一个值。



- 变量的定义格式：

  **数据类型 变量名 = 数据值；**

  ```java
  public class VariableDemo{
  	public static void main(String[] args){
  		//定义一个整数类型的变量
  		//数据类型 变量名 = 数据值;
  		int a = 16;
  		System.out.println(a);//16
  		
  		//定义一个小数类型的变量
  		double b = 10.1;
  		System.out.println(b);//10.1
  	}
  }
  ```

- 变量的注意事项

  1. 变量名不能重复
  2. 在一条语句中，可以定义多个变量。（影响代码的阅读，了解即可）
  3. 变量在使用之前必须要赋值。

  ```java
  public class VariableDemo2{
  	public static void main(String[] args){
  		//1.变量名不允许重复
  		//int a = 10;
  		//int a = 20;
  		//System.out.println(a);
  		
  		//2.一条语句可以定义多个变量
  		//了解。
  		//int a = 10, b = 20, c = 20,d = 20;
  		//System.out.println(a);//?
  		//System.out.println(b);//?
  		
  		
  		//3.变量在使用之前必须要赋值
  		int a = 30;
  		System.out.println(a);
  	}
  }
  ```


- 计算机中的存储方式

  ```java
  public static void main(String[] args) {
          System.out.println(0b1010); //二进制
          System.out.println(012); //八进制
          System.out.println(123);
          System.out.println(0x10); //十六进制
      }
  ```

  ```txt
  文字数据：
      ASCII
      GB2312 -> GBK编码（windows默认使用）
      Unicode编码 （统一码）
      
  图片数据：
  	分辨率：1920（宽） * 1080（长）
  	像素
  	灰度图（黑白图）：0（黑），255（白）
  	彩色图：R，G，B（值越大颜色越浓0-255）
  	
  声音数据：
  	进行采样
  ```

  



## 5. 数据类型

- Java数据类型的分类

  1. 基本数据类型
  2. 引用数据类型（面向对象的时候再深入学习）

- 基本数据类型的四类八种

  | 数据类型 | 关键字  | 内存占用 |                  取值范围                  |
  | :------: | :-----: | :------: | :----------------------------------------: |
  |   整数   |  byte   |    1     |    负的2的7次方 ~ 2的7次方-1(-128~127)     |
  |          |  short  |    2     | 负的2的15次方 ~ 2的15次方-1(-32768~32767)  |
  |          |   int   |    4     |        负的2的31次方 ~ 2的31次方-1         |
  |          |  long   |    8     |        负的2的63次方 ~ 2的63次方-1         |
  |  浮点数  |  float  |    4     |  1.401298e-45 ~ 3.402823e+38（23位小数）   |
  |          | double  |    8     | 4.9000000e-324 ~ 1.797693e+308（52位小数） |
  |   字符   |  char   |    2     |                  0-65535                   |
  |   布尔   | boolean |    1     |                true，false                 |

  1. 在java中**整数默认是int类型**，**浮点数默认是double类型**。
  2. **需要记忆以下几点:**
     - byte类型的取值范围：-128 ~ 127
     - int类型的大概取值范围：-21亿多  ~ 21亿多
     - 整数类型和小数类型的取值范围大小关系：**double > float > long > int > short > byte**
     - 最为常用的数据类型选择：
       1. 在定义变量的时候，要根据实际的情况来选择不同类型的变量。

       2. 如果整数类型中，不太确定范围，那么默认使用int类型。

       3. 如果小数类型中，不太确定范围，那么默认使用double类型。

       4. 如果要定义字符类型的变量，使用char

       5. 如果要定义布尔类型的变量，使用boolean

- 定义8种基本数据类型变量

  ```java
  public class VariableDemo3{
      public static void main(String[] args){
          //1.定义byte类型的变量
          //数据类型 变量名 = 数据值;
          byte a = 10;
          System.out.println(a);
  
          //2.定义short类型的变量
          short b = 20;
          System.out.println(b);
  
          //3.定义int类型的变量
          int c = 30;
          System.out.println(c);
  
          //4.定义long类型的变量
          long d = 123456789123456789L;
          System.out.println(d);
  
          //5.定义float类型的变量
          float e = 10.1F;
          System.out.println(e);
  
          //6.定义double类型的变量
          double f = 20.3;
          System.out.println(f);
  
          //7.定义char类型的变量
          char g = 'a';
          System.out.println(g);
  
          //8.定义boolean类型的变量
          boolean h = true;
          System.out.println(h);
  
      }
  }
  ```

  **注意点:**

  - 如果要定义一个long类型的变量，那么在数据值的后面**需要加上L后缀**。（大小写都可以，建议大写。）
  - 如果要定义一个float类型的变量，那么在数据值的后面**需要加上F后缀**。（大小写都可以）



## 6. 标识符

> 大多都在遵守阿里巴巴的命名规则。

- 硬性要求：

  ```java
  - 必须由数字、字母、下划线_、美元符号$组成。
  - 数字不能开头
  - 不能是关键字
  - 区分大小写的。
  ```

- 小驼峰命名法（适用于**变量名**和**方法名**）

  1. 如果是一个单词，那么全部小写，比如：name

  2. 如果是多个单词，那么从第二个单词开始，首字母大写，比如：firstName、maxAge

- 大驼峰命名法（适用于**类名**，**接口名**）

  1. 如果是一个单词，那么首字母大写。比如：Demo、Test。

  2. 如果是多个单词，那么每一个单词首字母都需要大写。比如：HelloWorld

- 阿里巴巴命名规范细节：

  1. 尽量不要用拼音。但是一些国际通用的拼音可视为英文单词。

     正确：alibaba、hangzhou、nanjing

     错误：jiage、dazhe

  2. 平时在给变量名、方法名、类名起名字的时候，不要使用下划线或美元符号。

     错误：_name

     正确：name



## 7. 键盘录入

- 快速使用

  ```java
  使用步骤：
  
  第一步：
  	导包：表示先找到Scanner这个类。
  
  第二步：
  	创建对象：表示申明一下，准备开始用Scanner这个类。
  
  第三步：
  	接收数据：也是真正的代码。
  ```

  代码示例：

  ```java
  //导包，其实就是先找到Scanner这个类在哪
  import java.util.Scanner;
  public class ScannerDemo1{
  	public static void main(String[] args){
  		//2.创建对象，其实就是申明一下，我准备开始用Scanner这个类了。
  		Scanner sc = new Scanner(System.in);
  		//3.接收数据
  		//当程序运行之后，我们在键盘输入的数据就会被变量i给接收了
  		System.out.println("请输入一个数字");
  		int n1 = sc.nextInt();
          int n2 = sc.nextInt();
  		System.out.println(n1+n2);
  	}
  }
  ```

- 深入学习

  > 键盘录入涉及到的方法如下：next（）、nextLine（）、nextInt（）、nextDouble（）。

  1. next（）、nextLine（）：

     - 可以接受任意数据，但是都会返回一个字符串。
     - 如：键盘录入abc，那么会把abc看做字符串返回。

  2. nextInt（）：

     - 只能接受整数。

     - 如：键盘录入123，会把123当做int类型的整数返回。

       > 键盘录入小数或者其他字母，就会报错。

  3. nextDouble（）：

     > 能接收整数和小数，但是都会看做小数返回。

- 方法底层细节 

  1. 第一个细节：

     next（），nextInt（），nextDouble（）在接收数据的时候，会遇到空格，回车，制表符其中一个就会停止接收数据。

  2. 第二个细节：

     next（），nextInt（），nextDouble（）在接收数据的时候，会遇到空格，回车，制表符其中一个就会停止接收数据。但是这些符号 + 后面的数据还在内存中并没有接收。如果后面还有其他键盘录入的方法，会自动将这些数据接收。

     ```java
     Scanner sc = new Scanner(System.in);
     String s1 = sc.next();
     String s2 = sc.next();
     System.out.println(s1);
     System.out.println(s2);
     //此时值键盘录入一次a b(注意a和b之间用空格隔开)
     //那么第一个next();会接收a，a后面是空格，那么就停止，所以打印s1是a
     //但是空格+b还在内存中。
     //第二个next会去掉前面的空格，只接收b
     //所以第二个s2打印出来是b
     ```

  3. 第三个细节：

     nextLine（）方法是把一整行全部接收完毕。

     ```java
     Scanner sc = new Scanner(System.in);
     String s = sc.nextLine();
     System.out.println(s);
     //键盘录入a b(注意a和b之间用空格隔开)
     //那么nextLine不会过滤前面和后面的空格，会把这一整行数据全部接收完毕。
     ```

- 结论（如何使用）

  键盘录入分为两套：

  1. next（）、nextInt（）、nextDouble（）这三个配套使用。

     如果用了这三个其中一个，就不要用nextLine（）。

  2. nextLine（）单独使用。

     如果想要整数，那么先接收，再使用Integer.parseInt进行类型转换。



## 8. `IDEA`

- IDEA概述

  **集成环境：**把代码**编写，编译，执行，调试**等多种功能综合到一起的开发工具。

- IDEA的下载、安装、设置

  1. 下载网址：[https://www.jetbrains.com/idea](https://www.jetbrains.com/idea)

  2. IDEA的设置

     - 修改主题

       ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/003.png?raw=true)

     - 修改字体和大小

       ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/004.png?raw=true)

     - 修改注释颜色

       ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/005.png?raw=true)

     - 自动导包

       ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/006.png?raw=true)

     - 提示忽略大小写

       ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/007.png?raw=true)

     



## 9.`IDEA`层级结构介绍

- 结构分类
  1. project（项目、工程）
  2. module（模块）
  3. package（包）
  4. class（类）：真正写代码的地方。
- 类的相关操作
  1. 新建类文件
  2. 删除类文件
  3. 修改类文件
- 模块的相关操作
  1. 新建模块
  2. 删除模块
  3. 修改模块
  4. 导入模块
- 项目的相关操作
  1. 关闭项目
  2. 打开项目
  3. 修改项目
  4. 新建项目





# 3.运算符

## 1.运算符和表达式

- 运算符：就是对常量或者变量进行操作的符号。比如： +  -  *  / 
- 表达式：用运算符把常量或者变量连接起来的，符合Java语法的式子就是表达式。比如：a + b 这个整体就是表达式。



## 2.算术运算符

- 分类：

  ```java
  + - * / %
  ```

  ```java
  /：
  1.整数相除结果只能得到整除，如果结果想要是小数，必须要有小数参数。
  2.小数直接参与运算，得到的结果有可能是不精确的。
  案例：
  System.out.println( 10 / 3);//3
  System.out.println(10.0 / 3);//3.3333333333333335
  ```

  ```java
  %：取模、取余。
      
  案例：
  System.out.println(10 % 2);//0
  System.out.println(10 % 3);//1
  应用场景：
  //可以利用取模来判断一个数是奇数还是偶数
  System.out.println(15 % 2);//1  奇数
  ```




## 3.隐式转换

- 概念：也叫自动类型提升。

  把取值范围小的数据或者变量，赋值给取值范围大的变量。（程序自动完成）

- 两种提升规则：

  1. 取值范围小的和取值范围大的进行运算，小的会先提升为大的，再进行运算。
  2. byte、short、char三种类型的数据在运算的时候，都会直接先提升为int，然后再进行运算。
  3. 取值范围从小到大的关系：byte--short--int--long--float--double



## 4.强制转换

- 概念：把取值范围大的数据或者变量赋值给另一个取值范围小的变量。是不允许直接操作。

- 书写格式：

  目标数据类型 变量名 = （目标数据类型）被强转的数据；

  ```java
  public class OperatorDemo2 {
      public static void main(String[] args) {
          double a = 12.3;
          int b = (int) a;
          System.out.println(b);//12
      }
  }
  ```

  强制转换有可能会导致数据发生错误。（数据的精度丢失）



## 5.字符串和字符 `+` 操作

- 字符串的+操作：

  1. 当+操作中出现字符串时，此时就是字符串的连接符，会将前后的数据进行拼接，并产生一个新的字符串。
  2. 当连续进行+操作时，从左到右逐个执行的。

  ```java
  1 + 2 + "abc" + 2 + 1 //结果：“3abc21”
  ```

- 字符的+操作

  1. 规则：当+操作中出现了字符，会拿着字符到计算机内置的ASCII码表中去查对应的数字，然后再进行计算。

  2. 案例：

     ```java
     char c = 'a';
     int result = c + 0;
     System.out.println(result);//97
     ```

     

## 6.自增自减运算符

- 分类：

  ```java
  ++  自增运算符
  --  自减运算符
  ```

- 使用方式：

  1. 放在变量的前面，先++。 比如：++a
  2. 放在变量的后面，后++。 比如：a++



## 7.赋值运算符

- 常用赋值运算符：=

  > 运算过程：就是把等号右边的结果赋值给左边的变量

- 扩展赋值运算符

  1. 分类：+=、-=、*=、/=、%=

  2. 注意点：扩展的赋值运算符中隐层还包含了一个强制转换。

     a += b ;实际上相当于 a = (byte)(a + b);



## 8.关系运算符

> 比较运算符，左边与右边进行判断。

- 分类：

  | 符号 | 解释                                                         |
  | ---- | ------------------------------------------------------------ |
  | ==   | 就是判断左边跟右边是否相等，如果成立就是true，如果不成立就是false |
  | !=   | 就是判断左边跟右边是否不相等，如果成立就是true，如果不成立就是false |
  | >    | 就是判断左边是否大于右边，如果成立就是true，如果不成立就是false |
  | >=   | 就是判断左边是否大于等于右边，如果成立就是true，如果不成立就是false |
  | <    | 就是判断左边是否小于右边，如果成立就是true，如果不成立就是false |
  | <=   | 就是判断左边是否小于等于右边，如果成立就是true，如果不成立就是false |

- 注意点：关系运算符最终的结果一定是布尔类型的。要么是true，要么是false



## 9.逻辑运算符

- & 和 | 的使用：

  1. &：逻辑与（而且）
  2. |：逻辑或（或者）

- ^（异或）的使用：

  计算规则：如果两边相同，结果为false，如果两边不同，结果为true

- !（取反）的使用：

  1. 计算规则：false取反就是true，true取反就是false
  2. **取反最多只用一个。**

- 短路逻辑运算符

  1. &&：
  2. ||：



## 10.三元运算符

> 又叫：三元表达式或者问号冒号表达式。

- 格式：

  关系表达式 ？ 表达式1 ：表达式2 ；

- 计算规则：

  1. 计算关系表达式的值。
  2. 值为真，执行表达式1。
  3. 值为假，执行表达式2。

* 注意点：

  三元运算符的最终结果一定要被使用，要么赋值给一个变量，要么直接打印出来。



## 11.其他

- 运算符的优先级

  小括号优先于所有。

- 原码反码补码

  1. 原码：十进制数据的二进制表现形式，最左为符号位，0为正，1为负。
  2. 反码：解决原码不能计算负数的问题。正数反码不变，负数的反码在原码的基础上符号位不变，数值取反。
  3. 补码：正数不变，负数反码基础上+1.（-128：1000 0000）

  注：计算机中的存储和计算都是以补码的形式进行的。





# 4.流程控制语句

## 1.流程控制语句分类

- 顺序结构：按照代码的先后顺序，依次执行。
- 判断和选择结构(if, switch)
- 循环结构(for, while, do…while)





## 2.判断和选择结构：

### 1.`if`语句

- if语句：

  ```java
  格式：
  if (关系表达式) {
      语句体;	
  } //如果大括号省略，if只能控制距离他最近的那一条语句。
  ```

- if-else:

  ```java
  格式：
  if (关系表达式) {
      语句体1;	
  } else {
      语句体2;	
  }
  ```

- if - else if - else： 

  - 

  ```java
  格式：
  if (关系表达式1) {
      语句体1;	
  } else if (关系表达式2) {
      语句体2;	
  } 
  …
  else {
      语句体n+1;
  }
  ```




### 2.`switch`语句

- 格式

  ```java
  switch (表达式) {
  	case 1:
  		语句体1;
  		break;
  	case 2:
  		语句体2;
  		break;
  	...
  	default:
  		语句体n+1;
  		break;
  }
  ```

- **执行流程：**

  1. 计算出表达式的值 
  2. 与case依次比较，有对应的值，执行相应的语句，在执行的过程中，遇到break结束。 
  3. 如果所有的case都和表达式的值不匹配，就会执行default语句体部分，然后程序结束掉。 

- 扩展知识：

  1. default的位置和省略情况

     default可以放在任意位置，也可以省略

  2. case穿透

     不写break会引发case穿透现象

  3. switch在JDK12的新特性

     ```java
     int number = 10;
     switch (number) {
         case 1 -> System.out.println("一");
         case 2 -> System.out.println("二");
         case 3 -> System.out.println("三");
         default -> System.out.println("其他");
     }
     ```

     

## 3.循环结构

- for循环格式：

  ```java
  for (初始化语句;条件判断语句;条件控制语句) {
  	循环体语句;
  }
  ```

- while循环格式：

  ```java
  初始化语句;
  while(条件判断语句){
  	循环体;
  	条件控制语句;
  }
  ```

- do...while循环

  ```java
  初始化语句;
  do{
      循环体;
      条件控制语句;
  }while(条件判断语句);
  ```

- 死循环

  ```java
  for(;;){
      System.out.println("循环执行一直在打印内容");
  }
  ```

  

## 4.条件控制语句

* break：可以用在switch和循环中，表示结束
* continue：不能单独存在的。只能存在于循环当中。表示：跳过本次循环，继续执行下次循环。



## 5.`Random`

- 导包

  ```java
  import java.util.Random;
  导包的动作必须出现在类定义的上边。
  ```

- 创建对象

  ```java
  Random r = new Random ();
  上面这个格式里面，只有r是变量名，可以变，其他的都不允许变。
  ```

- 生成随机数

  ```java
  int number = r.nextInt(随机数的范围);
  上面这个格式里面，只有number是变量名，可以变，其他的都不允许变。
  随机数范围的特点：从0开始，不包含指定值。比如：参数为10，生成的范围[0,10)
  ```




# 5.数组

> 指的是一种容器，可以同来存储同种数据类型的多个值。



## 1.数组的定义

- 格式一：
  1. 数据类型 [] 数组名
  2. 比如：int [] array
- 格式二：
  1. 数据类型  数组名 []
  2. 比如： int array []



## 2.数组的静态初始化

- 完整格式：

  1. 数据类型[] 数组名 = new 数据类型[]{元素1，元素2，元素3，元素4...};

     比如：int[] arr = new int[]{11,22,33};

  2. 注意：

     * 等号前后的数据类型必须保持一致。
     * 数组一旦创建之后，长度不能发生变化。

- 简化格式:

  1. 数据类型[] 数组名 = {元素1，元素2，元素3，元素4...};

     比如：int[] array = {1,2,3,4,5};





## 3.地址值

```java
int[] arr = {1,2,3,4,5};
System.out.println(arr);//[I@6d03e736

double[] arr2 = {1.1,2.2,3.3};
System.out.println(arr2);//[D@568db2f2
```

数组的地址值：就表示数组在内存中的位置。

```java
以[I@6d03e736为例：

[ ：表示现在打印的是一个数组。

I：表示现在打印的数组是int类型的。

@：仅仅是一个间隔符号而已。

6d03e736：就是数组在内存中真正的地址值。（十六进制的）

但是，习惯性会把[I@6d03e736整体称为数组的地址值。

```



## 4.数组元素访问

- 格式：

  数组名[索引];

- 索引：也叫角标、下标

  1. 索引一定是从0开始的。
  2. 连续不间断。
  3. 逐个+1增长。

- 数组的遍历

  1. 遍历：就是把数组里面所有的内容一个一个全部取出来。
  2. 数组的长度：数组名.length;

  ```java
  for(int i = 0; i < arr.length; i++){
      //在循环的过程中，i依次表示数组中的每一个索引
      sout(arr[i]);//就可以把数组里面的每一个元素都获取出来，并打印在控制台上了。
  }
  ```

  



## 5.数组的动态初始化

- 格式：

  数据类型[] 数组名 = new 数据类型[数组的长度];

  ```java
  //1.定义一个数组，存3个人的年龄，年龄未知
  int[] agesArr = new int[3];
  
  
  //2.定义一个数组，存班级10名学生的考试成绩，考试成绩暂时未知，考完才知道。
  int[] scoresArr = new int[10];
  ```

- 数组的默认初始化值：

  1. 整数类型：0
  2. 小数类型：0.0
  3. 布尔类型：false
  4. 字符类型：'\u0000'
  5. 引用类型：null



## 6.数组的内存图

- Java内存分配：

  1. 栈：方法运行使用的内存。
  2. 堆：存储对象或数组，new来创建的。
  3. 方法区（jdk8之后改为：元空间）：存储可以运行的class文件。
  4. 本地方法栈：JVM在操作系统功能的时候使用。
  5. 寄存器：给CPU使用。

- 两个数组指向同一个空间的内存图

  ```java
  int[] arr1 = {1,2,3};
  int[] arr2 = arr1;
  ```






## 7.二维数组

- 二维数组的初始化

  1. 静态初始化

     ```java
     数据类型[][] 数组名 = new 数据类型[][] {{元素1，元素2},{元素1，元素2}};
     
     简化：
     数据类型[][] 数组名 = {{元素1，元素2},{元素1，元素2}};
     ```

  2. 动态初始化

     ```java
     数据类型[][] 数组名 = new 数据类型[m][n]
     ```

- 二维数组的内存图





# 6.方法

>方法（method）是程序中最小的执行单元
>
>
>
>注意：
>
>* 方法必须先创建才可以使用，该过程称为方法定义
>* 方法创建后并不是直接可以运行的，需要手动使用后，才执行，该过程成为方法调用



## 1.方法的定义和调用

- 方法定义和调用

  1. 定义格式

     ```java
     public static 返回值类型 方法名(参数) {
        方法体; 
        return 数据 ;
     }
     
     /*
     public static:	修饰符，目前先记住这个格式
     返回值类型:		方法操作完毕之后返回的数据的数据类型(如果没有数据返回，写void，且方法体中不写return)
     方法名:		调用方法时候使用的标识
     参数:			由数据类型和变量名组成，多个参数之间用逗号隔开
     方法体:		完成功能的代码块
     return:			如果方法操作完毕，有数据返回，用于把数据返回给调用者
     */
     ```

  2. 调用格式

     ```java
     方法名 ( 参数 ) ;
     数据类型 变量名 = 方法名 ( 参数 ) ;
     ```

  3. 注意：

     * 方法的返回值通常会使用变量接收，否则该返回值将无意义
     * 方法定义时return后面的返回值与方法定义上的数据类型要匹配，否则程序将报错

- 形参和实参

  1. 形参：方法定义中的参数

  2. 实参：方法调用中的参数

- 方法的注意事项

  1. 方法不能嵌套定义
  2. void表示无返回值，可以省略return，也可以单独的书写return，后面不加数据



## 2.方法重载

* 方法重载概念

  * 多个方法在同一个类中
  * 多个方法具有相同的方法名
  * 多个方法的参数不相同，类型不同或者数量不同
* 注意：

  * 重载仅对应方法的定义，与方法的调用无关，调用方式参照标准格式
  * 重载仅针对同一个类中方法的名称与参数进行识别，与返回值无关。





# 7.面向对象（封装）

## 1.类和对象

- 类和对象的理解

  > 客观存在的事物皆为对象 ，所以我们也常常说万物皆对象。

  1. 类
     * 类的理解
       * 类是对现实生活中一类具有共同属性和行为的事物的抽象
       * 类是对象的数据类型，类是具有相同属性和行为的一组对象的集合
       * 简单理解：类就是对现实事物的一种描述
     * 类的组成
       * 属性：指事物的特征，例如：手机事物（品牌，价格，尺寸）
       * 行为：指事物能执行的操作，例如：手机事物（打电话，发短信）
  2. 类和对象的关系
     * 类：类是对现实生活中一类具有共同属性和行为的事物的抽象
     * 对象：是能够看得到摸的着的真实存在的实体
     * 简单理解：**类是对事物的一种描述，对象则为具体存在的事物**

- 类的定义

  > 类的组成是由属性和行为两部分组成
  >
  > * 属性：在类中通过成员变量来体现（类中方法外的变量）
  > * 行为：在类中通过成员方法来体现（和前面的方法相比去掉static关键字即可）
  >
  > 
  >
  > 注：一个java文件中可以定义多个class类，且只能一个类是public修饰，修饰的类名必须成为代码的文件名。（建议一个java文件写一个class类）

  1. 类的定义步骤：

     - 定义类
     - 编写类的成员变量
     - 编写类的成员方法

     ```java
     public class 类名 {
     	// 成员变量
     	变量1的数据类型 变量1；
     	变量2的数据类型 变量2;
     	…
     	// 成员方法
     	方法1;
     	方法2;	
     }
     ```

  2. 对象的使用

     - 创建对象的格式：

       ```java
       类名 对象名 = new 类名();
       ```

     - 调用成员的格式：

       ```java
       对象名.成员变量
       对象名.成员方法();
       ```

     ```java
     public class PhoneDemo {
         public static void main(String[] args) {
             //创建对象
             Phone p = new Phone();
     
             //使用成员变量
             System.out.println(p.brand);
             System.out.println(p.price);
     
             p.brand = "小米";
             p.price = 2999;
     
             System.out.println(p.brand);
             System.out.println(p.price);
     
             //使用成员方法
             p.call();
             p.sendMessage();
         }
     }
     ```

- 标准JavaBean类

  > javabean类：用来描述一类事物的类。（不写main方法）

  1. 类名见名知意

  2. 成员变量使用private

  3. 提供至少2个构造方法

     - 无参构造
     - 带全部参数的构造

  4. 成员方法

     - 提供每一个成员变量对应的setxxx(),getxxx()方法。

       快捷键生成：alt + instet（或alt + fn + inster）

     - 其他的行为

- 测试类：编写main方法的类。
- 成员变量和局部变量的区别
  1. 类中位置不同：成员变量（类中方法外）局部变量（方法内部或方法声明上）
  2. 内存中位置不同：成员变量（堆内存）局部变量（栈内存）
  3. 生命周期不同：成员变量（随着对象的存在而存在，随着对象的消失而消失）局部变量（随着方法的调用而存在，随着方法的调用完毕而消失）
  4. 初始化值不同：成员变量（有默认初始化值）局部变量（没有默认初始化值，必须先定义，赋值才能使用）





## 2.封装

- 封装思想

  1. 封装概述
     
     **对象代表什么，就得封装对应的数据，并提供数据对应的行为** 
     
  2. 封装代码实现
     将类的某些信息隐藏在类内部，不允许外部程序直接访问，而是通过该类提供的方法来实现对隐藏信息的操作和访问
     成员变量private，提供对应的getXxx()/setXxx()方法
  
- private关键字

  > private是一个修饰符，可以用来修饰成员（成员变量，成员方法）

  1. 被private修饰的成员，只能在本类进行访问，针对private修饰的成员变量，如果需要被其他类使用，提供相应的操作
     * 提供“get变量名()”方法，用于获取成员变量的值，方法用public修饰
     * 提供“set变量名(参数)”方法，用于设置成员变量的值，方法用public修饰

- 就近原则和this关键字

  this修饰的变量用于指代成员变量，其主要作用是（区分局部变量和成员变量的重名问题）

  1. 方法的形参如果与成员变量同名，不带this修饰的变量指的是形参，而不是成员变量
  2. 方法的形参没有与成员变量同名，不带this修饰的变量指的是成员变量

  



## 3.构造方法

- 构造方法概述

  构造方法（构造器，构造函数）是一种特殊的方法

  作用：创建对象时给成员变量赋值。

  1. 作用：创建对象   Student stu = **new Student();**

  2. 格式：

     ```java
     public class 类名{
     
             修饰符 类名( 参数 ) {
     
             }
     
     }
     ```

  3. 功能：主要是完成对象数据的初始化

  4. 特点：

     - 方法名与类名相同
     - 没有返回类型
     - 没有具体的返回值

  5. 执行时机：

     - 创建对象的时候由虚拟机调用（不能手动调用）
     - 每创建一次对象，就会调用一次构造方法

- 构造方法的注意事项

  1. 构造方法的创建

     如果没有定义构造方法，系统将给出一个默认的无参数构造方法

     如果定义了构造方法，系统将不再提供默认的构造方法

  2. 构造方法的重载

     如果自定义了带参构造方法，还要使用无参数构造方法，就必须再写一个无参数构造方法

  3. 推荐的使用方式

     无论是否使用，都需要写无参数构造方法

  4. 重要功能！

     可以使用带参构造，为成员变量进行初始化

- 标准类制作

  1. 类名需要见名知意

  2. 成员变量使用private修饰

  3. 提供至少两个构造方法 

     - 无参构造方法
     - 带全部参数的构造方法

  4. get和set方法 

     提供每一个成员变量对应的setXxx()/getXxx()

  5. 如果还有其他行为，也需要写上



## 4.基本数据类型与引用数据类型

- 基本数据类型：数据值存储在自己的空间中。

  特点：赋值给其他变量，也是赋的真实值。

- 引用数据类型：数据值存储在其他空间中，本身存储的是地址值。

  特点：赋值给其他变量，赋的地址值。





# 8.字符串

## 1.`API`

- API概述
  1. 什么是API (Application Programming Interface) ：应用程序编程接口

  2. java中的API：指的就是 JDK 中提供的各种功能的 Java类，这些类将底层的实现封装了起来，无需关心类如何实现，只需学习这些类如何使用即可。




## 2.`String`类

- String类概述

  String 类代表字符串，Java 程序中的所有字符串文字（例如“abc”）都被实现为此类的实例。也就是说，Java 程序中所有的双引号字符串，都是 String 类的对象。String 类在 java.lang 包下，所以使用的时候不需要导包！

- String类的特点

  1. 字符串不可变，其值在创建后不能被更改
  2. 虽然 String 的值是不可变的，但是它们可以被共享
  3. 字符串效果上相当于字符数组( char[] )，但是底层原理是字节数组( byte[] )

- String类的构造方法

  1. 常用的构造方法

     | 方法名                      | 说明                                      |
     | --------------------------- | ----------------------------------------- |
     | public   String()           | 创建一个空白字符串对象，不含有任何内容    |
     | public   String(char[] chs) | 根据字符数组的内容，来创建字符串对象      |
     | public   String(byte[] bys) | 根据字节数组的内容，来创建字符串对象      |
     | String s =   “abc”;         | 直接赋值的方式创建字符串对象，内容就是abc |

  2. 示例代码

     ```java
     public class StringDemo01 {
         public static void main(String[] args) {
             //public String()：创建一个空白字符串对象，不含有任何内容
             String s1 = new String();
             System.out.println("s1:" + s1);
     
             //public String(char[] chs)：根据字符数组的内容，来创建字符串对象
             char[] chs = {'a', 'b', 'c'};
             String s2 = new String(chs);
             System.out.println("s2:" + s2);
     
             //public String(byte[] bys)：根据字节数组的内容，来创建字符串对象
             byte[] bys = {97, 98, 99};
             String s3 = new String(bys);
             System.out.println("s3:" + s3);
     
             //String s = “abc”;	直接赋值的方式创建字符串对象，内容就是abc
             String s4 = "abc";
             System.out.println("s4:" + s4);
         }
     }
     ```

- 创建字符串对象两种方式的区别

  1. 通过构造方法创建：

     通过 new 创建的字符串对象，每一次 new 都会申请一个内存空间，虽然内容相同，但是地址值不同

  2. 直接赋值方式创建

     以“”方式给出的字符串，只要字符序列相同(顺序和大小写)，无论在程序代码中出现几次，JVM 都只会建立一个 String 对象，并在字符串池中维护

- 字符串的比较

  1. == 的作用

     - 比较基本数据类型：比较的是具体的值
     - 比较引用数据类型：比较的是对象地址值

  2. equals方法的作用

     ```java
     public boolean equals(String s)     // 比较两个字符串内容是否相同、区分大小写
     public boolean equalslgnoreCase(String s) // 比较两个字符串内容是否相同，忽略大小写的比较
     ```
  
- 遍历字符串

  ```java
  for (int i = 0; i < str.length(); i++) {
      //i 依次表示字符串的每一个索引
      //索引的范围：0 ~  长度-1
  
      //根据索引获取字符串里面的每一个字符
      //ctrl + alt + V 自动生成左边的接受变量
      char c = str.charAt(i);
      System.out.println(c);
  }
  
  ```

- 字符串截取

  ```java
  substring(0, 3); //左闭右开
  substring(3); //从3到末尾
  ```

- 字符串替换 

  ```java
  replace("TMD", "***"); //替换
  ```

  

## 3.`StringBuilder`

> StringBuilder 可以看成是一个容器，创建之后里面的内容是可变的。

- 基本使用

  ```java
  public class StringBuilderDemo3 {
      public static void main(String[] args) {
          //1.创建对象
          StringBuilder sb = new StringBuilder("abc");
  
          //2.添加元素
          /*sb.append(1);
          sb.append(2.3);
          sb.append(true);*/
  
          //反转
          sb.reverse();
  
          //获取长度
          int len = sb.length();
          System.out.println(len);
  
  
          //打印
          //普及：
          //因为StringBuilder是Java已经写好的类
          //java在底层对他做了一些特殊处理。
          //打印对象不是地址值而是属性值。
          System.out.println(sb);
          
          // toString()
          
      }
  }
  ```

- 链式编程

  ```java
  public class StringBuilderDemo4 {
      public static void main(String[] args) {
          //1.创建对象
          StringBuilder sb = new StringBuilder();
  
          //2.添加字符串
          sb.append("aaa").append("bbb").append("ccc").append("ddd");
  
          System.out.println(sb);//aaabbbcccddd
  
          //3.再把StringBuilder变回字符串
          String str = sb.toString();
          System.out.println(str);//aaabbbcccddd
  
      }
  }
  ```

- 反转字符串

  ```java
  //2.反转键盘录入的字符串
  String result = new StringBuilder().append(str).reverse().toString();
  ```

  

## 4.`StringJoiner`

>* StringJoiner跟StringBuilder一样，也可以看成是一个容器，创建之后里面的内容是可变的。
>* 作用：提高字符串的操作效率，而且代码编写特别简洁，但是目前市场上很少有人用。 
>* JDK8出现的

基本使用：

```java
//1.创建一个对象，并指定中间的间隔符号
StringJoiner sj = new StringJoiner("---");
//2.添加元素
sj.add("aaa").add("bbb").add("ccc");
//3.打印结果
System.out.println(sj);//aaa---bbb---ccc
```

```java
//1.创建对象
StringJoiner sj = new StringJoiner(", ","[","]");
//2.添加元素
sj.add("aaa").add("bbb").add("ccc");
int len = sj.length();
System.out.println(len);//15
//3.打印
System.out.println(sj);//[aaa, bbb, ccc]
String str = sj.toString();
System.out.println(str);//[aaa, bbb, ccc]
```



## 5.关于字符串的小扩展：

1. 字符串存储的内存原理

   ```java
   String s = “abc”；直接赋值
   
   特点：
   此时字符串abc是存在字符串常量池中的。
   先检查字符串常量池中有没有字符串abc，如果有，不会创建新的，而是直接复用。如果没有abc，才会创建一个新的。
   ```

2. new出来的字符串

   ```JAVA
   看到new关键字，一定是在堆里面开辟了一个小空间。
   
   String s1 = new String（“abc”）；
   
   String s2 = “abc”；
   
   s1记录的是new出来的，在堆里面的地址值。
   
   s2是直接赋值的，所以记录的是字符串常量池中的地址值。
   ```

3. ==号比较的到底是什么？

   ```JAVA
   如果比较的是基本数据类型：比的是具体的数值是否相等。
   
   如果比较的是引用数据类型：比的是地址值是否相等。
   
   结论：==只能用于比较基本数据类型。不能比较引用数据类型。
   ```





# 9.集合（`ArrayList`）

## 1.集合和数组的优势对比

1. 长度可变
2. 添加数据的时候不需要考虑索引，默认将数据添加到末尾



基本数据类型对应包装类：

| 基本数据类型 | 对应得包装类 |
| ------------ | ------------ |
| byte         | Byte         |
| short        | Short        |
| char         | Character    |
| int          | Integer      |
| long         | Long         |
| float        | Float        |
| double       | Double       |





## 2.`ArrayList`类

- 概述

  1. 什么是集合：提供一种存储空间可变的存储模型，存储的数据容量可以发生改变。
  2. ArrayList集合的特点：长度可以变化，只能存储引用数据类型。
  3. 泛型的使用：用于约束集合中存储元素的数据类型。

- ArrayList类常用方法

  1. 构造方法

     | 方法名             | 说明                 |
     | ------------------ | -------------------- |
     | public ArrayList() | 创建一个空的集合对象 |

  2. 成员方法

     | 方法名                                | 说明                                   |
     | ------------------------------------- | -------------------------------------- |
     | public boolean add(要添加的元素)      | 将指定的元素追加到此集合的末尾         |
     | public boolean remove(要删除的元素)   | 删除指定元素,返回值表示是否删除成功    |
     | public E  remove(int   index)         | 删除指定索引处的元素，返回被删除的元素 |
     | public E   set(int index,E   element) | 修改指定索引处的元素，返回被修改的元素 |
     | public E   get(int   index)           | 返回指定索引处的元素                   |
     | public int   size()                   | 返回集合中的元素的个数                 |

  3. 示例代码

     ```Java
     public class ArrayListDemo02 {
         public static void main(String[] args) {
             //创建集合
             // ArrayList<String> array = new ArrayList<String>();
             ArrayList<String> array = new ArrayList<>();
     
             //添加元素
             array.add("hello"); // 返回为true
             array.add("world");
             array.add("java");
     
             //public boolean remove(Object o)：删除指定的元素，返回删除是否成功
             //        System.out.println(array.remove("world"));
             //        System.out.println(array.remove("javaee"));
     
             //public E remove(int index)：删除指定索引处的元素，返回被删除的元素
             //        System.out.println(array.remove(1));
     
             //IndexOutOfBoundsException
             //        System.out.println(array.remove(3));
     
             //public E set(int index,E element)：修改指定索引处的元素，返回被修改的元素
             //        System.out.println(array.set(1,"javaee"));
     
             //IndexOutOfBoundsException
             //        System.out.println(array.set(3,"javaee"));
     
             //public E get(int index)：返回指定索引处的元素
             //        System.out.println(array.get(0));
             //        System.out.println(array.get(1));
             //        System.out.println(array.get(2));
             //System.out.println(array.get(3)); //？？？？？？ 自己测试
     
             //public int size()：返回集合中的元素的个数
             System.out.println(array.size());
     
             //输出集合
             System.out.println("array:" + array);
         }
     }
     ```

- ArrayList存储字符串并遍历

  ```java
  public class ArrayListDemo3 {
      public static void main(String[] args) {
          //1.创建集合对象
          ArrayList<String> list = new ArrayList<>();
  
          //2.添加元素
          list.add("aaa");
          list.add("bbb");
          list.add("ccc");
          list.add("ddd");
  
          //3.遍历
          //快捷键: list.fori 正向遍历
          //list.forr 倒着遍历
          System.out.print("[");
          for (int i = 0; i < list.size(); i++) {
              //i 依次表示集合里面的每一个索引
  
              if(i == list.size() - 1){
                  //最大索引
                  System.out.print(list.get(i));
              }else{
                  //非最大索引
                  System.out.print(list.get(i) + ", ");
              }
          }
          System.out.print("]");
      }
  }
  
  ```






# 10.面向对象（继承）

## 1.`static`关键字  

- 概述

   `static` 关键字可以用来修饰的成员变量和成员方法，被static修饰的成员是**属于类**的是放在静态区中，没有static修饰的成员变量和方法则是**属于对象**的。

- 定义格式和使用

  static是静态的意思。 static可以修饰成员变量或者修饰方法。

  1. 静态变量及其访问

     有static修饰成员变量，说明这个成员变量是属于类的，这个成员变量称为**类变量**或者**静态成员变量**。 直接用  类名访问即可。因为类只有一个，所以静态成员变量在内存区域中也只存在一份。**所有的对象都可以共享这个变量**。

  2. **定义格式**

     ```java
     修饰符 static 数据类型 变量名 = 初始值；    
     ```

  3. **静态成员变量的访问:**

     ```java
     // **格式：类名.静态变量**
     public static void  main(String[] args){
         System.out.println(Student.schoolName); // 传智播客
         Student.schoolName = "黑马程序员";
         System.out.println(Student.schoolName); // 黑马程序员
     }
     ```

- 静态方法及其访问

  有static修饰成员方法，说明这个成员方法是属于类的，这个成员方法称为**类方法或者静态方法**，直接用类名访问即可。因为类只有一个，所以静态方法在内存区域中也只存在一份。所有的对象都可以共享这个方法。

  1. 访问：

     静态方法也是直接通过**类名.方法名称**即可访问。

     ```java
     public class Student{
         public static String schoolName = "传智播客"； // 属于类，只有一份。
         // .....
         public static void study(){
         	System.out.println("我们都在黑马程序员学习");   
         }
     }
     ```

  2. **格式：类名.静态方法**

     ```java
     public static void  main(String[] args){
         Student.study();
     }
     ```

- 工具类

  私有化构造方法

  目的：为了不让外界创建他的对象

  ```java
  public class ArrayUtil {
  
      //私有化构造方法
      //目的：为了不让外界创建他的对象
      private ArrayUtil() {
      }
  
  
      //需要定义为静态的，方便调用
      public static String printArr(int[] arr) {
          StringBuilder sb = new StringBuilder();
          sb.append("[");
          for (int i = 0; i < arr.length; i++) {
              //i 索引 arr[i] 元素
              if (i == arr.length - 1) {
                  sb.append(arr[i]);
              } else {
                  sb.append(arr[i]).append(", ");
              }
          }
          sb.append("]");
          return sb.toString();
      }
  
  
      public static double getAverage(double[] arr) {
          double sum = 0;
          for (int i = 0; i < arr.length; i++) {
              sum = sum + arr[i];
          }
          return sum / arr.length;
      }
  
  }
  
  
  
  
  
  
  public class TestDemo {
      public static void main(String[] args) {
          //测试工具类中的两个方法是否正确
  
          int[] arr1 = {1, 2, 3, 4, 5};
          String str = ArrayUtil.printArr(arr1);
          System.out.println(str);
  
  
          double[] arr2 = {1.5, 3.7, 4.9, 5.8, 6.6};
          double avg = ArrayUtil.getAverage(arr2);
          System.out.println(avg);
      }
  }
  
  
  ```

- 小结

  1. 当 `static` 修饰成员变量或者成员方法时，该变量称为**静态变量**或**静态方法**。该类的每个对象都**共享**同一个类的静态变量和静态方法。更改该静态变量的值或者访问静态方法，通过类名访问即可。
  2. 无static修饰的成员变量或成员方法，称为**实例变量，实例方法**，实例变量和实例方法必须创建类的对象，然后通过对象来访问。
  3. static修饰的成员属于类，会存储在**静态区**，是随着类的加载而加载的，且只加载一次，节省内存。存储于一块固定的内存区域（静态区），所以，可以直接被类名调用。它优先于对象存在，所以，可以被所有对象共享。
  4. 无static修饰的成员，是属于对象，对象有多少个，就会出现多少份。所以必须由对象调用。

  ```java
  静态方法只能访问静态变量和静态方法
  
  非静态方法可以访问静态变量或静态方法，也可以访问非静态的成员变量和非静态的成员方法
  
  静态方法中是没有this关键字
  ```



## 2.继承 

- 继承的含义

  1. 继承描述的是事物之间的所属关系，通过继承，可以使多种事物之间形成一种关系体系。
  2. **继承**：就是子类继承父类的**属性**和**行为**，使得子类对象可以直接具有与父类相同的属性、相同的行为。子类可以直接访问父类中的**非私有**的属性和行为。
  3. 其中，多个类可以称为**子类**、**派生类**，单独被继承的那一个类称为**父类**、**超类（superclass）**或者**基类**。
  4. java中所有的类直接或间接继承于Object类。

- 继承的好处

  1. 提高**代码的复用性**（减少代码冗余，相同代码重复利用）。
  2. 使类与类之间产生了关系。

- 继承的格式

  通过 `extends` 关键字，可以声明一个子类继承另外一个父类，定义格式如下：

  ```java
  class 父类 {
  	...
  }
  
  class 子类 extends 父类 {
  	...
  }
  ```

  **需要注意：Java是单继承的，一个类只能继承一个直接父类，跟现实世界很像，但是Java中的子类是更加强大的。**

- 子类不能继承的内容

  1. **子类不能继承父类的构造方法。**
  2. **子类可以继承父类的私有成员（成员变量，方法），只是子类无法直接访问而已，可以通过getter/setter方法访问父类的private成员变量。**

- 继承后的特点—成员变量

  1. 成员变量不重名

     如果子类父类中出现**不重名**的成员变量，这时的访问是**没有影响的**。

  2. 成员变量重名

     - 如果子类父类中出现**重名**的成员变量，子类优先访问自己对象中的成员变量。如果访问父类成员变量可使用super关键字。
     
  3.  super访问父类成员变量
  
     - 子父类中出现了同名的成员变量时，在子类中需要访问中非私有成员变量时，需要使用`super` 关键字，修饰父类成员变量，类似于 `this` 。
  
     - 需要注意的是：**super代表的是父类对象的引用，this代表的是当前对象的引用。**
  
     - **使用格式：**
  
       ```java
       super.父类成员变量名
       ```
  
- 继承后的特点—成员方法

  1. 成员方法不重名：如果子类父类中出现**不重名**的成员方法，此时调用是**没有影响的**。对象调用方法时，会先在子类中查找有没有对应的方法，若子类中存在就会执行子类中的方法，若子类中不存在就会执行父类中相应的方法。
  2. 成员方法重名：如果子类父类中出现**重名**的成员方法，则创建子类对象调用该方法的时候，子类对象会优先调用自己的方法。

- 继承后的特点—构造方法

  1. 构造方法的名字是与类名一致的。所以子类是无法继承父类构造方法的。
  2. 构造方法的作用是初始化对象成员变量数据的。所以子类的初始化过程中，必须先执行父类的初始化动作。子类的构造方法中默认有一个`super()` ，表示调用父类的构造方法，父类成员变量初始化后，才可以给子类使用。（**先有爸爸，才能有儿子**）
  3. **继承后子类构方法器特点:子类所有构造方法的第一行都会默认先调用父类的无参构造方法**

  ```java
  class Person {
      private String name;
      private int age;
  
      public Person() {
          System.out.println("父类无参");
      }
  
      // getter/setter省略
  }
  
  class Student extends Person {
      private double score;
  
      public Student() {
          //super(); // 调用父类无参,默认就存在，可以不写，必须再第一行
          System.out.println("子类无参");
      }
      
       public Student(double score) {
          //super();  // 调用父类无参,默认就存在，可以不写，必须再第一行
          this.score = score;    
          System.out.println("子类有参");
       }
  
  }
  
  public class Demo07 {
      public static void main(String[] args) {
          Student s1 = new Student();
          System.out.println("----------");
          Student s2 = new Student(99.9);
      }
  }
  
  输出结果：
  父类无参
  子类无参
  ----------
  父类无参
  子类有参
  ```

- 继承的特点

  1. Java只支持单继承，不支持多继承。
  2. 一个类可以有多个子类。
  3. 可以多层继承。

    > 顶层父类是Object类。所有的类默认继承Object，作为父类。




## 3.方法重写

- 概念

  **方法重写** ：子类中出现与父类一模一样的方法时（返回值类型，方法名和参数列表都相同），会出现覆盖效果，也称为重写或者复写。**声明不变，重新实现**。

- @Override重写注解

  1. @Override:注解，重写注解校验！

  2. 这个注解标记的方法，就说明这个方法必须是重写父类的方法，否则编译阶段报错。

  3. 建议重写都加上这个注解，一方面可以提高代码的可读性，一方面可以防止重写出错！

     加上后的子类代码形式如下：

     ``` java
     public class Cat extends Animal {
          // 声明不变，重新实现
         // 方法名称与父类全部一样，只是方法体中的功能重写写了！
         @Override
         public void cry(){
             System.out.println("我们一起学猫叫，喵喵喵！喵的非常好听！");
         }
     }
     ```

- 注意事项

  1. 方法重写是发生在子父类之间的关系。
  2. 子类方法覆盖父类方法，必须要保证权限大于等于父类权限。
  3. 子类方法覆盖父类方法，返回值类型、函数名和参数列表都要一模一样。



## 4.`super(...)`和`this(...)`

- super和this的用法格式

  ```java
  this.成员变量    	--    本类的
  super.成员变量    	--    父类的
  
  this.成员方法名()  	--    本类的    
  super.成员方法名()   --    父类的
  ```

  接下来我们使用调用构造方法格式：

  ```java
  super(...) -- 调用父类的构造方法，根据参数匹配确认
  this(...) -- 调用本类的其他构造方法，根据参数匹配确认
  ```

- **super(...)用法注意：**

  **子类的每个构造方法中均有默认的super()，调用父类的空参构造。手动调用父类构造会覆盖默认的super()。**

  **super() 和 this() 都必须是在构造方法的第一行，所以不能同时出现。**

  super(..)是根据参数去确定调用父类哪个构造方法的。

- this(...)用法

  1. 默认是去找本类中的其他构造方法，根据参数来确定具体调用哪一个构造方法。
   2. 为了借用其他构造方法的功能。

- 小结

  1. **子类的每个构造方法中均有默认的super()，调用父类的空参构造。手动调用父类构造会覆盖默认的super()。**

  2. **super() 和 this() 都必须是在构造方法的第一行，所以不能同时出现。**

  3. **super(..)和this(...)是根据参数去确定调用父类哪个构造方法的。**
  4. super(..)可以调用父类构造方法初始化继承自父类的成员变量的数据。
  5. this(..)可以调用本类中的其他构造方法。





# 11.面向对象（多态）



## 1.多态

> 同类型的对象，表现出的不同形态。



- 多态的形式

  1. **多态是出现在继承或者实现关系中的**。

  2. **多态体现的格式**：

     ```java
     父类类型 变量名 = new 子类/实现类构造器;
     变量名.方法名();
     ```

  3. **多态的前提**：有继承关系，子类对象是可以赋值给父类类型的变量。例如Animal是一个动物类型，而Cat是一个猫类型。Cat继承了Animal，Cat对象也是Animal类型，自然可以赋值给父类类型的变量。

- 多态的使用场景

  1. 若没有多态，在下图中register方法只能传递学生对象，其他的Teacher和administrator对象是无法传递给register方法方法的，在这种情况下，只能定义三个不同的register方法分别接收学生，老师和管理员。（有了多态之后，方法的形参就可以定义为共同的父类Person。）

     ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/008.png?raw=true)

  2. **要注意的是：**

     * 当一个方法的形参是一个类，我们可以传递这个类所有的子类对象。
     * 当一个方法的形参是一个接口，我们可以传递这个接口所有的实现类对象。
     * 而且多态还可以根据传递的不同对象来调用不同类中的方法。

     代码示例：

     ```java
     父类：
     public class Person {
         private String name;
         private int age;
     
         //空参构造
         //带全部参数的构造
         //get和set方法
     
         public void show(){
             System.out.println(name + ", " + age);
         }
     }
     
     子类1：
     public class Administrator extends Person {
         @Override
         public void show() {
             System.out.println("管理员的信息为：" + getName() + ", " + getAge());
         }
     }
     
     子类2：
     public class Student extends Person{
     
         @Override
         public void show() {
             System.out.println("学生的信息为：" + getName() + ", " + getAge());
         }
     }
     
     子类3：
     public class Teacher extends Person{
     
         @Override
         public void show() {
             System.out.println("老师的信息为：" + getName() + ", " + getAge());
         }
     }
     
     测试类：
     public class Test {
         public static void main(String[] args) {
             //创建三个对象，并调用register方法
     
             Student s = new Student();
             s.setName("张三");
             s.setAge(18);
     
     
             Teacher t = new Teacher();
             t.setName("王建国");
             t.setAge(30);
     
             Administrator admin = new Administrator();
             admin.setName("管理员");
             admin.setAge(35);
     
     
     
             register(s);
             register(t);
             register(admin);
     
     
         }
     
     
     
         //这个方法既能接收老师，又能接收学生，还能接收管理员
         //只能把参数写成这三个类型的父类
         public static void register(Person p){
             p.show();
         }
     }
     ```

- 多态的定义和前提

  1. **多态**： 是指同一行为，具有多个不同表现形式。
  2.  **前提【重点】**
     - 有继承或者实现关系
     - 方法的重写【意义体现：不重写，无意义】
     - 父类引用指向子类对象【格式体现】

  > 父类类型：指子类对象继承的父类类型，或者实现的父接口类型。

- 多态的运行特点

  1. 调用成员变量时：编译看左边，运行看左边
  2. 调用成员方法时：编译看左边，运行看右边

  ```java
  Fu f = new Zi()；
  //编译看左边的父类中有没有name这个属性，没有就报错
  //在实际运行的时候，把父类name属性的值打印出来
  System.out.println(f.name);
  //编译看左边的父类中有没有show这个方法，没有就报错
  //在实际运行的时候，运行的是子类中的show方法
  f.show();
  ```

- 多态的弊端

  如果子类有些独有的功能，此时**多态的写法就无法访问子类独有功能了**。

  ```java 
  class Animal{
      public  void eat()｛
          System.out.println("动物吃东西！")
      ｝
  }
  class Cat extends Animal {  
      public void eat() {  
          System.out.println("吃鱼");  
      }  
     
      public void catchMouse() {  
          System.out.println("抓老鼠");  
      }  
  }  
  
  class Dog extends Animal {  
      public void eat() {  
          System.out.println("吃骨头");  
      }  
  }
  
  class Test{
      public static void main(String[] args){
          Animal a = new Cat();
          a.eat();
          a.catchMouse();//编译报错，编译看左边，Animal没有这个方法
      }
  }
  ```

- 引用类型转换

  1. 为什么要转型：**多态的写法就无法访问子类独有功能了。**多态的转型分为向上转型（自动转换）与向下转型（强制转换）两种。

  2. 向上转型（自动转换）：**向上转型**：多态本身是子类类型向父类类型向上转换（自动转换）的过程，这个过程是默认的。

     ```java
     父类类型  变量名 = new 子类类型();
     如：Animal a = new Cat();
     ```

     **原因是：父类类型相对与子类来说是大范围的类型，Animal是动物类，是父类类型。Cat是猫类，是子类类型。Animal类型的范围当然很大，包含一切动物。**所以子类范围小可以直接自动转型给父类类型的变量。

  3. 向下转型（强制转换）

     **向下转型**：父类类型向子类类型向下转换的过程，这个过程是强制的。

     ```java
     子类类型 变量名 = (子类类型) 父类变量名;
     如:Aniaml a = new Cat();
        Cat c =(Cat) a;  
     ```

  4. 转型的异常

     这段代码可通过编译，但是运行时，报错 `ClassCastException` ，类型转换异常！创建了Cat类型对象，不能转换成Dog对象。

     ```java
     public class Test {
         public static void main(String[] args) {
             // 向上转型  
             Animal a = new Cat();  
             a.eat();               // 调用的是 Cat 的 eat
     
             // 向下转型  
             Dog d = (Dog)a;       
             d.watchHouse();        // 调用的是 Dog 的 watchHouse 【运行报错】
         }  
     }
     ```

- `instanceof`关键字

  为了避免`ClassCastExceptio`的发生，Java提供了 `instanceof` 关键字，给引用变量做类型的校验，格式如下：

  ```java
  变量名 instanceof 数据类型 
  如果变量属于该数据类型或者其子类类型，返回true。
  如果变量不属于该数据类型或者其子类类型，返回false。
  ```

  ```java
  public class Test {
      public static void main(String[] args) {
          // 向上转型  
          Animal a = new Cat();  
          a.eat();               // 调用的是 Cat 的 eat
  
          // 向下转型  
          if (a instanceof Cat){
              Cat c = (Cat)a;       
              c.catchMouse();        // 调用的是 Cat 的 catchMouse
          } else if (a instanceof Dog){
              Dog d = (Dog)a;       
              d.watchHouse();       // 调用的是 Dog 的 watchHouse
          }
      }  
  }
  ```

- `instanceof`新特性

  JDK14的时候提出了新特性，把判断和强转合并成了一行

  ```java
  //新特性
  //先判断a是否为Dog类型，如果是，则强转成Dog类型，转换之后变量名为d
  //如果不是，则不强转，结果直接是false
  if(a instanceof Dog d){
      d.lookHome();
  }else if(a instanceof Cat c){
      c.catchMouse();
  }else{
      System.out.println("没有这个类型，无法转换");
  }
  ```


## 2.包

- 包

  包在操作系统中其实就是一个文件夹。**包是用来分门别类的管理技术，不同的技术类放在不同的包下**，方便管理和维护。

  **包名的命名规范**：

  ```java
  路径名.路径名.xxx.xxx
  // 例如：com.itheima.oa
  ```

  - 包名一般是公司域名的倒写。
  - 包名必须用”.“连接。
  - 包名的每个路径名必须是一个合法的标识符，而且不能是Java的关键字。

- 导包

  ```java
  import com.itheima.homework.demo1.Student;
  ```

  1. 什么时候需要导包？

     - 情况一：在使用Java中提供的非核心包中的类时
     - 情况二：使用自己写的其他包中的类时

  2. 什么时候不需要导包？

     - 情况一：在使用Java核心包（java.lang）中的类时
     - 情况二：在使用自己写的同一个包中的类时

  3. 使用不同包下的相同类

     假设demo1和demo2中都有一个Student该如何使用？

     代码示例：

     ```java
     //使用全类名的形式即可。
     //全类名：包名 + 类名
     //拷贝全类名的快捷键：选中类名crtl + shift + alt + c 或者用鼠标点copy，再点击copy Reference
     com.itheima.homework.demo1.Student s1 = new com.itheima.homework.demo1.Student();
     com.itheima.homework.demo2.Student s2 = new com.itheima.homework.demo2.Student();
     ```




## 3.权限修饰符

- 权限修饰符

  > 可以修饰成员变量，方法，构造方法，内部类

  在Java中提供了四种访问权限，使用不同的访问权限修饰符修饰时，被修饰的内容会有不同的访问权限。

  1. public：公共的，所有地方都可以访问。

  2. protected：本类 ，本包，其他包中的子类都可以访问。

  3. 默认（没有修饰符）：本类 ，本包可以访问。

    注意：默认是空着不写，不是default

  4. private：私有的，当前类可以访问。

  `public > protected > 默认 > private`

- 不同权限的访问能力

  | 修饰符    | 同一个类中 | 同一个包中其他类 | 不同包下的子类 | 不同包下的无关类 |
  | --------- | :--------: | :--------------: | :------------: | :--------------: |
  | private   |    True    |                  |                |                  |
  | 空着不写  |    True    |       True       |                |                  |
  | protected |    True    |       True       |      True      |                  |
  | public    |    True    |       True       |      True      |       True       |

  编写代码时，如果没有特殊的考虑，建议这样使用权限：

  - 成员变量使用`private` ，隐藏细节。
  - 构造方法使用` public` ，方便创建对象。
  - 成员方法使用`public` ，方便调用方法。

  > 小贴士：不加权限修饰符，就是默认权限



## 4.`final`关键字

- 概述

  `final` 关键字，表示修饰的内容不可变。

  - **final**：  不可改变，最终的含义。可以用于修饰类、方法和变量。
    - 类：被修饰的类，不能被继承。
    - 方法：被修饰的方法，不能被重写。
    - 变量：被修饰的变量，有且仅能被赋值一次。

- 使用方式

  1. 修饰类

     final修饰的类，不能被继承。

     ```java
     final class 类名 {
     }
     ```

     代码:

     ```java
     final class Fu {
     }
     // class Zi extends Fu {} // 报错,不能继承final的类
     ```

     提供使用，不能改变其内容。

  2. 修饰方法

     final修饰的方法，不能被重写。

     ```java
     修饰符 final 返回值类型 方法名(参数列表){
         //方法体
     }
     ```

     代码: 

     ```java
     class Fu2 {
     	final public void show1() {
     		System.out.println("Fu2 show1");
     	}
     	public void show2() {
     		System.out.println("Fu2 show2");
     	}
     }
     
     class Zi2 extends Fu2 {
     //	@Override
     //	public void show1() {
     //		System.out.println("Zi2 show1");
     //	}
     	@Override
     	public void show2() {
     		System.out.println("Zi2 show2");
     	}
     }
     ```

  3. 修饰变量-局部变量

     > 命名规范：全部大写，用 _ 隔开

     **局部变量——基本类型**：基本类型的局部变量，被final修饰后，只能赋值一次，不能再更改。代码如下：

     ```java
     public class FinalDemo1 {
         public static void main(String[] args) {
             // 声明变量，使用final修饰
             final int a;
             // 第一次赋值 
             a = 10;
             // 第二次赋值
             a = 20; // 报错,不可重新赋值
     
             // 声明变量，直接赋值，使用final修饰
             final int b = 10;
             // 第二次赋值
             b = 20; // 报错,不可重新赋值
         }
     }
     ```

  4. 修饰变量-成员变量

     > 被final修饰的常量名称，一般都有书写规范，所有字母都**大写**。

     成员变量涉及到初始化的问题，初始化方式有显示初始化和构造方法初始化，只能选择其中一个：

     - 显示初始化(在定义成员变量的时候立马赋值)（常用）；

       ```java
       public class Student {
           final int num = 10;
       }
       ```

     - 构造方法初始化(在构造方法中赋值一次)（不常用，了解即可）。

       **注意：每个构造方法中都要赋值一次！**

       ```java
       public class Student {
           final int num = 10;
           final int num2;
       
           public Student() {
               this.num2 = 20;
       //     this.num2 = 20;
           }
           
            public Student(String name) {
               this.num2 = 20;
       //     this.num2 = 20;
           }
       }
       ```




## 5.代码块

- 局部代码块
- 构造代码块
  1. 写在成员位置的代码块
  2. 可以把多个构造方法中重复的代码抽取出来
  3. 再创建本类对象时会先执行改造代码块再执行构造方法
- 静态代码块
  1. 在构造代码块前加static
  2. 随着类的加载而加载，只执行一次





# 12.面向对象（抽象类&接口&内部类）

## 1.抽象类

- 概述

  1. 抽象类：父类可能知道子类应该有哪个功能，但是功能具体怎么实现父类是不清楚的（由子类自己决定），父类只需要提供一个没有方法体的定义即可，具体实现交给子类自己去实现。**把没有方法体的方法称为抽象方法，包含抽象方法的类就是抽象类**。
     - **抽象方法** ： 没有方法体的方法。
     - **抽象类**：包含抽象方法的类。

- `abstract`使用格式

  > **abstract是抽象的意思，用于修饰方法和类，修饰的方法是抽象方法，修饰的类是抽象类。**

  1. 抽象方法

     > 使用`abstract` 关键字修饰方法，该方法就成了抽象方法，抽象方法只包含一个方法名，而没有方法体。

     定义格式：

     ```java
     修饰符 abstract 返回值类型 方法名 (参数列表)；
     ```

     代码举例：

     ```java
     public abstract void run()；
     ```

  2. 抽象类

     如果一个类包含抽象方法，那么该类必须是抽象类。**注意：抽象类不一定有抽象方法，但是有抽象方法的类必须定义成抽象类。**

     定义格式：

     ```java
     abstract class 类名字 { 
       
     }
     ```

     代码举例：

     ```java
     public abstract class Animal {
         public abstract void run()；
     }
     ```

  3. 抽象类的使用

     **要求**：继承抽象类的子类**必须重写父类所有的抽象方法**。否则，该子类也必须声明为抽象类。

     此时的方法重写，是子类对父类抽象方法的完成实现，我们将这种方法重写的操作，也叫做**实现方法**。

- 抽象类的特征

  1. **抽象类得到了拥有抽象方法的能力。**
  2. **抽象类失去了创建对象的能力。**

  其他成员（构造方法，实例方法，静态方法等）抽象类都是具备的。

- 抽象类的细节

  1. 抽象类**不能创建对象**，如果创建，编译无法通过而报错。只能创建其非抽象子类的对象。

     > 理解：假设创建了抽象类的对象，调用抽象的方法，而抽象方法没有具体的方法体，没有意义。

  2. 抽象类中，可以有构造方法，是供子类创建对象时，初始化父类成员使用的。

     > 理解：子类的构造方法中，有默认的super()，需要访问父类构造方法。

  3. 抽象类中，不一定包含抽象方法，但是有抽象方法的类必定是抽象类。

     > 理解：未包含抽象方法的抽象类，目的就是不想让调用者创建该类对象，通常用于某些特殊的类结构设计。

  4. 抽象类的子类，必须重写抽象父类中**所有的**抽象方法，否则子类也必须定义成抽象类，编译无法通过而报错。 

     > 理解：假设不重写所有抽象方法，则类中可能包含抽象方法。那么创建对象后，调用抽象的方法，没有意义。

  5. 抽象类存在的意义是为了被子类继承。

     > 理解：抽象类中已经实现的是模板中确定的成员，抽象类不确定如何实现的定义成抽象方法，交给具体的子类去实现。



## 2.接口

### 1.接口概述

- 接口

  1. 概述：**接口是更加彻底的抽象，JDK7之前，包括JDK7，接口中全部是抽象方法。接口同样是不能创建对象的**。

  2. 定义格式

     ```java
     //接口的定义格式：
     interface 接口名称{
         // 抽象方法
     }
     
     // 接口的声明：interface
     // 接口名称：首字母大写，满足“大驼峰模式”
     ```

- 接口成分的特点

  > 接口中**只**包含：抽象方法和常量

  1. 抽象方法

     - 注意：接口中的抽象方法默认会自动加上public abstract修饰无需自己手写！！
     - 按照规范：以后接口中的抽象方法建议不要写上public abstract。因为没有必要，默认会加上。

  2. 常量

     在接口中定义的成员变量默认会加上： public static final修饰。也就是说在接口中定义的成员变量实际上是一个常量。可以直接用接口名访问，常量必须要给初始值。常量命名规范建议字母全部大写，多个单词用下划线连接。

  3. 案例演示

     - 1. 

     ```java
     public interface InterF {
         // 抽象方法！
         //    public abstract void run();
         void run();
     
         //    public abstract String getName();
         String getName();
     
         //    public abstract int add(int a , int b);
         int add(int a , int b);
     
     
         // 它的最终写法是：
         // public static final int AGE = 12 ;
         int AGE  = 12; //常量
         String SCHOOL_NAME = "黑马程序员";
     
     }
     ```




### 2.基本的实现

- 实现接口

  1. 概述：

     类与接口的关系为实现关系，即**类实现接口**，该类可以称为接口的实现类，也可以称为接口的子类。实现的动作类似继承，格式相仿，只是关键字不同，实现使用 ` implements`关键字。

  2. 实现接口的格式：

     ```java
     /**接口的实现：
         在Java中接口是被实现的，实现接口的类称为实现类。
         实现类的格式:*/
     class 类名 implements 接口1,接口2,接口3...{
     
     }
     ```

  3. 类实现接口的要求和意义

     1. 必须重写实现的全部接口中所有抽象方法。
     2. 如果一个类实现了接口，但是没有重写完全部接口的全部抽象方法，这个类也必须定义成抽象类。
     3. **意义：接口体现的是一种规范，接口对实现类是一种强制性的约束，要么全部完成接口申明的功能，要么自己也定义成抽象类。这正是一种强制性的规范。**

- 类与接口基本实现案例

  1. 定义一个运动员的**接口**（规范），代码如下：

     ```java
     /**
        接口：接口体现的是规范。
      * */
     public interface SportMan {
         void run(); // 抽象方法，跑步。
         void law(); // 抽象方法，遵守法律。
         String compittion(String project);  // 抽象方法，比赛。
     }
     ```

  2. 定义一个乒乓球运动员类，实现接口，实现接口的**实现类**代码如下：

     ```java
     package com.itheima._03接口的实现;
     /**
      * 接口的实现：
      *    在Java中接口是被实现的，实现接口的类称为实现类。
      *    实现类的格式:
      *      class 类名 implements 接口1,接口2,接口3...{
      *
      *
      *      }
      * */
     public class PingPongMan  implements SportMan {
         @Override
         public void run() {
             System.out.println("乒乓球运动员稍微跑一下！！");
         }
     
         @Override
         public void law() {
             System.out.println("乒乓球运动员守法！");
         }
     
         @Override
         public String compittion(String project) {
             return "参加"+project+"得金牌！";
         }
     }
     ```

  3. **测试代码**：

     ```java
     public class TestMain {
         public static void main(String[] args) {
             // 创建实现类对象。
             PingPongMan zjk = new PingPongMan();
             zjk.run();
             zjk.law();
             System.out.println(zjk.compittion("全球乒乓球比赛"));
     
         }
     }
     ```

- 类与接口的多实现案例

  > **类与接口之间的关系是多实现的，一个类可以同时实现多个接口。**

  1. 定义两个接口，代码如下：

     ```java
     /** 法律规范：接口*/
     public interface Law {
         void rule();
     }
     
     /** 这一个运动员的规范：接口*/
     public interface SportMan {
         void run();
     }
     ```

  2. 定义一个实现类：

     ```java
     /**
      * Java中接口是可以被多实现的：
      *    一个类可以实现多个接口: Law, SportMan
      *
      * */
     public class JumpMan implements Law ,SportMan {
         @Override
         public void rule() {
             System.out.println("尊长守法");
         }
     
         @Override
         public void run() {
             System.out.println("训练跑步！");
         }
     }
     ```

     从上面可以看出类与接口之间是可以多实现的，我们可以理解成实现多个规范，这是合理的。

- 接口与接口的多继承

  > 接口与接口之间是可以多继承的：也就是一个接口可以同时继承多个接口。
  >
  > 
  >
  > 注意：
  >
  > 1. **类与接口是实现关系**
  > 2. **接口与接口是继承关系**

  接口继承接口就是把其他接口的抽象方法与本接口进行了合并。

  ```java 
  public interface Abc {
      void go();
      void test();
  }
  
  /** 法律规范：接口*/
  public interface Law {
      void rule();
      void test();
  }
  
   *
   *  总结：
   *     接口与类之间是多实现的。
   *     接口与接口之间是多继承的。
   * */
  public interface SportMan extends Law , Abc {
      void run();
  }
  ```

  

### 3.扩展：接口的细节

1. 当两个接口中存在相同抽象方法的时候，该怎么办？

   > 只要重写一次即可。此时重写的方法，既表示重写1接口的，也表示重写2接口的。

2. 实现类能不能继承A类的时候，同时实现其他接口呢？

   >继承的父类，就好比是亲爸爸一样
   >实现的接口，就好比是干爹一样
   >可以继承一个类的同时，再实现多个接口，只不过，要把接口里面所有的抽象方法，全部实现。

3. 实现类能不能继承一个抽象类的时候，同时实现其他接口呢？

   > 实现类可以继承一个抽象类的同时，再实现其他多个接口，只不过要把里面所有的抽象方法全部重写。

4. 实现类Zi，实现了一个接口，还继承了一个Fu类。假设在接口中有一个方法，父类中也有一个相同的方法。子类如何操作呢？

   >处理办法一：如果父类中的方法体，能满足当前业务的需求，在子类中可以不用重写。
   >处理办法二：如果父类中的方法体，不能满足当前业务的需求，需要在子类中重写。

5. 如果一个接口中，有10个抽象方法，但是我在实现类中，只需要用其中一个，该怎么办?

   >可以在接口跟实现类中间，新建一个中间类（适配器类）
   >让这个适配器类去实现接口，对接口里面的所有的方法做空重写。
   >让子类继承这个适配器类，想要用到哪个方法，就重写哪个方法。
   >因为中间类没有什么实际的意义，所以一般会把中间类定义为抽象的，不让外界创建对象



## 3.内部类

- 概述

  什么是内部类：将类A定义在类B里面，类A就称为**内部类**，B则称为**外部类**。

- 什么时候使用内部类

  一个事物内部还有一个独立的事物，内部的事物脱离外部的事物无法独立使用

  1. 人里面有一颗心脏。
  2. 汽车内部有一个发动机。
  3. 为了实现更好的封装性。

- 内部类的分类

  按定义的位置来分

  1. **成员内部内**，类定义在了成员位置 (类中方法外称为成员位置，无static修饰的内部类)
  2. **静态内部类**，类定义在了成员位置 (类中方法外称为成员位置，有static修饰的内部类)
  3. **局部内部类**，类定义在方法内
  4. **匿名内部类**，没有名字的内部类，可以在方法中，也可以在类中方法外。



### 1.成员内部类

- **成员内部类特点**：

  1. 无static修饰的内部类，属于外部类对象的。
  2. 宿主：外部类对象。

- **内部类的使用格式**：

  ```java
   外部类.内部类。 // 访问内部类的类型都是用 外部类.内部类
  ```

- **获取成员内部类对象的两种方式**：

  1. 方式一：外部直接创建成员内部类的对象

     ```java
     外部类.内部类 变量 = new 外部类（）.new 内部类（）;
     ```

  2. 方式二：在外部类中定义一个方法提供内部类的对象

- **案例演示**

  ```java
  方式一：
  public class Test {
      public static void main(String[] args) {
          //  宿主：外部类对象。
         // Outer out = new Outer();
          // 创建内部类对象。
          Outer.Inner oi = new Outer().new Inner();
          oi.method();
      }
  }
  
  class Outer {
      // 成员内部类，属于外部类对象的。
      // 拓展：成员内部类不能定义静态成员。
      public class Inner{
          // 这里面的东西与类是完全一样的。
          public void method(){
              System.out.println("内部类中的方法被调用了");
          }
      }
  }
  
  
  方式二：
  public class Outer {
      String name;
      private class Inner{
          static int a = 10;
      }
      public Inner getInstance(){
          return new Inner();
      }
  }
  
  public class Test {
      public static void main(String[] args) {
          Outer o = new Outer();
          System.out.println(o.getInstance());
  
  
      }
  }
  ```

- 成员内部类的细节

  1. 编写成员内部类的注意点：

     - 成员内部类可以被一些修饰符所修饰，比如： private，默认，protected，public，static等
     - 在成员内部类里面，JDK16之前不能定义静态变量，JDK16开始才可以定义静态变量。
     - 创建内部类对象时，对象中有一个隐含的Outer.this记录外部类对象的地址值。

  2. 详解：

     内部类被private修饰，外界无法直接获取内部类的对象，只能通过方式二获取内部类的对象

     被其他权限修饰符修饰的内部类一般用方式一直接获取内部类的对象

     内部类被static修饰是成员内部类中的特殊情况，叫做静态内部类下面单独学习。

     内部类如果想要访问外部类的成员变量，外部类的变量必须用final修饰，JDK8以前必须手动写final，JDK8之后不需要手动写，JDK默认加上。



### 2.静态内部类

- **静态内部类特点**：

  1. 静态内部类是一种特殊的成员内部类。
  2. 有static修饰，属于外部类本身的。
  3. 总结：静态内部类与其他类的用法完全一样。只是访问的时候需要加上外部类.内部类。
  4. **拓展1**:静态内部类可以直接访问外部类的静态成员。
  5. **拓展2**:静态内部类不可以直接访问外部类的非静态成员，如果要访问需要创建外部类的对象。
  6. **拓展3**:静态内部类中没有银行的Outer.this。

- **内部类的使用格式**：

  ```
  外部类.内部类。
  ```

- **静态内部类对象的创建格式**：

  ```java
  外部类.内部类  变量 = new  外部类.内部类构造器;
  ```

- **调用方法的格式：**

  1. 调用非静态方法的格式：先创建对象，用对象调用
  2. 调用静态方法的格式：外部类名.内部类名.方法名();

**案例演示**：

```java
// 外部类：Outer01
class Outer01{
    private static  String sc_name = "黑马程序";
    // 内部类: Inner01
    public static class Inner01{
        // 这里面的东西与类是完全一样的。
        private String name;
        public Inner01(String name) {
            this.name = name;
        }
        public void showName(){
            System.out.println(this.name);
            // 拓展:静态内部类可以直接访问外部类的静态成员。
            System.out.println(sc_name);
        }
    }
}

public class InnerClassDemo01 {
    public static void main(String[] args) {
        // 创建静态内部类对象。
        // 外部类.内部类  变量 = new  外部类.内部类构造器;
        Outer01.Inner01 in  = new Outer01.Inner01("张三");
        in.showName();
    }
}
```



### 3.局部内部类

- **局部内部类** ：定义在**方法中**的类。

定义格式:

```java
class 外部类名 {
	数据类型 变量名;
	
	修饰符 返回值类型 方法名(参数列表) {
		// …
		class 内部类 {
			// 成员变量
			// 成员方法
		}
	}
}
```



### 4.匿名内部类【重点】

- 概述

  **匿名内部类** ：是内部类的简化写法。他是一个隐含了名字的内部类。开发中，最常用到的内部类就是匿名内部类了。

- 格式

  ```java
  new 类名或者接口名() {
       重写方法;
  };
  ```

  包含了：

  1. 继承或者实现关系

  2. 方法重写
  3. 创建对象

- 什么时候用到匿名内部类 

  **实际上，如果希望定义一个只要使用一次的类，就可考虑使用匿名内部类。匿名内部类的本质作用**

  **是为了简化代码**。 

- 匿名内部类前提和格式

  匿名内部类必须**继承一个父类**或者**实现一个父接口**。

  **匿名内部类格式**

  ```java
  new 父类名或者接口名(){
      // 方法重写
      @Override 
      public void method() {
          // 执行语句
      }
  };
  ```

- 使用方式

  以接口为例，匿名内部类的使用，代码如下：

  ```java
  interface Swim {
      public abstract void swimming();
  }
  
  public class Demo07 {
      public static void main(String[] args) {
          // 使用匿名内部类
  		new Swim() {
  			@Override
  			public void swimming() {
  				System.out.println("自由泳...");
  			}
  		}.swimming();
  
          // 接口 变量 = new 实现类(); // 多态,走子类的重写方法
          Swim s2 = new Swim() {
              @Override
              public void swimming() {
                  System.out.println("蛙泳...");
              }
          };
  
          s2.swimming();
          s2.swimming();
      }
  }
  ```

- 匿名内部类的特点

  1. 定义一个没有名字的内部类
  2. 这个类实现了父类，或者父类接口
  3. 匿名内部类会创建这个没有名字的类的对象

- 匿名内部类的使用场景

  通常在方法的形式参数是接口或者抽象类时，也可以将匿名内部类作为参数传递。代码如下：

  ```java
  interface Swim {
      public abstract void swimming();
  }
  
  public class Demo07 {
      public static void main(String[] args) {
          // 普通方式传入对象
          // 创建实现类对象
          Student s = new Student();
          
          goSwimming(s);
          // 匿名内部类使用场景:作为方法参数传递
          Swim s3 = new Swim() {
              @Override
              public void swimming() {
                  System.out.println("蝶泳...");
              }
          };
          // 传入匿名内部类
          goSwimming(s3);
  
          // 完美方案: 一步到位
          goSwimming(new Swim() {
              public void swimming() {
                  System.out.println("大学生, 蛙泳...");
              }
          });
  
          goSwimming(new Swim() {
              public void swimming() {
                  System.out.println("小学生, 自由泳...");
              }
          });
      }
  
      // 定义一个方法,模拟请一些人去游泳
      public static void goSwimming(Swim s) {
          s.swimming();
      }
  }
  ```




# 13.常用`API`

## 1.Math类

- 概述

  Math类所在包为java.lang包，因此在使用的时候不需要进行导包。并且Math类被final修饰了，因此该类是不能被继承的。
  
- 常见方法

  ```java
  public static int abs(int a)					// 返回参数的绝对值
  public static double ceil(double a)				// 返回向上取整
  public static double floor(double a)			// 返回向下取整
  public static int round(float a)				// 按照四舍五入返回最接近参数的int类型的值
  public static int max(int a,int b)				// 获取两个int值中的较大值
  public static int min(int a,int b)				// 获取两个int值中的较小值
  public static double pow (double a,double b)	// 计算a的b次幂的值
  public static double random()					// 返回一个[0.0,1.0)的随机值
  ```

  ```java
  public class MathDemo01 {
  
      public static void main(String[] args) {
  
          // public static int abs(int a)         返回参数的绝对值
          System.out.println("-2的绝对值为：" + Math.abs(-2));
          System.out.println("2的绝对值为：" + Math.abs(2));
  
          // public static double ceil(double a)  返回大于或等于参数的最小整数
          System.out.println("大于或等于23.45的最小整数位：" + Math.ceil(23.45));
          System.out.println("大于或等于-23.45的最小整数位：" + Math.ceil(-23.45));
  
          // public static double floor(double a) 返回小于或等于参数的最大整数
          System.out.println("小于或等于23.45的最大整数位：" + Math.floor(23.45));
          System.out.println("小于或等于-23.45的最大整数位：" + Math.floor(-23.45));
  
          // public static int round(float a)     按照四舍五入返回最接近参数的int
          System.out.println("23.45四舍五入的结果为：" + Math.round(23.45));
          System.out.println("23.55四舍五入的结果为：" + Math.round(23.55));
  
          // public static int max(int a,int b)   返回两个int值中的较大值
          System.out.println("23和45的最大值为: " + Math.max(23, 45));
  
          // public static int min(int a,int b)   返回两个int值中的较小值
          System.out.println("12和34的最小值为: " + Math.min(12 , 34));
  
          // public static double pow (double a,double b)返回a的b次幂的值
          System.out.println("2的3次幂计算结果为: " + Math.pow(2,3));
  
          // public static double random()返回值为double的正值，[0.0,1.0)
          System.out.println("获取到的0-1之间的随机数为: " + Math.random());
      }
  
  }
  ```

  



## 2 System类

-  概述

  System类所在包为java.lang包，因此在使用的时候不需要进行导包。并且System类被final修饰了，因此该类是不能被继承的。

  System包含了系统操作的一些常用的方法。比如获取当前时间所对应的毫秒值，再比如终止当前JVM等等。

- 常见方法

  ```java
  public static long currentTimeMillis()			// 获取当前时间所对应的毫秒值（当前时间为0时区所对应的时间即就是英国格林尼治天文台旧址所在位置）
  public static void exit(int status)				// 终止当前正在运行的Java虚拟机，0表示正常退出，非零表示异常退出
  public static native void arraycopy(Object src,  int  srcPos, Object dest, int destPos, int length); // 进行数值元素copy
  ```

  ```java
  public class SystemDemo01 {
  
      public static void main(String[] args) {
  
          // 获取当前时间所对应的毫秒值
          long millis = System.currentTimeMillis();
  
          // 输出结果
          System.out.println("当前时间所对应的毫秒值为：" + millis);
  
      }
  
  }
  ```

  ```java
  public class SystemDemo01 {
  
      public static void main(String[] args) {
          
          // 输出
          System.out.println("程序开始执行了.....");
          
          // 终止JVM
          System.exit(0);
          
          // 输出
          System.out.println("程序终止了..........");
          
      }
      
  }
  ```

  <font color="blue" size="2">**案例3**</font>：arraycopy方法

  ```java
  // src: 	 源数组
  // srcPos：  源数值的开始位置
  // dest：    目标数组
  // destPos： 目标数组开始位置
  // length:   要复制的元素个数
  public static native void arraycopy(Object src,  int  srcPos, Object dest, int destPos, int length); 
  ```

  ```java
  public class SystemDemo01 {
  
      public static void main(String[] args) {
  
          // 定义源数组
          int[] srcArray = {23 , 45 , 67 , 89 , 14 , 56 } ;
  
          // 定义目标数组
          int[] desArray = new int[10] ;
  
          // 进行数组元素的copy: 把srcArray数组中从0索引开始的3个元素，从desArray数组中的1索引开始复制过去
          System.arraycopy(srcArray , 0 , desArray , 1 , 3);
  
          // 遍历目标数组
          for(int x = 0 ; x < desArray.length ; x++) {
              if(x != desArray.length - 1) {
                  System.out.print(desArray[x] + ", ");
              }else {
                  System.out.println(desArray[x]);
              }
  
          }
  
      }
  
  }
  ```

  **arraycopy方法底层细节：**

  1. 如果数据源数组和目的地数组都是基本数据类型，那么两者的类型必须保持一致，否则会报错
  2. 在拷贝的时候需要考虑数组的长度，如果超出范围也会报错
  3. 如果数据源数组和目的地数组都是引用数据类型，那么子类类型可以赋值给父类类型

  代码示例：

  ```java
  public class SystemDemo3 {
      public static void main(String[] args) {
          //public static void arraycopy(数据源数组，起始索引，目的地数组，起始索引，拷贝个数) 数组拷贝
          //细节:
          //1.如果数据源数组和目的地数组都是基本数据类型，那么两者的类型必须保持一致，否则会报错
          //2.在拷贝的时候需要考虑数组的长度，如果超出范围也会报错
          //3.如果数据源数组和目的地数组都是引用数据类型，那么子类类型可以赋值给父类类型
  
          Student s1 = new Student("zhangsan", 23);
          Student s2 = new Student("lisi", 24);
          Student s3 = new Student("wangwu", 25);
  
          Student[] arr1 = {s1, s2, s3};
          Person[] arr2 = new Person[3];
          //把arr1中对象的地址值赋值给arr2中
          System.arraycopy(arr1, 0, arr2, 0, 3);
  
          //遍历数组arr2
          for (int i = 0; i < arr2.length; i++) {
              Student stu = (Student) arr2[i];
              System.out.println(stu.getName() + "," + stu.getAge());
          }
      }
  }
  
  class Person {
      private String name;
      private int age;
  
      public Person() {
      }
  
      public Person(String name, int age) {
          this.name = name;
          this.age = age;
      }
  
      /**
       * 获取
       *
       * @return name
       */
      public String getName() {
          return name;
      }
  
      /**
       * 设置
       *
       * @param name
       */
      public void setName(String name) {
          this.name = name;
      }
  
      /**
       * 获取
       *
       * @return age
       */
      public int getAge() {
          return age;
      }
  
      /**
       * 设置
       *
       * @param age
       */
      public void setAge(int age) {
          this.age = age;
      }
  
      public String toString() {
          return "Person{name = " + name + ", age = " + age + "}";
      }
  }
  
  
  class Student extends Person {
  
      public Student() {
      }
  
      public Student(String name, int age) {
          super(name, age);
      }
  }
  ```

  

# 3 Runtime

## 3.1 概述

​	Runtime表示Java中运行时对象，可以获取到程序运行时设计到的一些信息

## 3.2 常见方法

<font color="red" size="3">**常见方法介绍**</font>

我们要学习的Object类中的常见方法如下所示：

```java
public static Runtime getRuntime()		//当前系统的运行环境对象
public void exit(int status)			//停止虚拟机
public int availableProcessors()		//获得CPU的线程数
public long maxMemory()				    //JVM能从系统中获取总内存大小（单位byte）
public long totalMemory()				//JVM已经从系统中获取总内存大小（单位byte）
public long freeMemory()				//JVM剩余内存大小（单位byte）
public Process exec(String command) 	//运行cmd命令
```

代码示例：

```java
public class RunTimeDemo1 {
    public static void main(String[] args) throws IOException {
        /*
            public static Runtime getRuntime() 当前系统的运行环境对象
            public void exit(int status) 停止虚拟机
            public int availableProcessors() 获得CPU的线程数
            public long maxMemory() JVM能从系统中获取总内存大小(单位byte)
            public long totalMemory() JVM已经从系统中获取总内存大小(单位byte)
            public long freeMemory() JVM剩余内存大小(单位byte)
            public Process exec(string command) 运行cmd命令
        */

        //1.获取Runtime的对象
        //Runtime r1 =Runtime.getRuntime();

        //2.exit 停止虚拟机
        //Runtime.getRuntime().exit(0);
        //System.out.println("看看我执行了吗?");


        //3.获得CPU的线程数
        System.out.println(Runtime.getRuntime().availableProcessors());//8
        //4.总内存大小,单位byte字节
        System.out.println(Runtime.getRuntime().maxMemory() / 1024 / 1024);//4064
        //5.已经获取的总内存大小,单位byte字节
        System.out.println(Runtime.getRuntime().totalMemory() / 1024 / 1024);//254
        //6.剩余内存大小
        System.out.println(Runtime.getRuntime().freeMemory() / 1024 / 1024);//251

        //7.运行cmd命令
        //shutdown :关机
        //加上参数才能执行
        //-s :默认在1分钟之后关机
        //-s -t 指定时间 : 指定关机时间
        //-a :取消关机操作
        //-r: 关机并重启
        Runtime.getRuntime().exec("shutdown -s -t 3600");


    }
}

```

## 3.3 恶搞好基友

需求：

​	界面上方按钮默认隐藏

​	界面中间有一个提示文本和三个按钮

​	当你的好基友点击中间三个按钮的时候就在N秒之后关机，不同的按钮N的值不一样

​	任意一个按钮被点击之后，上方了按钮出现。当点击上方按钮之后取消关机任务

 ![恶搞好基友](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\恶搞好基友.png)

```java
public class Test {
    public static void main(String[] args) {
        new MyJframe();
    }
}
```

```java
public class MyJframe extends JFrame implements ActionListener {

    JButton yesBut = new JButton("帅爆了");
    JButton midBut = new JButton("一般般吧");
    JButton noBut = new JButton("不帅，有点磕碜");
    JButton dadBut = new JButton("饶了我吧！");


    //决定了上方的按钮是否展示
    boolean flag = false;


    public MyJframe() {
        initJFrame();


        initView();


        //显示
        this.setVisible(true);
    }

    private void initView() {

        this.getContentPane().removeAll();

        if (flag) {
            //展示按钮
            dadBut.setBounds(50, 20, 100, 30);
            dadBut.addActionListener(this);
            this.getContentPane().add(dadBut);
        }


        JLabel text = new JLabel("你觉得自己帅吗？");
        text.setFont(new Font("微软雅黑", 0, 30));
        text.setBounds(120, 150, 300, 50);


        yesBut.setBounds(200, 250, 100, 30);
        midBut.setBounds(200, 325, 100, 30);
        noBut.setBounds(160, 400, 180, 30);

        yesBut.addActionListener(this);
        midBut.addActionListener(this);
        noBut.addActionListener(this);

        this.getContentPane().add(text);
        this.getContentPane().add(yesBut);
        this.getContentPane().add(midBut);
        this.getContentPane().add(noBut);

        this.getContentPane().repaint();
    }

    private void initJFrame() {
        //设置宽高
        this.setSize(500, 600);
        //设置标题
        this.setTitle("恶搞好基友");
        //设置关闭模式
        this.setDefaultCloseOperation(3);
        //置顶
        this.setAlwaysOnTop(true);
        //居中
        this.setLocationRelativeTo(null);
        //取消内部默认布局
        this.setLayout(null);
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        Object obj = e.getSource();
        if (obj == yesBut) {
            //给好基友一个弹框
            showJDialog("xxx，你太自信了，给你一点小惩罚");
            try {
                Runtime.getRuntime().exec("shutdown -s -t 3600");
            } catch (IOException ioException) {
                ioException.printStackTrace();
            }
            flag = true;
            initView();

        } else if (obj == midBut) {
            System.out.println("你的好基友点击了一般般吧");

            //给好基友一个弹框
            showJDialog("xxx，你还是太自信了，也要给你一点小惩罚");

            try {
                Runtime.getRuntime().exec("shutdown -s -t 7200");
            } catch (IOException ioException) {
                ioException.printStackTrace();
            }

            flag = true;
            initView();


        } else if (obj == noBut) {
            System.out.println("你的好基友点击了不帅");

            //给好基友一个弹框
            showJDialog("xxx，你还是有一点自知之明的，也要给你一点小惩罚");

            try {
                Runtime.getRuntime().exec("shutdown -s -t 1800");
            } catch (IOException ioException) {
                ioException.printStackTrace();
            }

            flag = true;
            initView();
        } else if (obj == dadBut) {
            //给好基友一个弹框
            showJDialog("xxx，这次就饶了你~");

            try {
                Runtime.getRuntime().exec("shutdown -a");
            } catch (IOException ioException) {
                ioException.printStackTrace();
            }

        }
    }

    public void showJDialog(String content) {
        //创建一个弹框对象
        JDialog jDialog = new JDialog();
        //给弹框设置大小
        jDialog.setSize(200, 150);
        //让弹框置顶
        jDialog.setAlwaysOnTop(true);
        //让弹框居中
        jDialog.setLocationRelativeTo(null);
        //弹框不关闭永远无法操作下面的界面
        jDialog.setModal(true);

        //创建Jlabel对象管理文字并添加到弹框当中
        JLabel warning = new JLabel(content);
        warning.setBounds(0, 0, 200, 150);
        jDialog.getContentPane().add(warning);

        //让弹框展示出来
        jDialog.setVisible(true);
    }
}

```

# 4 Object类

## 4.1 概述

> tips：重点讲解内容

查看API文档，我们可以看到API文档中关于Object类的定义如下：

![1576053677194](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576053677194.png) 



Object类所在包是java.lang包。Object 是类层次结构的根，每个类都可以将 Object 作为超类。所有类都直接或者间接的继承自该类；换句话说，该类所具备的方法，其他所有类都继承了。



查看API文档我们可以看到，在Object类中提供了一个无参构造方法，如下所示：

![1576053871503](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576053871503.png) 

但是一般情况下我们很少去主动的创建Object类的对象，调用其对应的方法。更多的是创建Object类的某个子类对象，然后通过子类对象调用Object类中的方法。

## 4.2 常见方法

> tips：重点讲解内容

<font color="red" size="3">**常见方法介绍**</font>

我们要学习的Object类中的常见方法如下所示：

```java
public String toString()				//返回该对象的字符串表示形式(可以看做是对象的内存地址值)
public boolean equals(Object obj)		//比较两个对象地址值是否相等；true表示相同，false表示不相同
protected Object clone()    			//对象克隆
```

<font color="red" size="3">**案例演示**</font>

接下来我们就来通过一些案例演示一下这些方法的特点。

<font color="blue" size="2">**案例1**</font>：演示toString方法

实现步骤：

1. 创建一个学生类，提供两个成员变量（name ， age）；并且提供对应的无参构造方法和有参构造方法以及get/set方法
2. 创建一个测试类（ObjectDemo01），在测试类的main方法中去创建学生对象，然后调用该对象的toString方法获取该对象的字符串表现形式，并将结果进行输出

如下所示：

Student类

```java
public class Student {

    private String name ;       // 姓名
    private String age ;        // 年龄

    // 无参构造方法和有参构造方法以及get和set方法略
    ...
        
}
```

ObjectDemo01测试类

```java
public class ObjectDemo01 {

    public static void main(String[] args) {

        // 创建学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用toString方法获取s1对象的字符串表现形式
        String result1 = s1.toString();

        // 输出结果
        System.out.println("s1对象的字符串表现形式为：" + result1);

    }

}
```

运行程序进行测试，控制台输出结果如下所示：

```java
s1对象的字符串表现形式为：com.itheima.api.system.demo04.Student@3f3afe78
```

为什么控制台输出的结果为：com.itheima.api.system.demo04.Student@3f3afe78； 此时我们可以查看一下Object类中toString方法的源码，如下所示：

```java
public String toString() {		// Object类中toString方法的源码定义
	return getClass().getName() + "@" + Integer.toHexString(hashCode());
}
```

其中getClass().getName()对应的结果就是：com.itheima.api.system.demo04.Student；Integer.toHexString(hashCode())对应的结果就是3f3afe78。

我们常常将"com.itheima.api.system.demo04.Student@3f3afe78"这一部分称之为对象的内存地址值。但是一般情况下获取对象的内存地址值没有太大的意义。获取对象的成员变量的字符串拼接形式才

算有意义，怎么实现呢？此时我们就需要在Student类中重写Object的toString方法。我们可以通过idea开发工具进行实现，具体步骤如下所示：

1. 在空白处使用快捷键：alt + insert。此时会弹出如下的对话框

![1576055135105](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576055135105.png) 

2. 选择toString，此时会弹出如下的对话框

![1576055198877](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576055198877.png) 

同时选择name和age属性，点击OK。此时就会完成toString方法的重写，代码如下所示：

```java
@Override
public String toString() {
    return "Student{" +
        "name='" + name + '\'' +
        ", age='" + age + '\'' +
        '}';
}
```

这段代码就是把Student类中的成员变量进行了字符串的拼接。重写完毕以后，再次运行程序，控制台输出结果如下所示：

```java
s1对象的字符串表现形式为：Student{name='itheima', age='14'}
```

此时我们就可以清楚的查看Student的成员变量值，因此重写toString方法的意义就是以良好的格式，更方便的展示对象中的属性值



我们再来查看一下如下代码的输出：

```java
// 创建学生对象
Student s1 = new Student("itheima" , "14") ;

// 直接输出对象s1
System.out.println(s1);
```

运行程序进行测试，控制台输出结果如下所示：

```java
Student{name='itheima', age='14'}
```

我们可以看到和刚才的输出结果是一致的。那么此时也就证明直接输出一个对象，那么会默认调用对象的toString方法，因此如上代码的等同于如下代码：

```java
// 创建学生对象
Student s1 = new Student("itheima" , "14") ;

// 调用s1的toString方法，把结果进行输出
System.out.println(s1.toString());
```

因此后期为了方便进行测试，我们常常是通过输出语句直接输出一个对象的名称。



小结：

1. 在通过输出语句输出一个对象时，默认调用的就是toString()方法
2. 输出地址值一般没有意义，我们可以通过重写toString方法去输出对应的成员变量信息（快捷键：atl + insert ， 空白处 右键 -> Generate -> 选择toString）
3. toString方法的作用：以良好的格式，更方便的展示对象中的属性值
4. 一般情况下Jdk所提供的类都会重写Object类中的toString方法

<font color="blue" size="2">**案例2**</font>：演示equals方法

实现步骤：

1. 在测试类（ObjectDemo02）的main方法中，创建两个学生对象，然后比较两个对象是否相同

代码如下所示：

```java
public class ObjectDemo02 {

    public static void main(String[] args) {

        // 创建两个学生对象
        Student s1 = new Student("itheima" , "14") ;
        Student s2 = new Student("itheima" , "14") ;

        // 比较两个对象是否相等
        System.out.println(s1 == s2);

    }

}
```

运行程序进行测试，控制台的输出结果如下所示：

```java
false
```

因为"=="号比较的是对象的地址值，而我们通过new关键字创建了两个对象，它们的地址值是不相同的。因此比较结果就是false。



我们尝试调用Object类中的equals方法进行比较，代码如下所示：

```java
// 调用equals方法比较两个对象是否相等
boolean result = s1.equals(s2);

// 输出结果
System.out.println(result);
```

运行程序进行测试，控制台的输出结果为：

```java
false
```

为什么结果还是false呢？我们可以查看一下Object类中equals方法的源码，如下所示：

```java
public boolean equals(Object obj) {		// Object类中的equals方法的源码
    return (this == obj);
}
```

通过源码我们可以发现默认情况下equals方法比较的也是对象的地址值。比较内存地址值一般情况下是没有意义的，我们希望比较的是对象的属性，如果两个对象的属性相同，我们认为就是同一个对象；

那么要比较对象的属性，我们就需要在Student类中重写Object类中的equals方法。equals方法的重写，我们也可以使用idea开发工具完成，具体的操作如下所示：

1. 在空白处使用快捷键：alt + insert。此时会弹出如下的对话框

 ![1576056718392](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576056718392.png) 

2. 选择equals() and hashCode()方法，此时会弹出如下的对话框

![1576057779458](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576057779458.png) 

点击next，会弹出如下对话框：

![1576057813175](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576057813175.png) 

选择neme和age属性点击next，此时就会弹出如下对话框：

![1576057892814](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576057892814.png) 

取消name和age属性（因为此时选择的是在生成hashCode方法时所涉及到的属性，关于hashCode方法后期再做重点介绍），点击Finish完成生成操作。生成的equals方法和hashCode方法如下：

```java
@Override
public boolean equals(Object o) {
    if (this == o) return true;
    if (o == null || getClass() != o.getClass()) return false;
    Student student = (Student) o;
    return Objects.equals(name, student.name) && Objects.equals(age, student.age);	// 比较的是对象的name属性值和age属性值
}

@Override
public int hashCode() {
    return 0;
}
```

hashCode方法我们暂时使用不到，可以将hashCode方法删除。重写完毕以后运行程序进行测试，控制台输出结果如下所示：

```java
true
```

此时equals方法比较的是对象的成员变量值，而s1和s2两个对象的成员变量值都是相同的。因此比较完毕以后的结果就是true。

小结：

1. 默认情况下equals方法比较的是对象的地址值
2. 比较对象的地址值是没有意义的，因此一般情况下我们都会重写Object类中的equals方法

<font color="blue" size="2">**案例2**</font>：对象克隆

​	把A对象的属性值完全拷贝给B对象，也叫对象拷贝,对象复制

**对象克隆的分类：**

>深克隆和浅克隆

**浅克隆：**

​	不管对象内部的属性是基本数据类型还是引用数据类型，都完全拷贝过来 

​	基本数据类型拷贝过来的是具体的数据，引用数据类型拷贝过来的是地址值。

​	Object类默认的是浅克隆

![浅克隆](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\浅克隆.png)

**深克隆：**

​	基本数据类型拷贝过来，字符串复用，引用数据类型会重新创建新的

![深克隆](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\深克隆.png)

代码实现：

```java
package com.itheima.a04objectdemo;

public class ObjectDemo4 {
    public static void main(String[] args) throws CloneNotSupportedException {
        // protected object clone(int a) 对象克隆 

        //1.先创建一个对象
        int[] data = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 0};
        User u1 = new User(1, "zhangsan", "1234qwer", "girl11", data);

        //2.克隆对象
        //细节:
        //方法在底层会帮我们创建一个对象,并把原对象中的数据拷贝过去。
        //书写细节:
        //1.重写Object中的clone方法
        //2.让javabean类实现Cloneable接口
        //3.创建原对象并调用clone就可以了
        //User u2 =(User)u1.clone();

        //验证一件事情：Object中的克隆是浅克隆
        //想要进行深克隆，就需要重写clone方法并修改里面的方法体
        //int[] arr = u1.getData();
        //arr[0] = 100;

        //System.out.println(u1);
        //System.out.println(u2);


        //以后一般会用第三方工具进行克隆
        //1.第三方写的代码导入到项目中
        //2.编写代码
        //Gson gson =new Gson();
        //把对象变成一个字符串
        //String s=gson.toJson(u1);
        //再把字符串变回对象就可以了
        //User user =gson.fromJson(s, User.class);

        //int[] arr=u1.getData();
        //arr[0] = 100;

        //打印对象
        //System.out.println(user);

    }
}

package com.itheima.a04objectdemo;

import java.util.StringJoiner;



//Cloneable
//如果一个接口里面没有抽象方法
//表示当前的接口是一个标记性接口
//现在Cloneable表示一旦实现了，那么当前类的对象就可以被克降
//如果没有实现，当前类的对象就不能克隆
public class User implements Cloneable {
    private int id;
    private String username;
    private String password;
    private String path;
    private int[] data;




    public User() {
    }

    public User(int id, String username, String password, String path, int[] data) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.path = path;
        this.data = data;
    }

    /**
     * 获取
     *
     * @return id
     */
    public int getId() {
        return id;
    }

    /**
     * 设置
     *
     * @param id
     */
    public void setId(int id) {
        this.id = id;
    }

    /**
     * 获取
     *
     * @return username
     */
    public String getUsername() {
        return username;
    }

    /**
     * 设置
     *
     * @param username
     */
    public void setUsername(String username) {
        this.username = username;
    }

    /**
     * 获取
     *
     * @return password
     */
    public String getPassword() {
        return password;
    }

    /**
     * 设置
     *
     * @param password
     */
    public void setPassword(String password) {
        this.password = password;
    }

    /**
     * 获取
     *
     * @return path
     */
    public String getPath() {
        return path;
    }

    /**
     * 设置
     *
     * @param path
     */
    public void setPath(String path) {
        this.path = path;
    }

    /**
     * 获取
     *
     * @return data
     */
    public int[] getData() {
        return data;
    }

    /**
     * 设置
     *
     * @param data
     */
    public void setData(int[] data) {
        this.data = data;
    }

    public String toString() {
        return "角色编号为：" + id + "，用户名为：" + username + "密码为：" + password + ", 游戏图片为:" + path + ", 进度:" + arrToString();
    }


    public String arrToString() {
        StringJoiner sj = new StringJoiner(", ", "[", "]");

        for (int i = 0; i < data.length; i++) {
            sj.add(data[i] + "");
        }
        return sj.toString();
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        //调用父类中的clone方法
        //相当于让Java帮我们克隆一个对象，并把克隆之后的对象返回出去。

        //先把被克隆对象中的数组获取出来
        int[] data = this.data;
        //创建新的数组
        int[] newData =new int[data.length];
        //拷贝数组中的数据
        for (int i = 0; i < data.length; i++) {
            newData[i] = data[i];
        }
        //调用父类中的方法克隆对象
            User u=(User)super.clone();
        //因为父类中的克隆方法是浅克隆，替换克隆出来对象中的数组地址值
        u.data =newData;
        return u;
    }
}

```



# 5 Objects类

## 5.1 概述

> tips：了解内容

查看API文档，我们可以看到API文档中关于Objects类的定义如下：

![1576058492444](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576058492444.png) 

Objects类所在包是在java.util包下，因此在使用的时候需要进行导包。并且Objects类是被final修饰的，因此该类不能被继承。

Objects类提供了一些对象常见操作的方法。比如判断对象是否相等，判断对象是否为null等等。



接下来我们来查看一下API文档，看一下Objects类中的成员，如下所示：

![1576058659628](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576058659628.png) 

我们可以发现Objects类中无无参构造方法，因此我们不能使用new关键字去创建Objects的对象。同时我们可以发现Objects类中所提供的方法都是静态的。因此我们可以通过类名直接去调用这些方法。

## 5.2 常见方法

> tips：重点讲解内容

<font color="red" size="3">**常见方法介绍**</font>

我们要重点学习的Objects类中的常见方法如下所示：

```java
public static String toString(Object o) 					// 获取对象的字符串表现形式
public static boolean equals(Object a, Object b)			// 比较两个对象是否相等
public static boolean isNull(Object obj)					// 判断对象是否为null
public static boolean nonNull(Object obj)					// 判断对象是否不为null
```



我们要了解的Objects类中的常见方法如下所示：

```java
public static <T> T requireNonNull(T obj)					// 检查对象是否不为null,如果为null直接抛出异常；如果不是null返回该对象；
public static <T> T requireNonNullElse(T obj, T defaultObj) // 检查对象是否不为null，如果不为null，返回该对象；如果为null返回defaultObj值
public static <T> T requireNonNullElseGet(T obj, Supplier<? extends T> supplier)	// 检查对象是否不为null，如果不为null，返回该对象；如果															 // 为null,返回由Supplier所提供的值
```

上述方法中的T可以理解为是Object类型。

<font color="red" size="3">**案例演示**</font>

接下来我们就来通过一些案例演示一下Objects类中的这些方法特点。

<font color="blue" size="2">**案例1**</font>：演示重点学习方法

实现步骤：

1. 创建一个学生类，提供两个成员变量（name ， age）；并且提供对应的无参构造方法和有参构造方法以及get/set方法，并且重写toString方法和equals方法
2. 创建一个测试类（ObjectsDemo01）, 在该类中编写测试代码

如下所示：

Student类

```java
public class Student {

    private String name ;       // 姓名
    private String age ;        // 年龄

    // 其他代码略
    ...
        
}
```

ObjectsDemo01测试类

```java
public class ObjectsDemo01 {

    public static void main(String[] args) {

        // 调用方法
        method_04() ;

    }

    // 测试nonNull方法
    public static void method_04() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects类中的nonNull方法
        boolean result = Objects.nonNull(s1);

        // 输出结果
        System.out.println(result);

    }

    // 测试isNull方法
    public static void method_03() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects类中的isNull方法
        boolean result = Objects.isNull(s1);

        // 输出结果
        System.out.println(result);

    }

    // 测试equals方法
    public static void method_02() {

        // 创建两个学生对象
        Student s1 = new Student("itheima" , "14") ;
        Student s2 = new Student("itheima" , "14") ;

        // 调用Objects类中的equals方法，比较两个对象是否相等
        boolean result = Objects.equals(s1, s2);     // 如果Student没有重写Object类中的equals方法，此处比较的还是对象的地址值

        // 输出结果
        System.out.println(result);

    }

    // 测试toString方法
    public static void method_01() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects中的toString方法,获取s1对象的字符串表现形式
        String result = Objects.toString(s1);       // 如果Student没有重写Object类中的toString方法，此处还是返回的对象的地址值

        // 输出结果
        System.out.println(result);

    }

}
```

<font color="blue" size="2">**案例2**</font>：演示需要了解的方法

```java
public class ObjectsDemo02 {

    public static void main(String[] args) {

        // 调用方法
        method_03();

    }

    // 演示requireNonNullElseGet
    public static void method_03() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects对象的requireNonNullElseGet方法,该方法的第二个参数是Supplier类型的，查看源码我们发现Supplier是一个函数式接口,
        // 那么我们就可以为其传递一个Lambda表达式，而在Supplier接口中所定义的方法是无参有返回值的方法，因此具体调用所传入的Lambda表达式如下所示
        Student student = Objects.requireNonNullElseGet(s1, () -> {
            return new Student("itcast", "14");
        });

        // 输出
        System.out.println(student);

    }

    // 演示requireNonNullElse
    public static void method_02() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects对象的requireNonNullElse方法
        Student student = Objects.requireNonNullElse(s1, new Student("itcast", "14"));

        // 输出
        System.out.println(student);

    }

    // 演示requireNonNull
    public static void method_01() {

        // 创建一个学生对象
        Student s1 = new Student("itheima" , "14") ;

        // 调用Objects对象的requireNonNull方法
        Student student = Objects.requireNonNull(s1);

        // 输出
        System.out.println(student);

    }

}
```

注：了解性的方法可以可以作为扩展视频进行下发。

# 6 BigInteger类

## 6.1 引入

​	平时在存储整数的时候，Java中默认是int类型，int类型有取值范围：-2147483648 ~ 2147483647。如果数字过大，我们可以使用long类型，但是如果long类型也表示不下怎么办呢？

​	就需要用到BigInteger，可以理解为：大的整数。

​	有多大呢？理论上最大到42亿的21亿次方

​	基本上在内存撑爆之前，都无法达到这个上限。

## 6.2  概述

查看API文档，我们可以看到API文档中关于BigInteger类的定义如下：

 ![Snipaste_2022-09-04_21-36-01](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\Snipaste_2022-09-04_21-36-01.png)

BigInteger所在包是在java.math包下，因此在使用的时候就需要进行导包。我们可以使用BigInteger类进行大整数的计算

## 6.3 常见方法

<font color="red" size="3">**构造方法**</font>

```java
public BigInteger(int num, Random rnd) 		//获取随机大整数，范围：[0 ~ 2的num次方-1]
public BigInteger(String val) 				//获取指定的大整数
public BigInteger(String val, int radix) 	//获取指定进制的大整数
    
下面这个不是构造，而是一个静态方法获取BigInteger对象
public static BigInteger valueOf(long val) 	//静态方法获取BigInteger的对象，内部有优化
```

**构造方法小结：**

* 如果BigInteger表示的数字没有超出long的范围，可以用静态方法获取。
* 如果BigInteger表示的超出long的范围，可以用构造方法获取。
* 对象一旦创建，BigInteger内部记录的值不能发生改变。
* 只要进行计算都会产生一个新的BigInteger对象



<font color="red" size="3">**常见成员方法**</font>

BigDecimal类中使用最多的还是提供的进行四则运算的方法，如下：

```java
public BigInteger add(BigInteger val)					//加法
public BigInteger subtract(BigInteger val)				//减法
public BigInteger multiply(BigInteger val)				//乘法
public BigInteger divide(BigInteger val)				//除法
public BigInteger[] divideAndRemainder(BigInteger val)	 //除法，获取商和余数
public  boolean equals(Object x) 					    //比较是否相同
public  BigInteger pow(int exponent) 					//次幂、次方
public  BigInteger max/min(BigInteger val) 				//返回较大值/较小值
public  int intValue(BigInteger val) 					//转为int类型整数，超出范围数据有误
```

代码实现：

```java
package com.itheima.a06bigintegerdemo;

import java.math.BigInteger;

public class BigIntegerDemo1 {
    public static void main(String[] args) {
        /*
            public BigInteger(int num, Random rnd) 获取随机大整数，范围:[0~ 2的num次方-11
            public BigInteger(String val) 获取指定的大整数
            public BigInteger(String val, int radix) 获取指定进制的大整数

            public static BigInteger valueOf(long val) 静态方法获取BigInteger的对象，内部有优化

            细节:
            对象一旦创建里面的数据不能发生改变。
        */


        //1.获取一个随机的大整数
        /* Random r=new Random();
            for (int i = e; i < 100; i++) {
            BigInteger bd1 = new BigInteger(4,r);
            System.out.println(bd1);//[@ ~ 15]}
            }
        */

        //2.获取一个指定的大整数，可以超出long的取值范围
        //细节:字符串中必须是整数，否则会报错
        /* BigInteger bd2 = new BigInteger("1.1");
            System.out.println(bd2);
        */

        /*
            BigInteger bd3 = new BigInteger("abc");
            System.out.println(bd3);
         */

        //3.获取指定进制的大整数
        //细节:
        //1.字符串中的数字必须是整数
        //2.字符串中的数字必须要跟进制吻合。
        //比如二进制中，那么只能写日和1，写其他的就报错。
        BigInteger bd4 = new BigInteger("123", 2);
        System.out.println(bd4);

        //4.静态方法获取BigInteger的对象，内部有优化
        //细节:
        //1.能表示范围比较小，只能在long的取值范围之内，如果超出long的范围就不行了。
        //2.在内部对常用的数字: -16 ~ 16 进行了优化。
        //  提前把-16~16 先创建好BigInteger的对象，如果多次获取不会重新创建新的。
        BigInteger bd5 = BigInteger.valueOf(16);
        BigInteger bd6 = BigInteger.valueOf(16);
        System.out.println(bd5 == bd6);//true


        BigInteger bd7 = BigInteger.valueOf(17);
        BigInteger bd8 = BigInteger.valueOf(17);
        System.out.println(bd7 == bd8);//false


        //5.对象一旦创建内部的数据不能发生改变
        BigInteger bd9 =BigInteger.valueOf(1);
        BigInteger bd10 =BigInteger.valueOf(2);
        //此时，不会修改参与计算的BigInteger对象中的借，而是产生了一个新的BigInteger对象记录
        BigInteger result=bd9.add(bd10);
        System.out.println(result);//3

    }
}

```

```java
package com.itheima.a06bigintegerdemo;

import java.math.BigInteger;

public class BigIntegerDemo2 {
    public static void main(String[] args) {
        /*
            public BigInteger add(BigInteger val) 加法
            public BigInteger subtract(BigInteger val) 减法
            public BigInteger multiply(BigInteger val) 乘法
            public BigInteger divide(BigInteger val) 除法，获取商
            public BigInteger[] divideAndRemainder(BigInteger val) 除法，获取商和余数
            public boolean equals(Object x) 比较是否相同
            public BigInteger pow(int exponent) 次幂
            public BigInteger max/min(BigInteger val) 返回较大值/较小值
            public int intValue(BigInteger val) 转为int类型整数，超出范围数据有误
        */

        //1.创建两个BigInteger对象
        BigInteger bd1 = BigInteger.valueOf(10);
        BigInteger bd2 = BigInteger.valueOf(5);

        //2.加法
        BigInteger bd3 = bd1.add(bd2);
        System.out.println(bd3);

        //3.除法，获取商和余数
        BigInteger[] arr = bd1.divideAndRemainder(bd2);
        System.out.println(arr[0]);
        System.out.println(arr[1]);

        //4.比较是否相同
        boolean result = bd1.equals(bd2);
        System.out.println(result);

        //5.次幂
        BigInteger bd4 = bd1.pow(2);
        System.out.println(bd4);

        //6.max
        BigInteger bd5 = bd1.max(bd2);


        //7.转为int类型整数，超出范围数据有误
        /* BigInteger bd6 = BigInteger.valueOf(2147483647L);
         int i = bd6.intValue();
         System.out.println(i);
         */

        BigInteger bd6 = BigInteger.valueOf(200);
        double v = bd6.doubleValue();
        System.out.println(v);//200.0
    }
}

```



## 6.4 底层存储方式：

对于计算机而言，其实是没有数据类型的概念的，都是0101010101，数据类型是编程语言自己规定的，所以在实际存储的时候，先把具体的数字变成二进制，每32个bit为一组，存储在数组中。 

数组中最多能存储元素个数：21亿多

数组中每一位能表示的数字：42亿多

理论上，BigInteger能表示的最大数字为：42亿的21亿次方。

但是还没到这个数字，电脑的内存就会撑爆，所以一般认为BigInteger是无限的。 

存储方式如图所示：

![bigInteger的底层原理](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\bigInteger的底层原理.png)









# 7 BigDecimal类

## 7.1 引入

首先我们来分析一下如下程序的执行结果：

```java
public class BigDecimalDemo01 {

    public static void main(String[] args) {
        System.out.println(0.09 + 0.01);
    }

}
```

这段代码比较简单，就是计算0.09和0.01之和，并且将其结果在控制台进行输出。那么按照我们的想法在控制台输出的结果应该为0.1。那么实际的运行结果是什么呢？我们来运行一下程序，控制台的输出

结果如下所示：

```java
0.09999999999999999
```

这样的结果其实就是一个丢失精度的结果。为什么会产生精度丢失呢？

在使用float或者double类型的数据在进行数学运算的时候，很有可能会产生精度丢失问题。我们都知道计算机底层在进行运算的时候，使用的都是二进制数据； 当我们在程序中写了一个十进制数据 ，在

进行运算的时候，计算机会将这个十进制数据转换成二进制数据，然后再进行运算，计算完毕以后计算机会把运算的结果再转换成十进制数据给我们展示； 如果我们使用的是整数类型的数据进行计算，那

么在把十进制数据转换成二进制数据的时候不会存在精度问题； 如果我们的数据是一个浮点类型的数据，有的时候计算机并不会将这个数据完全转换成一个二进制数据，而是将这个将其转换成一个无限的

趋近于这个十进数的二进制数据； 这样使用一个不太准确的数据进行运算的时候， 最终就会造成精度丢失；为了提高精度，Java就给我们提供了BigDecimal供我们进行数据运算。

## 7.2 概述

查看API文档，我们可以看到API文档中关于BigDecimal类的定义如下：

 ![1576132679789](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576132679789.png)

BigDecimal所在包是在java.math包下，因此在使用的时候就需要进行导包。我们可以使用BigDecimal类进行更加精准的数据计算。

## 7.3 常见方法

<font color="red" size="3">**构造方法**</font>

要用BigDecimal类，那么就需要首先学习一下如何去创建BigDecimal的对象。通过查看API文档，我们可以发现Jdk中针对BigDecimal类提供了很多的构造方法，但是最常用的构造方法是：

 ![1576134383441](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\1576134383441.png)

了解完常见的构造方法以后，我们接下来就重点介绍一下常见的成员方法。

<font color="red" size="3">**常见成员方法**</font>

BigDecimal类中使用最多的还是提供的进行四则运算的方法，如下：

```java
public BigDecimal add(BigDecimal value)				// 加法运算
public BigDecimal subtract(BigDecimal value)		// 减法运算
public BigDecimal multiply(BigDecimal value)		// 乘法运算
public BigDecimal divide(BigDecimal value)			// 触发运算
```

接下来我们就来通过一些案例演示一下这些成员方法的使用。

<font color="blue" size="2">**案例1**</font>：演示基本的四则运算

代码如下所示：

```java
public class BigDecimalDemo01 {

    public static void main(String[] args) {

        // 创建两个BigDecimal对象
        BigDecimal b1 = new BigDecimal("0.3") ;
        BigDecimal b2 = new BigDecimal("4") ;

        // 调用方法进行b1和b2的四则运算，并将其运算结果在控制台进行输出
        System.out.println(b1.add(b2));         // 进行加法运算
        System.out.println(b1.subtract(b2));    // 进行减法运算
        System.out.println(b1.multiply(b2));    // 进行乘法运算
        System.out.println(b1.divide(b2));      // 进行除法运算

    }

}
```

运行程序进行测试，控制台输出结果如下：

```java
4.3
-3.7
1.2
0.075
```

此时我们可以看到使用BigDecimal类来完成浮点数的计算不会存在损失精度的问题。

<font color="blue" size="2">**案例2**</font>：演示除法的特殊情况

如果使用BigDecimal类型的数据进行除法运算的时候，得到的结果是一个无限循环小数，那么就会报错：ArithmeticException。 如下代码所示：

```java
public class BigDecimalDemo02 {

    public static void main(String[] args) {

        // 创建两个BigDecimal对象
        BigDecimal b1 = new BigDecimal("1") ;
        BigDecimal b2 = new BigDecimal("3") ;

        // 调用方法进行b1和b2的除法运算，并且将计算结果在控制台进行输出
        System.out.println(b1.divide(b2));

    }

}
```

运行程序进行测试，控制台输出结果如下所示：

```java
Exception in thread "main" java.lang.ArithmeticException: Non-terminating decimal expansion; no exact representable decimal result.
	at java.base/java.math.BigDecimal.divide(BigDecimal.java:1716)
	at com.itheima.api.bigdecimal.demo02.BigDecimalDemo02.main(BigDecimalDemo02.java:14)
```

针对这个问题怎么解决，此时我们就需要使用到BigDecimal类中另外一个divide方法，如下所示：

```java
BigDecimal divide(BigDecimal divisor, int scale, int roundingMode)
```

上述divide方法参数说明：

```
divisor:			除数对应的BigDecimal对象；
scale:				精确的位数；
roundingMode:		取舍模式；
取舍模式被封装到了RoundingMode这个枚举类中（关于枚举我们后期再做重点讲解），在这个枚举类中定义了很多种取舍方式。最常见的取舍方式有如下几个：
UP(直接进1) ， FLOOR(直接删除) ， HALF_UP(4舍五入),我们可以通过如下格式直接访问这些取舍模式：枚举类名.变量名
```

接下来我们就来演示一下这些取舍模式，代码如下所示：

```java
public class BigDecimalDemo02 {

    public static void main(String[] args) {

        // 调用方法
        method_03() ;

    }

    // 演示取舍模式HALF_UP
    public static void method_03() {

        // 创建两个BigDecimal对象
        BigDecimal b1 = new BigDecimal("0.3") ;
        BigDecimal b2 = new BigDecimal("4") ;

        // 调用方法进行b1和b2的除法运算，并且将计算结果在控制台进行输出
        System.out.println(b1.divide(b2 , 2 , RoundingMode.HALF_UP));

    }

    // 演示取舍模式FLOOR
    public static void method_02() {

        // 创建两个BigDecimal对象
        BigDecimal b1 = new BigDecimal("1") ;
        BigDecimal b2 = new BigDecimal("3") ;

        // 调用方法进行b1和b2的除法运算，并且将计算结果在控制台进行输出
        System.out.println(b1.divide(b2 , 2 , RoundingMode.FLOOR));

    }

    // 演示取舍模式UP
    public static void method_01() {

        // 创建两个BigDecimal对象
        BigDecimal b1 = new BigDecimal("1") ;
        BigDecimal b2 = new BigDecimal("3") ;

        // 调用方法进行b1和b2的除法运算，并且将计算结果在控制台进行输出
        System.out.println(b1.divide(b2 , 2 , RoundingMode.UP));

    }

}
```

小结：后期在进行两个数的除法运算的时候，我们常常使用的是可以设置取舍模式的divide方法。

## 7.4 底层存储方式：

把数据看成字符串，遍历得到里面的每一个字符，把这些字符在ASCII码表上的值，都存储到数组中。

 ![bigdecimal存储原理](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day18-API（常见API，对象克隆）\笔记\assets\bigdecimal存储原理.png)





## 今日内容

* 正则表达式

## 教学目标  

- [ ] 能够理解正则表达式的作用
- [ ] 能够使用正则表达式的字符类
- [ ] 能够使用正则表达式的逻辑运算符
- [ ] 能够使用正则表达式的预定义字符类
- [ ] 能够使用正则表达式的限定符
- [ ] 能够使用正则表达式的分组
- [ ] 能够在String的split方法中使用正则表达式

# 正则表达式

## 1.1 正则表达式的概念及演示

- 在Java中，我们经常需要验证一些字符串，例如：年龄必须是2位的数字、用户名必须是8位长度而且只能包含大小写字母、数字等。正则表达式就是用来验证各种字符串的规则。它内部描述了一些规则，我们可以验证用户输入的字符串是否匹配这个规则。
- 先看一个不使用正则表达式验证的例子：下面的程序让用户输入一个QQ号码，我们要验证：
  - QQ号码必须是5--15位长度
  - 而且必须全部是数字
  - 而且首位不能为0

```java
package com.itheima.a08regexdemo;

public class RegexDemo1 {
    public static void main(String[] args) {
        /* 假如现在要求校验一个qq号码是否正确。
            规则:6位及20位之内，日不能在开头，必须全部是数字。
            先使用目前所学知识完成校验需求然后体验一下正则表达式检验。
        */

        String qq ="1234567890";
        System.out.println(checkQQ(qq));

        System.out.println(qq.matches("[1-9]\\d{5,19}"));

    }

    public static boolean checkQQ(String qq) {
        //规则:6位及20位之内，日不能在开头，必须全部是数字 。
        //核心思想:
        //先把异常数据进行过滤
        //下面的就是满足要求的数据了。
        int len = qq.length();
        if (len < 6 || len > 20) {
            return false;
        }
        //0不能在开头
        if (qq.startsWith("0")) {
            return false;
        }
        //必须全部是数字
        for (int i = 0; i < qq.length(); i++) {
            char c = qq.charAt(i);
            if (c < '0' | c > '9') {
                return false;
            }
        }
        return true;
    }
}
```

- 使用正则表达式验证：

```java
public class Demo {
    public static void main(String[] args) {
        String qq ="1234567890";
        System.out.println(qq.matches("[1-9]\\d{5,19}"));
    }
}
```

**我们接下来就重点学习怎样写正则表达式**

## 1.2 正则表达式-字符类

- 语法示例：

1. \[abc\]：代表a或者b，或者c字符中的一个。
2. \[^abc\]：代表除a,b,c以外的任何字符。
3. [a-z]：代表a-z的所有小写字符中的一个。
4. [A-Z]：代表A-Z的所有大写字符中的一个。
5. [0-9]：代表0-9之间的某一个数字字符。
6. [a-zA-Z0-9]：代表a-z或者A-Z或者0-9之间的任意一个字符。
7. [a-dm-p]：a 到 d 或 m 到 p之间的任意一个字符。 

- 代码示例：

```java
package com.itheima.a08regexdemo;

public class RegexDemo2 {
    public static void main(String[] args) {
        //public boolean matches(String regex):判断是否与正则表达式匹配，匹配返回true
        // 只能是a b c
        System.out.println("-----------1-------------");
        System.out.println("a".matches("[abc]")); // true
        System.out.println("z".matches("[abc]")); // false

        // 不能出现a b c
        System.out.println("-----------2-------------");
        System.out.println("a".matches("[^abc]")); // false
        System.out.println("z".matches("[^abc]")); // true
        System.out.println("zz".matches("[^abc]")); //false
        System.out.println("zz".matches("[^abc][^abc]")); //true

        // a到zA到Z(包括头尾的范围)
        System.out.println("-----------3-------------");
        System.out.println("a".matches("[a-zA-z]")); // true
        System.out.println("z".matches("[a-zA-z]")); // true
        System.out.println("aa".matches("[a-zA-z]"));//false
        System.out.println("zz".matches("[a-zA-Z]")); //false
        System.out.println("zz".matches("[a-zA-Z][a-zA-Z]")); //true
        System.out.println("0".matches("[a-zA-Z]"));//false
        System.out.println("0".matches("[a-zA-Z0-9]"));//true


        // [a-d[m-p]] a到d，或m到p
        System.out.println("-----------4-------------");
        System.out.println("a".matches("[a-d[m-p]]"));//true
        System.out.println("d".matches("[a-d[m-p]]")); //true
        System.out.println("m".matches("[a-d[m-p]]")); //true
        System.out.println("p".matches("[a-d[m-p]]")); //true
        System.out.println("e".matches("[a-d[m-p]]")); //false
        System.out.println("0".matches("[a-d[m-p]]")); //false

        // [a-z&&[def]] a-z和def的交集。为:d，e，f
        System.out.println("----------5------------");
        System.out.println("a".matches("[a-z&[def]]")); //false
        System.out.println("d".matches("[a-z&&[def]]")); //true
        System.out.println("0".matches("[a-z&&[def]]")); //false

        // [a-z&&[^bc]] a-z和非bc的交集。(等同于[ad-z])
        System.out.println("-----------6------------_");
        System.out.println("a".matches("[a-z&&[^bc]]"));//true
        System.out.println("b".matches("[a-z&&[^bc]]")); //false
        System.out.println("0".matches("[a-z&&[^bc]]")); //false

        // [a-z&&[^m-p]] a到z和除了m到p的交集。(等同于[a-1q-z])
        System.out.println("-----------7-------------");
        System.out.println("a".matches("[a-z&&[^m-p]]")); //true
        System.out.println("m".matches("[a-z&&[^m-p]]")); //false
        System.out.println("0".matches("[a-z&&[^m-p]]")); //false

    }
}

```

## 1.3 正则表达式-逻辑运算符

- 语法示例：
  1. &&：并且
  2. |    ：或者
  3. \  ：转义字符
- 代码示例：

```java
public class Demo {
	public static void main(String[] args) {
		String str = "had";
		
		//1.要求字符串是小写辅音字符开头，后跟ad
		String regex = "[a-z&&[^aeiou]]ad";
		System.out.println("1." + str.matches(regex));
		
		//2.要求字符串是aeiou中的某个字符开头，后跟ad
		regex = "[a|e|i|o|u]ad";//这种写法相当于：regex = "[aeiou]ad";
		System.out.println("2." + str.matches(regex));
	}
}

```

```java
package com.itheima.a08regexdemo;

public class RegexDemo3 {
    public static void main(String[] args) {
        // \ 转义字符 改变后面那个字符原本的含义
        //练习:以字符串的形式打印一个双引号
        //"在Java中表示字符串的开头或者结尾

        //此时\表示转义字符，改变了后面那个双引号原本的含义
        //把他变成了一个普普通通的双引号而已。
        System.out.println("\"");

        // \表示转义字符
        //两个\的理解方式：前面的\是一个转义字符，改变了后面\原本的含义，把他变成一个普普通通的\而已。
        System.out.println("c:Users\\moon\\IdeaProjects\\basic-code\\myapi\\src\\com\\itheima\\a08regexdemo\\RegexDemo1.java");




    }
}

```



## 1.4 正则表达式-预定义字符

- 语法示例：
  1. "." ： 匹配任何字符。
  2. "\d"：任何数字[0-9]的简写；
  3. "\D"：任何非数字\[^0-9\]的简写；
  4. "\s"： 空白字符：[ \t\n\x0B\f\r] 的简写
  5. "\S"： 非空白字符：\[^\s\] 的简写
  6. "\w"：单词字符：[a-zA-Z_0-9]的简写
  7. "\W"：非单词字符：\[^\w\]
- 代码示例：

```java
public class Demo {
	public static void main(String[] args) {
        //.表示任意一个字符
        System.out.println("你".matches("..")); //false
        System.out.println("你".matches(".")); //true
        System.out.println("你a".matches(".."));//true

        // \\d 表示任意的一个数字
        // \\d只能是任意的一位数字
        // 简单来记:两个\表示一个\
        System.out.println("a".matches("\\d")); // false
        System.out.println("3".matches("\\d")); // true
        System.out.println("333".matches("\\d")); // false

        //\\w只能是一位单词字符[a-zA-Z_0-9]
        System.out.println("z".matches("\\w")); // true
        System.out.println("2".matches("\\w")); // true
        System.out.println("21".matches("\\w")); // false
        System.out.println("你".matches("\\w"));//false

        // 非单词字符
        System.out.println("你".matches("\\W")); // true
        System.out.println("---------------------------------------------");
        // 以上正则匹配只能校验单个字符。


        // 必须是数字 字母 下划线 至少 6位
        System.out.println("2442fsfsf".matches("\\w{6,}"));//true
        System.out.println("244f".matches("\\w{6,}"));//false

        // 必须是数字和字符 必须是4位
        System.out.println("23dF".matches("[a-zA-Z0-9]{4}"));//true
        System.out.println("23 F".matches("[a-zA-Z0-9]{4}"));//false
        System.out.println("23dF".matches("[\\w&&[^_]]{4}"));//true
        System.out.println("23_F".matches("[\\w&&[^_]]{4}"));//false
		
	}
}
```

## 1.5 正则表达式-数量词

- 语法示例：
  1. X? : 0次或1次
  2. X* : 0次到多次
  3. X+ : 1次或多次
  4. X{n} : 恰好n次
  5. X{n,} : 至少n次
  6. X{n,m}: n到m次(n和m都是包含的)
- 代码示例：

```java
public class Demo {
	public static void main(String[] args) {
		 // 必须是数字 字母 下划线 至少 6位
        System.out.println("2442fsfsf".matches("\\w{6,}"));//true
        System.out.println("244f".matches("\\w{6,}"));//false

        // 必须是数字和字符 必须是4位
        System.out.println("23dF".matches("[a-zA-Z0-9]{4}"));//true
        System.out.println("23 F".matches("[a-zA-Z0-9]{4}"));//false
        System.out.println("23dF".matches("[\\w&&[^_]]{4}"));//true
        System.out.println("23_F".matches("[\\w&&[^_]]{4}"));//false
	}
}

```

## 1.6 正则表达式练习1

需求：

​	请编写正则表达式验证用户输入的手机号码是否满足要求。

​	请编写正则表达式验证用户输入的邮箱号是否满足要求。

​	请编写正则表达式验证用户输入的电话号码是否满足要求。

​	验证手机号码 13112345678 13712345667 13945679027 139456790271

​	验证座机电话号码 020-2324242 02122442 027-42424 0712-3242434

​	验证邮箱号码 3232323@qq.com zhangsan@itcast.cnn dlei0009@163.com dlei0009@pci.com.cn

代码示例：

```java
package com.itheima.a08regexdemo;

public class RegexDemo4 {
    public static void main(String[] args) {
        /*
            需求
            请编写正则表达式验证用户输入的手机号码是否满足要求。请编写正则表达式验证用户输入的邮箱号是否满足要求。请编写正则表达式验证用户输入的电话号码是否满足要求。
            验证手机号码 13112345678 13712345667 13945679027 139456790271
            验证座机电话号码 020-2324242 02122442 027-42424 0712-3242434
            验证邮箱号码 3232323@qq.com zhangsan@itcast.cnn dlei0009@163.com dlei0009@pci.com.cn
        */

        //心得:
        //拿着一个正确的数据，从左到右依次去写。
        //13112345678
        //分成三部分:
        //第一部分:1 表示手机号码只能以1开头
        //第二部分:[3-9] 表示手机号码第二位只能是3-9之间的
        //第三部分:\\d{9} 表示任意数字可以出现9次，也只能出现9次
        String regex1 = "1[3-9]\\d{9}";
        System.out.println("13112345678".matches(regex1));//true
        System.out.println("13712345667".matches(regex1));//true
        System.out.println("13945679027".matches(regex1));//true
        System.out.println("139456790271".matches(regex1));//false
        System.out.println("-----------------------------------");

        //座机电话号码
        //020-2324242 02122442 027-42424 0712-3242434
        //思路:
        //在书写座机号正则的时候需要把正确的数据分为三部分
        //一:区号@\\d{2,3}
        //      0:表示区号一定是以0开头的
        //      \\d{2,3}:表示区号从第二位开始可以是任意的数字，可以出现2到3次。
        //二:- ?表示次数，0次或一次
        //三:号码 号码的第一位也不能以日开头，从第二位开始可以是任意的数字，号码的总长度:5-10位
        String regex2 = "0\\d{2,3}-?[1-9]\\d{4,9}";
        System.out.println("020-2324242".matches(regex2));
        System.out.println("02122442".matches(regex2));
        System.out.println("027-42424".matches(regex2));
        System.out.println("0712-3242434".matches(regex2));

        //邮箱号码
        //3232323@qq.com zhangsan@itcast.cnn dlei0009@163.com dlei0009@pci.com.cn
        //思路:
        //在书写邮箱号码正则的时候需要把正确的数据分为三部分
        //第一部分:@的左边 \\w+
        //      任意的字母数字下划线，至少出现一次就可以了
        //第二部分:@ 只能出现一次
        //第三部分:
        //      3.1         .的左边[\\w&&[^_]]{2,6}
        //                  任意的字母加数字，总共出现2-6次(此时不能出现下划线)
        //      3.2         . \\.
        //      3.3         大写字母，小写字母都可以，只能出现2-3次[a-zA-Z]{2,3}
        //      我们可以把3.2和3.3看成一组，这一组可以出现1次或者两次
        String regex3 = "\\w+@[\\w&&[^_]]{2,6}(\\.[a-zA-Z]{2,3}){1,2}";
        System.out.println("3232323@qq.com".matches(regex3));
        System.out.println("zhangsan@itcast.cnn".matches(regex3));
        System.out.println("dlei0009@163.com".matches(regex3));
        System.out.println("dlei0009@pci.com.cn".matches(regex3));


        //24小时的正则表达式
        String regex4 = "([01]\\d|2[0-3]):[0-5]\\d:[0-5]\\d";
        System.out.println("23:11:11".matches(regex4));

        String regex5 = "([01]\\d 2[0-3])(:[0-5]\\d){2}";
        System.out.println("23:11:11".matches(regex5));
    }
}

```

## 1.7 正则表达式练习2

需求
	请编写正则表达式验证用户名是否满足要求。要求:大小写字母，数字，下划线一共4-16位
	请编写正则表达式验证身份证号码是否满足要求。
	简单要求:
    		18位，前17位任意数字，最后一位可以是数字可以是大写或小写的x
	复杂要求:
    		按照身份证号码的格式严格要求。

​	身份证号码:
​		41080119930228457x
​		510801197609022309
​		15040119810705387X
​		130133197204039024 
​		430102197606046442

代码示例：

```java
public class RegexDemo5 {
    public static void main(String[] args) {
        /*
            正则表达式练习:
            需求
            请编写正则表达式验证用户名是否满足要求。要求:大小写字母，数字，下划线一共4-16位
            请编写正则表达式验证身份证号码是否满足要求。
            简单要求:
                18位，前17位任意数字，最后一位可以是数字可以是大写或小写的x
            复杂要求:
                按照身份证号码的格式严格要求。

            身份证号码:
            41080119930228457x
            510801197609022309
            15040119810705387X
            130133197204039024 I
            430102197606046442
        */

        //用户名要求:大小写字母，数字，下划线一共4-16位
        String regex1 = "\\w{4,16}";
        System.out.println("zhangsan".matches(regex1));
        System.out.println("lisi".matches(regex1));
        System.out.println("wangwu".matches(regex1));
        System.out.println("$123".matches(regex1));


        //身份证号码的简单校验:
        //18位，前17位任意数字，最后一位可以是数字可以是大写或小写的x
        String regex2 = "[1-9]\\d{16}(\\d|x|x)";
        String regex3 = "[1-9]\\d{16}[\\dXx]";
        String regex5 = "[1-9]\\d{16}(\\d(?i)x)";

        System.out.println("41080119930228457x".matches(regex3));
        System.out.println("510801197609022309".matches(regex3));
        System.out.println("15040119810705387X".matches(regex3));
        System.out.println("130133197204039024".matches(regex3));
        System.out.println("430102197606046442".matches(regex3));


        //忽略大小写的书写方式
        //在匹配的时候忽略abc的大小写
        String regex4 = "a((?i)b)c";
        System.out.println("------------------------------");
        System.out.println("abc".matches(regex4));//true
        System.out.println("ABC".matches(regex4));//false
        System.out.println("aBc".matches(regex4));//true


        //身份证号码的严格校验
        //编写正则的小心得:
        //第一步:按照正确的数据进行拆分
        //第二步:找每一部分的规律，并编写正则表达式
        //第三步:把每一部分的正则拼接在一起，就是最终的结果
        //书写的时候:从左到右去书写。

        //410801 1993 02 28 457x
        //前面6位:省份，市区，派出所等信息，第一位不能是0，后面5位是任意数字       [1-9]\\d{5}
        //年的前半段: 18 19 20                                                (18|19|20)
        //年的后半段: 任意数字出现两次                                           \\d{2}
        //月份: 01~ 09 10 11 12                                               (@[1-9]|1[0-2])
        //日期: 01~09 10~19 20~29 30 31                                       (0[1-9]|[12]\\d|3[01])
        //后面四位: 任意数字出现3次 最后一位可以是数字也可以是大写x或者小写x        \\d{3}[\\dXx]
        String regex6 = "[1-9]\\d{5}(18|19|20)\\d{2}(@[1-9]|1[0-2])(@[1-9]|[12]\\d|3[01])\\d{3}[\\dxXx]";

        System.out.println("41080119930228457x".matches(regex6));
        System.out.println("510801197609022309".matches(regex6));
        System.out.println("15040119810705387X".matches(regex6));
        System.out.println("130133197204039024".matches(regex6));
        System.out.println("430102197606046442".matches(regex6));


    }
}

```

## 1.8 本地数据爬取

Pattern：表示正则表达式
Matcher：文本匹配器，作用按照正则表达式的规则去读取字符串，从头开始读取。
         	在大串中去找符合匹配规则的子串。

代码示例：

```java
package com.itheima.a08regexdemo;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class RegexDemo6 {
    public static void main(String[] args) {
        /* 有如下文本，请按照要求爬取数据。
                Java自从95年问世以来，经历了很多版本，目前企业中用的最多的是Java8和Java11，
                因为这两个是长期支持版本，下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台
                要求:找出里面所有的JavaXX
         */

        String str = "Java自从95年问世以来，经历了很多版本，目前企业中用的最多的是Java8和Java11，" +
                "因为这两个是长期支持版本，下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台";


        //1.获取正则表达式的对象
        Pattern p = Pattern.compile("Java\\d{0,2}");
        //2.获取文本匹配器的对象
        //拿着m去读取str，找符合p规则的子串
        Matcher m = p.matcher(str);

        //3.利用循环获取
        while (m.find()) {
            String s = m.group();
            System.out.println(s);
        }


    }

    private static void method1(String str) {
        //Pattern:表示正则表达式
        //Matcher: 文本匹配器，作用按照正则表达式的规则去读取字符串，从头开始读取。
        //          在大串中去找符合匹配规则的子串。

        //获取正则表达式的对象
        Pattern p = Pattern.compile("Java\\d{0,2}");
        //获取文本匹配器的对象
        //m:文本匹配器的对象
        //str:大串
        //p:规则
        //m要在str中找符合p规则的小串
        Matcher m = p.matcher(str);

        //拿着文本匹配器从头开始读取，寻找是否有满足规则的子串
        //如果没有，方法返回false
        //如果有，返回true。在底层记录子串的起始索引和结束索引+1
        // 0,4
        boolean b = m.find();

        //方法底层会根据find方法记录的索引进行字符串的截取
        // substring(起始索引，结束索引);包头不包尾
        // (0,4)但是不包含4索引
        // 会把截取的小串进行返回。
        String s1 = m.group();
        System.out.println(s1);


        //第二次在调用find的时候，会继续读取后面的内容
        //读取到第二个满足要求的子串，方法会继续返回true
        //并把第二个子串的起始索引和结束索引+1，进行记录
        b = m.find();

        //第二次调用group方法的时候，会根据find方法记录的索引再次截取子串
        String s2 = m.group();
        System.out.println(s2);
    }
}
```

## 1.9 网络数据爬取（了解）

需求：

​	把连接:https://m.sengzan.com/jiaoyu/29104.html?ivk sa=1025883i中所有的身份证号码都爬取出来。

代码示例：

```java
public class RegexDemo7 {
    public static void main(String[] args) throws IOException {
        /* 扩展需求2:
            把连接:https://m.sengzan.com/jiaoyu/29104.html?ivk sa=1025883i
            中所有的身份证号码都爬取出来。
        */

        //创建一个URL对象
        URL url = new URL("https://m.sengzan.com/jiaoyu/29104.html?ivk sa=1025883i");
        //连接上这个网址
        //细节:保证网络是畅通
        URLConnection conn = url.openConnection();//创建一个对象去读取网络中的数据
        BufferedReader br = new BufferedReader(new InputStreamReader(conn.getInputStream()));
        String line;
        //获取正则表达式的对象pattern
        String regex = "[1-9]\\d{17}";
        Pattern pattern = Pattern.compile(regex);//在读取的时候每次读一整行
        while ((line = br.readLine()) != null) {
            //拿着文本匹配器的对象matcher按照pattern的规则去读取当前的这一行信息
            Matcher matcher = pattern.matcher(line);
            while (matcher.find()) {
                System.out.println(matcher.group());
            }
        }
        br.close();
    }
}

```

## 1.10 爬取数据练习

需求：

​	把下面文本中的座机电话，邮箱，手机号，热线都爬取出来。

来黑马程序员学习Java，手机号:18512516758，18512508907或者联系邮箱:boniu@itcast.cn，座机电话:01036517895，010-98951256邮箱:bozai@itcast.cn，热线电话:400-618-9090 ，400-618-4000，4006184000，4006189090手机号的正则表达式:1[3-9]\d{9}

代码示例：

```java
package com.itheima.a08regexdemo;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class RegexDemo8 {
    public static void main(String[] args) {
        /*
            需求:把下面文本中的座机电话，邮箱，手机号，热线都爬取出来。
            来黑马程序员学习Java，
            手机号:18512516758，18512508907或者联系邮箱:boniu@itcast.cn，
            座机电话:01036517895，010-98951256邮箱:bozai@itcast.cn，
            热线电话:400-618-9090 ，400-618-4000，4006184000，4006189090

            手机号的正则表达式:1[3-9]\d{9}
            邮箱的正则表达式:\w+@[\w&&[^_]]{2,6}(\.[a-zA-Z]{2,3}){1,2}座机电话的正则表达式:θ\d{2,3}-?[1-9]\d{4,9}
            热线电话的正则表达式:400-?[1-9]\\d{2}-?[1-9]\\d{3}

        */

        String s = "来黑马程序员学习Java，" +
                "电话:18512516758，18512508907" + "或者联系邮箱:boniu@itcast.cn，" +
                "座机电话:01036517895，010-98951256" + "邮箱:bozai@itcast.cn，" +
                "热线电话:400-618-9090 ，400-618-4000，4006184000，4006189090";

        System.out.println("400-618-9090");

        String regex = "(1[3-9]\\d{9})|(\\w+@[\\w&&[^_]]{2,6}(\\.[a-zA-Z]{2,3}){1,2})" +
                "|(0\\d{2,3}-?[1-9]\\d{4,9})" +
                "(400-?[1-9]\\d{2}-?[1-9]\\d{3})";

        //1.获取正则表达式的对象
        Pattern p = Pattern.compile(regex);

        //2.获取文本匹配器的对象
        //利用m去读取s，会按照p的规则找里面的小串
        Matcher m = p.matcher(s);
        //3.利用循环获取每一个数据 while(m.find()){
        String str = m.group();
        System.out.println(str);

    }
}
```

## 1.11 按要求爬取

需求：

​	有如下文本，按要求爬取数据。   

​	 Java自从95年问世以来，经历了很多版本，目前企业中用的最多的是Java8和Java11，因为这两个是长期支持版本，下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台。

需求1：

​	爬取版本号为8，11.17的Java文本，但是只要Java，不显示版本号。

需求2：

​	爬取版本号为8，11，17的Java文本。正确爬取结果为：Java8 Java11 Java17 Java17

需求3：

​	爬取除了版本号为8，11，17的Java文本。
代码示例：

```java
public class RegexDemo9 {
    public static void main(String[] args) {
        /*
            有如下文本，按要求爬取数据。
                Java自从95年问世以来，经历了很多版本，目前企业中用的最多的是Java8和Java11，
                因为这两个是长期支持版本，下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台


            需求1:爬取版本号为8，11.17的Java文本，但是只要Java，不显示版本号。
            需求2:爬取版本号为8，11，17的Java文本。正确爬取结果为:Java8 Java11 Java17 Java17
            需求3:爬取除了版本号为8，11.17的Java文本，
        */
        String s = "Java自从95年问世以来，经历了很多版本，目前企业中用的最多的是Java8和Java11，" +
            "因为这两个是长期支持版本，下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台";

        //1.定义正则表达式
        //?理解为前面的数据Java
        //=表示在Java后面要跟随的数据
        //但是在获取的时候，只获取前半部分
        //需求1:
        String regex1 = "((?i)Java)(?=8|11|17)";
        //需求2:
        String regex2 = "((?i)Java)(8|11|17)";
        String regex3 = "((?i)Java)(?:8|11|17)";
        //需求3:
        String regex4 = "((?i)Java)(?!8|11|17)";

        Pattern p = Pattern.compile(regex4);
        Matcher m = p.matcher(s);
        while (m.find()) {
            System.out.println(m.group());
        }
    }
}

```

## 1.12 贪婪爬取和非贪婪爬取

```java
只写+和表示贪婪匹配，如果在+和后面加问号表示非贪婪爬取
+? 非贪婪匹配
*? 非贪婪匹配
贪婪爬取:在爬取数据的时候尽可能的多获取数据
非贪婪爬取:在爬取数据的时候尽可能的少获取数据

举例：
如果获取数据：ab+
贪婪爬取获取结果:abbbbbbbbbbbb
非贪婪爬取获取结果:ab
```

代码示例：

```java
public class RegexDemo10 {
    public static void main(String[] args) {
        /*
            只写+和*表示贪婪匹配

            +? 非贪婪匹配
            *? 非贪婪匹配

            贪婪爬取:在爬取数据的时候尽可能的多获取数据
            非贪婪爬取:在爬取数据的时候尽可能的少获取数据

            ab+:
            贪婪爬取:abbbbbbbbbbbb
            非贪婪爬取:ab
        */
        String s = "Java自从95年问世以来，abbbbbbbbbbbbaaaaaaaaaaaaaaaaaa" +
                "经历了很多版木，目前企业中用的最多的是]ava8和]ava11，因为这两个是长期支持版木。" +
                "下一个长期支持版本是Java17，相信在未来不久Java17也会逐渐登上历史舞台";

        String regex = "ab+";
        Pattern p = Pattern.compile(regex);
        Matcher m = p.matcher(s);

        while (m.find()) {
            System.out.println(m.group());
        }


    }
}

```

## 1.13 String的split方法中使用正则表达式

- String类的split()方法原型：

  ```java
  public String[] split(String regex)
  //参数regex表示正则表达式。可以将当前字符串中匹配regex正则表达式的符号作为"分隔符"来切割字符串。
  ```

- 代码示例：

```java
/*
            有一段字符串:小诗诗dqwefqwfqwfwq12312小丹丹dqwefqwfqwfwq12312小惠惠
            要求1:把字符串中三个姓名之间的字母替换为vs
            要求2:把字符串中的三个姓名切割出来*/

String s = "小诗诗dqwefqwfqwfwq12312小丹丹dqwefqwfqwfwq12312小惠惠";
//细节:
//方法在底层跟之前一样也会创建文本解析器的对象
//然后从头开始去读取字符串中的内容，只要有满足的，那么就切割。
String[] arr = s.split("[\\w&&[^_]]+");
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

## 1.14 String类的replaceAll方法中使用正则表达式

- String类的replaceAll()方法原型：

```java
public String replaceAll(String regex,String newStr)
//参数regex表示一个正则表达式。可以将当前字符串中匹配regex正则表达式的字符串替换为newStr。
```

- 代码示例：

```java
/*
            有一段字符串:小诗诗dqwefqwfqwfwq12312小丹丹dqwefqwfqwfwq12312小惠惠
            要求1:把字符串中三个姓名之间的字母替换为vs
            要求2:把字符串中的三个姓名切割出来*/

String s = "小诗诗dqwefqwfqwfwq12312小丹丹dqwefqwfqwfwq12312小惠惠";
//细节:
//方法在底层跟之前一样也会创建文本解析器的对象
//然后从头开始去读取字符串中的内容，只要有满足的，那么就用第一个参数去替换。
String result1 = s.replaceAll("[\\w&&[^_]]+", "vs");
System.out.println(result1);
```

## 1.15 正则表达式-分组括号( )

细节：如何识别组号？

只看左括号，不看有括号，按照左括号的顺序，从左往右，依次为第一组，第二组，第三组等等

```java
//需求1:判断一个字符串的开始字符和结束字符是否一致?只考虑一个字符
//举例: a123a b456b 17891 &abc& a123b(false)
// \\组号:表示把第X组的内容再出来用一次
String regex1 = "(.).+\\1";
System.out.println("a123a".matches(regex1));
System.out.println("b456b".matches(regex1));
System.out.println("17891".matches(regex1));
System.out.println("&abc&".matches(regex1));
System.out.println("a123b".matches(regex1));
System.out.println("--------------------------");


//需求2:判断一个字符串的开始部分和结束部分是否一致?可以有多个字符
//举例: abc123abc b456b 123789123 &!@abc&!@ abc123abd(false)
String regex2 = "(.+).+\\1";
System.out.println("abc123abc".matches(regex2));
System.out.println("b456b".matches(regex2));
System.out.println("123789123".matches(regex2));
System.out.println("&!@abc&!@".matches(regex2));
System.out.println("abc123abd".matches(regex2));
System.out.println("---------------------");

//需求3:判断一个字符串的开始部分和结束部分是否一致?开始部分内部每个字符也需要一致
//举例: aaa123aaa bbb456bbb 111789111 &&abc&&
//(.):把首字母看做一组
// \\2:把首字母拿出来再次使用
// *:作用于\\2,表示后面重复的内容出现日次或多次
String regex3 = "((.)\\2*).+\\1";
System.out.println("aaa123aaa".matches(regex3));
System.out.println("bbb456bbb".matches(regex3));
System.out.println("111789111".matches(regex3));
System.out.println("&&abc&&".matches(regex3));
System.out.println("aaa123aab".matches(regex3));
```

## 1.16 分组练习

需求:

​    将字符串：我要学学编编编编程程程程程程。

​    替换为：我要学编程

```java
String str = "我要学学编编编编程程程程程程";

//需求:把重复的内容 替换为 单个的
//学学                学
//编编编编            编
//程程程程程程        程
//  (.)表示把重复内容的第一个字符看做一组
//  \\1表示第一字符再次出现
//  + 至少一次
//  $1 表示把正则表达式中第一组的内容，再拿出来用
String result = str.replaceAll("(.)\\1+", "$1");
System.out.println(result);
```

## 1.17 忽略大小写的写法

```java
//(?i) ：表示忽略后面数据的大小写
//忽略abc的大小写
String regex = "(?i)abc";
//a需要一模一样，忽略bc的大小写
String regex = "a(?i)bc";
//ac需要一模一样，忽略b的大小写
String regex = "a((?i)b)c";
```

## 1.18 非捕获分组

非捕获分组：分组之后不需要再用本组数据，仅仅是把数据括起来。

```java
//身份证号码的简易正则表达式
//非捕获分组:仅仅是把数据括起来
//特点:不占用组号
//这里\\1报错原因:(?:)就是非捕获分组，此时是不占用组号的。


//(?:) (?=) (?!)都是非捕获分组//更多的使用第一个
//String regex1 ="[1-9]\\d{16}(?:\\d|x|x)\\1";
String regex2 ="[1-9]\\d{16}(\\d Xx)\\1";
//^([01]\d|2[0-3]):[0-5]\d:[@-5]\d$

System.out.println("41080119930228457x".matches(regex2));
```

## 1.19 正则表达式练习

```java
手机号码:1[3-9]\\d{9}
座机号码：0\\d{2,3}-?[1-9]\\d{4,9}
邮箱号码：\\w+@[\\w&&[^_]]{2,6}(\\.[a-zA-Z]{2,3}){1,2}
24小时：([01]\\d|2[0-3]):[0-5]\\d:[0-5]\\d
	   ([01]\\d|2[0-3])(:[0-5]\\d){2}
用户名:	\\w{4,16}
身份证号码，简单校验：
		[1-9]\\d{16}(\\d|X|x)
		[1-9]\\d{16}[\\dXx]
		[1-9]\\d{16}(\\d(?i)X)
身份证号码，严格校验：
		[1-9]\\d{5}(18|19|20)\\d{2}(0[1-9]|1[0-2])(0[1-9|[12])\\d|3[01])\\d{3}[\\dXx]
```





# day04【常用API】

## 今日内容

* JDK7时间相关类
* JDK8时间相关类
* 包装类
* 综合练习
* Collection集合

## 教学目标

- [ ] 能够使用日期类输出当前日期
- [ ] 能够使用将日期格式化为字符串的方法
- [ ] 能够使用将字符串转换成日期的方法
- [ ] 能够说出8种基本类型对应的包装类名称
- [ ] 能够说出自动装箱、自动拆箱的概念
- [ ] 能够将字符串转换为对应的基本类型
- [ ] 能够将基本类型转换为对应的字符串
- [ ] 能够完成课题上讲解的所有练习

# 第一章 Date类

## 1.1 Date概述

java.util.Date`类 表示特定的瞬间，精确到毫秒。

继续查阅Date类的描述，发现Date拥有多个构造函数，只是部分已经过时，我们重点看以下两个构造函数

- `public Date()`：从运行程序的此时此刻到时间原点经历的毫秒值,转换成Date对象，分配Date对象并初始化此对象，以表示分配它的时间（精确到毫秒）。
- `public Date(long date)`：将指定参数的毫秒值date,转换成Date对象，分配Date对象并初始化此对象，以表示自从标准基准时间（称为“历元（epoch）”，即1970年1月1日00:00:00 GMT）以来的指定毫秒数。

> tips: 由于中国处于东八区（GMT+08:00）是比世界协调时间/格林尼治时间（GMT）快8小时的时区，当格林尼治标准时间为0:00时，东八区的标准时间为08:00。

简单来说：使用无参构造，可以自动设置当前系统时间的毫秒时刻；指定long类型的构造参数，可以自定义毫秒时刻。例如：

```java
import java.util.Date;

public class Demo01Date {
    public static void main(String[] args) {
        // 创建日期对象，把当前的时间
        System.out.println(new Date()); // Tue Jan 16 14:37:35 CST 2020
        // 创建日期对象，把当前的毫秒值转成日期对象
        System.out.println(new Date(0L)); // Thu Jan 01 08:00:00 CST 1970
    }
}
```

> tips:在使用println方法时，会自动调用Date类中的toString方法。Date类对Object类中的toString方法进行了覆盖重写，所以结果为指定格式的字符串。

## 1.2 Date常用方法

Date类中的多数方法已经过时，常用的方法有：

- `public long getTime()` 把日期对象转换成对应的时间毫秒值。
- `public void setTime(long time)` 把方法参数给定的毫秒值设置给日期对象

示例代码

```java
public class DateDemo02 {
    public static void main(String[] args) {
        //创建日期对象
        Date d = new Date();
        
        //public long getTime():获取的是日期对象从1970年1月1日 00:00:00到现在的毫秒值
        //System.out.println(d.getTime());
        //System.out.println(d.getTime() * 1.0 / 1000 / 60 / 60 / 24 / 365 + "年");

        //public void setTime(long time):设置时间，给的是毫秒值
        //long time = 1000*60*60;
        long time = System.currentTimeMillis();
        d.setTime(time);

        System.out.println(d);
    }
}
```

> 小结：Date表示特定的时间瞬间，我们可以使用Date对象对时间进行操作。

# 第二章 SimpleDateFormat类

`java.text.SimpleDateFormat` 是日期/时间格式化类，我们通过这个类可以帮我们完成日期和文本之间的转换,也就是可以在Date对象与String对象之间进行来回转换。

- **格式化**：按照指定的格式，把Date对象转换为String对象。
- **解析**：按照指定的格式，把String对象转换为Date对象。

## 2.1 构造方法

由于DateFormat为抽象类，不能直接使用，所以需要常用的子类`java.text.SimpleDateFormat`。这个类需要一个模式（格式）来指定格式化或解析的标准。构造方法为：

- `public SimpleDateFormat(String pattern)`：用给定的模式和默认语言环境的日期格式符号构造SimpleDateFormat。参数pattern是一个字符串，代表日期时间的自定义格式。

## 2.2 格式规则

常用的格式规则为：

| 标识字母（区分大小写） | 含义 |
| ---------------------- | ---- |
| y                      | 年   |
| M                      | 月   |
| d                      | 日   |
| H                      | 时   |
| m                      | 分   |
| s                      | 秒   |

> 备注：更详细的格式规则，可以参考SimpleDateFormat类的API文档。

## 2.3 常用方法

DateFormat类的常用方法有：

- `public String format(Date date)`：将Date对象格式化为字符串。

- `public Date parse(String source)`：将字符串解析为Date对象。

  ```java
  package com.itheima.a01jdk7datedemo;
  
  import java.text.ParseException;
  import java.text.SimpleDateFormat;
  import java.util.Date;
  
  public class A03_SimpleDateFormatDemo1 {
      public static void main(String[] args) throws ParseException {
          /*
              public simpleDateFormat() 默认格式
              public simpleDateFormat(String pattern) 指定格式
              public final string format(Date date) 格式化(日期对象 ->字符串)
              public Date parse(string source) 解析(字符串 ->日期对象)
          */
  
          //1.定义一个字符串表示时间
          String str = "2023-11-11 11:11:11";
          //2.利用空参构造创建simpleDateFormat对象
          // 细节:
          //创建对象的格式要跟字符串的格式完全一致
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
          Date date = sdf.parse(str);
          //3.打印结果
          System.out.println(date.getTime());//1699672271000
  
  
      }
  
      private static void method1() {
          //1.利用空参构造创建simpleDateFormat对象，默认格式
          SimpleDateFormat sdf1 = new SimpleDateFormat();
          Date d1 = new Date(0L);
          String str1 = sdf1.format(d1);
          System.out.println(str1);//1970/1/1 上午8:00
  
          //2.利用带参构造创建simpleDateFormat对象，指定格式
          SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy年MM月dd日HH:mm:ss");
          String str2 = sdf2.format(d1);
          System.out.println(str2);//1970年01月01日 08:00:00
  
          //课堂练习:yyyy年MM月dd日 时:分:秒 星期
      }
  }
  
  ```

> 小结：DateFormat可以将Date对象和字符串相互转换。

## 2.4 练习1(初恋女友的出生日期)

```java
/*
     假设，你初恋的出生年月日为:2000-11-11
     请用字符串表示这个数据，并将其转换为:2000年11月11日

     创建一个Date对象表示2000年11月11日
     创建一个SimpleDateFormat对象，并定义格式为年月日把时间变成:2000年11月11日
*/

//1.可以通过2000-11-11进行解析，解析成一个Date对象
String str = "2000-11-11";
//2.解析
SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd");
Date date = sdf1.parse(str);
//3.格式化
SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy年MM月dd日");
String result = sdf2.format(date);
System.out.println(result);
```

## 2.5 练习2(秒杀活动)

```java
/* 需求:
            秒杀活动开始时间:2023年11月11日 0:0:0(毫秒值)
            秒杀活动结束时间:2023年11月11日 0:10:0(毫秒值)

            小贾下单并付款的时间为:2023年11月11日 0:01:0
            小皮下单并付款的时间为:2023年11月11日 0:11:0
            用代码说明这两位同学有没有参加上秒杀活动?
         */

//1.定义字符串表示三个时间
String startstr = "2023年11月11日 0:0:0";
String endstr = "2023年11月11日 0:10:0";
String orderstr = "2023年11月11日 0:01:00";
//2.解析上面的三个时间，得到Date对象
SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日HH:mm:ss");
Date startDate = sdf.parse(startstr);
Date endDate = sdf.parse(endstr);
Date orderDate = sdf.parse(orderstr);

//3.得到三个时间的毫秒值
long startTime = startDate.getTime();
long endTime = endDate.getTime();
long orderTime = orderDate.getTime();

//4.判断
if (orderTime >= startTime && orderTime <= endTime) {
    System.out.println("参加秒杀活动成功");
} else {
    System.out.println("参加秒杀活动失败");
}
```

# 第三章 Calendar类

## 3.1 概述

- java.util.Calendar类表示一个“日历类”，可以进行日期运算。它是一个抽象类，不能创建对象，我们可以使用它的子类：java.util.GregorianCalendar类。
- 有两种方式可以获取GregorianCalendar对象：
  - 直接创建GregorianCalendar对象；
  - 通过Calendar的静态方法getInstance()方法获取GregorianCalendar对象【本次课使用】

## 3.2 常用方法

| 方法名                                | 说明                                                         |
| ------------------------------------- | ------------------------------------------------------------ |
| public static Calendar getInstance()  | 获取一个它的子类GregorianCalendar对象。                      |
| public int get(int field)             | 获取某个字段的值。field参数表示获取哪个字段的值，<br />可以使用Calender中定义的常量来表示：<br />Calendar.YEAR : 年<br />Calendar.MONTH ：月<br />Calendar.DAY_OF_MONTH：月中的日期<br />Calendar.HOUR：小时<br />Calendar.MINUTE：分钟<br />Calendar.SECOND：秒<br />Calendar.DAY_OF_WEEK：星期 |
| public void set(int field,int value)  | 设置某个字段的值                                             |
| public void add(int field,int amount) | 为某个字段增加/减少指定的值                                  |

## 3.3 get方法示例

```java
public class Demo {
    public static void main(String[] args) {
        //1.获取一个GregorianCalendar对象
        Calendar instance = Calendar.getInstance();//获取子类对象

        //2.打印子类对象
        System.out.println(instance);

        //3.获取属性
        int year = instance.get(Calendar.YEAR);
        int month = instance.get(Calendar.MONTH) + 1;//Calendar的月份值是0-11
        int day = instance.get(Calendar.DAY_OF_MONTH);

        int hour = instance.get(Calendar.HOUR);
        int minute = instance.get(Calendar.MINUTE);
        int second = instance.get(Calendar.SECOND);

        int week = instance.get(Calendar.DAY_OF_WEEK);//返回值范围：1--7，分别表示："星期日","星期一","星期二",...,"星期六"

        System.out.println(year + "年" + month + "月" + day + "日" + 
                           	hour + ":" + minute + ":" + second);
        System.out.println(getWeek(week));

    }

    //查表法，查询星期几
    public static String getWeek(int w) {//w = 1 --- 7
        //做一个表(数组)
        String[] weekArray = {"星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"};
        //            索引      [0]      [1]       [2]      [3]       [4]      [5]      [6]
        //查表
        return weekArray[w - 1];
    }
}

```

## 3.4 set方法示例：

```java
public class Demo {
    public static void main(String[] args) {
        //设置属性——set(int field,int value):
		Calendar c1 = Calendar.getInstance();//获取当前日期

		//计算班长出生那天是星期几(假如班长出生日期为：1998年3月18日)
		c1.set(Calendar.YEAR, 1998);
		c1.set(Calendar.MONTH, 3 - 1);//转换为Calendar内部的月份值
		c1.set(Calendar.DAY_OF_MONTH, 18);

		int w = c1.get(Calendar.DAY_OF_WEEK);
		System.out.println("班长出生那天是：" + getWeek(w));

        
    }
    //查表法，查询星期几
    public static String getWeek(int w) {//w = 1 --- 7
        //做一个表(数组)
        String[] weekArray = {"星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"};
        //            索引      [0]      [1]       [2]      [3]       [4]      [5]      [6]
        //查表
        return weekArray[w - 1];
    }
}
```



## 3.5 add方法示例：

```java
public class Demo {
    public static void main(String[] args) {
        //计算200天以后是哪年哪月哪日，星期几？
		Calendar c2 = Calendar.getInstance();//获取当前日期
        c2.add(Calendar.DAY_OF_MONTH, 200);//日期加200

        int y = c2.get(Calendar.YEAR);
        int m = c2.get(Calendar.MONTH) + 1;//转换为实际的月份
        int d = c2.get(Calendar.DAY_OF_MONTH);

        int wk = c2.get(Calendar.DAY_OF_WEEK);
        System.out.println("200天后是：" + y + "年" + m + "月" + d + "日" + getWeek(wk));

    }
    //查表法，查询星期几
    public static String getWeek(int w) {//w = 1 --- 7
        //做一个表(数组)
        String[] weekArray = {"星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"};
        //            索引      [0]      [1]       [2]      [3]       [4]      [5]      [6]
        //查表
        return weekArray[w - 1];
    }
}
```

# 第四章 JDK8时间相关类

| JDK8时间类类名    | 作用                   |
| ----------------- | ---------------------- |
| ZoneId            | 时区                   |
| Instant           | 时间戳                 |
| ZoneDateTime      | 带时区的时间           |
| DateTimeFormatter | 用于时间的格式化和解析 |
| LocalDate         | 年、月、日             |
| LocalTime         | 时、分、秒             |
| LocalDateTime     | 年、月、日、时、分、秒 |
| Duration          | 时间间隔（秒，纳，秒） |
| Period            | 时间间隔（年，月，日） |
| ChronoUnit        | 时间间隔（所有单位）   |

## 4.1  ZoneId 时区

```java
/*
        static Set<string> getAvailableZoneIds() 获取Java中支持的所有时区
        static ZoneId systemDefault() 获取系统默认时区
        static Zoneld of(string zoneld) 获取一个指定时区
        */

//1.获取所有的时区名称
Set<String> zoneIds = ZoneId.getAvailableZoneIds();
System.out.println(zoneIds.size());//600
System.out.println(zoneIds);// Asia/Shanghai

//2.获取当前系统的默认时区
ZoneId zoneId = ZoneId.systemDefault();
System.out.println(zoneId);//Asia/Shanghai

//3.获取指定的时区
ZoneId zoneId1 = ZoneId.of("Asia/Pontianak");
System.out.println(zoneId1);//Asia/Pontianak
```

## 4.2  Instant 时间戳

```java
/*
            static Instant now() 获取当前时间的Instant对象(标准时间)
            static Instant ofXxxx(long epochMilli) 根据(秒/毫秒/纳秒)获取Instant对象
            ZonedDateTime atZone(ZoneIdzone) 指定时区
            boolean isxxx(Instant otherInstant) 判断系列的方法
            Instant minusXxx(long millisToSubtract) 减少时间系列的方法
            Instant plusXxx(long millisToSubtract) 增加时间系列的方法
        */
//1.获取当前时间的Instant对象(标准时间)
Instant now = Instant.now();
System.out.println(now);

//2.根据(秒/毫秒/纳秒)获取Instant对象
Instant instant1 = Instant.ofEpochMilli(0L);
System.out.println(instant1);//1970-01-01T00:00:00z

Instant instant2 = Instant.ofEpochSecond(1L);
System.out.println(instant2);//1970-01-01T00:00:01Z

Instant instant3 = Instant.ofEpochSecond(1L, 1000000000L);
System.out.println(instant3);//1970-01-01T00:00:027

//3. 指定时区
ZonedDateTime time = Instant.now().atZone(ZoneId.of("Asia/Shanghai"));
System.out.println(time);


//4.isXxx 判断
Instant instant4=Instant.ofEpochMilli(0L);
Instant instant5 =Instant.ofEpochMilli(1000L);

//5.用于时间的判断
//isBefore:判断调用者代表的时间是否在参数表示时间的前面
boolean result1=instant4.isBefore(instant5);
System.out.println(result1);//true

//isAfter:判断调用者代表的时间是否在参数表示时间的后面
boolean result2 = instant4.isAfter(instant5);
System.out.println(result2);//false

//6.Instant minusXxx(long millisToSubtract) 减少时间系列的方法
Instant instant6 =Instant.ofEpochMilli(3000L);
System.out.println(instant6);//1970-01-01T00:00:03Z

Instant instant7 =instant6.minusSeconds(1);
System.out.println(instant7);//1970-01-01T00:00:02Z

```



## 4.3 ZoneDateTime  带时区的时间

```java
/*
            static ZonedDateTime now() 获取当前时间的ZonedDateTime对象
            static ZonedDateTime ofXxxx(。。。) 获取指定时间的ZonedDateTime对象
            ZonedDateTime withXxx(时间) 修改时间系列的方法
            ZonedDateTime minusXxx(时间) 减少时间系列的方法
            ZonedDateTime plusXxx(时间) 增加时间系列的方法
         */
//1.获取当前时间对象(带时区)
ZonedDateTime now = ZonedDateTime.now();
System.out.println(now);

//2.获取指定的时间对象(带时区)1/年月日时分秒纳秒方式指定
ZonedDateTime time1 = ZonedDateTime.of(2023, 10, 1,
                                       11, 12, 12, 0, ZoneId.of("Asia/Shanghai"));
System.out.println(time1);

//通过Instant + 时区的方式指定获取时间对象
Instant instant = Instant.ofEpochMilli(0L);
ZoneId zoneId = ZoneId.of("Asia/Shanghai");
ZonedDateTime time2 = ZonedDateTime.ofInstant(instant, zoneId);
System.out.println(time2);


//3.withXxx 修改时间系列的方法
ZonedDateTime time3 = time2.withYear(2000);
System.out.println(time3);

//4. 减少时间
ZonedDateTime time4 = time3.minusYears(1);
System.out.println(time4);

//5.增加时间
ZonedDateTime time5 = time4.plusYears(1);
System.out.println(time5);
```



## 4.4DateTimeFormatter   用于时间的格式化和解析

```java
/*
            static DateTimeFormatter ofPattern(格式) 获取格式对象
            String format(时间对象) 按照指定方式格式化
        */
//获取时间对象
ZonedDateTime time = Instant.now().atZone(ZoneId.of("Asia/Shanghai"));

// 解析/格式化器
DateTimeFormatter dtf1=DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm;ss EE a");
// 格式化
System.out.println(dtf1.format(time));
```



## 4.5LocalDate  年、月、日

```java
//1.获取当前时间的日历对象(包含 年月日)
LocalDate nowDate = LocalDate.now();
//System.out.println("今天的日期:" + nowDate);
//2.获取指定的时间的日历对象
LocalDate ldDate = LocalDate.of(2023, 1, 1);
System.out.println("指定日期:" + ldDate);

System.out.println("=============================");

//3.get系列方法获取日历中的每一个属性值//获取年
int year = ldDate.getYear();
System.out.println("year: " + year);
//获取月//方式一:
Month m = ldDate.getMonth();
System.out.println(m);
System.out.println(m.getValue());

//方式二:
int month = ldDate.getMonthValue();
System.out.println("month: " + month);


//获取日
int day = ldDate.getDayOfMonth();
System.out.println("day:" + day);

//获取一年的第几天
int dayofYear = ldDate.getDayOfYear();
System.out.println("dayOfYear:" + dayofYear);

//获取星期
DayOfWeek dayOfWeek = ldDate.getDayOfWeek();
System.out.println(dayOfWeek);
System.out.println(dayOfWeek.getValue());

//is开头的方法表示判断
System.out.println(ldDate.isBefore(ldDate));
System.out.println(ldDate.isAfter(ldDate));

//with开头的方法表示修改，只能修改年月日
LocalDate withLocalDate = ldDate.withYear(2000);
System.out.println(withLocalDate);

//minus开头的方法表示减少，只能减少年月日
LocalDate minusLocalDate = ldDate.minusYears(1);
System.out.println(minusLocalDate);


//plus开头的方法表示增加，只能增加年月日
LocalDate plusLocalDate = ldDate.plusDays(1);
System.out.println(plusLocalDate);

//-------------
// 判断今天是否是你的生日
LocalDate birDate = LocalDate.of(2000, 1, 1);
LocalDate nowDate1 = LocalDate.now();

MonthDay birMd = MonthDay.of(birDate.getMonthValue(), birDate.getDayOfMonth());
MonthDay nowMd = MonthDay.from(nowDate1);

System.out.println("今天是你的生日吗? " + birMd.equals(nowMd));//今天是你的生日吗?
```



## 4.6 LocalTime  时、分、秒

```java
// 获取本地时间的日历对象。(包含 时分秒)
LocalTime nowTime = LocalTime.now();
System.out.println("今天的时间:" + nowTime);

int hour = nowTime.getHour();//时
System.out.println("hour: " + hour);

int minute = nowTime.getMinute();//分
System.out.println("minute: " + minute);

int second = nowTime.getSecond();//秒
System.out.println("second:" + second);

int nano = nowTime.getNano();//纳秒
System.out.println("nano:" + nano);
System.out.println("------------------------------------");
System.out.println(LocalTime.of(8, 20));//时分
System.out.println(LocalTime.of(8, 20, 30));//时分秒
System.out.println(LocalTime.of(8, 20, 30, 150));//时分秒纳秒
LocalTime mTime = LocalTime.of(8, 20, 30, 150);

//is系列的方法
System.out.println(nowTime.isBefore(mTime));
System.out.println(nowTime.isAfter(mTime));

//with系列的方法，只能修改时、分、秒
System.out.println(nowTime.withHour(10));

//plus系列的方法，只能修改时、分、秒
System.out.println(nowTime.plusHours(10));
```



## 4.7 LocalDateTime  年、月、日、时、分、秒

```java
// 当前时间的的日历对象(包含年月日时分秒)
LocalDateTime nowDateTime = LocalDateTime.now();

System.out.println("今天是:" + nowDateTime);//今天是：
System.out.println(nowDateTime.getYear());//年
System.out.println(nowDateTime.getMonthValue());//月
System.out.println(nowDateTime.getDayOfMonth());//日
System.out.println(nowDateTime.getHour());//时
System.out.println(nowDateTime.getMinute());//分
System.out.println(nowDateTime.getSecond());//秒
System.out.println(nowDateTime.getNano());//纳秒
// 日:当年的第几天
System.out.println("dayofYear:" + nowDateTime.getDayOfYear());
//星期
System.out.println(nowDateTime.getDayOfWeek());
System.out.println(nowDateTime.getDayOfWeek().getValue());
//月份
System.out.println(nowDateTime.getMonth());
System.out.println(nowDateTime.getMonth().getValue());

LocalDate ld = nowDateTime.toLocalDate();
System.out.println(ld);

LocalTime lt = nowDateTime.toLocalTime();
System.out.println(lt.getHour());
System.out.println(lt.getMinute());
System.out.println(lt.getSecond());
```



## 4.8 Duration  时间间隔（秒，纳，秒）

```java
// 本地日期时间对象。
LocalDateTime today = LocalDateTime.now();
System.out.println(today);

// 出生的日期时间对象
LocalDateTime birthDate = LocalDateTime.of(2000, 1, 1, 0, 0, 0);
System.out.println(birthDate);

Duration duration = Duration.between(birthDate, today);//第二个参数减第一个参数
System.out.println("相差的时间间隔对象:" + duration);

System.out.println("============================================");
System.out.println(duration.toDays());//两个时间差的天数
System.out.println(duration.toHours());//两个时间差的小时数
System.out.println(duration.toMinutes());//两个时间差的分钟数
System.out.println(duration.toMillis());//两个时间差的毫秒数
System.out.println(duration.toNanos());//两个时间差的纳秒数
```



## 4.9 Period  时间间隔（年，月，日）

```java
// 当前本地 年月日
LocalDate today = LocalDate.now();
System.out.println(today);

// 生日的 年月日
LocalDate birthDate = LocalDate.of(2000, 1, 1);
System.out.println(birthDate);

Period period = Period.between(birthDate, today);//第二个参数减第一个参数

System.out.println("相差的时间间隔对象:" + period);
System.out.println(period.getYears());
System.out.println(period.getMonths());
System.out.println(period.getDays());

System.out.println(period.toTotalMonths());
```



## 4.10 ChronoUnit  时间间隔（所有单位）

```java
// 当前时间
LocalDateTime today = LocalDateTime.now();
System.out.println(today);
// 生日时间
LocalDateTime birthDate = LocalDateTime.of(2000, 1, 1,0, 0, 0);
System.out.println(birthDate);

System.out.println("相差的年数:" + ChronoUnit.YEARS.between(birthDate, today));
System.out.println("相差的月数:" + ChronoUnit.MONTHS.between(birthDate, today));
System.out.println("相差的周数:" + ChronoUnit.WEEKS.between(birthDate, today));
System.out.println("相差的天数:" + ChronoUnit.DAYS.between(birthDate, today));
System.out.println("相差的时数:" + ChronoUnit.HOURS.between(birthDate, today));
System.out.println("相差的分数:" + ChronoUnit.MINUTES.between(birthDate, today));
System.out.println("相差的秒数:" + ChronoUnit.SECONDS.between(birthDate, today));
System.out.println("相差的毫秒数:" + ChronoUnit.MILLIS.between(birthDate, today));
System.out.println("相差的微秒数:" + ChronoUnit.MICROS.between(birthDate, today));
System.out.println("相差的纳秒数:" + ChronoUnit.NANOS.between(birthDate, today));
System.out.println("相差的半天数:" + ChronoUnit.HALF_DAYS.between(birthDate, today));
System.out.println("相差的十年数:" + ChronoUnit.DECADES.between(birthDate, today));
System.out.println("相差的世纪(百年)数:" + ChronoUnit.CENTURIES.between(birthDate, today));
System.out.println("相差的千年数:" + ChronoUnit.MILLENNIA.between(birthDate, today));
System.out.println("相差的纪元数:" + ChronoUnit.ERAS.between(birthDate, today));
```

# 第五章  包装类

## 5.1 概述

Java提供了两个类型系统，基本类型与引用类型，使用基本类型在于效率，然而很多情况，会创建对象使用，因为对象可以做更多的功能，如果想要我们的基本类型像对象一样操作，就可以使用基本类型对应的包装类，如下：

| 基本类型 | 对应的包装类（位于java.lang包中） |
| -------- | --------------------------------- |
| byte     | Byte                              |
| short    | Short                             |
| int      | **Integer**                       |
| long     | Long                              |
| float    | Float                             |
| double   | Double                            |
| char     | **Character**                     |
| boolean  | Boolean                           |

## 5.2 Integer类

- Integer类概述

  包装一个对象中的原始类型 int 的值

- Integer类构造方法及静态方法

| 方法名                                  | 说明                                   |
| --------------------------------------- | -------------------------------------- |
| public Integer(int   value)             | 根据 int 值创建 Integer 对象(过时)     |
| public Integer(String s)                | 根据 String 值创建 Integer 对象(过时)  |
| public static Integer valueOf(int i)    | 返回表示指定的 int 值的 Integer   实例 |
| public static Integer valueOf(String s) | 返回保存指定String值的 Integer 对象    |
| static string tobinarystring(int i)     | 得到二进制                             |
| static string tooctalstring(int i)      | 得到八进制                             |
| static string toHexstring(int i)        | 得到十六进制                           |
| static int parseInt(string s)           | 将字符串类型的整数转成int类型的整数    |

- 示例代码

```java
//public Integer(int value)：根据 int 值创建 Integer 对象(过时)
Integer i1 = new Integer(100);
System.out.println(i1);

//public Integer(String s)：根据 String 值创建 Integer 对象(过时)
Integer i2 = new Integer("100");
//Integer i2 = new Integer("abc"); //NumberFormatException
System.out.println(i2);
System.out.println("--------");

//public static Integer valueOf(int i)：返回表示指定的 int 值的 Integer 实例
Integer i3 = Integer.valueOf(100);
System.out.println(i3);

//public static Integer valueOf(String s)：返回保存指定String值的Integer对象 
Integer i4 = Integer.valueOf("100");
System.out.println(i4);
```

```java
/*
            public static string tobinarystring(int i) 得到二进制
            public static string tooctalstring(int i) 得到八进制
            public static string toHexstring(int i) 得到十六进制
            public static int parseInt(string s) 将字符串类型的整数转成int类型的整数
 */

//1.把整数转成二进制，十六进制
String str1 = Integer.toBinaryString(100);
System.out.println(str1);//1100100

//2.把整数转成八进制
String str2 = Integer.toOctalString(100);
System.out.println(str2);//144

//3.把整数转成十六进制
String str3 = Integer.toHexString(100);
System.out.println(str3);//64

//4.将字符串类型的整数转成int类型的整数
//强类型语言:每种数据在java中都有各自的数据类型
//在计算的时候，如果不是同一种数据类型，是无法直接计算的。
int i = Integer.parseInt("123");
System.out.println(i);
System.out.println(i + 1);//124
//细节1:
//在类型转换的时候，括号中的参数只能是数字不能是其他，否则代码会报错
//细节2:
//8种包装类当中，除了Character都有对应的parseXxx的方法，进行类型转换
String str = "true";
boolean b = Boolean.parseBoolean(str);
System.out.println(b);
```

## 5.3 装箱与拆箱

基本类型与对应的包装类对象之间，来回转换的过程称为”装箱“与”拆箱“：

- **装箱**：从基本类型转换为对应的包装类对象。
- **拆箱**：从包装类对象转换为对应的基本类型。

用Integer与 int为例：（看懂代码即可）

基本数值---->包装对象

```java
Integer i = new Integer(4);//使用构造函数函数
Integer iii = Integer.valueOf(4);//使用包装类中的valueOf方法
```

包装对象---->基本数值

```java
int num = i.intValue();
```

## 5.4 自动装箱与自动拆箱

由于我们经常要做基本类型与包装类之间的转换，从Java 5（JDK 1.5）开始，基本类型与包装类的装箱、拆箱动作可以自动完成。例如：

```java
Integer i = 4;//自动装箱。相当于Integer i = Integer.valueOf(4);
i = i + 5;//等号右边：将i对象转成基本数值(自动拆箱) i.intValue() + 5;
//加法运算完成后，再次装箱，把基本数值转成对象。
```

## 5.5 基本类型与字符串之间的转换

### 基本类型转换为String

- 转换方式
- 方式一：直接在数字后加一个空字符串
- 方式二：通过String类静态方法valueOf()
- 示例代码

```java
public class IntegerDemo {
    public static void main(String[] args) {
        //int --- String
        int number = 100;
        //方式1
        String s1 = number + "";
        System.out.println(s1);
        //方式2
        //public static String valueOf(int i)
        String s2 = String.valueOf(number);
        System.out.println(s2);
        System.out.println("--------");
    }
}
```

### String转换成基本类型 

除了Character类之外，其他所有包装类都具有parseXxx静态方法可以将字符串参数转换为对应的基本类型：

- `public static byte parseByte(String s)`：将字符串参数转换为对应的byte基本类型。
- `public static short parseShort(String s)`：将字符串参数转换为对应的short基本类型。
- **`public static int parseInt(String s)`：将字符串参数转换为对应的int基本类型。**
- **`public static long parseLong(String s)`：将字符串参数转换为对应的long基本类型。**
- `public static float parseFloat(String s)`：将字符串参数转换为对应的float基本类型。
- `public static double parseDouble(String s)`：将字符串参数转换为对应的double基本类型。
- `public static boolean parseBoolean(String s)`：将字符串参数转换为对应的boolean基本类型。

代码使用（仅以Integer类的静态方法parseXxx为例）如：

- 转换方式
  - 方式一：先将字符串数字转成Integer，再调用valueOf()方法
  - 方式二：通过Integer静态方法parseInt()进行转换
- 示例代码

```java
public class IntegerDemo {
    public static void main(String[] args) {
        //String --- int
        String s = "100";
        //方式1：String --- Integer --- int
        Integer i = Integer.valueOf(s);
        //public int intValue()
        int x = i.intValue();
        System.out.println(x);
        //方式2
        //public static int parseInt(String s)
        int y = Integer.parseInt(s);
        System.out.println(y);
    }
}
```

> 注意:如果字符串参数的内容无法正确转换为对应的基本类型，则会抛出`java.lang.NumberFormatException`异常。

## 5.6 底层原理

建议：获取Integer对象的时候不要自己new，而是采取直接赋值或者静态方法valueOf的方式

因为在实际开发中，-128~127之间的数据，用的比较多。如果每次使用都是new对象，那么太浪费内存了。

所以，提前把这个范围之内的每一个数据都创建好对象，如果要用到了不会创建新的，而是返回已经创建好的对象。

```java
//1.利用构造方法获取Integer的对象(JDK5以前的方式)
/*Integer i1 = new Integer(1);
        Integer i2 = new Integer("1");
        System.out.println(i1);
        System.out.println(i2);*/

//2.利用静态方法获取Integer的对象(JDK5以前的方式)
Integer i3 = Integer.valueOf(123);
Integer i4 = Integer.valueOf("123");
Integer i5 = Integer.valueOf("123", 8);

System.out.println(i3);
System.out.println(i4);
System.out.println(i5);

//3.这两种方式获取对象的区别(掌握)
//底层原理：
//因为在实际开发中，-128~127之间的数据，用的比较多。
//如果每次使用都是new对象，那么太浪费内存了
//所以，提前把这个范围之内的每一个数据都创建好对象
//如果要用到了不会创建新的，而是返回已经创建好的对象。
Integer i6 = Integer.valueOf(127);
Integer i7 = Integer.valueOf(127);
System.out.println(i6 == i7);//true

Integer i8 = Integer.valueOf(128);
Integer i9 = Integer.valueOf(128);
System.out.println(i8 == i9);//false

//因为看到了new关键字，在Java中，每一次new都是创建了一个新的对象
//所以下面的两个对象都是new出来，地址值不一样。
/*Integer i10 = new Integer(127);
        Integer i11 = new Integer(127);
        System.out.println(i10 == i11);

        Integer i12 = new Integer(128);
        Integer i13 = new Integer(128);
        System.out.println(i12 == i13);*/
```

# 第六章：算法小题

## 练习一：

需求：

​	键盘录入一些1~10日之间的整数，并添加到集合中。直到集合中所有数据和超过200为止。

代码示例：

```java
public class Test1 {
    public static void main(String[] args) {
        /*
            键盘录入一些1~10日之间的整数，并添加到集合中。直到集合中所有数据和超过200为止。
        */
        //1.创建一个集合用来添加整数
        ArrayList<Integer> list = new ArrayList<>();
        //2.键盘录入数据添加到集合中
        Scanner sc = new Scanner(System.in);
        while (true) {
            System.out.println("请输入一个整数");
            String numStr = sc.nextLine();
            int num = Integer.parseInt(numStr);//先把异常数据先进行过滤
            if (num < 1 || num > 100){
                System.out.println("当前数字不在1~100的范围当中，请重新输入");
                continue;
            }
            //添加到集合中//细节:
            //num:基本数据类型
            //集合里面的数据是Integer
            //在添加数据的时候触发了自动装箱
            list.add(num);
            //统计集合中所有的数据和
            int sum = getSum(list);
            //对sum进行判断
            if(sum > 200){
            System.out.println("集合中所有的数据和已经满足要求");
            break;
        }
    }

}


    private static int getSum(ArrayList<Integer> list) {
        int sum = 0;
        for (int i = 0; i < list.size(); i++) {
            //i :索引
            //list.get(i);
            int num = list.get(i);
            sum = sum + num;//+=
        }
        return sum;
    }
}

```

## 练习二：

需求：

​	自己实现parseInt方法的效果，将字符串形式的数据转成整数。要求:字符串中只能是数字不能有其他字符最少一位，最多10位日不能开头

代码示例：

```java
public class Test2 {
    public static void main(String[] args) {
        /*
            自己实现parseInt方法的效果，将字符串形式的数据转成整数。要求:
            字符串中只能是数字不能有其他字符最少一位，最多10位日不能开头
        */

        //1.定义一个字符串
        String str = "123";
        //2.校验字符串
        //习惯:会先把异常数据进行过滤，剩下来就是正常的数据。
        if (!str.matches("[1-9]\\d{0,9}")) {
            //错误的数据
            System.out.println("数据格式有误");
        } else {
            //正确的数据
            System.out.println("数据格式正确");
            //3.定义一个变量表示最终的结果
            int number = 0;
            //4.遍历字符串得到里面的每一个字符
            for (int i = 0; i < str.length(); i++) {
                int c = str.charAt(i) - '0';//把每一位数字放到number当中
                number = number * 10 + c;
            }
            System.out.println(number);
            System.out.println(number + 1);
        }
    }
}
```

## 练习三：

需求：

​	定义一个方法自己实现toBinaryString方法的效果，将一个十进制整数转成字符串表示的二进制

代码示例：

```java
package com.itheima.a04test;

public class Test3 {
    public static void main(String[] args) {
        /*

            定义一个方法自己实现toBinaryString方法的效果，将一个十进制整数转成字符串表示的二进制

         */
    }


    public static String tobinarystring(int number) {//6
        //核心逻辑:
        //不断的去除以2，得到余数，一直到商为日就结束。
        //还需要把余数倒着拼接起来

        //定义一个StringBuilder用来拼接余数
        StringBuilder sb = new StringBuilder();
        //利用循环不断的除以2获取余数
        while (true) {
            if (number == 0) {
                break;
            }
            //获取余数 %
            int remaindar = number % 2;//倒着拼接
            sb.insert(0, remaindar);
            //除以2 /
            number = number / 2;
        }
        return sb.toString();
    }
}

```

## 练习四：

需求：

​	请使用代码实现计算你活了多少天，用JDK7和JDK8两种方式完成

代码示例：

```java
public class Test4 {
    public static void main(String[] args) throws ParseException {
        //请使用代码实现计算你活了多少天，用JDK7和JDK8两种方式完成
        //JDK7
        //规则:只要对时间进行计算或者判断，都需要先获取当前时间的毫秒值
        //1.计算出生年月日的毫秒值
        String birthday = "2000年1月1日";
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日");
        Date date = sdf.parse(birthday);
        long birthdayTime = date.getTime();
        //2.获取当前时间的毫秒值
        long todayTime = System.currentTimeMillis();
        //3.计算间隔多少天
        long time = todayTime - birthdayTime;
        System.out.println(time / 1000 / 60 / 60 / 24);


        //JDK8
        LocalDate ld1 = LocalDate.of(2000, 1, 1);
        LocalDate ld2 = LocalDate.now();
        long days = ChronoUnit.DAYS.between(ld1, ld2);
        System.out.println(days);
    }
}
```

## 练习五：

需求：

​	判断任意的一个年份是闰年还是平年要求:用JDK7和JDK8两种方式判断提示:二月有29天是闰年一年有366天是闰年

代码示例：

```java
public class Test5 {
    public static void main(String[] args) {
        /*
            判断任意的一个年份是闰年还是平年要求:用JDK7和JDK8两种方式判断提示:
            二月有29天是闰年一年有366天是闰年
        */

        //jdk7
        //我们可以把时间设置为2000年3月1日
        Calendar c = Calendar.getInstance();
        c.set(2000, 2, 1);
        //月份的范围:0~11
        //再把日历往前减一天
        c.add(Calendar.DAY_OF_MONTH, -1);
        //看当前的时间是28号还是29号?
        int day = c.get(Calendar.DAY_OF_MONTH);
        System.out.println(day);


        //jdk8
        //月份的范围:1~12
        //设定时间为2000年的3月1日
        LocalDate ld = LocalDate.of(2001, 3, 1);
        //把时间往前减一天
        LocalDate ld2 = ld.minusDays(1);
        //获取这一天是一个月中的几号
        int day2 = ld2.getDayOfMonth();
        System.out.println(day2);

        //true:闰年
        //false:平年
        System.out.println(ld.isLeapYear());
    }
}
```



# 常见的七种查找算法：

​	数据结构是数据存储的方式，算法是数据计算的方式。所以在开发中，算法和数据结构息息相关。今天的讲义中会涉及部分数据结构的专业名词，如果各位铁粉有疑惑，可以先看一下哥们后面录制的数据结构，再回头看算法。

## 1. 基本查找 

​	也叫做顺序查找

​        说明：顺序查找适合于存储结构为数组或者链表。

**基本思想**：顺序查找也称为线形查找，属于无序查找算法。从数据结构线的一端开始，顺序扫描，依次将遍历到的结点与要查找的值相比较，若相等则表示查找成功；若遍历结束仍没有找到相同的，表示查找失败。

示例代码：

```java
public class A01_BasicSearchDemo1 {
    public static void main(String[] args) {
        //基本查找/顺序查找
        //核心：
        //从0索引开始挨个往后查找

        //需求：定义一个方法利用基本查找，查询某个元素是否存在
        //数据如下：{131, 127, 147, 81, 103, 23, 7, 79}


        int[] arr = {131, 127, 147, 81, 103, 23, 7, 79};
        int number = 82;
        System.out.println(basicSearch(arr, number));

    }

    //参数：
    //一：数组
    //二：要查找的元素

    //返回值：
    //元素是否存在
    public static boolean basicSearch(int[] arr, int number){
        //利用基本查找来查找number在数组中是否存在
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] == number){
                return true;
            }
        }
        return false;
    }
}
```

## 2. 二分查找

​	也叫做折半查找

说明：元素必须是有序的，从小到大，或者从大到小都是可以的。

如果是无序的，也可以先进行排序。但是排序之后，会改变原有数据的顺序，查找出来元素位置跟原来的元素可能是不一样的，所以排序之后再查找只能判断当前数据是否在容器当中，返回的索引无实际的意义。

　　**基本思想**：也称为是折半查找，属于有序查找算法。用给定值先与中间结点比较。比较完之后有三种情况：

* 相等

  说明找到了

* 要查找的数据比中间节点小

  说明要查找的数字在中间节点左边

* 要查找的数据比中间节点大

  说明要查找的数字在中间节点右边

代码示例：

```java
package com.itheima.search;

public class A02_BinarySearchDemo1 {
    public static void main(String[] args) {
        //二分查找/折半查找
        //核心：
        //每次排除一半的查找范围

        //需求：定义一个方法利用二分查找，查询某个元素在数组中的索引
        //数据如下：{7, 23, 79, 81, 103, 127, 131, 147}

        int[] arr = {7, 23, 79, 81, 103, 127, 131, 147};
        System.out.println(binarySearch(arr, 150));
    }

    public static int binarySearch(int[] arr, int number){
        //1.定义两个变量记录要查找的范围
        int min = 0;
        int max = arr.length - 1;

        //2.利用循环不断的去找要查找的数据
        while(true){
            if(min > max){
                return -1;
            }
            //3.找到min和max的中间位置
            int mid = (min + max) / 2;
            //4.拿着mid指向的元素跟要查找的元素进行比较
            if(arr[mid] > number){
                //4.1 number在mid的左边
                //min不变，max = mid - 1；
                max = mid - 1;
            }else if(arr[mid] < number){
                //4.2 number在mid的右边
                //max不变，min = mid + 1;
                min = mid + 1;
            }else{
                //4.3 number跟mid指向的元素一样
                //找到了
                return mid;
            }

        }
    }
}
```

## 3. 插值查找

在介绍插值查找之前，先考虑一个问题：

​	为什么二分查找算法一定要是折半，而不是折四分之一或者折更多呢？

其实就是因为方便，简单，但是如果我能在二分查找的基础上，让中间的mid点，尽可能靠近想要查找的元素，那不就能提高查找的效率了吗？

二分查找中查找点计算如下：

　　mid=(low+high)/2, 即mid=low+1/2*(high-low);

我们可以将查找的点改进为如下：

　　mid=low+(key-a[low])/(a[high]-a[low])*(high-low)，

这样，让mid值的变化更靠近关键字key，这样也就间接地减少了比较次数。

　　基本思想：基于二分查找算法，将查找点的选择改进为自适应选择，可以提高查找效率。当然，差值查找也属于有序查找。

**细节：**对于表长较大，而关键字分布又比较均匀的查找表来说，插值查找算法的平均性能比折半查找要好的多。反之，数组中如果分布非常不均匀，那么插值查找未必是很合适的选择。

代码跟二分查找类似，只要修改一下mid的计算方式即可。



## 4. 斐波那契查找

在介绍斐波那契查找算法之前，我们先介绍一下很它紧密相连并且大家都熟知的一个概念——黄金分割。

　　黄金比例又称黄金分割，是指事物各部分间一定的数学比例关系，即将整体一分为二，较大部分与较小部分之比等于整体与较大部分之比，其比值约为1:0.618或1.618:1。

　　0.618被公认为最具有审美意义的比例数字，这个数值的作用不仅仅体现在诸如绘画、雕塑、音乐、建筑等艺术领域，而且在管理、工程设计等方面也有着不可忽视的作用。因此被称为黄金分割。

　　在数学中有一个非常有名的数学规律：斐波那契数列：1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89…….

（从第三个数开始，后边每一个数都是前两个数的和）。

然后我们会发现，随着斐波那契数列的递增，前后两个数的比值会越来越接近0.618，利用这个特性，我们就可以将黄金比例运用到查找技术中。

![img](https://img-blog.csdn.net/20150323100632467?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2hlbmJvMjAzMA==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center) 

基本思想：也是二分查找的一种提升算法，通过运用黄金比例的概念在数列中选择查找点进行查找，提高查找效率。同样地，斐波那契查找也属于一种有序查找算法。

斐波那契查找也是在二分查找的基础上进行了优化，优化中间点mid的计算方式即可

代码示例：

```java
public class FeiBoSearchDemo {
    public static int maxSize = 20;

    public static void main(String[] args) {
        int[] arr = {1, 8, 10, 89, 1000, 1234};
        System.out.println(search(arr, 1234));
    }

    public static int[] getFeiBo() {
        int[] arr = new int[maxSize];
        arr[0] = 1;
        arr[1] = 1;
        for (int i = 2; i < maxSize; i++) {
            arr[i] = arr[i - 1] + arr[i - 2];
        }
        return arr;
    }

    public static int search(int[] arr, int key) {
        int low = 0;
        int high = arr.length - 1;
        //表示斐波那契数分割数的下标值
        int index = 0;
        int mid = 0;
        //调用斐波那契数列
        int[] f = getFeiBo();
        //获取斐波那契分割数值的下标
        while (high > (f[index] - 1)) {
            index++;
        }
        //因为f[k]值可能大于a的长度，因此需要使用Arrays工具类，构造一个新法数组，并指向temp[],不足的部分会使用0补齐
        int[] temp = Arrays.copyOf(arr, f[index]);
        //实际需要使用arr数组的最后一个数来填充不足的部分
        for (int i = high + 1; i < temp.length; i++) {
            temp[i] = arr[high];
        }
        //使用while循环处理，找到key值
        while (low <= high) {
            mid = low + f[index - 1] - 1;
            if (key < temp[mid]) {//向数组的前面部分进行查找
                high = mid - 1;
                /*
                  对k--进行理解
                  1.全部元素=前面的元素+后面的元素
                  2.f[k]=k[k-1]+f[k-2]
                  因为前面有k-1个元素没所以可以继续分为f[k-1]=f[k-2]+f[k-3]
                  即在f[k-1]的前面继续查找k--
                  即下次循环,mid=f[k-1-1]-1
                 */
                index--;
            } else if (key > temp[mid]) {//向数组的后面的部分进行查找
                low = mid + 1;
                index -= 2;
            } else {//找到了
                //需要确定返回的是哪个下标
                if (mid <= high) {
                    return mid;
                } else {
                    return high;
                }
            }
        }
        return -1;
    }
}

```

## 5. 分块查找 

当数据表中的数据元素很多时，可以采用分块查找。

汲取了顺序查找和折半查找各自的优点，既有动态结构，又适于快速查找

分块查找适用于数据较多，但是数据不会发生变化的情况，如果需要一边添加一边查找，建议使用哈希查找

分块查找的过程：

1. 需要把数据分成N多小块，块与块之间不能有数据重复的交集。
2. 给每一块创建对象单独存储到数组当中
3. 查找数据的时候，先在数组查，当前数据属于哪一块
4. 再到这一块中顺序查找

代码示例：

```java
package com.itheima.search;

public class A03_BlockSearchDemo {
    public static void main(String[] args) {
        /*
            分块查找
            核心思想：
                块内无序，块间有序
            实现步骤：
                1.创建数组blockArr存放每一个块对象的信息
                2.先查找blockArr确定要查找的数据属于哪一块
                3.再单独遍历这一块数据即可
        */
        int[] arr = {16, 5, 9, 12,21, 18,
                     32, 23, 37, 26, 45, 34,
                     50, 48, 61, 52, 73, 66};

        //创建三个块的对象
        Block b1 = new Block(21,0,5);
        Block b2 = new Block(45,6,11);
        Block b3 = new Block(73,12,17);

        //定义数组用来管理三个块的对象（索引表）
        Block[] blockArr = {b1,b2,b3};

        //定义一个变量用来记录要查找的元素
        int number = 37;

        //调用方法，传递索引表，数组，要查找的元素
        int index = getIndex(blockArr,arr,number);

        //打印一下
        System.out.println(index);



    }

    //利用分块查找的原理，查询number的索引
    private static int getIndex(Block[] blockArr, int[] arr, int number) {
        //1.确定number是在那一块当中
        int indexBlock = findIndexBlock(blockArr, number);

        if(indexBlock == -1){
            //表示number不在数组当中
            return -1;
        }

        //2.获取这一块的起始索引和结束索引   --- 30
        // Block b1 = new Block(21,0,5);   ----  0
        // Block b2 = new Block(45,6,11);  ----  1
        // Block b3 = new Block(73,12,17); ----  2
        int startIndex = blockArr[indexBlock].getStartIndex();
        int endIndex = blockArr[indexBlock].getEndIndex();

        //3.遍历
        for (int i = startIndex; i <= endIndex; i++) {
            if(arr[i] == number){
                return i;
            }
        }
        return -1;
    }


    //定义一个方法，用来确定number在哪一块当中
    public static int findIndexBlock(Block[] blockArr,int number){ //100


        //从0索引开始遍历blockArr，如果number小于max，那么就表示number是在这一块当中的
        for (int i = 0; i < blockArr.length; i++) {
            if(number <= blockArr[i].getMax()){
                return i;
            }
        }
        return -1;
    }



}

class Block{
    private int max;//最大值
    private int startIndex;//起始索引
    private int endIndex;//结束索引


    public Block() {
    }

    public Block(int max, int startIndex, int endIndex) {
        this.max = max;
        this.startIndex = startIndex;
        this.endIndex = endIndex;
    }

    /**
     * 获取
     * @return max
     */
    public int getMax() {
        return max;
    }

    /**
     * 设置
     * @param max
     */
    public void setMax(int max) {
        this.max = max;
    }

    /**
     * 获取
     * @return startIndex
     */
    public int getStartIndex() {
        return startIndex;
    }

    /**
     * 设置
     * @param startIndex
     */
    public void setStartIndex(int startIndex) {
        this.startIndex = startIndex;
    }

    /**
     * 获取
     * @return endIndex
     */
    public int getEndIndex() {
        return endIndex;
    }

    /**
     * 设置
     * @param endIndex
     */
    public void setEndIndex(int endIndex) {
        this.endIndex = endIndex;
    }

    public String toString() {
        return "Block{max = " + max + ", startIndex = " + startIndex + ", endIndex = " + endIndex + "}";
    }
}
```

## 6. 哈希查找

哈希查找是分块查找的进阶版，适用于数据一边添加一边查找的情况。

一般是数组 + 链表的结合体或者是数组+链表 + 红黑树的结合体

在课程中，为了让大家方便理解，所以规定：

- 数组的0索引处存储1~100
- 数组的1索引处存储101~200
- 数组的2索引处存储201~300
- 以此类推

但是实际上，我们一般不会采取这种方式，因为这种方式容易导致一块区域添加的元素过多，导致效率偏低。

更多的是先计算出当前数据的哈希值，用哈希值跟数组的长度进行计算，计算出应存入的位置，再挂在数组的后面形成链表，如果挂的元素太多而且数组长度过长，我们也会把链表转化为红黑树，进一步提高效率。

具体的过程，大家可以参见B站阿玮讲解课程：从入门到起飞。在集合章节详细讲解了哈希表的数据结构。全程采取动画形式讲解，让大家一目了然。

在此不多做阐述。

 ![Snipaste_2022-09-05_21-36-50](F:/JavaSE%E6%9C%80%E6%96%B0%E7%89%88/day21-API%EF%BC%88%E7%AE%97%E6%B3%95%EF%BC%8Clambda%EF%BC%8C%E7%BB%83%E4%B9%A0%EF%BC%89/%E7%AC%94%E8%AE%B0/img/Snipaste_2022-09-05_21-36-50.png)

## 7. 树表查找 

本知识点涉及到数据结构：树。

建议先看一下后面阿玮讲解的数据结构，再回头理解。

基本思想：二叉查找树是先对待查找的数据进行生成树，确保树的左分支的值小于右分支的值，然后在就行和每个节点的父节点比较大小，查找最适合的范围。 这个算法的查找效率很高，但是如果使用这种查找方法要首先创建树。 

　　二叉查找树（BinarySearch Tree，也叫二叉搜索树，或称二叉排序树Binary Sort Tree），具有下列性质的二叉树：

　　1）若任意节点左子树上所有的数据，均小于本身；

　　2）若任意节点右子树上所有的数据，均大于本身；

　　二叉查找树性质：对二叉查找树进行中序遍历，即可得到有序的数列。

​        不同形态的二叉查找树如下图所示：

 ![20180226113852869](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day21-API（算法，lambda，练习）\笔记\img\20180226113852869.png) 



　　基于二叉查找树进行优化，进而可以得到其他的树表查找算法，如平衡树、红黑树等高效算法。

具体细节大家可以参见B站阿玮讲解课程：从入门到起飞。在集合章节详细讲解了树数据结构。全程采取动画形式讲解，让大家一目了然。

在此不多做阐述。

​	不管是二叉查找树，还是平衡二叉树，还是红黑树，查找的性能都比较高







# 十大排序算法：

## 1. 冒泡排序

冒泡排序（Bubble Sort）也是一种简单直观的排序算法。

它重复的遍历过要排序的数列，一次比较相邻的两个元素，如果他们的顺序错误就把他们交换过来。

这个算法的名字由来是因为越大的元素会经由交换慢慢"浮"到最后面。

当然，大家可以按照从大到小的方式进行排列。

### 1.1 算法步骤

1. 相邻的元素两两比较，大的放右边，小的放左边
2. 第一轮比较完毕之后，最大值就已经确定，第二轮可以少循环一次，后面以此类推
3. 如果数组中有n个数据，总共我们只要执行n-1轮的代码就可以

### 1.2 动图演示

![冒泡](F:\JavaSE最新版\day21-API（算法，lambda，练习）\笔记\img\冒泡.gif)

### 1.3 代码示例

```java
public class A01_BubbleDemo {
    public static void main(String[] args) {
        /*
            冒泡排序：
            核心思想：
            1，相邻的元素两两比较，大的放右边，小的放左边。
            2，第一轮比较完毕之后，最大值就已经确定，第二轮可以少循环一次，后面以此类推。
            3，如果数组中有n个数据，总共我们只要执行n-1轮的代码就可以。
        */


        //1.定义数组
        int[] arr = {2, 4, 5, 3, 1};

        //2.利用冒泡排序将数组中的数据变成 1 2 3 4 5

        //外循环：表示我要执行多少轮。 如果有n个数据，那么执行n - 1 轮
        for (int i = 0; i < arr.length - 1; i++) {
            //内循环：每一轮中我如何比较数据并找到当前的最大值
            //-1：为了防止索引越界
            //-i：提高效率，每一轮执行的次数应该比上一轮少一次。
            for (int j = 0; j < arr.length - 1 - i; j++) {
                //i 依次表示数组中的每一个索引：0 1 2 3 4
                if(arr[j] > arr[j + 1]){
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        printArr(arr);




    }

    private static void printArr(int[] arr) {
        //3.遍历数组
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}
```



## 2. 选择排序

### 2.1 算法步骤

1. 从0索引开始，跟后面的元素一一比较
2. 小的放前面，大的放后面
3. 第一次循环结束后，最小的数据已经确定
4. 第二次循环从1索引开始以此类推
5. 第三轮循环从2索引开始以此类推
6. 第四轮循环从3索引开始以此类推。 

### 2.2 动图演示

![选择排序](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day21-API（算法，lambda，练习）\笔记\img\选择排序.gif)

 

```java
public class A02_SelectionDemo {
    public static void main(String[] args) {

        /*
            选择排序：
                1，从0索引开始，跟后面的元素一一比较。
                2，小的放前面，大的放后面。
                3，第一次循环结束后，最小的数据已经确定。
                4，第二次循环从1索引开始以此类推。

         */


        //1.定义数组
        int[] arr = {2, 4, 5, 3, 1};


        //2.利用选择排序让数组变成 1 2 3 4 5
       /* //第一轮：
        //从0索引开始，跟后面的元素一一比较。
        for (int i = 0 + 1; i < arr.length; i++) {
            //拿着0索引跟后面的数据进行比较
            if(arr[0] > arr[i]){
                int temp = arr[0];
                arr[0] = arr[i];
                arr[i] = temp;
            }
        }*/

        //最终代码：
        //外循环：几轮
        //i:表示这一轮中，我拿着哪个索引上的数据跟后面的数据进行比较并交换
        for (int i = 0; i < arr.length -1; i++) {
            //内循环：每一轮我要干什么事情？
            //拿着i跟i后面的数据进行比较交换
            for (int j = i + 1; j < arr.length; j++) {
                if(arr[i] > arr[j]){
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }


        printArr(arr);


    }
    private static void printArr(int[] arr) {
        //3.遍历数组
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

}

```



## 3. 插入排序

插入排序的代码实现虽然没有冒泡排序和选择排序那么简单粗暴，但它的原理应该是最容易理解的了，因为只要打过扑克牌的人都应该能够秒懂。插入排序是一种最简单直观的排序算法，它的工作原理是通过创建有序序列和无序序列，然后再遍历无序序列得到里面每一个数字，把每一个数字插入到有序序列中正确的位置。

插入排序在插入的时候，有优化算法，在遍历有序序列找正确位置时，可以采取二分查找

### 3.1 算法步骤

将0索引的元素到N索引的元素看做是有序的，把N+1索引的元素到最后一个当成是无序的。

遍历无序的数据，将遍历到的元素插入有序序列中适当的位置，如遇到相同数据，插在后面。

N的范围：0~最大索引

### 3.2 动图演示

![插入排序](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day21-API（算法，lambda，练习）\笔记\img\插入排序.gif)

```java
package com.itheima.mysort;


public class A03_InsertDemo {
    public static void main(String[] args) {
        /*
            插入排序：
                将0索引的元素到N索引的元素看做是有序的，把N+1索引的元素到最后一个当成是无序的。
                遍历无序的数据，将遍历到的元素插入有序序列中适当的位置，如遇到相同数据，插在后面。
                N的范围：0~最大索引

        */
        int[] arr = {3, 44, 38, 5, 47, 15, 36, 26, 27, 2, 46, 4, 19, 50, 48};

        //1.找到无序的哪一组数组是从哪个索引开始的。  2
        int startIndex = -1;
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] > arr[i + 1]){
                startIndex = i + 1;
                break;
            }
        }

        //2.遍历从startIndex开始到最后一个元素，依次得到无序的哪一组数据中的每一个元素
        for (int i = startIndex; i < arr.length; i++) {
            //问题：如何把遍历到的数据，插入到前面有序的这一组当中

            //记录当前要插入数据的索引
            int j = i;

            while(j > 0 && arr[j] < arr[j - 1]){
                //交换位置
                int temp = arr[j];
                arr[j] = arr[j - 1];
                arr[j - 1] = temp;
                j--;
            }

        }
        printArr(arr);
    }

    private static void printArr(int[] arr) {
        //3.遍历数组
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

}

```





## 4. 快速排序 

快速排序是由东尼·霍尔所发展的一种排序算法。

快速排序又是一种分而治之思想在排序算法上的典型应用。

快速排序的名字起的是简单粗暴，因为一听到这个名字你就知道它存在的意义，就是快，而且效率高！

它是处理大数据最快的排序算法之一了。

### 4.1 算法步骤

1. 从数列中挑出一个元素，一般都是左边第一个数字，称为 "基准数";
2. 创建两个指针，一个从前往后走，一个从后往前走。
3. 先执行后面的指针，找出第一个比基准数小的数字
4. 再执行前面的指针，找出第一个比基准数大的数字
5. 交换两个指针指向的数字
6. 直到两个指针相遇
7. 将基准数跟指针指向位置的数字交换位置，称之为：基准数归位。
8. 第一轮结束之后，基准数左边的数字都是比基准数小的，基准数右边的数字都是比基准数大的。
9. 把基准数左边看做一个序列，把基准数右边看做一个序列，按照刚刚的规则递归排序

### 4.2 动图演示

![快速排序](C:\Users\wuhen\Desktop\2.java基础\1.Java基础与进阶\java黑马程序员\上\day21-API（算法，lambda，练习）\笔记\img\快速排序.gif)

 ```java
package com.itheima.mysort;

import java.util.Arrays;

public class A05_QuickSortDemo {
    public static void main(String[] args) {
        System.out.println(Integer.MAX_VALUE);
        System.out.println(Integer.MIN_VALUE);
      /*
        快速排序：
            第一轮：以0索引的数字为基准数，确定基准数在数组中正确的位置。
            比基准数小的全部在左边，比基准数大的全部在右边。
            后面以此类推。
      */

        int[] arr = {1,1, 6, 2, 7, 9, 3, 4, 5, 1,10, 8};


        //int[] arr = new int[1000000];

       /* Random r = new Random();
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt();
        }*/


        long start = System.currentTimeMillis();
        quickSort(arr, 0, arr.length - 1);
        long end = System.currentTimeMillis();

        System.out.println(end - start);//149

        System.out.println(Arrays.toString(arr));
        //课堂练习：
        //我们可以利用相同的办法去测试一下，选择排序，冒泡排序以及插入排序运行的效率
        //得到一个结论：快速排序真的非常快。

       /* for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }*/

    }


    /*
     *   参数一：我们要排序的数组
     *   参数二：要排序数组的起始索引
     *   参数三：要排序数组的结束索引
     * */
    public static void quickSort(int[] arr, int i, int j) {
        //定义两个变量记录要查找的范围
        int start = i;
        int end = j;

        if(start > end){
            //递归的出口
            return;
        }



        //记录基准数
        int baseNumber = arr[i];
        //利用循环找到要交换的数字
        while(start != end){
            //利用end，从后往前开始找，找比基准数小的数字
            //int[] arr = {1, 6, 2, 7, 9, 3, 4, 5, 10, 8};
            while(true){
                if(end <= start || arr[end] < baseNumber){
                    break;
                }
                end--;
            }
            System.out.println(end);
            //利用start，从前往后找，找比基准数大的数字
            while(true){
                if(end <= start || arr[start] > baseNumber){
                    break;
                }
                start++;
            }



            //把end和start指向的元素进行交换
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
        }

        //当start和end指向了同一个元素的时候，那么上面的循环就会结束
        //表示已经找到了基准数在数组中应存入的位置
        //基准数归位
        //就是拿着这个范围中的第一个数字，跟start指向的元素进行交换
        int temp = arr[i];
        arr[i] = arr[start];
        arr[start] = temp;

        //确定6左边的范围，重复刚刚所做的事情
        quickSort(arr,i,start - 1);
        //确定6右边的范围，重复刚刚所做的事情
        quickSort(arr,start + 1,j);

    }
}
 ```



其他排序方式待更新~



# 14.集合进阶

## 1.`Collection`集合

- 数组和集合的区别

  1. 相同点

     都是容器,可以存储多个数据

  2. 不同点

     - 数组的长度是不可变的,集合的长度是可变的

     - 数组可以存基本数据类型和引用数据类型

       集合只能存引用数据类型,如果要存基本数据类型,需要存对应的包装类

- 集合类体系结构

  ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/009.png?raw=true)

- Collection 集合概述和使用

  1. Collection集合概述

     - 是单列集合的顶层接口,它表示一组对象,这些对象也称为Collection的元素
     - JDK 不提供此接口的任何直接实现.它提供更具体的子接口(如Set和List)实现

  2. 创建Collection集合的对象

     - 多态的方式
     - 具体的实现类ArrayList

  3. Collection集合常用方法

     | 方法名                     | 说明                               |
     | :------------------------- | :--------------------------------- |
     | boolean add(E e)           | 添加元素                           |
     | boolean remove(Object o)   | 从集合中移除指定的元素             |
     | boolean removeIf(Object o) | 根据条件进行移除                   |
     | void   clear()             | 清空集合中的元素                   |
     | boolean contains(Object o) | 判断集合中是否存在指定的元素       |
     | boolean isEmpty()          | 判断集合是否为空                   |
     | int   size()               | 集合的长度，也就是集合中元素的个数 |

- Collection集合的遍历

  1. 迭代器遍历

     - 迭代器介绍

       - 迭代器,集合的专用遍历方式
       - Iterator<E> iterator(): 返回此集合中元素的迭代器,通过集合对象的iterator()方法得到

     - Iterator中的常用方法

       `boolean hasNext()`: 判断当前位置是否有元素可以被取出

       E next(): 获取当前位置的元素,将迭代器对象移向下一个索引位置

     - Collection集合的遍历

       ```java
       public class IteratorDemo1 {
           public static void main(String[] args) {
               //创建集合对象
               Collection<String> c = new ArrayList<>();
       
               //添加元素
               c.add("hello");
               c.add("world");
               c.add("java");
               c.add("javaee");
       
               //Iterator<E> iterator()：返回此集合中元素的迭代器，通过集合的iterator()方法得到
               Iterator<String> it = c.iterator();
       
               //用while循环改进元素的判断和获取
               while (it.hasNext()) {
                   String s = it.next();
                   System.out.println(s);
               }
           }
       }
       ```

  2. 迭代器中删除的方法

     void remove(): 删除迭代器对象当前指向的元素

     ```java
     public class IteratorDemo2 {
         public static void main(String[] args) {
             ArrayList<String> list = new ArrayList<>();
             list.add("a");
             list.add("b");
             list.add("b");
             list.add("c");
             list.add("d");
     
             Iterator<String> it = list.iterator();
             while(it.hasNext()){
                 String s = it.next();
                 if("b".equals(s)){
                     //指向谁,那么此时就删除谁.
                     it.remove();
                 }
             }
             System.out.println(list);
         }
     }
     ```

- 增强for

  1. 介绍

     - 它是JDK5之后出现的,其内部原理是一个Iterator迭代器
     - 实现Iterable接口的类才可以使用迭代器和增强for
     - 简化数组和Collection集合的遍历

  2. 格式

     ```java
     for(集合/数组中元素的数据类型 变量名 :  集合/数组名) {
     		// 已经将当前遍历到的元素封装到变量中了,直接使用变量即可
     
     }
     ```

  3. 代码

     ```java
     public class MyCollectonDemo1 {
         public static void main(String[] args) {
             ArrayList<String> list =  new ArrayList<>();
             list.add("a");
             list.add("b");
             list.add("c");
             list.add("d");
             list.add("e");
             list.add("f");
     
             //1,数据类型一定是集合或者数组中元素的类型
             //2,str仅仅是一个变量名而已,在循环的过程中,依次表示集合或者数组中的每一个元素
             //3,list就是要遍历的集合或者数组
             for(String str : list){
                 System.out.println(str);
             }
         }
     }
     ```

  4. 细节点注意：

     - 报错NoSuchElementException 

     - 迭代器遍历完毕，指针不会复位 

     - 循环中只能用一次next方法        

     - 迭代器遍历时，不能用集合的方法进行增加或者删除

       ```java
       public class A04_CollectionDemo4 {
           public static void main(String[] args) {
             /*
               迭代器的细节注意点：
                   1.报错NoSuchElementException
                   2.迭代器遍历完毕，指针不会复位
                   3.循环中只能用一次next方法
                   4.迭代器遍历时，不能用集合的方法进行增加或者删除
                   	暂时当做一个结论先行记忆，在今天我们会讲解源码详细的再来分析。
                       如果我实在要删除：那么可以用迭代器提供的remove方法进行删除。
                       如果我要添加，暂时没有办法。(只是暂时)
              */
       
               //1.创建集合并添加元素
               Collection<String> coll = new ArrayList<>();
               coll.add("aaa");
               coll.add("bbb");
               coll.add("ccc");
               coll.add("ddd");
       
               //2.获取迭代器对象
               //迭代器就好比是一个箭头，默认指向集合的0索引处
               Iterator<String> it = coll.iterator();
               //3.利用循环不断的去获取集合中的每一个元素
               while(it.hasNext()){
                   //4.next方法的两件事情：获取元素并移动指针
                   String str = it.next();
                   System.out.println(str);
               }
       
               //当上面循环结束之后，迭代器的指针已经指向了最后没有元素的位置
               //System.out.println(it.next());//NoSuchElementException
       
               //迭代器遍历完毕，指针不会复位
               System.out.println(it.hasNext());
       
               //如果我们要继续第二次遍历集合，只能再次获取一个新的迭代器对象
               Iterator<String> it2 = coll.iterator();
               while(it2.hasNext()){
                   String str = it2.next();
                   System.out.println(str);
               }
           }
       }
       ```

- lambda表达式

  利用forEach方法，再结合lambda表达式的方式进行遍历

  ```java
  public class A07_CollectionDemo7 {
      public static void main(String[] args) {
         /* 
          lambda表达式遍历：
                  default void forEach(Consumer<? super T> action):
          */
  
          //1.创建集合并添加元素
          Collection<String> coll = new ArrayList<>();
          coll.add("zhangsan");
          coll.add("lisi");
          coll.add("wangwu");
          //2.利用匿名内部类的形式
          //底层原理：
          //其实也会自己遍历集合，依次得到每一个元素
          //把得到的每一个元素，传递给下面的accept方法
          //s依次表示集合中的每一个数据
         /* coll.forEach(new Consumer<String>() {
              @Override
              public void accept(String s) {
                  System.out.println(s);
              }
          });*/
  
          //lambda表达式
          coll.forEach(s -> System.out.println(s));
      }
  }
  ```

  

### 1.`List`集合

- List集合的概述和特点
  1. List集合的概述
     - 有序集合,这里的有序指的是存取顺序
     - 可精确控制列表中每个元素的插入位置，通过整数索引访问元素,并搜索列表中的元素
     - 与Set集合不同,列表通常允许重复的元素
  2. List集合的特点
     - 存取有序
     - 可以重复
     - 有索引

- List集合的特有方法

  1. 方法介绍

     | 方法名                          | 描述                                   |
     | ------------------------------- | -------------------------------------- |
     | void add(int index,E   element) | 在此集合中的指定位置插入指定的元素     |
     | E remove(int   index)           | 删除指定索引处的元素，返回被删除的元素 |
     | E set(int index,E   element)    | 修改指定索引处的元素，返回被修改的元素 |
     | E get(int   index)              | 返回指定索引处的元素                   |

  2. 示例代码

     ```java
     public class MyListDemo {
         public static void main(String[] args) {
             List<String> list = new ArrayList<>();
             list.add("aaa");
             list.add("bbb");
             list.add("ccc");
             //method1(list);
             //method2(list);
             //method3(list);
             //method4(list);
         }
     
         private static void method4(List<String> list) {
             //        E get(int index)		返回指定索引处的元素
             String s = list.get(0);
             System.out.println(s);
         }
     
         private static void method3(List<String> list) {
             //        E set(int index,E element)	修改指定索引处的元素，返回被修改的元素
             //被替换的那个元素,在集合中就不存在了.
             String result = list.set(0, "qqq");
             System.out.println(result);
             System.out.println(list);
         }
     
         private static void method2(List<String> list) {
             //        E remove(int index)		删除指定索引处的元素，返回被删除的元素
             //在List集合中有两个删除的方法
             //第一个 删除指定的元素,返回值表示当前元素是否删除成功
             //第二个 删除指定索引的元素,返回值表示实际删除的元素
             String s = list.remove(0);
             System.out.println(s);
             System.out.println(list);
         }
     
         private static void method1(List<String> list) {
             //        void add(int index,E element)	在此集合中的指定位置插入指定的元素
             //原来位置上的元素往后挪一个索引.
             list.add(0,"qqq");
             System.out.println(list);
         }
     }
     ```


- List集合的五种遍历方式

  1. 迭代器
  2. 列表迭代器
  3. 增强for
  4. Lambda表达式
  5. 普通for循环

  代码示例：

  ```java
  //创建集合并添加元素
  List<String> list = new ArrayList<>();
  list.add("aaa");
  list.add("bbb");
  list.add("ccc");
  
  //1.迭代器
  /*Iterator<String> it = list.iterator();
       while(it.hasNext()){
          String str = it.next();
          System.out.println(str);
  }*/
  
  
  //2.增强for
  //下面的变量s，其实就是一个第三方的变量而已。
  //在循环的过程中，依次表示集合中的每一个元素
  /* for (String s : list) {
         System.out.println(s);
     }*/
  
  //3.Lambda表达式
  //forEach方法的底层其实就是一个循环遍历，依次得到集合中的每一个元素
  //并把每一个元素传递给下面的accept方法
  //accept方法的形参s，依次表示集合中的每一个元素
  //list.forEach(s->System.out.println(s) );
  
  
  //4.普通for循环
  //size方法跟get方法还有循环结合的方式，利用索引获取到集合中的每一个元素
  /*for (int i = 0; i < list.size(); i++) {
              //i:依次表示集合中的每一个索引
              String s = list.get(i);
              System.out.println(s);
          }*/
  
  // 5.列表迭代器
  //获取一个列表迭代器的对象，里面的指针默认也是指向0索引的
  
  //额外添加了一个方法：在遍历的过程中，可以添加元素
  ListIterator<String> it = list.listIterator();
  while(it.hasNext()){
      String str = it.next();
      if("bbb".equals(str)){
          //qqq
          it.add("qqq");
      }
  }
  System.out.println(list);
  ```

- 细节点注意：

  List系列集合中的两个删除的方法

  ```java
  1.直接删除元素
  2.通过索引进行删除
  ```

  代码示例:

  ```java
  //List系列集合中的两个删除的方法
  //1.直接删除元素
  //2.通过索引进行删除
  
  //1.创建集合并添加元素
  List<Integer> list = new ArrayList<>();
  
  list.add(1);
  list.add(2);
  list.add(3);
  
  
  //2.删除元素
  //请问：此时删除的是1这个元素，还是1索引上的元素？
  //为什么？
  //因为在调用方法的时候，如果方法出现了重载现象
  //优先调用，实参跟形参类型一致的那个方法。
  
  //list.remove(1);
  
  
  //手动装箱，手动把基本数据类型的1，变成Integer类型
  Integer i = Integer.valueOf(1);
  
  list.remove(i);
  
  System.out.println(list);
  
  ```




### 2.`List`集合的实现类

- List集合子类的特点【记忆】

  1. ArrayList集合

     底层是数组结构实现，查询快、增删慢

  2. LinkedList集合

     底层是链表结构实现，查询慢、增删快

- LinkedList集合的特有功能【应用】

  1. 特有方法

     | 方法名                    | 说明                             |
     | ------------------------- | -------------------------------- |
     | public void addFirst(E e) | 在该列表开头插入指定的元素       |
     | public void addLast(E e)  | 将指定的元素追加到此列表的末尾   |
     | public E getFirst()       | 返回此列表中的第一个元素         |
     | public   E getLast()      | 返回此列表中的最后一个元素       |
     | public E removeFirst()    | 从此列表中删除并返回第一个元素   |
     | public   E removeLast()   | 从此列表中删除并返回最后一个元素 |

  2. 示例代码

     ```java
     public class MyLinkedListDemo4 {
         public static void main(String[] args) {
             LinkedList<String> list = new LinkedList<>();
             list.add("aaa");
             list.add("bbb");
             list.add("ccc");
     //        public void addFirst(E e)	在该列表开头插入指定的元素
             //method1(list);
     
     //        public void addLast(E e)	将指定的元素追加到此列表的末尾
             //method2(list);
     
     //        public E getFirst()		返回此列表中的第一个元素
     //        public E getLast()		返回此列表中的最后一个元素
             //method3(list);
     
     //        public E removeFirst()		从此列表中删除并返回第一个元素
     //        public E removeLast()		从此列表中删除并返回最后一个元素
             //method4(list);
           
         }
     
         private static void method4(LinkedList<String> list) {
             String first = list.removeFirst();
             System.out.println(first);
     
             String last = list.removeLast();
             System.out.println(last);
     
             System.out.println(list);
         }
     
         private static void method3(LinkedList<String> list) {
             String first = list.getFirst();
             String last = list.getLast();
             System.out.println(first);
             System.out.println(last);
         }
     
         private static void method2(LinkedList<String> list) {
             list.addLast("www");
             System.out.println(list);
         }
     
         private static void method1(LinkedList<String> list) {
             list.addFirst("qqq");
             System.out.println(list);
         }
     }
     ```




### 3.源码分析

- ArrayList源码分析：

  1. 核心步骤：

     - 创建ArrayList对象时，底层先创建了一个长度为0的数组。（添加第一个元素时，底层会创建一个新的长度为10的数组）

       数组名字：elementDate，定义变量size。

       size这个变量有两层含义：
       ①：元素的个数，也就是集合的长度
       ②：下一个元素的存入位置

     - 添加元素，添加完毕后，size++

  2. 扩容时机一：

     当存满时候，会创建一个新的数组，新数组的长度，是原来的1.5倍，也就是长度为15.再把所有的元素，全拷贝到新数组中。

  3. 扩容时机二：

     如果一次添加多个元素，超过1.5倍，新创建数组的长度以实际为准。

- LinkedList源码分析：

  > 底层是双向链表结构

  核心步骤如下：

  1. 刚开始创建的时候，底层创建了两个变量：一个记录头结点first，一个记录尾结点last，默认为null
  2. 添加第一个元素时，底层创建一个结点对象，first和last都记录这个结点的地址值
  3. 添加第二个元素时，底层创建一个结点对象，第一个结点会记录第二个结点的地址值，last会记录新结点的地址值

- 迭代器源码分析：

  迭代器遍历相关的三个方法：

  1. Iterator<E> iterator()  ：获取一个迭代器对象

  2. boolean hasNext()       ：判断当前指向的位置是否有元素

  3. E next()                ：获取当前指向的元素并移动指针



### 4.泛型

- 泛型概述：

  1. 泛型的介绍

     泛型是JDK5中引入的特性，它提供了编译时类型安全检测机制

  2. 泛型的好处

     - 把运行时期的问题提前到了编译期间，避免了强制类型转换
     - 统一数据类型

  3. 泛型的定义格式

     - <类型>: 指定一种类型的格式.尖括号里面可以任意书写,一般只写一个字母.例如: <E> <T>

       注：泛型只能支持引用数据类型。

     - <类型1,类型2…>: 指定多种类型的格式,多种类型之间用逗号隔开.例如: <E,T> <K,V>

- 泛型类

  格式

  ```Java
  修饰符 class 类名<类型>{
      
  }
  
  
  public class ArryList<E>{
      
  }
  ```

- 泛型方法

  1. 方案一：使用类名后面定义的泛型（所有方法都可使用）

  2. 方案二：在方法申明上定义自己的泛型（只有本方法使用）

     ```java
     public static<E> void addAll(ArrayList<E> list){
         
     }
     ```

- 泛型接口

  ```java
  public interface List<E>{
  
  }
  ```

  1. 实现类给出具体类型
  2. 实现类延续泛型，创建对象时在确定

- 泛型的继承

  泛型不具备继承性，但是数据具备继承性

- 泛型的通配符

  1. ？：表示不确定的通配符。

     ```java
     ? extends E: //表示可以传递E或E所有的子类类型
     ? super E: //表示可以传递E或E所有的父类类型
     
     public static void method(ArraryList<? extends Ye> list){
         
     }
     
     public static void method(ArraryList<? super zi> list){
         
     }
     ```



### 5.数据结构（树）

- 二叉树

  任意一个节点的度要小于等于2

- 二叉查找树

  1. 二叉查找树的特点

     + 二叉查找树,又称二叉排序树或者二叉搜索树
     + 每一个节点上最多有两个子节点
     + 左子树上所有节点的值都小于根节点的值
     + 右子树上所有节点的值都大于根节点的值
  2. 二叉查找树添加节点规则

     + 小的存左边
     + 大的存右边
     + 一样的不存

- 平衡二叉树

  1. 平衡二叉树的特点

     + 二叉树左右两个子树的高度差不超过1
     + 任意节点的左右两个子树都是一颗平衡二叉树

  2. 平衡二叉树旋转

     + 旋转触发时机

       当添加一个节点之后,该树不再是一颗平衡二叉树

     + 左旋

       就是将根节点的右侧往左拉,原先的右子节点变成新的父节点,并把多余的左子节点出让,给已经降级的根节点当右子节点

     + 右旋

       就是将根节点的左侧往右拉,左子节点变成了新的父节点,并把多余的右子节点出让,给已经降级根节点当左子节点

  3. 平衡二叉树旋转的四种情况

     + 左左

       + 左左: 当根节点左子树的左子树有节点插入,导致二叉树不平衡

       + 如何旋转: 直接对整体进行右旋即可

     + 左右

       + 左右: 当根节点左子树的右子树有节点插入,导致二叉树不平衡

       + 如何旋转: 先在左子树对应的节点位置进行左旋,在对整体进行右旋

     + 右右

       + 右右: 当根节点右子树的右子树有节点插入,导致二叉树不平衡

       + 如何旋转: 直接对整体进行左旋即可

     + 右左

       + 右左:当根节点右子树的左子树有节点插入,导致二叉树不平衡

       + 如何旋转: 先在右子树对应的节点位置进行右旋,在对整体进行左旋

- 红黑树

  1. 红黑树的特点

     - 平衡二叉B树
     - 每一个节点可以是红或者黑
     - 红黑树不是高度平衡的,它的平衡是通过"自己的红黑规则"进行实现的

  2. 红黑树的红黑规则

     1. 每一个节点或是红色的,或者是黑色的

     2. 根节点必须是黑色

     3. 如果一个节点没有子节点或者父节点,则该节点相应的指针属性值为Nil,这些Nil视为叶节点,每个叶节点(Nil)是黑色的

     4. 如果某一个节点是红色,那么它的子节点必须是黑色(不能出现两个红色节点相连 的情况)

     5. 对每一个节点,从该节点到其所有后代叶节点的简单路径上,均包含相同数目的黑色节点

  3. 红黑树添加节点的默认颜色

     - 添加节点时,默认为红色,效率高

  4. 红黑树添加节点后如何保持红黑规则

     - 根节点位置
       - 直接变为黑色
     - 非根节点位置
       - 父节点为黑色
         - 不需要任何操作,默认红色即可
       - 父节点为红色
         - 叔叔节点为红色
           1. 将"父节点"设为黑色,将"叔叔节点"设为黑色
           2. 将"祖父节点"设为红色
           3. 如果"祖父节点"为根节点,则将根节点再次变成黑色
         - 叔叔节点为黑色
           1. 将"父节点"设为黑色
           2. 将"祖父节点"设为红色
           3. 以"祖父节点"为支点进行旋转

  



### 6.`Set`集合

- Set集合概述和特点

  1. 不可以存储重复元素
  2. 没有索引,不能使用普通for循环遍历

- Set集合的使用

  存储字符串并遍历

  ```java
  public class MySet1 {
      public static void main(String[] args) {
        	//创建集合对象
          Set<String> set = new TreeSet<>();
        	//添加元素
          set.add("ccc");
          set.add("aaa");
          set.add("aaa");
          set.add("bbb");
  
  //        for (int i = 0; i < set.size(); i++) {
  //            //Set集合是没有索引的，所以不能使用通过索引获取元素的方法
  //        }
        
        	//遍历集合
          Iterator<String> it = set.iterator();
          while (it.hasNext()){
              String s = it.next();
              System.out.println(s);
          }
          
          
          System.out.println("-----------------------------------");
          
          // 增强for
          for (String s : set) {
              System.out.println(s);
          }
          
          
          //Lambda表达式
          s.forEach(str -> Sout(str))
          
      }
  }
  ```



### 7.`HashSet`集合

- HashSet集合概述和特点

  1. 底层数据结构是哈希表
  2. 存取无序
  3. 不可以存储重复元素
  4. 没有索引,不能使用普通for循环遍历

- HashSet集合的基本应用

  存储字符串并遍历

  ```java
  public class HashSetDemo {
      public static void main(String[] args) {
          //创建集合对象
          HashSet<String> set = new HashSet<String>();
  
          //添加元素
          set.add("hello");
          set.add("world");
          set.add("java");
          //不包含重复元素的集合
          set.add("world");
  
          //遍历
          for(String s : set) {
              System.out.println(s);
          }
      }
  }
  ```

- 哈希值

  1. 哈希值简介

     是JDK根据对象的地址或者字符串或者数字算出来的int类型的数值

  2. 获取哈希值

     Object类中的public int hashCode()：返回对象的哈希码值

  3. 哈希值的特点

     - 同一个对象多次调用hashCode()方法返回的哈希值是相同的
     - 默认情况下，不同对象的哈希值是不同的。而重写hashCode()方法，可以实现让不同对象的哈希值相同

- 哈希表结构

  1. JDK1.8以前：	数组 + 链表

  2. JDK1.8以后：

     - 节点个数少于等于8个

       ​	数组 + 链表

     - 节点个数多于8个

       ​	数组 + 红黑树

- HashSet集合存储学生对象并遍历

  1. 案例需求

     - 创建一个存储学生对象的集合，存储多个学生对象，使用程序实现在控制台遍历该集合
     - 要求：学生对象的成员变量值相同，我们就认为是同一个对象

  2. 代码实现

     学生类

     ```java
     public class Student {
         private String name;
         private int age;
     
         public Student() {
         }
     
         public Student(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     
         @Override
         public boolean equals(Object o) {
             if (this == o) return true;
             if (o == null || getClass() != o.getClass()) return false;
     
             Student student = (Student) o;
     
             if (age != student.age) return false;
             return name != null ? name.equals(student.name) : student.name == null;
         }
     
         @Override
         public int hashCode() {
             int result = name != null ? name.hashCode() : 0;
             result = 31 * result + age;
             return result;
         }
     }
     ```

     测试类

     ```java
     public class HashSetDemo02 {
         public static void main(String[] args) {
             //创建HashSet集合对象
             HashSet<Student> hs = new HashSet<Student>();
     
             //创建学生对象
             Student s1 = new Student("林青霞", 30);
             Student s2 = new Student("张曼玉", 35);
             Student s3 = new Student("王祖贤", 33);
     
             Student s4 = new Student("王祖贤", 33);
     
             //把学生添加到集合
             hs.add(s1);
             hs.add(s2);
             hs.add(s3);
             hs.add(s4);
     
             //遍历集合(增强for)
             for (Student s : hs) {
                 System.out.println(s.getName() + "," + s.getAge());
             }
         }
     }
     ```

  3. 总结

     ​	HashSet集合存储自定义类型元素,要想实现元素的唯一,要求必须重写hashCode方法和equals方法

  






### 8.`TreeSet`集合

- TreeSet集合概述和特点
  1. 不可以存储重复元素
  2. 没有索引
  3. 可以将元素按照规则进行排序
     + TreeSet()：根据其元素的自然排序进行排序
     + TreeSet(Comparator comparator) ：根据指定的比较器进行排序
  
- TreeSet集合基本使用

  存储Integer类型的整数并遍历

  ```java
  public class TreeSetDemo01 {
      public static void main(String[] args) {
          //创建集合对象
          TreeSet<Integer> ts = new TreeSet<Integer>();
  
          //添加元素
          ts.add(10);
          ts.add(40);
          ts.add(30);
          ts.add(50);
          ts.add(20);
  
          ts.add(30);
  
          //遍历集合
          for(Integer i : ts) {
              System.out.println(i);
          }
      }
  }
  ```

- 自然排序Comparable的使用

  1. 案例需求

     - 存储学生对象并遍历，创建TreeSet集合使用无参构造方法
     - 要求：按照年龄从小到大排序，年龄相同时，按照姓名的字母顺序排序

  2. 实现步骤

     - 使用空参构造创建TreeSet集合

       用TreeSet集合存储自定义对象，无参构造方法使用的是自然排序对元素进行排序的

     - 自定义的Student类实现Comparable接口

       自然排序，就是让元素所属的类实现Comparable接口，重写compareTo(T o)方法

     - 重写接口中的compareTo方法

       重写方法时，一定要注意排序规则必须按照要求的主要条件和次要条件来写

  3. 代码实现

     学生类

     ```java
     public class Student implements Comparable<Student>{
         private String name;
         private int age;
     
         public Student() {
         }
     
         public Student(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     
         @Override
         public String toString() {
             return "Student{" +
                     "name='" + name + '\'' +
                     ", age=" + age +
                     '}';
         }
     
         @Override
         public int compareTo(Student o) {
             //按照对象的年龄进行排序
             //主要判断条件: 按照年龄从小到大排序
             int result = this.age - o.age;
             //次要判断条件: 年龄相同时，按照姓名的字母顺序排序
             result = result == 0 ? this.name.compareTo(o.getName()) : result;
             return result;
         }
     }
     ```

     测试类

     ```java
     public class MyTreeSet2 {
         public static void main(String[] args) {
             //创建集合对象
             TreeSet<Student> ts = new TreeSet<>();
     	    //创建学生对象
             Student s1 = new Student("zhangsan",28);
             Student s2 = new Student("lisi",27);
             Student s3 = new Student("wangwu",29);
             Student s4 = new Student("zhaoliu",28);
             Student s5 = new Student("qianqi",30);
     		//把学生添加到集合
             ts.add(s1);
             ts.add(s2);
             ts.add(s3);
             ts.add(s4);
             ts.add(s5);
     		//遍历集合
             for (Student student : ts) {
                 System.out.println(student);
             }
         }
     }
     ```


- 比较器排序Comparator的使用

  1. 案例需求

     - 存储老师对象并遍历，创建TreeSet集合使用带参构造方法
     - 要求：按照年龄从小到大排序，年龄相同时，按照姓名的字母顺序排序

  2. 实现步骤

     - 用TreeSet集合存储自定义对象，带参构造方法使用的是比较器排序对元素进行排序的
     - 比较器排序，就是让集合构造方法接收Comparator的实现类对象，重写compare(T o1,T o2)方法
     - 重写方法时，一定要注意排序规则必须按照要求的主要条件和次要条件来写

  3. 代码实现

     老师类

     ```java
     public class Teacher {
         private String name;
         private int age;
     
         public Teacher() {
         }
     
         public Teacher(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     
         @Override
         public String toString() {
             return "Teacher{" +
                     "name='" + name + '\'' +
                     ", age=" + age +
                     '}';
         }
     }
     ```

     测试类

     ```java
     public class MyTreeSet4 {
         public static void main(String[] args) {
           	//创建集合对象
             TreeSet<Teacher> ts = new TreeSet<>(new Comparator<Teacher>() {
                 @Override
                 public int compare(Teacher o1, Teacher o2) {
                     //o1表示现在要存入的那个元素
                     //o2表示已经存入到集合中的元素
                   
                     //主要条件
                     int result = o1.getAge() - o2.getAge();
                     //次要条件
                     result = result == 0 ? o1.getName().compareTo(o2.getName()) : result;
                     return result;
                 }
             });
     		//创建老师对象
             Teacher t1 = new Teacher("zhangsan",23);
             Teacher t2 = new Teacher("lisi",22);
             Teacher t3 = new Teacher("wangwu",24);
             Teacher t4 = new Teacher("zhaoliu",24);
     		//把老师添加到集合
             ts.add(t1);
             ts.add(t2);
             ts.add(t3);
             ts.add(t4);
     		//遍历集合
             for (Teacher teacher : ts) {
                 System.out.println(teacher);
             }
         }
     }
     ```


- 两种比较方式总结
  1. 两种比较方式小结
     + 自然排序: 自定义类实现Comparable接口,重写compareTo方法,根据返回值进行排序
     + 比较器排序: 创建TreeSet对象的时候传递Comparator的实现类对象,重写compare方法,根据返回值进行排序
     + 在使用的时候,默认使用自然排序,当自然排序不满足现在的需求时,必须使用比较器排序
  2. 两种方式中关于返回值的规则
     + 如果返回值为负数，表示当前存入的元素是较小值，存左边
     + 如果返回值为0，表示当前存入的元素跟集合中元素重复了，不存
     + 如果返回值为正数，表示当前存入的元素是较大值，存右边



## 2.`Map`集合

- Map集合概述和特点【理解】

  1. Map集合概述

     ```java
     interface Map<K,V>  K：键的类型；V：值的类型 
         // 键值对
         // 或 键值对对象
         // 或 Entry
     ```

  2. Map集合的特点

     - 双列集合,一个键对应一个值
     - 键不可以重复,值可以重复

  3. Map集合的基本使用

     ```java
     public class MapDemo01 {
         public static void main(String[] args) {
             //创建集合对象
             Map<String,String> map = new HashMap<String,String>();
     
             //V put(K key, V value) 将指定的值与该映射中的指定键相关联
             map.put("itheima001","林青霞");
             map.put("itheima002","张曼玉");
             map.put("itheima003","王祖贤");
             map.put("itheima003","柳岩");
     
             //输出集合对象
             System.out.println(map);
         }
     }
     ```


- Map集合的基本功能

  1. 方法介绍

     | 方法名                              | 说明                                               |
     | ----------------------------------- | -------------------------------------------------- |
     | V   put(K key,V   value)            | 添加元素（若覆盖，返回被覆盖的值，若空，返回null） |
     | V   remove(Object key)              | 根据键删除键值对元素                               |
     | void   clear()                      | 移除所有的键值对元素                               |
     | boolean containsKey(Object key)     | 判断集合是否包含指定的键                           |
     | boolean containsValue(Object value) | 判断集合是否包含指定的值                           |
     | boolean isEmpty()                   | 判断集合是否为空                                   |
     | int size()                          | 集合的长度，也就是集合中键值对的个数               |

  2. 示例代码

     ```java
     public class MapDemo02 {
         public static void main(String[] args) {
             //创建集合对象
             Map<String,String> map = new HashMap<String,String>();
     
             //V put(K key,V value)：添加元素
             map.put("张无忌","赵敏");
             map.put("郭靖","黄蓉");
             map.put("杨过","小龙女");
     
             //V remove(Object key)：根据键删除键值对元素
     //        System.out.println(map.remove("郭靖"));
     //        System.out.println(map.remove("郭襄"));
     
             //void clear()：移除所有的键值对元素
     //        map.clear();
     
             //boolean containsKey(Object key)：判断集合是否包含指定的键
     //        System.out.println(map.containsKey("郭靖"));
     //        System.out.println(map.containsKey("郭襄"));
     
             //boolean isEmpty()：判断集合是否为空
     //        System.out.println(map.isEmpty());
     
             //int size()：集合的长度，也就是集合中键值对的个数
             System.out.println(map.size());
     
             //输出集合对象
             System.out.println(map);
         }
     }
     ```


- Map集合的获取功能

  1. 方法介绍

     | 方法名                           | 说明                     |
     | -------------------------------- | ------------------------ |
     | V   get(Object key)              | 根据键获取值             |
     | Set<K>   keySet()                | 获取所有键的集合         |
     | Collection<V>   values()         | 获取所有值的集合         |
     | Set<Map.Entry<K,V>>   entrySet() | 获取所有键值对对象的集合 |

  2. 示例代码

     ```java
     public class MapDemo03 {
         public static void main(String[] args) {
             //创建集合对象
             Map<String, String> map = new HashMap<String, String>();
     
             //添加元素
             map.put("张无忌", "赵敏");
             map.put("郭靖", "黄蓉");
             map.put("杨过", "小龙女");
     
             //V get(Object key):根据键获取值
     //        System.out.println(map.get("张无忌"));
     //        System.out.println(map.get("张三丰"));
     
             //Set<K> keySet():获取所有键的集合
     //        Set<String> keySet = map.keySet();
     //        for(String key : keySet) {
     //            System.out.println(key);
     //        }
     
             //Collection<V> values():获取所有值的集合
             Collection<String> values = map.values();
             for(String value : values) {
                 System.out.println(value);
             }
         }
     }
     ```


- Map集合的遍历(方式1)

  1. 步骤分析

     - 获取所有键的集合。用keySet()方法实现
     - 遍历键的集合，获取到每一个键。用增强for实现  
     - 根据键去找值。用get(Object key)方法实现

  2. 代码实现

     ```java
     public class MapDemo01 {
         public static void main(String[] args) {
             //创建集合对象
             Map<String, String> map = new HashMap<String, String>();
     
             //添加元素
             map.put("张无忌", "赵敏");
             map.put("郭靖", "黄蓉");
             map.put("杨过", "小龙女");
     
             //获取所有键的集合。用keySet()方法实现
             Set<String> keySet = map.keySet();
             //遍历键的集合，获取到每一个键。用增强for实现
             for (String key : keySet) {
                 //根据键去找值。用get(Object key)方法实现
                 String value = map.get(key);
                 System.out.println(key + "," + value);
             }
         }
     }
     ```

- Map集合的遍历(方式2)

  1. 步骤分析

     - 获取所有键值对对象的集合
       - Set<Map.Entry<K,V>> entrySet()：获取所有键值对对象的集合
     - 遍历键值对对象的集合，得到每一个键值对对象
       - 用增强for实现，得到每一个Map.Entry
     - 根据键值对对象获取键和值
       - 用getKey()得到键
       - 用getValue()得到值

  2. 代码实现

     ```java
     public class MapDemo02 {
         public static void main(String[] args) {
             //创建集合对象
             Map<String, String> map = new HashMap<String, String>();
     
             //添加元素
             map.put("张无忌", "赵敏");
             map.put("郭靖", "黄蓉");
             map.put("杨过", "小龙女");
     
             //获取所有键值对对象的集合
             Set<Map.Entry<String, String>> entrySet = map.entrySet();
             //遍历键值对对象的集合，得到每一个键值对对象
             for (Map.Entry<String, String> me : entrySet) {
                 //根据键值对对象获取键和值
                 String key = me.getKey();
                 String value = me.getValue();
                 System.out.println(key + "," + value);
             }
         }
     }
     ```

  

### 1.`HashMap`集合

> 直接使用map中的方法即可。

- HashMap集合概述和特点

  1. HashMap底层是哈希表结构的
  2. 依赖hashCode方法和equals方法保证键的唯一
  3. 如果键要存储的是自定义对象，需要重写hashCode和equals方法

- HashMap集合应用案例

  1. 案例需求

     - 创建一个HashMap集合，键是学生对象(Student)，值是居住地 (String)。存储多个元素，并遍历。
     - 要求保证键的唯一性：如果学生对象的成员变量值相同，我们就认为是同一个对象

  2. 代码实现

     学生类

     ```java
     public class Student {
         private String name;
         private int age;
     
         public Student() {
         }
     
         public Student(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     
         @Override
         public boolean equals(Object o) {
             if (this == o) return true;
             if (o == null || getClass() != o.getClass()) return false;
     
             Student student = (Student) o;
     
             if (age != student.age) return false;
             return name != null ? name.equals(student.name) : student.name == null;
         }
     
         @Override
         public int hashCode() {
             int result = name != null ? name.hashCode() : 0;
             result = 31 * result + age;
             return result;
         }
     }
     ```

     测试类

     ```java
     public class HashMapDemo {
         public static void main(String[] args) {
             //创建HashMap集合对象
             HashMap<Student, String> hm = new HashMap<Student, String>();
     
             //创建学生对象
             Student s1 = new Student("林青霞", 30);
             Student s2 = new Student("张曼玉", 35);
             Student s3 = new Student("王祖贤", 33);
             Student s4 = new Student("王祖贤", 33);
     
             //把学生添加到集合
             hm.put(s1, "西安");
             hm.put(s2, "武汉");
             hm.put(s3, "郑州");
             hm.put(s4, "北京");
     
             //遍历集合
             Set<Student> keySet = hm.keySet();
             for (Student key : keySet) {
                 String value = hm.get(key);
                 System.out.println(key.getName() + "," + key.getAge() + "," + value);
             }
         }
     }
     ```

  

### 2.`TreeMap`集合

- TreeMap集合概述和特点

  1. TreeMap底层是红黑树结构
  2. 依赖自然排序或者比较器排序,对键进行排序
  3. 如果键存储的是自定义对象,需要实现Comparable接口或者在创建TreeMap对象时候给出比较器排序规则

- TreeMap集合应用案例

  1. 案例需求

     + 创建一个TreeMap集合,键是学生对象(Student),值是籍贯(String),学生属性姓名和年龄,按照年龄进行排序并遍历
     + 要求按照学生的年龄进行排序,如果年龄相同则按照姓名进行排序

  2. 代码实现

     学生类

     ```java
     public class Student implements Comparable<Student>{
         private String name;
         private int age;
     
         public Student() {
         }
     
         public Student(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     
         @Override
         public String toString() {
             return "Student{" +
                     "name='" + name + '\'' +
                     ", age=" + age +
                     '}';
         }
     
         @Override
         public int compareTo(Student o) {
             //按照年龄进行排序
             int result = o.getAge() - this.getAge();
             //次要条件，按照姓名排序。
             result = result == 0 ? o.getName().compareTo(this.getName()) : result;
             return result;
         }
     }
     ```

     测试类

     ```java
     public class Test1 {
         public static void main(String[] args) {
           	// 创建TreeMap集合对象
             TreeMap<Student,String> tm = new TreeMap<>();
           
     		// 创建学生对象
             Student s1 = new Student("xiaohei",23);
             Student s2 = new Student("dapang",22);
             Student s3 = new Student("xiaomei",22);
           
     		// 将学生对象添加到TreeMap集合中
             tm.put(s1,"江苏");
             tm.put(s2,"北京");
             tm.put(s3,"天津");
           
     		// 遍历TreeMap集合,打印每个学生的信息
             tm.forEach(
                     (Student key, String value)->{
                         System.out.println(key + "---" + value);
                     }
             );
         }
     }
     ```



## 3.可变参数

> 方法形参的个数可以改变。

- 格式

  ```Java
  类型 ...名字
  ```

- 注意：

  1. 方法的形参中最多只能有一个可变参数。
  2. 有其他形参，可变参数要写在最后。

- 举例

  ```java
  public static void main(String[] args) {
  
      System.out.println( getSum(1, 2, 3, 4, 5, 6, 7, 8, 9, 10));
  }
  
  public static int getSum(int ...args){
      int sum = 0;
      for (int i = 0; i < args.length; i++) {
          sum += args[i];
      }
      return sum;
  }
  ```





## 4.`collections`

- 概述：

  `java.utils.Collections`是集合工具类，用来对集合进行操作。

- 常用方法如下：

  1. `public static void shuffle(List<?> list) `:打乱集合顺序。
  2. `public static <T> void sort(List<T> list)`:将集合中元素按照默认规则排序。
  3. `public static <T> void sort(List<T> list，Comparator<? super T> )`:将集合中元素按照指定规则排序。

- 代码演示：

  ```java
  public class CollectionsDemo {
      public static void main(String[] args) {
          ArrayList<Integer> list = new ArrayList<Integer>();
     
          list.add(100);
          list.add(300);
          list.add(200);
          list.add(50);
          //排序方法 
          Collections.sort(list);
          System.out.println(list);
      }
  }
  结果：
  [50,100, 200, 300]
  ```

  



## 5.不可变集合

- 什么是不可变集合

  是一个长度不可变，内容也无法修改的集合

- 使用场景

  如果某个数据不能被修改，把它防御性地拷贝到不可变集合中是个很好的实践。

  当集合对象被不可信的库调用时，不可变形式是安全的。

- 不可变集合分类

  1. 不可变的list集合
  2. 不可变的set集合
  3. 不可变的map集合

### 1.不可变的`list`集合

```java
public class ImmutableDemo1 {
    public static void main(String[] args) {
        /*
            创建不可变的List集合
            "张三", "李四", "王五", "赵六"
        */

        //一旦创建完毕之后，是无法进行修改的，在下面的代码中，只能进行查询操作
        List<String> list = List.of("张三", "李四", "王五", "赵六");

        System.out.println(list.get(0));
        System.out.println(list.get(1));
        System.out.println(list.get(2));
        System.out.println(list.get(3));

        System.out.println("---------------------------");

        for (String s : list) {
            System.out.println(s);
        }

        System.out.println("---------------------------");


        Iterator<String> it = list.iterator();
        while(it.hasNext()){
            String s = it.next();
            System.out.println(s);
        }
        System.out.println("---------------------------");

        for (int i = 0; i < list.size(); i++) {
            String s = list.get(i);
            System.out.println(s);
        }
        System.out.println("---------------------------");

        //list.remove("李四");
        //list.add("aaa");
        list.set(0,"aaa");
    }
}
```



### 2.不可变的`Set`集合

```java
public class ImmutableDemo2 {
    public static void main(String[] args) {
        /*
           创建不可变的Set集合
           "张三", "李四", "王五", "赵六"


           细节：
                当我们要获取一个不可变的Set集合时，里面的参数一定要保证唯一性
        */

        //一旦创建完毕之后，是无法进行修改的，在下面的代码中，只能进行查询操作
        Set<String> set = Set.of("张三", "张三", "李四", "王五", "赵六");

        for (String s : set) {
            System.out.println(s);
        }

        System.out.println("-----------------------");

        Iterator<String> it = set.iterator();
        while(it.hasNext()){
            String s = it.next();
            System.out.println(s);
        }

        System.out.println("-----------------------");
        //set.remove("王五");
    }
}
```



### 3.不可变的`Map`集合

- 键值对个数小于等于10

  ```Java
  public class ImmutableDemo3 {
      public static void main(String[] args) {
         /*
          创建Map的不可变集合
              细节1：
                  键是不能重复的
              细节2：
                  Map里面的of方法，参数是有上限的，最多只能传递20个参数，10个键值对
              细节3：
                  如果我们要传递多个键值对对象，数量大于10个，在Map接口中还有一个方法
          */
  
          //一旦创建完毕之后，是无法进行修改的，在下面的代码中，只能进行查询操作
          Map<String, String> map = Map.of("张三", "南京", "张三", "北京", "王五", "上海",
                  "赵六", "广州", "孙七", "深圳", "周八", "杭州",
                  "吴九", "宁波", "郑十", "苏州", "刘一", "无锡",
                  "陈二", "嘉兴");
  
          Set<String> keys = map.keySet();
          for (String key : keys) {
              String value = map.get(key);
              System.out.println(key + "=" + value);
          }
  
          System.out.println("--------------------------");
  
          Set<Map.Entry<String, String>> entries = map.entrySet();
          for (Map.Entry<String, String> entry : entries) {
              String key = entry.getKey();
              String value = entry.getValue();
              System.out.println(key + "=" + value);
          }
          System.out.println("--------------------------");
      }
  }
  ```

- 键值对个数大于10

  ```java
  public class ImmutableDemo4 {
      public static void main(String[] args) {
  
          /*
              创建Map的不可变集合,键值对的数量超过10个
          */
  
          //1.创建一个普通的Map集合
          HashMap<String, String> hm = new HashMap<>();
          hm.put("张三", "南京");
          hm.put("李四", "北京");
          hm.put("王五", "上海");
          hm.put("赵六", "北京");
          hm.put("孙七", "深圳");
          hm.put("周八", "杭州");
          hm.put("吴九", "宁波");
          hm.put("郑十", "苏州");
          hm.put("刘一", "无锡");
          hm.put("陈二", "嘉兴");
          hm.put("aaa", "111");
  
          //2.利用上面的数据来获取一个不可变的集合
  /*
          //获取到所有的键值对对象（Entry对象）
          Set<Map.Entry<String, String>> entries = hm.entrySet();
          //把entries变成一个数组
          Map.Entry[] arr1 = new Map.Entry[0];
          //toArray方法在底层会比较集合的长度跟数组的长度两者的大小
          //如果集合的长度 > 数组的长度 ：数据在数组中放不下，此时会根据实际数据的个数，重新创建数组
          //如果集合的长度 <= 数组的长度：数据在数组中放的下，此时不会创建新的数组，而是直接用
          Map.Entry[] arr2 = entries.toArray(arr1);
          //不可变的map集合
          Map map = Map.ofEntries(arr2);
          map.put("bbb","222");*/
  
  
          //Map<Object, Object> map = Map.ofEntries(hm.entrySet().toArray(new Map.Entry[0]));
  
          Map<String, String> map = Map.copyOf(hm);
          map.put("bbb","222");
      }
  }
  ```





## 6.`Stream`流

- 体验Stream流

  1. 案例需求

     - 创建一个集合，存储多个字符串元素
     - 把集合中所有以"张"开头的元素存储到一个新的集合
     - 把"张"开头的集合中的长度为3的元素存储到一个新的集合
     - 遍历上一步得到的集合

  2. 原始方式示例代码

     ```java
     public class MyStream1 {
         public static void main(String[] args) {
             //集合的批量添加
             ArrayList<String> list1 = new ArrayList<>(List.of("张三丰","张无忌","张翠山","王二麻子","张良","谢广坤"));
             //list.add()
     
             //遍历list1把以张开头的元素添加到list2中。
             ArrayList<String> list2 = new ArrayList<>();
             for (String s : list1) {
                 if(s.startsWith("张")){
                     list2.add(s);
                 }
             }
             //遍历list2集合，把其中长度为3的元素，再添加到list3中。
             ArrayList<String> list3 = new ArrayList<>();
             for (String s : list2) {
                 if(s.length() == 3){
                     list3.add(s);
                 }
             }
             for (String s : list3) {
                 System.out.println(s);
             }      
         }
     }
     ```

  3. 使用Stream流示例代码

     ```java
     public class StreamDemo {
         public static void main(String[] args) {
             //集合的批量添加
             ArrayList<String> list1 = new ArrayList<>(List.of("张三丰","张无忌","张翠山","王二麻子","张良","谢广坤"));
     
             //Stream流
             list1.stream().filter(s->s.startsWith("张"))
                     .filter(s->s.length() == 3)
                     .forEach(s-> System.out.println(s));
         }
     }
     ```

  4. Stream流的好处

     - 直接阅读代码的字面意思即可完美展示无关逻辑方式的语义：获取流、过滤姓张、过滤长度为3、逐一打印
     - Stream流把真正的函数式编程风格引入到Java中
     - 代码简洁

- Stream流的常见生成方式

  1. Stream流的三类方法

     - 获取Stream流
       - 创建一条流水线,并把数据放到流水线上准备进行操作
     - 中间方法
       - 流水线上的操作
       - 一次操作完毕之后,还可以继续进行其他操作
     - 终结方法
       - 一个Stream流只能有一个终结方法
       - 是流水线上的最后一个操作

  2. 生成Stream流的方式

     - Collection体系集合

       使用默认方法stream()生成流， default Stream<E> stream()

     - Map体系集合

       把Map转成Set集合，间接的生成流

     - 数组

       通过Arrays中的静态方法stream生成流

     - 同种数据类型的多个数据

       通过Stream接口的静态方法of(T... values)生成流

  3. 代码演示

     ```java
     public class StreamDemo {
         public static void main(String[] args) {
             //Collection体系的集合可以使用默认方法stream()生成流
             List<String> list = new ArrayList<String>();
             Stream<String> listStream = list.stream();
     
             Set<String> set = new HashSet<String>();
             Stream<String> setStream = set.stream();
     
             //Map体系的集合间接的生成流
             Map<String,Integer> map = new HashMap<String, Integer>();
             Stream<String> keyStream = map.keySet().stream();
             Stream<Integer> valueStream = map.values().stream();
             Stream<Map.Entry<String, Integer>> entryStream = map.entrySet().stream();
     
             //数组可以通过Arrays中的静态方法stream生成流
             String[] strArray = {"hello","world","java"};
             Stream<String> strArrayStream = Arrays.stream(strArray);
           
           	//同种数据类型的多个数据可以通过Stream接口的静态方法of(T... values)生成流
             Stream<String> strArrayStream2 = Stream.of("hello", "world", "java");
             Stream<Integer> intStream = Stream.of(10, 20, 30);
         }
     }
     ```

- Stream流中间操作方法

  1. 概念

     中间操作的意思是,执行完此方法之后,Stream流依然可以继续执行其他操作

  2. 常见方法

     | 方法名                                          | 说明                                                       |
     | ----------------------------------------------- | ---------------------------------------------------------- |
     | Stream<T> filter(Predicate predicate)           | 用于对流中的数据进行过滤                                   |
     | Stream<T> limit(long maxSize)                   | 返回此流中的元素组成的流，截取前指定参数个数的数据         |
     | Stream<T> skip(long n)                          | 跳过指定参数个数的数据，返回由该流的剩余元素组成的流       |
     | static <T> Stream<T> concat(Stream a, Stream b) | 合并a和b两个流为一个流                                     |
     | Stream<T> distinct()                            | 返回由该流的不同元素（根据Object.equals(Object) ）组成的流 |

  3. filter代码演示

     ```java
     public class MyStream3 {
         public static void main(String[] args) {
     //        Stream<T> filter(Predicate predicate)：过滤
     //        Predicate接口中的方法	boolean test(T t)：对给定的参数进行判断，返回一个布尔值
     
             ArrayList<String> list = new ArrayList<>();
             list.add("张三丰");
             list.add("张无忌");
             list.add("张翠山");
             list.add("王二麻子");
             list.add("张良");
             list.add("谢广坤");
     
             //filter方法获取流中的 每一个数据.
             //而test方法中的s,就依次表示流中的每一个数据.
             //我们只要在test方法中对s进行判断就可以了.
             //如果判断的结果为true,则当前的数据留下
             //如果判断的结果为false,则当前数据就不要.
     //        list.stream().filter(
     //                new Predicate<String>() {
     //                    @Override
     //                    public boolean test(String s) {
     //                        boolean result = s.startsWith("张");
     //                        return result;
     //                    }
     //                }
     //        ).forEach(s-> System.out.println(s));
     
             //因为Predicate接口中只有一个抽象方法test
             //所以我们可以使用lambda表达式来简化
     //        list.stream().filter(
     //                (String s)->{
     //                    boolean result = s.startsWith("张");
     //                        return result;
     //                }
     //        ).forEach(s-> System.out.println(s));
     
             list.stream().filter(s ->s.startsWith("张")).forEach(s-> System.out.println(s));
     
         }
     }
     ```

  4. limit&skip代码演示

     ```java
     public class StreamDemo02 {
         public static void main(String[] args) {
             //创建一个集合，存储多个字符串元素
             ArrayList<String> list = new ArrayList<String>();
     
             list.add("林青霞");
             list.add("张曼玉");
             list.add("王祖贤");
             list.add("柳岩");
             list.add("张敏");
             list.add("张无忌");
     
             //需求1：取前3个数据在控制台输出
             list.stream().limit(3)
                 .forEach(s-> System.out.println(s));
             System.out.println("--------");
     
             //需求2：跳过3个元素，把剩下的元素在控制台输出
             list.stream().skip(3)
                 .forEach(s-> System.out.println(s));
             System.out.println("--------");
     
             //需求3：跳过2个元素，把剩下的元素中前2个在控制台输出
             list.stream().skip(2).limit(2).forEach(s-> System.out.println(s));
         }
     }
     ```

  5. concat&distinct代码演示
  
     ```java
     public class StreamDemo03 {
         public static void main(String[] args) {
             //创建一个集合，存储多个字符串元素
             ArrayList<String> list = new ArrayList<String>();
     
             list.add("林青霞");
             list.add("张曼玉");
             list.add("王祖贤");
             list.add("柳岩");
             list.add("张敏");
             list.add("张无忌");
     
             //需求1：取前4个数据组成一个流
             Stream<String> s1 = list.stream().limit(4);
     
             //需求2：跳过2个数据组成一个流
             Stream<String> s2 = list.stream().skip(2);
     
             //需求3：合并需求1和需求2得到的流，并把结果在控制台输出
     //        Stream.concat(s1,s2).forEach(s-> System.out.println(s));
     
             //需求4：合并需求1和需求2得到的流，并把结果在控制台输出，要求字符串元素不能重复
             Stream.concat(s1,s2).distinct().forEach(s-> System.out.println(s));
         }
     }
     ```


- Stream流终结操作方法

  1. 概念

    终结操作的意思是,执行完此方法之后,Stream流将不能再执行其他操作

  2. 常见方法

    | 方法名                        | 说明                     |
    | ----------------------------- | ------------------------ |
    | void forEach(Consumer action) | 对此流的每个元素执行操作 |
    | long count()                  | 返回此流中的元素数       |

  3. 代码演示

    ```java
    public class MyStream5 {
        public static void main(String[] args) {
            ArrayList<String> list = new ArrayList<>();
            list.add("张三丰");
            list.add("张无忌");
            list.add("张翠山");
            list.add("王二麻子");
            list.add("张良");
            list.add("谢广坤");
    
            //method1(list);
            
    //        long count()：返回此流中的元素数
            long count = list.stream().count();
            System.out.println(count);
        }
    
        private static void method1(ArrayList<String> list) {
            //  void forEach(Consumer action)：对此流的每个元素执行操作
            //  Consumer接口中的方法void accept(T t)：对给定的参数执行此操作
            //在forEach方法的底层,会循环获取到流中的每一个数据.
            //并循环调用accept方法,并把每一个数据传递给accept方法
            //s就依次表示了流中的每一个数据.
            //所以,我们只要在accept方法中,写上处理的业务逻辑就可以了.
            list.stream().forEach(
                    new Consumer<String>() {
                        @Override
                        public void accept(String s) {
                            System.out.println(s);
                        }
                    }
            );
          
            System.out.println("====================");
            //lambda表达式的简化格式
            //是因为Consumer接口中,只有一个accept方法
            list.stream().forEach(
                    (String s)->{
                        System.out.println(s);
                    }
            );
            System.out.println("====================");
            //lambda表达式还是可以进一步简化的.
            list.stream().forEach(s->System.out.println(s));
        }
    }
    ```


- Stream流的收集操作

  1. 概念

    对数据使用Stream流的方式操作完毕后,可以把流中的数据收集到集合中

  2. 常用方法

    | 方法名                         | 说明               |
    | ------------------------------ | ------------------ |
    | R collect(Collector collector) | 把结果收集到集合中 |

  3. 工具类Collectors提供了具体的收集方式

    | 方法名                                                       | 说明                   |
    | ------------------------------------------------------------ | ---------------------- |
    | public static <T> Collector toList()                         | 把元素收集到List集合中 |
    | public static <T> Collector toSet()                          | 把元素收集到Set集合中  |
    | public static  Collector toMap(Function keyMapper,Function valueMapper) | 把元素收集到Map集合中  |

  4. 代码演示

    ```java
    // toList和toSet方法演示 
    public class MyStream7 {
        public static void main(String[] args) {
            ArrayList<Integer> list1 = new ArrayList<>();
            for (int i = 1; i <= 10; i++) {
                list1.add(i);
            }
    
            list1.add(10);
            list1.add(10);
            list1.add(10);
            list1.add(10);
            list1.add(10);
    
            //filter负责过滤数据的.
            //collect负责收集数据.
                    //获取流中剩余的数据,但是他不负责创建容器,也不负责把数据添加到容器中.
            //Collectors.toList() : 在底层会创建一个List集合.并把所有的数据添加到List集合中.
            List<Integer> list = list1.stream().filter(number -> number % 2 == 0)
                    .collect(Collectors.toList());
    
            System.out.println(list);
    
        Set<Integer> set = list1.stream().filter(number -> number % 2 == 0)
                .collect(Collectors.toSet());
        System.out.println(set);
    }
    }
    /**
    Stream流的收集方法 toMap方法演示
    创建一个ArrayList集合，并添加以下字符串。字符串中前面是姓名，后面是年龄
    "zhangsan,23"
    "lisi,24"
    "wangwu,25"
    保留年龄大于等于24岁的人，并将结果收集到Map集合中，姓名为键，年龄为值
    */
    public class MyStream8 {
    	public static void main(String[] args) {
          	ArrayList<String> list = new ArrayList<>();
            list.add("zhangsan,23");
            list.add("lisi,24");
            list.add("wangwu,25");
    
            Map<String, Integer> map = list.stream().filter(
                    s -> {
                        String[] split = s.split(",");
                        int age = Integer.parseInt(split[1]);
                        return age >= 24;
                    }
    
             //   collect方法只能获取到流中剩余的每一个数据.
             //在底层不能创建容器,也不能把数据添加到容器当中
    
             //Collectors.toMap 创建一个map集合并将数据添加到集合当中
    
              // s 依次表示流中的每一个数据
    
              //第一个lambda表达式就是如何获取到Map中的键
              //第二个lambda表达式就是如何获取Map中的值
            ).collect(Collectors.toMap(
                    s -> s.split(",")[0],
                    s -> Integer.parseInt(s.split(",")[1]) ));
    
            System.out.println(map);
    	}
    }
    ```


- Stream流综合练习

  1. 案例需求

    现在有两个ArrayList集合，分别存储6名男演员名称和6名女演员名称，要求完成如下的操作

    - 男演员只要名字为3个字的前三人
    - 女演员只要姓林的，并且不要第一个
    - 把过滤后的男演员姓名和女演员姓名合并到一起
    - 把上一步操作后的元素作为构造方法的参数创建演员对象,遍历数据

    演员类Actor已经提供，里面有一个成员变量，一个带参构造方法，以及成员变量对应的get/set方法

  2. 代码实现

    演员类

    ```java
    public class Actor {
        private String name;
    
        public Actor(String name) {
            this.name = name;
        }
    
        public String getName() {
            return name;
        }
    
        public void setName(String name) {
            this.name = name;
        }
    }
    ```

    测试类

    ```java
    public class StreamTest {
        public static void main(String[] args) {
            //创建集合
            ArrayList<String> manList = new ArrayList<String>();
            manList.add("周润发");
            manList.add("成龙");
            manList.add("刘德华");
            manList.add("吴京");
            manList.add("周星驰");
            manList.add("李连杰");
      
            ArrayList<String> womanList = new ArrayList<String>();
            womanList.add("林心如");
            womanList.add("张曼玉");
            womanList.add("林青霞");
            womanList.add("柳岩");
            womanList.add("林志玲");
            womanList.add("王祖贤");
      
            //男演员只要名字为3个字的前三人
            Stream<String> manStream = manList.stream().filter(s -> s.length() == 3).limit(3);
      
            //女演员只要姓林的，并且不要第一个
            Stream<String> womanStream = womanList.stream().filter(s -> s.startsWith("林")).skip(1);
      
            //把过滤后的男演员姓名和女演员姓名合并到一起
            Stream<String> stream = Stream.concat(manStream, womanStream);
      
          	// 将流中的数据封装成Actor对象之后打印
          	stream.forEach(name -> {
                Actor actor = new Actor(name);
                System.out.println(actor);
            }); 
        }
    }
    ```



## 7.方法引用

- 方法引用的使用

  1. 方法引用条件

     - 引用处需要是函数式接口。
     - 被引用的方法需要已经存在。
     - 被引用方法的形参和返回值需要跟抽象方法的形参和返回值保持一致。
     - 被引用方法的功能需要满足当前的要求。

  2. 代码演示

     ```java
     public interface Printable {
         void printString(String s);
     }
     
     public class PrintableDemo {
         public static void main(String[] args) {
             //在主方法中调用usePrintable方法
     //        usePrintable((String s) -> {
     //            System.out.println(s);
     //        });
     	    //Lambda简化写法
             usePrintable(s -> System.out.println(s));
     
             //方法引用
             usePrintable(System.out::println);
     
         }
     
         private static void usePrintable(Printable p) {
             p.printString("爱生活爱Java");
         }
     }
     
     ```

- 方法引用符

  1. 方法引用符

     ::  该符号为引用运算符，而它所在的表达式被称为方法引用

     ```java
     类名：：静态方法
     ```

  2. 推导与省略

     - 如果使用Lambda，那么根据“可推导就是可省略”的原则，无需指定参数类型，也无需指定的重载形式，它们都将被自动推导
     - 如果使用方法引用，也是同样可以根据上下文进行推导
     - 方法引用是Lambda的孪生兄弟
  
- 引用类方法

  引用类方法，其实就是引用类的静态方法

  1. 格式

     ```java
     类名::静态方法
     ```

  2. 范例

     Integer::parseInt

     Integer类的方法：public static int parseInt(String s) 将此String转换为int类型数据

  3. 练习描述

     - 定义一个接口(Converter)，里面定义一个抽象方法 int convert(String s);
     - 定义一个测试类(ConverterDemo)，在测试类中提供两个方法
       - 一个方法是：useConverter(Converter c)
       - 一个方法是主方法，在主方法中调用useConverter方法

  4. 代码演示

     ```java
     public interface Converter {
         int convert(String s);
     }
     
     public class ConverterDemo {
         public static void main(String[] args) {
     
     		//Lambda写法
             useConverter(s -> Integer.parseInt(s));
     
             //引用类方法
             useConverter(Integer::parseInt);
     
         }
     
         private static void useConverter(Converter c) {
             int number = c.convert("666");
             System.out.println(number);
         }
     }
     ```

  5. 使用说明

     Lambda表达式被类方法替代的时候，它的形式参数全部传递给静态方法作为参数

- 引用对象的实例方法

  引用对象的实例方法，其实就引用类中的成员方法

  1. 格式

     ```java
     对象::成员方法
     ```

  2. 范例

     "HelloWorld"::toUpperCase

       String类中的方法：public String toUpperCase() 将此String所有字符转换为大写

  3. 练习描述

     - 定义一个类(PrintString)，里面定义一个方法

       public void printUpper(String s)：把字符串参数变成大写的数据，然后在控制台输出

     - 定义一个接口(Printer)，里面定义一个抽象方法

       void printUpperCase(String s)

     - 定义一个测试类(PrinterDemo)，在测试类中提供两个方法

       - 一个方法是：usePrinter(Printer p)
       - 一个方法是主方法，在主方法中调用usePrinter方法

  4. 代码演示

     ```java
     public class PrintString {
         //把字符串参数变成大写的数据，然后在控制台输出
         public void printUpper(String s) {
             String result = s.toUpperCase();
             System.out.println(result);
         }
     }
     
     public interface Printer {
         void printUpperCase(String s);
     }
     
     public class PrinterDemo {
         public static void main(String[] args) {
     
     		//Lambda简化写法
             usePrinter(s -> System.out.println(s.toUpperCase()));
     
             //引用对象的实例方法
             PrintString ps = new PrintString();
             usePrinter(ps::printUpper);
     
         }
     
         private static void usePrinter(Printer p) {
             p.printUpperCase("HelloWorld");
         }
     }
     
     ```

  5. 使用说明

     Lambda表达式被对象的实例方法替代的时候，它的形式参数全部传递给该方法作为参数

- 引用类的实例方法

  引用类的实例方法，其实就是引用类中的成员方法

  1. 格式

     类名::成员方法

  2. 范例

     String::substring

     public String substring(int beginIndex,int endIndex) 

     从beginIndex开始到endIndex结束，截取字符串。返回一个子串，子串的长度为endIndex-beginIndex

  3. 练习描述

     - 定义一个接口(MyString)，里面定义一个抽象方法：

       String mySubString(String s,int x,int y);

     - 定义一个测试类(MyStringDemo)，在测试类中提供两个方法

       - 一个方法是：useMyString(MyString my)
       - 一个方法是主方法，在主方法中调用useMyString方法

  4. 代码演示

     ```java
     public interface MyString {
         String mySubString(String s,int x,int y);
     }
     
     public class MyStringDemo {
         public static void main(String[] args) {
     		//Lambda简化写法
             useMyString((s,x,y) -> s.substring(x,y));
     
             //引用类的实例方法
             useMyString(String::substring);
     
         }
     
         private static void useMyString(MyString my) {
             String s = my.mySubString("HelloWorld", 2, 5);
             System.out.println(s);
         }
     }
     ```

  5. 使用说明

     Lambda表达式被类的实例方法替代的时候
     ​第一个参数作为调用者
     ​后面的参数全部传递给该方法作为参数

- 引用构造器

  引用构造器，其实就是引用构造方法

  1. l格式

     ```java
     类名::new
     ```

  2. 范例

     Student::new

  3. 练习描述

     - 定义一个类(Student)，里面有两个成员变量(name,age)

       并提供无参构造方法和带参构造方法，以及成员变量对应的get和set方法

     - 定义一个接口(StudentBuilder)，里面定义一个抽象方法

       Student build(String name,int age);

     - 定义一个测试类(StudentDemo)，在测试类中提供两个方法

       - 一个方法是：useStudentBuilder(StudentBuilder s)
       - 一个方法是主方法，在主方法中调用useStudentBuilder方法

  4. 代码演示

     ```java
     public class Student {
         private String name;
         private int age;
     
         public Student() {
         }
     
         public Student(String name, int age) {
             this.name = name;
             this.age = age;
         }
     
         public String getName() {
             return name;
         }
     
         public void setName(String name) {
             this.name = name;
         }
     
         public int getAge() {
             return age;
         }
     
         public void setAge(int age) {
             this.age = age;
         }
     }
     
     public interface StudentBuilder {
         Student build(String name,int age);
     }
     
     public class StudentDemo {
         public static void main(String[] args) {
     
     		//Lambda简化写法
             useStudentBuilder((name,age) -> new Student(name,age));
     
             //引用构造器
             useStudentBuilder(Student::new);
     
         }
     
         private static void useStudentBuilder(StudentBuilder sb) {
             Student s = sb.build("林青霞", 30);
             System.out.println(s.getName() + "," + s.getAge());
         }
     }
     ```

  5. 使用说明

     Lambda表达式被构造器替代的时候，它的形式参数全部传递给构造器作为参数





# 15.`IO`

## 1. 异常

### 1.概念

- 异常概念

  **异常** ：指的是程序在执行过程中，出现的非正常的情况，最终会导致JVM的非正常停止。

  在Java等面向对象编程语言，异常本身是一个类，产生异常会创建异常对象并抛出一个异常对象。Java处理异常的方式是中断处理。

  > 异常指的并不是语法错误,语法出错,编译不通过,不会产生字节码文件,根本不能运行.

- 异常体系

  1. 异常机制其实是帮助**找到**程序中的问题，异常的根类是`java.lang.Throwable`：

     其下有两个子类：`java.lang.Error`与`java.lang.Exception`，平常所说的异常指`java.lang.Exception`。

     ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/010.png?raw=true)

  2. **Throwable体系：**

     * **Error**:严重错误Error，无法通过处理的错误，只能事先避免。
     * **Exception**:表示异常，异常产生后程序员可以通过代码的方式纠正，使程序继续运行，是必须要处理的。

  3. **Throwable中的常用方法：**

     * `public void printStackTrace()`:打印异常的详细信息。

       *包含了异常的类型,异常的原因,还包括异常出现的位置,在开发和调试阶段,都得使用printStackTrace。*

     * `public String getMessage()`:获取发生异常的原因。

       *提示给用户的时候,就提示错误原因。*

     * `public String toString()`:获取异常的类型和异常描述信息(不用)。

- 异常分类

  平常异常就是指Exception，因为这类异常一旦出现，要对代码进行更正，修复程序。

  **异常(Exception)的分类**:根据在编译时期还是运行时期去检查异常?

  * **编译时期异常**:checked异常。在编译时期,就会检查,如果没有处理异常,则编译失败。(如日期格式化异常)
  * **运行时期异常**:runtime异常。在运行时期,检查异常.在编译时期,运行异常不会编译器检测(不报错)。(如数学异常)

     ![001](https://cdn.jsdelivr.net/gh/silent-wuhen/Blog_picture01/H03_其他/2.java/2.java基础/011.png?raw=true)



### 2.抛出异常throw

> 编写程序时，需要考虑程序出现问题的情况。如，在定义方法时，方法需要接受参数，当调用方法使用接受到的参数时，首先需要先对参数数据进行合法的判断，数据若不合法，就应该告诉调用者，传递合法的数据进来。这时需要使用抛出异常的方式来告诉调用者。

- **throw**关键字，用来抛出一个指定的异常对象。

  1. 创建一个异常对象。封装一些提示信息(信息可以自己编写)。

  2. 需要将这个异常对象告知给调用者。throw 异常对象。

     throw**用在方法内**，用来抛出一个异常对象，将这个异常对象传递到调用者处，并结束当前方法的执行。

- **使用格式：**

  ```
  throw new 异常类名(参数);
  ```

   例如：

  ```java
  throw new NullPointerException("要访问的arr数组不存在");
  
  throw new ArrayIndexOutOfBoundsException("该索引在数组中不存在，已超出范围");。
  ```

  ```java
  public class ThrowDemo {
      public static void main(String[] args) {
          //创建一个数组 
          int[] arr = {2,4,52,2};
          //根据索引找对应的元素 
          int index = 4;
          int element = getElement(arr, index);
  
          System.out.println(element);
          System.out.println("over");
      }
      /*
       * 根据 索引找到数组中对应的元素
       */
      public static int getElement(int[] arr,int index){ 
         	//判断  索引是否越界
          if(index<0 || index>arr.length-1){
               /*
               判断条件如果满足，当执行完throw抛出异常对象后，方法已经无法继续运算。
               这时就会结束当前方法的执行，并将异常告知给调用者。这时就需要通过异常来解决。 
                */
               throw new ArrayIndexOutOfBoundsException("哥们，角标越界了```");
          }
          int element = arr[index];
          return element;
      }
  }
  ```

  > 注意：如果产生了问题，我们就会throw将问题描述类即异常进行抛出，也就是将问题返回给该方法的调用者。
  >
  > 处理方式：一种是进行捕获处理，另一种就是继续讲问题声明出去，使用throws声明处理。

  

### 3.声明异常throws

- **声明异常**：将问题标识出来，报告给调用者。如果方法内通过throw抛出了编译时异常，而没有捕获处理，那么必须通过throws进行声明，让调用者去处理。

  关键字**throws**运用于方法声明之上,用于表示当前方法不处理异常,而是提醒该方法的调用者来处理异常(抛出异常).

- **声明异常格式：**

  ```
  修饰符 返回值类型 方法名(参数) throws 异常类名1,异常类名2…{   }	
  ```

  声明异常的代码演示：

  ```java
  public class ThrowsDemo {
      public static void main(String[] args) throws FileNotFoundException {
          read("a.txt");
      }
  
      // 如果定义功能时有问题发生需要报告给调用者。可以通过在方法上使用throws关键字进行声明
      public static void read(String path) throws FileNotFoundException {
          if (!path.equals("a.txt")) {//如果不是 a.txt这个文件 
              // 我假设  如果不是 a.txt 认为 该文件不存在 是一个错误 也就是异常  throw
              throw new FileNotFoundException("文件不存在");
          }
      }
  }
  ```

  throws用于进行异常类的声明，若该方法可能有多种异常情况产生，那么在throws后面可以写多个异常类，用逗号隔开。

  ```java
  public class ThrowsDemo2 {
      public static void main(String[] args) throws IOException {
          read("a.txt");
      }
  
      public static void read(String path)throws FileNotFoundException, IOException {
          if (!path.equals("a.txt")) {//如果不是 a.txt这个文件 
              // 我假设  如果不是 a.txt 认为 该文件不存在 是一个错误 也就是异常  throw
              throw new FileNotFoundException("文件不存在");
          }
          if (!path.equals("b.txt")) {
              throw new IOException();
          }
      }
  }
  ```



### 4.捕获异常try…catch...finally

> 如果异常出现的话,会立刻终止程序,所以得处理异常:
>
> 1. 方法不处理,而是声明抛出,由该方法的调用者来处理(throws)。
> 2. 在方法中使用try-catch的语句块来处理异常。

- **try-catch**的方式就是捕获异常。

  1. **捕获异常**：Java中对异常有针对性的语句进行捕获，可以对出现的异常进行指定方式的处理。

     捕获异常语法：

     ```java
     try{
          编写可能会出现异常的代码
     }catch(异常类型  e){
          处理异常的代码
          //记录日志/打印异常信息/继续抛出异常
     }
     ```

     **try：**该代码块中编写可能产生异常的代码。

     **catch：**用来进行某种异常的捕获，实现对捕获到的异常进行处理。

     > 注意:try和catch都不能单独使用,必须连用。


* 演示如下：

  ```java
  public class TryCatchDemo {
      public static void main(String[] args) {
          try {// 当产生异常时，必须有处理方式。要么捕获，要么声明。
              read("b.txt");
          } catch (FileNotFoundException e) {// 括号中需要定义什么呢？
            	//try中抛出的是什么异常，在括号中就定义什么异常类型
              System.out.println(e);
          }
          System.out.println("over");
      }
      /*
       *
       * 我们 当前的这个方法中 有异常  有编译期异常
       */
      public static void read(String path) throws FileNotFoundException {
          if (!path.equals("a.txt")) {//如果不是 a.txt这个文件 
              // 我假设  如果不是 a.txt 认为 该文件不存在 是一个错误 也就是异常  throw
              throw new FileNotFoundException("文件不存在");
          }
      }
  }
  ```

* 如何获取异常信息：

  1. Throwable类中定义了一些查看方法:

     * `public String getMessage()`:获取异常的描述信息,原因(提示给用户的时候,就提示错误原因。


     * `public String toString()`:获取异常的类型和异常描述信息(不用)。
    
     * `public void printStackTrace()`:打印异常的跟踪栈信息并输出到控制台。
    
       *包含了异常的类型,异常的原因,还包括异常出现的位置,在开发和调试阶段,都得使用printStackTrace。*

  2. 在catch将编译期异常转换成运行期异常处理。

     多个异常使用捕获处理:

     1. 多个异常分别处理。
     2. 多个异常一次捕获，多次处理。
     3. 多个异常一次捕获一次处理。

     ```java
     try{
          编写可能会出现异常的代码
     }catch(异常类型A  e){  当try中出现A类型异常,就用该catch来捕获.
          处理异常的代码
          //记录日志/打印异常信息/继续抛出异常
     }catch(异常类型B  e){  当try中出现B类型异常,就用该catch来捕获.
          处理异常的代码
          //记录日志/打印异常信息/继续抛出异常
     }
     ```

     > 注意:这种异常处理方式，要求多个catch中的异常不能相同，并且若catch中的多个异常之间有子父类异常的关系，那么子类异常要求在上面的catch处理，父类异常在下面的catch处理。

* **finally**：

  在finally代码块中存放的代码都是一定会被执行的。

  ```java
  public class TryCatchDemo4 {
      public static void main(String[] args) {
          try {
              read("a.txt");
          } catch (FileNotFoundException e) {
              //抓取到的是编译期异常  抛出去的是运行期 
              throw new RuntimeException(e);
          } finally {
              System.out.println("不管程序怎样，这里都将会被执行。");
          }
          System.out.println("over");
      }
      /*
       *
       * 我们 当前的这个方法中 有异常  有编译期异常
       */
      public static void read(String path) throws FileNotFoundException {
          if (!path.equals("a.txt")) {//如果不是 a.txt这个文件 
              // 我假设  如果不是 a.txt 认为 该文件不存在 是一个错误 也就是异常  throw
              throw new FileNotFoundException("文件不存在");
          }
      }
  }
  ```

  > 当只有在try或者catch中调用退出JVM的相关方法,此时finally才不会执行,否则finally永远会执行。

* 异常注意事项

  1. 运行时异常被抛出可以不处理。即不捕获也不声明抛出。
  2. 如果父类抛出了多个异常,子类覆盖父类方法时,只能抛出相同的异常或者是他的子集。
  3. 父类方法没有抛出异常，子类覆盖父类该方法时也不可抛出异常。此时子类产生该异常，只能捕获处理，不能声明抛出
  4. 当多异常处理时，捕获处理，前边的类不能是后边类的父类
  5. 在try/catch后可以追加finally代码块，其中的代码一定会被执行，通常用于资源回收。

### 5.自定义异常类

- **自定义异常类:**

  在开发中根据自己业务的异常情况来定义异常类.

  自定义一个业务逻辑异常: **LoginException**。一个登陆异常类。

- **异常类如何定义:**

  1. 自定义一个编译期异常: 自定义类 并继承于`java.lang.Exception`。
  2. 自定义一个运行时期的异常类:自定义类 并继承于`java.lang.RuntimeException`。

- 自定义异常的练习

  要求：我们模拟登陆操作，如果用户名已存在，则抛出异常并提示：亲，该用户名已经被注册。

  首先定义一个登陆异常类LoginException：

  ```java
  // 业务逻辑异常
  public class LoginException extends Exception {
      /**
       * 空参构造
       */
      public LoginException() {
      }
  
      /**
       *
       * @param message 表示异常提示
       */
      public LoginException(String message) {
          super(message);
      }
  }
  ```

  模拟登陆操作，使用数组模拟数据库中存储的数据，并提供当前注册账号是否存在方法用于判断。

  ```java
  public class Demo {
      // 模拟数据库中已存在账号
      private static String[] names = {"bill","hill","jill"};
     
      public static void main(String[] args) {     
          //调用方法
          try{
              // 可能出现异常的代码
              checkUsername("nill");
              System.out.println("注册成功");//如果没有异常就是注册成功
          } catch(LoginException e) {
              //处理异常
              e.printStackTrace();
          }
      }
  
      //判断当前注册账号是否存在
      //因为是编译期异常，又想调用者去处理 所以声明该异常
      public static boolean checkUsername(String uname) throws LoginException {
          for (String name : names) {
              if(name.equals(uname)){//如果名字在这里面 就抛出登陆异常
                  throw new LoginException("亲"+name+"已经被注册了！");
              }
          }
          return true;
      }
  }
  ```




## 2. File类

>`java.io.File` 类是文件和目录路径名的抽象表示，主要用于文件和目录的创建、查找和删除等操作。

- 构造方法

  1. `public File(String pathname) ` ：通过将给定的**路径名字符串**转换为抽象路径名来创建新的 File实例。  
  2. `public File(String parent, String child) ` ：从**父路径名字符串和子路径名字符串**创建新的 File实例。
  3. `public File(File parent, String child)` ：从**父抽象路径名和子路径名字符串**创建新的 File实例。 

- 构造举例，代码如下：

  ```java
  // 文件路径名
  String pathname = "D:\\aaa.txt";
  File file1 = new File(pathname); 
  
  // 文件路径名
  String pathname2 = "D:\\aaa\\bbb.txt";
  File file2 = new File(pathname2); 
  
  // 通过父路径和子路径字符串
   String parent = "d:\\aaa";
   String child = "bbb.txt";
   File file3 = new File(parent, child);
  
  // 通过父级File对象和子路径字符串
  File parentDir = new File("d:\\aaa");
  String child = "bbb.txt";
  File file4 = new File(parentDir, child);
  ```

  > 注：
  >
  > 1. 一个File对象代表硬盘中实际存在的一个文件或者目录。
  > 2. 无论该路径下是否存在文件或者目录，都不影响File对象的创建。



### 1.常用方法

- 获取功能的方法

  1. `public String getAbsolutePath() ` ：返回此File的绝对路径名字符串。
  2. ` public String getPath() ` ：将此File转换为路径名字符串。 

  3. `public String getName()`  ：返回由此File表示的文件或目录的名称。  

  4. `public long length()`  ：返回由此File表示的文件的长度。 

  方法演示，代码如下：

  ```java
  public class FileGet {
      public static void main(String[] args) {
          File f = new File("d:/aaa/bbb.java");     
          System.out.println("文件绝对路径:"+f.getAbsolutePath());
          System.out.println("文件构造路径:"+f.getPath());
          System.out.println("文件名称:"+f.getName());
          System.out.println("文件长度:"+f.length()+"字节");
  
          File f2 = new File("d:/aaa");     
          System.out.println("目录绝对路径:"+f2.getAbsolutePath());
          System.out.println("目录构造路径:"+f2.getPath());
          System.out.println("目录名称:"+f2.getName());
          System.out.println("目录长度:"+f2.length());
      }
  }
  输出结果：
  文件绝对路径:d:\aaa\bbb.java
  文件构造路径:d:\aaa\bbb.java
  文件名称:bbb.java
  文件长度:636字节
  
  目录绝对路径:d:\aaa
  目录构造路径:d:\aaa
  目录名称:aaa
  目录长度:4096
  ```

  > API中说明：length()，表示文件的长度。但是File对象表示目录，则返回值未指定。

- 绝对路径和相对路径

  1. **绝对路径**：从盘符开始的路径，这是一个完整的路径。
  2. **相对路径**：相对于项目目录的路径，这是一个便捷的路径，开发中经常使用。

- 判断功能的方法

  1. `public boolean exists()` ：此File表示的文件或目录是否实际存在。
  2. `public boolean isDirectory()` ：此File表示的是否为目录。
  3. `public boolean isFile()` ：此File表示的是否为文件。

  ```java
  public class FileIs {
      public static void main(String[] args) {
          File f = new File("d:\\aaa\\bbb.java");
          File f2 = new File("d:\\aaa");
        	// 判断是否存在
          System.out.println("d:\\aaa\\bbb.java 是否存在:"+f.exists());
          System.out.println("d:\\aaa 是否存在:"+f2.exists());
        	// 判断是文件还是目录
          System.out.println("d:\\aaa 文件?:"+f2.isFile());
          System.out.println("d:\\aaa 目录?:"+f2.isDirectory());
      }
  }
  输出结果：
  d:\aaa\bbb.java 是否存在:true
  d:\aaa 是否存在:true
  d:\aaa 文件?:false
  d:\aaa 目录?:true
  ```


- 创建删除功能的方法

  1. `public boolean createNewFile()` ：当且仅当具有该名称的文件尚不存在时，创建一个新的空文件。 
  2. `public boolean delete()` ：删除由此File表示的文件或目录。  
  3. `public boolean mkdir()` ：创建由此File表示的目录。
  4. `public boolean mkdirs()` ：创建由此File表示的目录，包括任何必需但不存在的父目录。

  ```java
  public class FileCreateDelete {
      public static void main(String[] args) throws IOException {
          // 文件的创建
          File f = new File("aaa.txt");
          System.out.println("是否存在:"+f.exists()); // false
          System.out.println("是否创建:"+f.createNewFile()); // true
          System.out.println("是否存在:"+f.exists()); // true
  		
       	// 目录的创建
        	File f2= new File("newDir");	
          System.out.println("是否存在:"+f2.exists());// false
          System.out.println("是否创建:"+f2.mkdir());	// true
          System.out.println("是否存在:"+f2.exists());// true
  
  		// 创建多级目录
        	File f3= new File("newDira\\newDirb");
          System.out.println(f3.mkdir());// false
          File f4= new File("newDira\\newDirb");
          System.out.println(f4.mkdirs());// true
        
        	// 文件的删除
         	System.out.println(f.delete());// true
        
        	// 目录的删除
          System.out.println(f2.delete());// true
          System.out.println(f4.delete());// false
      }
  }
  ```

  > API中说明：delete方法，如果此File表示目录，则目录必须为空才能删除。



### 2.目录的遍历

- `public String[] list()` ：返回一个String数组，表示该File目录中的所有子文件或目录。
- `public File[] listFiles()` ：返回一个File数组，表示该File目录中的所有的子文件或目录。  

```java
public class FileFor {
    public static void main(String[] args) {
        File dir = new File("d:\\java_code");
      
      	//获取当前目录下的文件以及文件夹的名称。
		String[] names = dir.list();
		for(String name : names){
			System.out.println(name);
		}
        //获取当前目录下的文件以及文件夹对象，只要拿到了文件对象，那么就可以获取更多信息
        File[] files = dir.listFiles();
        for (File file : files) {
            System.out.println(file);
        }
    }
}
```

> 小贴士：
>
> 调用listFiles方法的File对象，表示的必须是实际存在的目录，否则返回null，无法进行遍历。





## 3.`IO`流

