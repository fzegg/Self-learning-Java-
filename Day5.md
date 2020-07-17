# Java面向对象学习的三条主线

## Java类和类的成员：属性、方法、构造器、代码块、内部类

### 设计类

- 属性：对应类中的成员变量（field  域、字段）
- 方法：对应类中的成员方法（method  函数）
- 创建类的对象：实例化类、类的实例化

### 类和对象的使用

- 创建类，设计类的成员
- 创建类的对象
- 通过对象.属性/对象.方法调用对象的结构

### 如果创建了一个类的多个对象，每个对象都独立拥有一套类的属性（非static）

如果我们修改一个对象属性的值，不影响另外一个对象同属性的值

### 对象的内存解析

- 通常所说的栈是指虚拟机栈
- 堆（heap）的唯一目的就是存放对象实例
- 方法区用于存储已被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据

```java
Person p1 = new Person( ) ;
p1.name = "Tom";
p1.isMale = true;
Person p2 = new Person();
System.out.print(p2.name);//null
Person p3= p1;//在堆中和p1共用同一存储空间
p3.age = 10;//此时p1.age = 10
```

### 类中属性的使用

- 成员变量与局部变量：

1. 不同点：

   1）在类中声明的位置不同：属性直接定义在类的{}内；局部变量声明在方法内、方法形参、代码块内、构造器形参、构造器内部的变量

   2）权限修饰符不同：属性可以在声明时指明其权限，使用权限修饰符（常用的权限修饰符：private、public、缺省、protected）；局部变量不可以使用权限修饰符

   3）默认初始化值：类的属性根据其类型都有默认初始化值；局部变量没有默认初始化值，在调用前需要显式赋值，特别地，形参在调用时赋值即可

   4）在内存中加载的位置不同：属性加载在堆中（非static）；局部变量加载在栈空间中

2. 相同点：

   1）定义变量的格式、数据类型

   2）先声明，后使用

   3）变量都有其对应的作用域

### 类中方法的声明和使用

- 方法：描述类应该具有的功能

- 方法的声明：

  权限修饰符 返回值类型 方法名（形参列表）{

  ​				方法体

  }

- 说明：

  1.关于权限修饰符

  2.返回值类型：

  如果方法有返回值，必须在方法声明时指定返回值类型，方法中使用return返回指定类型的变量或常量；如果方法没有返回值，声明时使用void表示，如果使用“return;”表示结束此方法

  3.方法名：属于标识符，“见明知意”

  4.形参列表：可以声明零到多个形参

  5.方法体：方法功能的实现

- return关键词的使用：

  使用在方法体中，用于结束方法、针对有返回值类型的方法，使用“return”数据方法返回所要的值；在return语句后不能声明执行语句

- 方法使用时，可以调用当前类的属性和方法




