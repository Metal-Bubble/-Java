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
	


            
   

