# -Java
1.0 计算机与编程语言
1.1 第一个Java程序
1.2 变量与计算

1.2.1 输入
		System.out.println("你好");
		Scanner in = new Scanner(System.in);
		System.out.println("echo:"+in.nextLine());
		System.out.println(2+3+"=2+3="+(2+3));

1.2.2 变量

变量定义
  变量定义的一般形式就是：<类型名称><变量名称>；
  int price;
  int amount;
  int price,amount;
  例子：
    	
	public class hello {

  	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("你好");
		Scanner in = new Scanner(System.in);
    //		System.out.println("echo:"+in.nextLine());
		int price;
		price = in.nextInt();
		System.out.println("100-"+price+"="+(100-price));
	   }

     }
     
    
变量的名字 
  变量需要一个名字，变量的名字是一种“标识符”，意思是它是用来识别这个和那个的不同的名字
  标识符有标识符的构造规则。基本的原则是：标识符只能由字母、数字和下划线组成，数字不可以出现在第一个位置上，Java的关键字（有的地方叫它们保留字）不可以用做标识符

变量类型
  int price = 0;
  这一行，定义了一个变量。变量的名字是price，类型是int，初始值是0
  Java是一种强类型语言，所有的变量在使用之前必须定义或声明，所有的变量必须具有确定的数据类型。
  数据类型表示在变量中可以存放什么样的数据，变量中只能存放指定类型的数据，程序运行过程中也不能改变变量的类型

1.2.3 赋值
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("你好");
		Scanner in = new Scanner(System.in);
		System.out.println("echo:"+in.nextLine());
		int amount = 100;
		int price = 0;
		System.out.println("请输入票面：");
		amount = in.nextInt();
		System.out.println("请输入金额：");
		price = in.nextInt();
		System.out.println(amount + "-"+price+"="+(amount - price));

1.3 浮点数计算

1.3.1 浮点数

两个整数的运算的结果只能是整数
10和10.0在Java中式完全不同的数
10.0是浮点数

浮点数
	带小数点的数值

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int foot;
		int inch;
		Scanner in = new Scanner(System.in);
		foot = in.nextInt();
		inch = in.nextInt();
		System.out.println(foot+inch/12.0*0.3048);
	}	

浮点运算的精度
	浮点计算是有误差的
        System.out.println(1.2-1.1) ;正常的是0.1，但计算机给出的结果是0.0999999999987，无限接近于0.1但不是0.1

整数
整数类型不能表达有小数部分的数，整数和整数的运算结果还是整数。

1.3.2 计算的优先级

与数学上的优先级是一样的，赋值的优先级很低。

1.3.3 类型的转换
	
类型的强制转换
	int 30/3.0 可转换成 foot = （int）（30/3.0）;

(类型)值

例如：
	double b = 10.3;
	int a = (int)b;
只是从那个变量计算出了一个新的类型的值，它并不改变那个变量，无论是值还是类型都不改变。

2、 判断

2.1 比较

2.1.1 比较
2.1.2 关系运算

优先级
	所有的关系运算符的优先级比算术运算的低，但是比赋值运算符高
	判断是否相等的==和!=的优先级比其他的低，而连续的关系运算是从左到右进行的
	6>5>4这种东西在Java中是错误的，因为两个>的优先级是一样的，所以会从左到右计算，6>5是true然后true>4是不存在的	
	5和5.0是可以进行比较的，5==5.0是true的

double a = 1.0	
double b = 0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1
	这种情况下a和b是不相等的，因为浮点数运算是有误差的，所以10个0.1加起来和1.0之间是有差距的。

Math.abs(数字)可计算绝对值

2.2 判断

2.2.1 判断
2.2.2 判断语句

2.3 分支

2.3.1 嵌套和级联的判断

else的匹配
	else总会和最近的那个if相匹配
级联
	就是if-else if
switch(控制表达式)
控制表达式只能是整数型的结果，而case后的常量可以是常数，也可以是常数计算的表达式

2.4 判断语句常见问题

3、 循环

3.1 循环
3.1.1 循环
3.1.2 数数字

3.1.3 while循环

当条件满足，不断重复循环体内语句。

括号里是循环成立的条件

3.1.4 do-while的循环

3.2 循环的例子
3.2.1 计数循环
3.2.2 算平均数

3.2.3 猜数游戏

如何获得一个计算机随机出现的数：
	Scanner in = new Scanner(System.in);
	int number = (int)(Math.random()* 100+1);
Math.random()是让计算机输出一个 【0，1）之间的数，如果想更改范围就在这个的基础上改
例如我想让计算机生成一个【0.100】的整数那就要（int）(Math.random()* 100+1)

3.2.4 整数分解

4、 循环控制
4.1 for 循环

4.1.1 for 循环
	
表达累计的结果应该初始化为1

int : 4-byte [2^31-1,-2^31]

for = 对于 
	for ( count = 10; count > 10; count = count - 1 )
	就读成：“对于一开始的count=10，当count>0时，重复做循环体，每一轮循环在做完循环体内语句后，使得count递减。”
	
三个循环

	如果有固定次数，用for
	如果必须执行一次，用do_while
	其他情况用while
	
4.1.2 复合赋值

a=a+6 <--> a+=6 

4.2 循环控制
4.2.1 循环控制

break VS continue
	break:跳出循环
	continue:跳过循环这一轮剩下的语句进入下一轮

4.2.2 多重循环

在循环前可以放一个标号来标示循环：
OUT：
带标号的break和continue对那个循环起作用

4.2.3 逻辑类型

关系运算的结果是一个逻辑值，true或false。这个值可以保存在一个对应的逻辑类型变量中，这样的变量类型是boolean
	boolean flag = true;
	boolean tooHigh,tooSmall,tooRough;
	boolean done = false;

逻辑运算
	逻辑运算是对逻辑量进行的运算，只有逻辑量可以参与运算
	！ 逻辑非 !a
	&& 逻辑与 a&&b
	|| 逻辑或 a||b
优先级
!>&&>||
!done&&(count>MAX)

4.3 循环的例子
4.3.1 求和

辗转相除法
	1、如果b等于0，计算结束，a就是最大公约数；
	2、否则，计算a除以b的余数，让a等于b，而b等于那个余数；
	3、回到第一步。

