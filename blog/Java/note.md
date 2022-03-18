# Java 学习笔记

———————————————————————————

# Java学习笔记-1 主类结构

```java
public class hello {
    public static void main(String[] args) {
        String s1 = "hello"; //定义变量字符值
        String s2 = "Java";
        String s3 = "is sooooooo hard";

        System.out.println(s1);
        System.out.println(s2);
        System.out.println(s3);
    }
}
```

- 开始需定义public 类(class)

[!Note]class 不等同于Class (严格区分大小写)

- public class 定义初始类, 继续class可继续定义新类
```java
public static void main 
```
- 定义类: main 
- 括号后面的内容进行内容定义(args)
- double(用处不明)
- System.out.printIn()和print一样, system在terminal输出print字符串

```java
public class BMI{
    public static void main(String[] args) {
        double height = 180;
        int weight = 65;
        double exponent = weight/(height*height);
        System.out.println(
                "您的身高是: " + height
        );
        System.out.println(
                "您的体重是: " + weight
        );
        System.out.println("您的BMI指数为");
        if (exponent < 18.5) {
            System.out.println("您体重太轻了");
        }
        if (exponent >= 18.5 && exponent <29.9) {
            System.out.println("体重过重");
        }
        if (exponent >= 29.9){
            System.out.println("肥胖");
        }
    }
}
```

//演示转义字符的使用 public class ChangeChar { //编写一个 main 方法 public static void main(String[] args) { //\t ：一个制表位，实现对齐的功能 System.out.println("北京\t 天津\t 上海"); // \n ：换行符 System.out.println("jack\nsmith\nmary"); // \\ ：一个\ \\ System.out.println("C:\\Windows\\System32\\cmd.exe"); // \" :一个" System.out.println("老韩说:\"要好好学习 java,有前途\""); // \' ：一个' System.out.println("老韩说:\'要好好学习 java,有前途\'"); // \r :一个回车 System.out.println("韩顺平教育\r 北京"); // 解读 // 1. 输出 韩顺平教育 // 2. \r 表示回车 System.out.println("韩顺平教育\r 北京"); // 北京平教育 } }



# Java学习笔记-2  基本数据类型

#### 	整数数据类型:

int	64位 (***默认类型***)

声明: 

```java
int a = 15;
int b = 30;
int c = a-b;
System.out.printIn(c);
```

- byte	8位
-   声明: 和int一样

```java
byte a, b, c;
```

- short	16位
  - 声明: 和int相同

```java
short a = 90;
```
- long	32位
  - 声明:  结尾加L 或者l 其他和int一样

```java
long number;
long number = 30L;
```
- float 单精度浮点类型
  - 声明: 小数后面+ F or f

```java
float f1 = 2.2132132f;
```

- Double  双精度浮点类型:
  - 声明: 默认都是double数据类型, 小数后面+ D 或者d.
  - 但是没有特定要求

```java
double f2 = 2.2323423;
double f3 = 2.3242234d;
```

#### 字符类型:

- char 型:
  - 用于储存单个字符, 占用16位内存空间.
  - 用单引号表示, ‘s’ 

***注意! 双引号就是字符串了***

```java
char a = 'b';
```

可以用unicode 来表示, 所以上面的也可以用

```java
char a = 98;
```

#### 转义字符:

- \123 八进制
- \u0052 四位16进制
- \\' 单引号
- \\\ 反斜杠

- \t 垂直制表符
- \r 回车
- \n 换行
- \b back space
- \f 换页





#### 布尔类型:

```java
boolean b;
boolean b1, b2;
boolean b True;
```

- 逻辑类型, 简称布尔型.
  - Boolean只有 True 或者是 False, 且不可以和整数类型转换.

***一般是在流程判断中做为条件变量以及条件判断 来定义布尔类型.***



# Java 学习笔记-3 变量与常量 & 运算符

#### 声明变量 

```java
int age = 33;
double number3 = 2.3333d;
char word = 'w';
```

**系统内存 ⇢ program区 ⇢  Data 区**

写程序的时候在系统内存, 执行时进入内存中的program区, 数据暂存数据(Data)区.



#### 声明常量(一直不会改变的量, 也叫 final 常量)

- 声明要指定数据类型 + final关键字
- final 数据类型 常量类型 [= 值]
- 常量一般全拼用大写字母, 如:

```java
final float PI = 3.1415926f;
```

#### 变量的有效范围

- 变量定义出后都暂存在内存中, 等程序执行到某个点, 变量会随内存释放, 就失去有效范围.

- 因此, 分出了“_成员变量_” 和 “_局部变量_”.

- 在变量名前加上 **static** 就是静态变量, 可以跨类和整个应用程序进行应用(类似python的function “def” )



