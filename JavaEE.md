# 

# JavaEE

## Java基础语法(第1级)

### Demo01_前言、入门程序、常量、变量



#### 1.1计算机存储单元

位（bit）：0或1代表一位

字节（Byte）：每逢8位是一个字节，是数据存储的最小单位

1Byte=8bit，1Kb=1024Byte，1Mb=1024Kb,1Gb=1024Mb…

#### 1.2Cmd操作

| 切换盘符       | 盘符名称：                 |
| -------------- | -------------------------- |
| 进入文件夹     | cd 文件夹名称              |
| 进入多级文件夹 | cd 文件夹1\文件夹2\文件夹3 |
| 返回上一级     | cd ..                      |
| 返回根目录     | cd \                       |
| 查看当前内容   | dir                        |
| 清屏           | dls                        |
| 退出           | exit                       |

#### 1.3注释

单行注释：//   

多行注释（区块）/* */

#### 1.4配置环境变量

高级系统设置>高级>环境变量>系统环境变量内新建>

1.变量名为JAVA_HOME 变量值为java路径

2.找到path目录添加java路径

#### 1.5关键字特点

1.完全小写的字母

2.在增强版记事本中（如notepad++）有特殊颜色

#### 1.6标识符

- 命名规则： 硬性要求

1.标识符可以包含英文字母26个(区分大小写) 、0-9数字 、$（美元符号） 和_（下划线） 

2.标识符不能以数字开头

3.标识符不能是关键字

- 命名规范： 软性建议

1.类名规范首字母大写，后面每个单词首字母大写  大驼峰式。

2.方法名规范首字母小写，后面每个单词首字母大写 小驼峰式。

3.变量名规范：全部小写。

#### 1.7常量

是指在Java程序中固定不变的数据。

| 类型       | 含义                                   | 数据举例                |
| ---------- | -------------------------------------- | ----------------------- |
| 整数常量   | 所有的整数                             | 0，1， 567， -9         |
| 小数常量   | 所有的小数                             | 0.0， -0.1， 2.55       |
| 字符常量   | 单引号引起来,只能写一个字符,必须有内容 | 'a' ， ' '， '好'       |
| 字符串常量 | 双引号引起来,可以写多个字符,也可以不写 | "A" ，"Hello"  ，"你好" |
| 布尔常量   | 只有两个值（流程控制中讲解）           | true ， false           |
| 空常量     | 只有一个值（引用数据类型中讲解）       | null                    |

#### 1.8数据类型

| 数据类型     | 关键字         | 内存占用 | 取值范围               |
| ------------ | -------------- | -------- | ---------------------- |
| 字节型       | byte           | 1个字节  | -128~127               |
| 短整型       | short          | 2个字节  | -32768~32767           |
| 整型         | int（默认）    | 4个字节  | -231次方~2的31次方-1   |
| 长整型       | long           | 8个字节  | -2的63次方~2的63次方-1 |
| 单精度浮点数 | ﬂoat           | 4个字节  | 1.4013E-45~3.4028E+38  |
| 双精度浮点数 | double（默认） | 8个字节  | 4.9E-324~1.7977E+308   |
| 字符型       | char           | 2个字节  | 0-65535                |
| 布尔类型     | boolean        | 1个字节  | true，false            |

### **Dem02_****数据类型转换、运算符、方法入门**



#### 2.1自动类型转换

1.特点：代买不需要进行特殊出来，自动完成

 2.规则：数据范围从小到大

#### 2.2强制类型转换

1.特点：代码需要进行特殊的格式处理，不能自动完成

2.格式：范围小的类型 范围小的变量名 = (范围小的类型) 原本范围大的数据

**注意事项：**

1.强制类型转换一般不推荐使用，因为有可能发生精度损失、数据溢出。

2.byte/short/char这三种类型都可以发生数学运算，例如加法“+”

```java
char zifu1=’A’;
System.out.println(zifu1+1);  //66
```

3.byte/short/char这三种类型在运算的时候，都会被首先提升成为int类型，然后再计算。

```java
byte num1=40;
byte num2=50;
//byte+byte》》int+int=int
Int result=num1+num2;   //90
```

4.boolean类型不能发生数据类型转换

#### 2.3ASCII编码表

| 字符 | 数值 |
| ---- | ---- |
| 0    | 48   |
| 9    | 57   |
| A    | 65   |
| Z    | 90   |
| a    | 97   |
| z    | 122  |

#### 2.4四则运算加号“+”用法

1.于数值来说，那就是加法。

2.对于字符char类型来说，在计算之前，char会被提升成为int，然后再计算。

char类型字符，和int类型数字，之间的对照关系表：ASCII、Unicode

3.对于字符串String（首字母大写，并不是关键字）来说，加号代表字符串连接操作。

任何数据类型和字符串进行连接的时候，结果都会变成字符串

#### 2.5四则运算符“/”，“%”用法

1.对于一个整数的表达式来说，除法用得上整除，整数除以整数，结果仍然是整数，只看商，不看余数。

2.只有对于整数的除法来说，区模运算符才有余数的意义。

#### 2.6自增自减符

> 自增运算符：++
>
> 自减运算符：--

1.基本含义：让一个变量涨一个数字1，或者让一个变量降一个数字1

2.使用格式：写在变量名称之前，或者写在变量名称之后。例如：++num，也可以num++

3.使用方式

A. 单独使用：不和其他任何操作混合，自己独立成为一个步骤。

B. 混合使用：和其他操作混合，例如与赋值混合，或者与打印操作混合，等。

4.使用区别

A. 在单独使用的时候，前++和后++没有任何区别。也就是：++num;和num++;是完全一样的。

B. 在混合的时候，有【重大区别】

 如果是【前++】，那么变量【立刻马上+1】，然后拿着结果进行使用。【先加后用】

 如果是【后++】，那么首先使用变量本来的数值，【然后再让变量+1】。【先用后加】

5.注意事项

只有变量才能使用自增、自减运算符。常量不可发生改变，所以不能用。

#### 2.7赋值运算符

- 1.基本赋值运算符

就是一个等号“=”，代表将右侧的数据交给左侧的变量。如int a = 30；

- 2.复合赋值运算符

| +=   | a+=3   | 相当于 | a=a+3     |
| ---- | ------ | ------ | --------- |
| -=   | b -= 4 | 相当于 | b=b-4     |
| *=   | c *= 5 | 相当于 | c=c*5     |
| /=   | d/=6   | 相当于 | d=d/6     |
| %=   | e %= 7 | 相当于 | e = e % 7 |

注意事项：

1.只有变量才能使用赋值运算符，常量不能进行赋值。

2.复合赋值运算符其中隐含了一个强制类型转换。

- 3.比较运算符

  | 大于     | >    |
  | -------- | ---- |
  | 小于     | <    |
  | 大于等于 | >=   |
  | 小于等于 | <=   |
  | 相等     | ==   |
  | 不相等   | !=   |

#### 2.8逻辑运算符

|  && 与（并且）  | 两边都是true，结果是true   |
| :-------------: | :------------------------- |
|                 | 一边是false，结果是false   |
| \|\| 或（或者） | 两边都是false，结果是false |
|                 | 一边是true，结果是true     |
|  ！ 非（取反）  | ！true结果是false          |
|                 | ！fals结果是true           |

注意事项：

1.比较运算符的结果一定是一个boolean值，成立就是true，不成立就是false

2.如果进行多次判断，不能连着写。

A.数学当中的写法，例如：1 < x < 3

B.程序当中【不允许】这种写法。

#### 2.9任意进制转换为10进制

> 系数*基数的权次幂相加

#### 2.10十进制转换为任意进制

> 公式：除基取余
>
> 使用源数据，不断地除以基数（几进制，基数就是几）得到余数，知道商为0，再将余数倒着拼起来即可

#### 2.11三元运算符

定义：需要三个数据才可以进行操作的运算符。 

> 格式：
>
> 数据类型 变量名称 = 条件判断 ? 表达式A : 表达式B;

流程：

1.首先判断条件是否成立：

2.如果成立为true，那么将表达式A的值赋值给左侧的变量；

3.如果不成立为false，那么将表达式B的值赋值给左侧的变量；

注意事项：

1.必须同时保证表达式A和表达式B都符合左侧数据类型的要求。

2.三元运算符的结果必须被使用。

#### 2.12定义方法的格式

方法名称的命名规则和变量一样，使用小驼峰。

> 格式
>
> ```java
> public static void 方法名称() {
> 
> 方法体}
> ```
>
> 

方法体：也就是大括号当中可以包含任意条语句。

注意事项：

1.方法定义的先后顺序无所谓。

2.方法的定义不能产生嵌套包含关系。

3.方法定义好了之后，不会执行的。如果要想执行，一定要进行方法的【调用】。

```java
调用方法格式：方法名称();
```



```java
//例
Public class demo01{
Public static void main（String[] rags）{
farmer();
}
Public static void farmer(){
System.out.println(“1”)
System.out.println(“2”)
System.out.println(“3”)
} }
```

### Demo03_流程控制语句

#### 3.1判断语句1--if

```java
if(关系表达式)｛语句体;｝
```

例

```java
public static void main(String[] args)

{ System.out.println("开始"); // 定义两个变量

int a = 10; int b = 20;

 //变量使用if判断 if (a == b){

System.out.println("a等于b"); }

 int c = 10;

 if(a == c){ System.out.println("a等于c"); }

 System.out.println("结束");
```

#### 3.2判断语句2--if...else

```java
if(关系表达式) { 语句体1}

else {语句体2}
```

例

```java
public static void main(String[] args){

// 判断给定的数据是奇数还是偶数

int a = 1;

if(a % 2 == 0) {

System.out.println("a是偶数"); }

else{System.out.println("a是奇数"); }

System.out.println("结束");
```

#### 3.3判断语句3--if..else if...elsejava

```java
if (判断条件1) {执行语句1;} 

else if (判断条件2) {执行语句2;}

...

else if (判断条件n) {执行语句n;} 

else {}
```

例

```java
// x和y的关系满足如下：x>=3 y = 2x + 1;-1<=x<3 
//y = 2x ; x<=-1 y = 2x – 1;
 // 根据给定的x的值，计算出y的值并输出。 
public static void main(String[] args) {
int x = 5;
int y;
if (x>= 3) {y = 2 * x + 1;} 
else if (x >= -1 && x < 3) {y = 2 * x;} 

else {y = 2 * x - 1;}

System.out.println("y的值是："+y);
```

#### 3.4switch语句

```java
switch(表达式) {

case 常量值1:语句体1;break;

case 常量值2:语句体2;break;

default:语句体n+1;break;}
```

例

```java
public static void main(String[] args) {

//定义变量，判断是星期几a

int weekday = 6;

//switch语句实现选择

switch(weekday) {

case 1:System.out.println("星期一");break;

case 2:System.out.println("星期二");break;

case 3: System.out.println("星期三");break;

case 4:System.out.println("星期四");break;

case 5:System.out.println("星期五");break;

case 6:System.out.println("星期六");break;

case 7:System.out.println("星期日");break;

default:System.out.println("你输入的数字有误");break;}}
```

- 注意事项

​      \1. 多个case后面的数值不可以重复。

​       \2. switch后面小括号当中只能是下列数据类型：

​                A.基本数据类型：byte/short/char/int

​                B.引用数据类型：String字符串、enum枚举

\3. switch语句格式可以很灵活：前后顺序可以颠倒，而且break语句还可以省略。

#### 3.5Case的穿透性

在switch语句中，如果case的后面不写break，将出现穿透现象，也就是不会在判断下一个case的值，直接向后运行，直到遇到break，或者整体switch结束

```java
public static void main(String[] args) {

int i = 5;

switch (i){

case 0:System.out.println("执行case0");break;

case 5:System.out.println("执行case5");

case 10:System.out.println("执行case10");

default:System.out.println("执行default");}}
```

#### 3.6for循环

\1. 初始化语句：在循环开始最初执行，而且只做唯一一次。

\2. 条件判断：如果成立，则循环继续；如果不成立，则循环退出。

\3. 循环体：重复要做的事情内容，若干行语句。

\4. 步进语句：每次循环之后都要进行的扫尾工作，每次循环结束之后都要执行一次。

格式：

```java
for(初始化表达式①; 布尔表达式②; 步进表达式④){循环体③}
```

例：使用循环，计算1-100之间的偶数和

```java
public static void main(String[] args) {

int sum = 0;

for (int i = 1; i <= 100; i++) {

if(i % 2==0){sum += i;}}

System.out.println("sum:"+sum);}
```

#### 3.7循环语句2--while

格式：

```java
 初始化表达式①

while(布尔表达式②){循环体③

步进表达式④}
```

例：while循环输出10次HelloWorld

```java
public static void main(String[] args) {

int i = 1;

while(i<=10){System.out.println("HelloWorld");i++;}}
```

#### 3.8循环语句3--do...while

格式：

```java
 初始化表达式①

do{循环体③

步进表达式④}while(布尔表达式②);
```

例 ：while循环输出10次HelloWorld

```java
public static void main(String[] args) {

int x=1;

do {System.out.println("HelloWorld");x++;}

while(x<=10);}
```

#### 3.9跳出语句Break

- 用法：

​      \1. 可以用在switch语句当中，一旦执行，整个switch语句立刻结束。

​      \2. 还可以用在循环语句当中，一旦执行，整个循环语句立刻结束。打断循环。

例

```java
public static void main(String[] args) {

for (int i = 1; i<=10; i++) {

//需求:打印完两次HelloWorld之后结束循环

if(i == 3){break;}

System.out.println("HelloWorld"+i);}}
```

#### 3.10循环控制语句continue关键字

> 定义：执行，则立刻跳过当前次循环剩余内容，马上开始下一次循环。

例

```java
public static void main(String[] args) {

for (int i = 1; i <= 10; i++) {

//需求:不打印第三次HelloWorld

if(i == 3){continue;}

System.out.println("HelloWorld"+i);}}
```

#### 3.11死循环

标准格式

```java
While（true）{循环体}
```

●IDEA的快捷键

| 快捷键             | 功能                                   |
| ------------------ | -------------------------------------- |
| Alt+Enter          | 导入包，自动修正代码                   |
| Ctrl+Y             | 删除光标所在行                         |
| Ctrl+D             | 复制光标所在行的内容，插入光标位置下面 |
| Ctrl+Alt+L         | 格式化代码                             |
| Ctrl+/             | 单行注释                               |
| Ctrl+Shift+/       | 选中代码注释，多行注释，再按取消注释   |
| Alt+Ins            | 自动生成代码，toString，get，set等方法 |
| Alt+Shift+上下箭头 | 移动当前代码行                         |
| Shift+f6           | 修改所有相同的内容                     |
| Shift+enter        | 在下方生成空行                         |
| Ctrl+enter         | 在上方生成空行                         |
| Alt+space          | 自动补全                               |
| Ctrl+alt+M         | 抽取方法                               |
| ctrl+alt+t         | 生成try...catch                        |

### Demo04_IDEA、方法

#### 4.1方法定义格式

```java
 public static void 方法名称() {方法体}
```

 调用格式：方法名称();

-  注意事项：
   \1. 方法定义的先后顺序无所谓。
   \2. 方法定义必须是挨着，不能在一个方法内部定义另外一个方法。
   \3. 方法定义之后，自己不会执行的；如果希望执行，一定要进行方法的调用。

#### 4.2定义方法的完整格式

```java
 修饰符 返回值类型 方法名称(参数类型 参数名称, ...) {
 方法体

return 返回值;}
```



> Static：静态的; 静止的; 停滞的; 静力的;
>
> Void:空虚; 空白; 空间; 真空;
>
> 修饰符：现阶段的固定写法，public static
>
> 返回值类型：也就是方法最终产生的数据结果是什么类型
>
> 方法名称：方法的名字，规则和变量一样，小驼峰 
>
> 参数类型：进入方法的数据是什么类型 参数名称：进入方法的数据对应的变量名称

#### 4.3return

> 作用

1.停止当前方法

2.将后面的返回值还给调用处
 返回值：也就是方法执行后最终产生的数据结果

- 注意：return后面的“返回值”，必须和方法名称前面的“返回值类型”，保持对应。

![image-20210401220224795](JavaEE.assets/image-20210401220224795.png)

例  实现不定次数打印

```java
public class Method_Demo5 {

public static void main(String[] args) {

printHelloWorld(9);}

public static void printHelloWorld(int n) {

for (int i = 0; i < n; i++) 

{System.out.println("HelloWorld");}}}
```

#### 4.4方法的三种调用格式。

 \1. 单独调用：方法名称(参数);
 \2. 打印调用：System.out.println(方法名称(参数));
 \3. 赋值调用：数据类型 变量名称 = 方法名称(参数);
 注意：此前学习的方法，返回值类型固定写为void，这种方法只能够单独调用，不能进行打印调用或者赋值调用。
 对于有返回值的方法，可以使用单独调用、打印调用或者赋值调用。
 但是对于无返回值的方法，只能使用单独调用，不能使用打印调用或者赋值调用。

 

#### 4.5方法的重载（Overload）

> 定义：多个方法的名称一样，但是参数列表不一样。  

 好处：只需要记住唯一个方法名称，就可以实现类似的多个功能。

方法重载与下列因素相关：

- 参数个数不同。
- 参数类型不同。
- 参数的多类型顺序不同。

方法重载与下列因素无关：

- 参数的名称无关

- 方法的返回值类型无关。



例：实现重载的print

```java
public class exercise {
 public static void main(String[] args) {
 me(20);me("hello");me(true);

me(3.15);me("1");me('a');}
 public static void me(int a){
 System.out.println(a);}
 public static void me(short a){
 System.out.println(a);} 

public static void me(long a){
 System.out.println(a); }
public static void me(byte a){
 System.out.println(a);}
 public static void me(char zifu){
 System.out.println(zifu);}
 public static void me(boolean x){
 System.out.println(x);}
 public static void me(double a){
 System.out.println(a);}
 public static void me(float a){
 System.out.println(a);}
 public static void me(String gao){
 System.out.println(gao);}} 
```

### Demo05_数组

#### 5.1数组

> 概念：是一种容器，可以同时存放多个数据值。

-  数组的特点：
   \1. 数组是一种引用数据类型
   \2. 数组当中的多个数据，类型必须统一
   \3. 数组的长度在程序运行期间不可改变

-  数组的初始化：在内存当中创建一个数组，并且向其中赋予一些默认值。

-  两种常见的初始化方式：
   \1. 动态初始化（指定长度）
   \2. 静态初始化（指定内容）

A.动态初始化（指定长度）：在创建数组的时候，直接指定数组当中的数据元素个数。

B.静态初始化（指定内容）：在创建数组的时候，不直接指定数据个数多少，而是直接将具体的数据内容进行指定。

动态初始化数组的格式：

```java
 数据类型[] 数组名称 = new 数据类型[数组长度];
```

>  左侧数据类型：也就是数组当中保存的数据，全都是统一的类型
>  左侧的中括号：代表我是一个数组
>  左侧数组名称：给数组取一个名字
>  右侧的new：代表创建数组的动作
>  右侧数据类型：必须和左边的数据类型保持一致
>  右侧中括号的长度：也就是数组当中，到底可以保存多少个数据，是一个int数字

 静态初始化基本格式：

```java
 数据类型[] 数组名称 = new 数据类型[] { 元素1, 元素2, ... };
```

 省略格式：

```java
 数据类型[] 数组名称 = { 元素1, 元素2, ... };
```

-  注意事项

   \1. 静态初始化没有直接指定长度，但是仍然会自动推算得到长度。
   \2. 静态初始化标准格式可以拆分成为两个步骤。
   \3. 动态初始化也可以拆分成为两个步骤。
   \4. 静态初始化一旦使用省略格式，就不能拆分成为两个步骤了。

- 注意：直接打印数组名称得到的是数组对应的：内存地址哈希值。

####  5.2访问数组元素的格式

```
数组名称[索引值]
```

使用动态初始化数组的时候，其中的元素将会自动拥有一个默认值。规则如下：

-  如果是整数类型，那么默认为0；
   如果是浮点类型，那么默认为0.0；
   如果是字符类型，那么默认为'\u0000'；
   如果是布尔类型，那么默认为false；
   如果是引用类型，那么默认为null。

-  注意事项：
   静态初始化其实也有默认值的过程，只不过系统自动马上将默认值替换成为了大括号当中的具体数值。

#### 5.3获取数组长度

每个数组都具有长度，而且是固定的，Java中赋予了数组的一个属性，可以获取到数组的长度

```
语句为： 数组名.length 
```

#### 5.4java内存划分及工作

![image-20210401221748964](JavaEE.assets/image-20210401221748964.png)

![image-20210401221757494](JavaEE.assets/image-20210401221757494.png)

#### 5.5数组常见问题

> 1.数组索引越界异常
>  ArrayIndexOutOfBoundsException

所有的引用类型变量，都可以赋值为一个null值。但是代表其中什么都没有。

>  2.空指针异常 NullPointerException

 数组必须进行new初始化才能使用其中的元素。如果只是赋值了一个null，没有进行new创建，
 那么将会发生：
 原因：忘了new
 解决：补上new

#### 5.6数组作为方法的参数

当调用方法的时候，向方法的小括号进行传参，传递进去的其实是数组的地址值。

```java
public class exe2 {
 public static void main(String[] args) {
 int[] array = { 10, 20, 30, 40, 50 };
 System.out.println(array); // 地址值
 printArray(array); // 传递的就是array当中保存的地址值    System.out.println("==========AAA==========");
 printArray(array);
 System.out.println("==========BBB==========");
 printArray(array);}
 public static void printArray(int[] array) {
 System.out.println("printArray方法收到的参数是：");
 System.out.println(array); // 地址值

for (int i = 0; i < array.length; i++) {
 System.out.println(array[i]);}}}
```

5.7数组作为返回值类型

> 任何数据类型都能作为方法的参数类型，或者返回值类型。
>
> 数组作为方法的参数，传递进去的其实是数组的地址值。
>
> 数组作为方法的返回值，返回的其实也是数组的地址值。

例

```java
public class exe2 {
 public static void main(String[] args) {
 int[] result = calculate(10, 20, 30);
 System.out.println("main方法接收到的返回值数组是：");
 System.out.println(result); // 地址值
 System.out.println("总和：" + result[0]);
 System.out.println("平均数：" + result[1]); }
 public static int[] calculate(int a, int b, int c) {
 int sum = a + b + c; // 总和
 int avg = sum / 3; // 平均数
 // 两个结果都希望进行返回
 int[] array = {sum, avg};
 System.out.println("calculate方法内部数组是：");
 System.out.println(array); // 地址值
 return array; }}

```

## Java的面向对象和常用类(第 2级)

### Demo06_类与对象、封装、构造方法

#### 6.1类和对象

> 类：是一组相关属性和行为的集合。可以看成是一类事物的模板，使用事物的属性特征和行为特征来描述该类事物。

> 对象：是一类事物的具体体现。对象是类的一个实例，必然具备该类事物的属性和行为。

#### 6.2面向对象三大特征：封装、继承、多态。

#### 6.3成员变量及成员方法的创建和使用

要求：

1.成员变量是直接定义在类当中的，在方法外边。

2.成员方法不要写static关键字。

```java
public class Student {
 // 成员变量
 String name; // 姓名
 int age; // 姓名
 // 成员方法
 public void eat() {
 System.out.println("吃饭饭！");}
 public void sleep(){System.out.println("睡觉觉");}
 public void study() {System.out.println("学习");}
```

#### 6.4对象使用的内存图

> 两个对象使用同一个方法（内存图）

 ![image-20210401224829460](JavaEE.assets/image-20210401224829460.png)

> 使用对象类型作为方法的参数（内存图）

 ![image-20210401224833349](JavaEE.assets/image-20210401224829460.png)

> 使用对象类型作为方法的返回值（内存图）

 ![image-20210401224837542](JavaEE.assets/image-20210401224837542.png)

#### 6.5成员变量和局部变量的区别

-  \1. 定义的位置不一样【重点】

局部变量：在方法的内部
 成员变量：在方法的外部，直接写在类当中

-  \2. 作用范围不一样【重点】

 局部变量：只有方法当中才可以使用，出了方法就不能再用
 成员变量：整个类全都可以通用。

-  \3. 默认值不一样【重点】

 局部变量：没有默认值，如果要想使用，必须手动进行赋值
 成员变量：如果没有赋值，会有默认值，规则和数组一样

-  \4. 内存的位置不一样（了解）

 局部变量：位于栈内存
 成员变量：位于堆内存

-  \5. 生命周期不一样（了解）

 局部变量：随着方法进栈而诞生，随着方法出栈而消失
 成员变量：随着对象创建而诞生，随着对象被垃圾回收而消失

####  6.6封装性在Java当中的体现

 \1. 方法就是一种封装

 \2. 关键字private也是一种封装

 \3.封装就是将一些细节信息隐藏起来，对于外界不可

#### 6.7间接访问private成员变量

定义一对儿Getter/Setter方法
 必须叫setXxx或者是getXxx命名规则
 对于Getter来说，不能有参数，返回值类型和成员变量对应；
 对于Setter来说，不能有返回值，参数类型和成员变量对应。

例

```java
public class Student {
 private String name; // 姓名

private int age; // 年龄 

public void setName(String str){name = str; } public String getName(){return name; }
 public void setAge(int num) {age = num; }
 public int getAge() {return age; }}
```

对于基本类型当中的boolean值，Getter方法一定要写成isXxx的形式，而setXxx规则不变。

例

```java
private boolean male; // 是不是爷们儿
 public void setMale(boolean b) {
 male = b;}
 public boolean isMale() 

{return male;}
```

#### 6.8this关键字的使用

当方法的局部变量和类的成员变量重名的时候，根据“就近原则”，优先使用局部变量。
 如果需要访问本类当中的成员变量，需要使用格式：

```
 this.成员变量名
```

 


 “通过谁调用的方法，谁就是this。”

例

```java
public class Person {
 String name; // 我自己的名字
 // 参数name是对方的名字
 // 成员变量name是自己的名字
 public void sayHello(String name) {
 System.out.println(name + "，你好。我是" + this.name);
 System.out.println(this);}}
public class Demo01Person {
 public static void main(String[] args) {
 Person person = new Person();
 // 设置我自己的名字
 person.name = "王健林";
 person.sayHello("王思聪");
 System.out.println(person); // 地址值}}
```

#### 6.9构造方法

\1. 构造方法的名称必须和所在的类名称完全一样，就连大小写也要一样
 \2. 构造方法不要写返回值类型，连void都不写
 \3. 构造方法不能return一个具体的返回值
 \4. 如果没有编写任何构造方法，那么编译器将会默认赠送一个构造方法，没有参数、方法体什么事情都不做。
 public Student() {}
 \5. 一旦编写了至少一个构造方法，那么编译器将不再赠送。
 \6. 构造方法也是可以进行重载的。

 重载：方法名称相同，参数列表不同。

#### 6.10一个标准类的组成部分

 \1.所有的成员变量都要使用private关键字修饰

 \2.快捷键：alt+inse中getter &setter
 \3. 为每一个成员变量编写一对儿Getter/Setter方法
 \4.编写一个无参数的构造方法
 \5. 编写一个全参数的构造方法

 这样标准的类也叫做Java Bean（快捷键：alt+inse中constructor 全选的是全参  不选的是无参）

### Demo07_常见API及其方法

#### 7.1API(Application Programming Interface)

应用程序编程接口。Java API是一本程序员的字典 ，是JDK中提供给我们使用的类的说明文档。这些类将底层的代码实现封装了起来，我们不需要关心这些类是如何实现的，只需要学习这些类如何使用即可。所以我们可以通过查询API的方式，来学习Java提供的类，并得知如何使用它们。

#### 7.2引用类型的一般使用步骤

1.导包

```
 import 包路径.类名称;
```

 如果需要使用的目标类，和当前类位于同一个包下，则可以省略导包语句不写。
 只有java.lang包下的内容不需要导包，其他的包都需要import语句。

2.创建

```
类名称 对象名 = new 类名称();
```

3.使用

```
 对象名.成员方法名()
```

#### 7.3 Scanner类

可以实现键盘输入数据，到程序当中。


```java
 Scanner sc = new Scanner(System.in);
 //获取键盘输入的一个int数字：
int num = sc.nextInt();
 //获取键盘输入的一个字符串：
String str = sc.next();
```



```java
例
//1. 导包
import java.util.Scanner;
public class Demo01_Scanner {
public static void main(String[] args) {
//2. 创建键盘录入数据的对象
Scanner sc = new Scanner(System.in);
//3. 接收数据
System.out.println("请录入一个整数：");
int i = sc.nextInt();
//4. 输出数据
System.out.println("i:"+i);}}
```

#### 7.4匿名对象

```java
// 匿名对象
 new Person().name = "赵又廷";
 new Person().showName(); // 我叫：null
```

#### 7.5匿名对象作为方法的参数 &返回值

1.作为方法的参数

```java
public class demo02 {
 public static void main(String[] args) {
 *methodParam*(new Scanner(System.*in*));}
 public static void methodParam(Scanner sc) {
 System.*out*.println(sc.next());}}
```

2.作为方法的返回值

```java
public class demo03 {
 public static void main(String[] args) {
 Scanner sc = *methodreturn*();
 System.*out*.println(sc.nextInt());}
 public static Scanner methodreturn() {
 return new Scanner(System.*in*);}
```

#### 7.6Random类（同理Scanner）

\1. 导包

```java
import java.util.Random;
```

 \2. 创建

```java
 Random r = new Random(); // 小括号当中留空即可
```

#### 7.7Arraylist类

特征：

1.数组的长度不可以发生改变。
 2.ArrayList集合的长度是可以随意变化的。
 3.对于ArrayList来说，有一个尖括号<E>代表泛型。
 泛型：也就是装在集合当中的所有元素，全都是统一的什么类型。
 注意：泛型只能是引用类型，不能是基本类型。

注意事项：
 对于ArrayList集合来说，直接打印得到的不是地址值，而是内容。如果内容是空，得到的是空的中括号：[]

> #### 集合（Arraylist）的方法

```java
ArrayList<String> list = new ArrayList<>();
1.list.add（Inteage e）
    //向集合内添加数据
2.public E get(int index)
    //从集合当中获取元素，参数是索引编号，返回值就是对应位置的元素。
3.public E remove(int index)
    //从集合当中删除元素，参数是索引编号，返回值就是被删除掉的元素。
4.public int size()
    //获取集合的尺寸长度，返回值是集合中包含的元素个数。
```

```java
//例1
public static void main(String[] args) {
 // 创建了一个ArrayList集合，集合的名称是list，里面装的全都是String字符串类型的数据
 // 备注：从JDK 1.7+开始，右侧的尖括号内部可以不写内容，但是<>本身还是要写的。
 ArrayList<String> list = new ArrayList<>();
 System.out.println(list); // []
 // 向集合当中添加一些数据，需要用到add方法。
 list.add("赵丽颖");
** System.out.println(list); // [赵丽颖]
 list.add("****迪丽热巴****");
 list.add("****古力娜扎****");
 list.add("****玛尔扎哈****");
 System.out.println(list); // [赵丽颖, 迪丽热巴, 古力娜扎, 玛尔扎哈]
 //list.add(100); // 错误写法！因为创建的时候尖括号泛型已经说了是字符串，添加进去的元素就必须都是字符串才行
```

**例** 2

```java
//例2
public static void main(String[] args) {
   ArrayList<String> list = new ArrayList<>();
   System.out.println(list); // []
   // 向集合中添加元素：add
   boolean success = list.add(**"柳岩");
   System.out.println(list); // [柳岩]
   System.out.println("添加的动作是否成功：" + success); // true
   list.add("高圆圆");
   list.add("赵又廷");
   list.add("****李小璐");
   list.add("贾乃亮");
   System.out.println(list); // [柳岩, 高圆圆, 赵又廷, 李小璐, 贾乃亮]
   //从集合中获取元素get。索引值从0开始
   String name = list.get(2);
   System.out.println*"第2号索引位置：" + name); // 赵又廷
   //从集合中删除元素：remove。索引值从0开始。
   String whoRemoved = list.remove(3);
   System.out.println("被删除的人是：" + whoRemoved); // 李小璐
   System.out.println(list); // [柳岩, 高圆圆, 赵又廷, 贾乃亮]
   //获取集合的长度尺寸，也就是其中元素的个数
   int **size = list.size();
   System.out.println("集合的长度是：" + size);
```

#### 7.8集合的遍历

```java
//例
**public static void** main(String[] args) {
 ArrayList<String> list = new ArrayList<>();
list.add("迪丽热巴");
 list.add("古力娜扎");
 list.add("玛尔扎哈");
```

```java
// 遍历集合(list.fori)
 for (int i = 0; i < list.size(); i++) {
 System.out.println(list.get(i));}
```

#### 7.9集合ArrayList对应基本类型的“包装类”

（引用类型，包装类都位于java.lang包下）

| 基本类型 | 包装类          |
| -------- | --------------- |
| byte     | Byte            |
| short    | Short           |
| int      | Integer（特）   |
| long     | Long            |
| float    | Float           |
| double   | Double          |
| char     | Character（特） |
| boolean  | Boolean         |

```java
//例1
public static void main(String[] args) {
 ArrayList<Integer> listC = new ArrayList<>();
 listC.add(100);
 listC.add(200);
 System.out.println(listC); // [100, 200]
 int num = listC.get(1);
 System.out.println("第1号元素是：" + num);
```



```java
//例题:用一个大集合存入20个随机数字，然后筛选其中的偶数元素，放到小集合中，要求使用自定义的方法来进行筛选
public class exe9 {
 public static void main(String[] args){
 Random r = new Random();
 ArrayList<Integer> allmax = new ArrayList<>();
 for (int i = 0; i < 20; i++) {
 int x = r.nextInt(100);
 allmax.add(x);}
 System.*out*.println(allmax);
 System.*out*.println(*method*(allmax));}
 public static ArrayList<Integer> method(ArrayList<Integer> allmax) {
 ArrayList<Integer> allmix = new ArrayList<>();
 for (int j = 0; j < allmax.size(); j++) {
 if (allmax.get(j) % 2 == 0) {
 allmix.add(allmax.get(j));}}
 System.*out*.println(allmix);
 return allmix;}}
```

#### 7.10Math类

java.long.Math类是数学相关的工具类，里面提供了大量的静态方法，完成与数学运算相关的操作。

> #### Math类的方法

```java
 public static double abs(double num)：获取绝对值。有多种重载。
 public static double ceil(double num)：向上取整。
 public static double floor(double num)：向下取整。
 public static long round(double num)：四舍五入。
 Math.PI代表近似的圆周率常量（double）。
```

```java
// 获取绝对值
 System.out.println(Math.abs(3.14)); // 3.14
// 向上取整
 System.out.println(Math.ceil(3.9)); // 4.0
// 向下取整，抹零
 System.out.println(Math.floor(30.1)); // 30.0
//四舍五入
System.out.println(Math.round(20.4)); // 20
System.out.println(Math.round(10.5)); // 11}
```



```java
//例：计算在-10.8到5.9之间，绝对值大于6或者小于2.1的整数有多少个？
public class Demo07MathPractice {
 public static void main(String[] args) {
 double max = 5.9;
 double min = -10.8;
 int num = 0;
 for (int i = (int) min; i < max; i++) {
 if (Math.abs(i) > 6 || Math.abs(i) < 2.1) {
 num++;}}
 System.out.println("在-10.8到5.9之间，绝对值大于6或者小于2.1的整数有:" + num + "个");//9}}
```



#### 7.11System类

> #### System类的常用方法 

```java
1.public   static void exit(int status)
    //终止当前运行的   Java   虚拟机，非零表示异常终止
2.public   static long currentTimeMillis()
    //返回当前时间(以毫秒为单位)
```



```java
//示例代码
//需求：在控制台输出1-10000，计算这段代码执行了多少毫秒 
public class SystemDemo {
    public static void main(String[] args) {
        // 获取开始的时间节点
        long start = System.currentTimeMillis();
        for (int i = 1; i <= 10000; i++) {
            System.out.println(i);
        }
        // 获取代码运行结束后的时间节点
        long end = System.currentTimeMillis();
        System.out.println("共耗时：" + (end - start) + "毫秒");
    }
}
```

#### 7.12Object类

- Object类概述


Object 是类层次结构的根，每个类都可以将 Object 作为超类。所有类都直接或者间接的继承自该类，换句话说，该类所具备的方法，所有类都会有一份

- 查看方法源码的方式

  选中方法，按下Ctrl + B

> #### Object类的toString方法

重写toString方法的方式

1. Alt + Insert 选择toString

1. 在类的空白区域，右键 -> Generate -> 选择toString

toString方法的作用：

以良好的格式，更方便的展示对象中的属性值

```java
//示例代码：
class Student extends Object {
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
}
public class ObjectDemo {
    public static void main(String[] args) {
        Student s = new Student();
        s.setName("林青霞");
        s.setAge(30);
        System.out.println(s); 
        System.out.println(s.toString()); 
    }
}
//结果
//Student{name='林青霞', age=30}
//Student{name='林青霞', age=30}
```

> #### Object类的equals方法
>

equals方法的作用

​    用于对象之间的比较，返回true和false的结果

​    举例：s1.equals(s2);    s1和s2是两个对象

重写equals方法的场景

​     不希望比较对象的地址值，想要结合对象属性进行比较的时候。

重写equals方法的方式

1. alt + insert  选择equals() and hashCode()，IntelliJ Default，一路next，finish即可
2. 在类的空白区域，右键 -> Generate -> 选择equals() and hashCode()，后面的同上。



```java
//示例代码
class Student {
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
        //this -- s1
        //o -- s2
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Student student = (Student) o; //student -- s2
        if (age != student.age) return false;
        return name != null ? name.equals(student.name) : student.name == null;
    }
}
public class ObjectDemo {
    public static void main(String[] args) {
        Student s1 = new Student();
        s1.setName("林青霞");
        s1.setAge(30);
        Student s2 = new Student();
        s2.setName("林青霞");
        s2.setAge(30);
        //需求：比较两个对象的内容是否相同
        System.out.println(s1.equals(s2));
    }
}
```

> #### Object面试题

```java
// 看程序,分析结果
String s = “abc”;
StringBuilder sb = new StringBuilder(“abc”);
s.equals(sb); 
sb.equals(s); 

public class InterviewTest {
    public static void main(String[] args) {
        String s1 = "abc";
        StringBuilder sb = new StringBuilder("abc");
        //1.此时调用的是String类中的equals方法.
        //保证参数也是字符串,否则不会比较属性值而直接返回false
        //System.out.println(s1.equals(sb)); // false

        //StringBuilder类中是没有重写equals方法,用的就是Object类中的.
        System.out.println(sb.equals(s1)); // false
    }
}
```



#### 7.13Obejects类

> #### Objects类的方法

```java
1.public static String toString(对象)  
    //返回参数中对象的字符串表示形式。 
2.public static String toString(对象, 默认字符串)  
    //返回对象的字符串表示形式。  
3.public static Boolean isNull(对象)  
    //判断对象是否为空  
4.public static Boolean nonNull(对象)  
    //判断对象是否不为空
```



```java
//示例代码
//学生类
class Student {
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
  }
```



```java
//测试类
public class MyObjectsDemo {
          public static void main(String[] args) {
      //        public static String toString(对象): 返回参数中对象的字符串表示形式。
      //        Student s = new Student("小罗同学",50);
      //        String result = Objects.toString(s);
      //        System.out.println(result);
      //        System.out.println(s);

      //        public static String toString(对象, 默认字符串): 返回对象的字符串表示形式。如果对象为空,那么返回第二个参数.
              //Student s = new Student("小花同学",23);
      //        Student s = null;
      //        String result = Objects.toString(s, "随便写一个");
      //        System.out.println(result);
      
      //        public static Boolean isNull(对象): 判断对象是否为空
              //Student s = null;
      //        Student s = new Student();
      //        boolean result = Objects.isNull(s);
      //        System.out.println(result);

      //        public static Boolean nonNull(对象): 判断对象是否不为空
              //Student s = new Student();
              Student s = null;
              boolean result = Objects.nonNull(s);
              System.out.println(result);
          }
  }
```

#### 7.14.BigDecimal类

可以用来进行精确计算

构造方法

| 方法名                 | 说明         |
| ---------------------- | ------------ |
| BigDecimal(double val) | 参数为double |
| BigDecimal(String val) | 参数为String |

常用方法

| 方法名                                                       | 说明 |
| ------------------------------------------------------------ | ---- |
| public BigDecimal add(另一个BigDecimal对象)                  | 加法 |
| public BigDecimal subtract (另一个BigDecimal对象)            | 减法 |
| public BigDecimal multiply (另一个BigDecimal对象)            | 乘法 |
| public BigDecimal divide (另一个BigDecimal对象)              | 除法 |
| public BigDecimal divide (另一个BigDecimal对象，精确几位，舍入模式) | 除法 |

总结

1. BigDecimal是用来进行精确计算的
2. 创建BigDecimal的对象，构造方法使用参数类型为字符串的。
3. 四则运算中的除法，如果除不尽请使用divide的三个参数的方法。

+ 代码示例：

  ```java
  BigDecimal divide = bd1.divide(参与运算的对象,小数点后精确到多少位,舍入模式);
  参数1 ，表示参与运算的BigDecimal 对象。
  参数2 ，表示小数点后面精确到多少位
  参数3 ，舍入模式  
    BigDecimal.ROUND_UP  进一法
    BigDecimal.ROUND_FLOOR 去尾法
    BigDecimal.ROUND_HALF_UP 四舍五入
  ```

#### 7.15基本类包装类

基本类型包装类的作用

将基本数据类型封装成对象的好处在于可以在对象中定义更多的功能方法操作该数据

常用的操作之一：用于基本数据类型与字符串之间的转换

#### 7.16Integer类

- Integer类概述

  包装一个对象中的原始类型 int 的值

  


> #### Integer类构造方法

```java
public Integer(int   value)  
    //根据 int 值创建 Integer 对象(过时)  
public Integer(String s)  
    //根据 String 值创建 Integer 对象(过时)  
public static Integer valueOf(int i)  
    //返回表示指定的 int 值的 Integer   实例  
public static Integer valueOf(String s)  
    //返回一个保存指定值的 Integer 对象 String
```

- 示例代码

```java
public class IntegerDemo {
    public static void main(String[] args) {
        //public Integer(int value)：根据 int 值创建 Integer 对象(过时)
        Integer i1 = new Integer(100);
        System.out.println(i1);
        //public Integer(String s)：根据 String 值创建 Integer 对象(过时)
        Integer i2 = new Integer("100");
//        Integer i2 = new Integer("abc"); //NumberFormatException
        System.out.println(i2);
        System.out.println("--------");
        //public static Integer valueOf(int i)：返回表示指定的 int 值的 Integer 实例
        Integer i3 = Integer.valueOf(100);
        System.out.println(i3);
        //public static Integer valueOf(String s)：返回一个保存指定值的Integer对象 String
        Integer i4 = Integer.valueOf("100");
        System.out.println(i4);
    }
}
```

> ####  自动拆箱和自动装箱
>

- 自动装箱

  ​	把基本数据类型转换为对应的包装类类型

- 自动拆箱

  ​	把包装类类型转换为对应的基本数据类型

- 示例代码

  ```java
  Integer i = 100;  // 自动装箱
  i += 200;         // i = i + 200;  i + 200 自动拆箱；i = i + 200; 是自动装箱
  ```

> ####  int和String类型的相互转换
>

- int转换为String

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

- String转换为int

  - 转换方式

    - 方式一：先将字符串数字转成Integer，再调用valueOf()方法

      Integer.valueOf（String str）；

      对象.intvalue（）；

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

#### 7.17数组高级操作

> #### 二分查找

+ 二分查找概述

  查找指定元素在数组中的位置时,以前的方式是通过遍历,逐个获取每个元素,看是否是要查找的元素,这种方式当数组元素较多时,查找的效率很低

  二分查找也叫折半查找,每次可以去掉一半的查找范围,从而提高查找的效率


+ 需求

  在数组{1,2,3,4,5,6,7,8,9,10}中,查找某个元素的位置

+ 实现步骤

  1. 定义两个变量，表示要查找的范围。默认min = 0 ，max = 最大索引
  2. 循环查找，但是min <= max
  3. 计算出mid的值
  4. 判断mid位置的元素是否为要查找的元素，如果是直接返回对应索引
  5. 如果要查找的值在mid的左半边，那么min值不变，max = mid -1.继续下次循环查找
  6. 如果要查找的值在mid的右半边，那么max值不变，min = mid + 1.继续下次循环查找
  7. 当min > max 时，表示要查找的元素在数组中不存在，返回-1.

+ 代码实现

  ```java
  public class My
      Demo {
      public static void main(String[] args) {
          int [] arr = {1,2,3,4,5,6,7,8,9,10};
          int number = 11;
          //1,我现在要干嘛? --- 二分查找
          //2.我干这件事情需要什么? --- 数组 元素
          //3,我干完了,要不要把结果返回调用者 --- 把索引返回给调用者
          int index = binarySearchForIndex(arr,number);
          System.out.println(index);
      }
      private static int binarySearchForIndex(int[] arr, int number) {
          //1,定义查找的范围
          int min = 0;
          int max = arr.length - 1;
          //2.循环查找 min <= max
          while(min <= max){
              //3.计算出中间位置 mid
              int mid = (min + max) >> 1;
              //mid指向的元素 > number
              if(arr[mid] > number){
                  //表示要查找的元素在左边.
                  max = mid -1;
              }else if(arr[mid] < number){
                  //mid指向的元素 < number
                  //表示要查找的元素在右边.
                  min = mid + 1;
              }else{
                  //mid指向的元素 == number
                  return mid;
              }
          }
          //如果min大于了max就表示元素不存在,返回-1.
          return -1;
      }
  }
  ```

+ 注意事项

  有一个前提条件，数组内的元素一定要按照大小顺序排列，如果没有大小顺序，是不能使用二分查找法的

> #### 冒泡排序 
>

+ 冒泡排序概述

  一种排序的方式，对要进行排序的数据中相邻的数据进行两两比较，将较大的数据放在后面，依次对所有的数据进行操作，直至所有数据按要求完成排序

  如果有n个数据进行排序，总共需要比较n-1次

  每一次比较完毕，下一次的比较就会少一个数据参与

+ 代码实现

  ```java
  public class MyBubbleSortDemo2 {
      public static void main(String[] args) {
          int[] arr = {3, 5, 2, 1, 4};
          //1 2 3 4 5
          bubbleSort(arr);
      }
  
      private static void bubbleSort(int[] arr) {
          //外层循环控制的是次数 比数组的长度少一次.
          for (int i = 0; i < arr.length -1; i++) {
              //内存循环就是实际循环比较的
              //-1 是为了让数组不要越界
              //-i 每一轮结束之后,我们就会少比一个数字.
              for (int j = 0; j < arr.length - 1 - i; j++) {
                  if (arr[j] > arr[j + 1]) {
                      int temp = arr[j];
                      arr[j] = arr[j + 1];
                      arr[j + 1] = temp;
                  }
              }
          }
  
          printArr(arr);
      }
  
      private static void printArr(int[] arr) {
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
      }
    
  }
  ```

> #### 快速排序 (理解)

- 快速排序概述

  冒泡排序算法中,一次循环结束,就相当于确定了当前的最大值,也能确定最大值在数组中应存入的位置

  快速排序算法中,每一次递归时以第一个数为基准数,找到数组中所有比基准数小的.再找到所有比基准数大的.小的全部放左边,大的全部放右边,确定基准数的正确位置

- 核心步骤

  1. 从右开始找比基准数小的
  2. 从左开始找比基准数大的
  3. 交换两个值的位置
  4. 红色继续往左找，蓝色继续往右找，直到两个箭头指向同一个索引为止
  5. 基准数归位

- 代码实现

  ```java
   public class MyQuiteSortDemo2 {
       public static void main(String[] args) {
   //        1，从右开始找比基准数小的
   //        2，从左开始找比基准数大的
   //        3，交换两个值的位置
   //        4，红色继续往左找，蓝色继续往右找，直到两个箭头指向同一个索引为止
   //        5，基准数归位
           int[] arr = {6, 1, 2, 7, 9, 3, 4, 5, 10, 8};
   
           quiteSort(arr,0,arr.length-1);
   
           for (int i = 0; i < arr.length; i++) {
               System.out.print(arr[i] + " ");
           }
       }
   
       private static void quiteSort(int[] arr, int left, int right) {
           // 递归结束的条件
           if(right < left){
               return;
           }
   
           int left0 = left;
           int right0 = right;
   
           //计算出基准数
           int baseNumber = arr[left0];
   
           while(left != right){
   //        1，从右开始找比基准数小的
               while(arr[right] >= baseNumber && right > left){
                   right--;
               }
   //        2，从左开始找比基准数大的
               while(arr[left] <= baseNumber && right > left){
                   left++;
               }
   //        3，交换两个值的位置
               int temp = arr[left];
               arr[left] = arr[right];
               arr[right] = temp;
           }
           //基准数归位
           int temp = arr[left];
           arr[left] = arr[left0];
           arr[left0] = temp;
         
           // 递归调用自己,将左半部分排好序
           quiteSort(arr,left0,left-1);
           // 递归调用自己,将右半部分排好序
           quiteSort(arr,left +1,right0);
   
       }
   }
  ```

#### 7.18Arrays类

- Arrays的常用方法

  | 方法名                                           | 说明                               |
  | ------------------------------------------------ | ---------------------------------- |
  | public static String toString(int[] a)           | 返回指定数组的内容的字符串表示形式 |
  | public static void sort(int[] a)                 | 按照数字顺序排列指定的数组         |
  | public static int binarySearch(int[] a, int key) | 利用二分查找返回指定元素的索引     |

- 示例代码

  ```java
  public class MyArraysDemo {
        public static void main(String[] args) {
    //        public static String toString(int[] a)    返回指定数组的内容的字符串表示形式
    //        int [] arr = {3,2,4,6,7};
    //        System.out.println(Arrays.toString(arr));
  
    //        public static void sort(int[] a)	  按照数字顺序排列指定的数组
    //        int [] arr = {3,2,4,6,7};
    //        Arrays.sort(arr);
    //        System.out.println(Arrays.toString(arr));
  
    //        public static int binarySearch(int[] a, int key) 利用二分查找返回指定元素的索引
            int [] arr = {1,2,3,4,5,6,7,8,9,10};
            int index = Arrays.binarySearch(arr, 0);
            System.out.println(index);
            //1,数组必须有序
            //2.如果要查找的元素存在,那么返回的是这个元素实际的索引
            //3.如果要查找的元素不存在,那么返回的是 (-插入点-1)
                //插入点:如果这个元素在数组中,他应该在哪个索引上.
        }
    }
  
  ```

  



####  7.19时间日期类

> #### Date类
>

+ 计算机中时间原点

  1970年1月1日 00:00:00

+ 时间换算单位

  1秒 = 1000毫秒

+ Date类概述

  Date 代表了一个特定的时间，精确到毫秒

+ Date类构造方法

  | 方法名                 | 说明                                                         |
  | ---------------------- | ------------------------------------------------------------ |
  | public Date()          | 分配一个 Date对象，并初始化，以便它代表它被分配的时间，精确到毫秒 |
  | public Date(long date) | 分配一个 Date对象，并将其初始化为表示从标准基准时间起指定的毫秒数 |

+ 示例代码

  ```java
  public class DateDemo01 {
      public static void main(String[] args) {
          //public Date()：分配一个 Date对象，并初始化，以便它代表它被分配的时间，精确到毫秒
          Date d1 = new Date();
          System.out.println(d1);
  
          //public Date(long date)：分配一个 Date对象，并将其初始化为表示从标准基准时间起指定的毫秒数
          long date = 1000*60*60;
          Date d2 = new Date(date);
          System.out.println(d2);
      }
  }
  ```

> #### Date类常用方法
>

- 常用方法

  | 方法名                         | 说明                                                  |
  | ------------------------------ | ----------------------------------------------------- |
  | public long getTime()          | 获取的是日期对象从1970年1月1日 00:00:00到现在的毫秒值 |
  | public void setTime(long time) | 设置时间，给的是毫秒值                                |

- 示例代码

  ```java
  public class DateDemo02 {
      public static void main(String[] args) {
          //创建日期对象
          Date d = new Date();
  
          //public long getTime():获取的是日期对象从1970年1月1日 00:00:00到现在的毫秒值
  //        System.out.println(d.getTime());
  //        System.out.println(d.getTime() * 1.0 / 1000 / 60 / 60 / 24 / 365 + "年");
  
          //public void setTime(long time):设置时间，给的是毫秒值
  //        long time = 1000*60*60;
          long time = System.currentTimeMillis();
          d.setTime(time);
  
          System.out.println(d);
      }
  }
  ```

> #### SimpleDateFormat类
>

- SimpleDateFormat类概述

  ​	SimpleDateFormat是一个具体的类，用于以区域设置敏感的方式格式化和解析日期。

  ​	我们重点学习日期格式化和解析

- SimpleDateFormat类构造方法

  | 方法名                                  | 说明                                                   |
  | --------------------------------------- | ------------------------------------------------------ |
  | public   SimpleDateFormat()             | 构造一个SimpleDateFormat，使用默认模式和日期格式       |
  | public SimpleDateFormat(String pattern) | 构造一个SimpleDateFormat使用给定的模式和默认的日期格式 |

- SimpleDateFormat类的常用方法

  - 格式化(从Date到String)
    - public final String format(Date date)：将日期格式化成日期/时间字符串
  - 解析(从String到Date)
    - public Date parse(String source)：从给定字符串的开始解析文本以生成日期

- 示例代码

  ```java
  public class SimpleDateFormatDemo {
      public static void main(String[] args) throws ParseException {
          //格式化：从 Date 到 String
          Date d = new Date();
  //        SimpleDateFormat sdf = new SimpleDateFormat();
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日 HH:mm:ss");
          String s = sdf.format(d);
          System.out.println(s);
          System.out.println("--------");
  
          //从 String 到 Date
          String ss = "2048-08-09 11:11:11";
          //ParseException
          SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
          Date dd = sdf2.parse(ss);
          System.out.println(dd);
      }
  }
  ```

练习：

+ 需求

  秒杀开始时间是2020年11月11日 00:00:00,结束时间是2020年11月11日 00:10:00,用户小贾下单时间是2020年11月11日 00:03:47,用户小皮下单时间是2020年11月11日 00:10:11,判断用户有没有成功参与秒杀活动

+ 实现步骤

  1. 判断下单时间是否在开始到结束的范围内
  2. 把字符串形式的时间变成毫秒值

+ 代码实现

  ```java
  public class DateDemo5 {
      public static void main(String[] args) throws ParseException {
          //开始时间：2020年11月11日 0:0:0
         //结束时间：2020年11月11日 0:10:0
          //小贾2020年11月11日 0:03:47
          //小皮2020年11月11日 0:10:11
          //1.判断两位同学的下单时间是否在范围之内就可以了。
          //2.要把每一个时间都换算成毫秒值。
          String start = "2020年11月11日 0:0:0";
          String end = "2020年11月11日 0:10:0";
          String jia = "2020年11月11日 0:03:47";
          String pi = "2020年11月11日 0:10:11";
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日 HH:mm:ss");
          long startTime = sdf.parse(start).getTime();
          long endTime = sdf.parse(end).getTime();
  //        System.out.println(startTime);
  //        System.out.println(endTime);
          long jiaTime = sdf.parse(jia).getTime();
          long piTime = sdf.parse(pi).getTime();
          if(jiaTime >= startTime && jiaTime <= endTime){
              System.out.println("小贾同学参加上了秒杀活动");
          }else{
              System.out.println("小贾同学没有参加上秒杀活动");
          }
          System.out.println("------------------------");
          if(piTime >= startTime && piTime <= endTime){
              System.out.println("小皮同学参加上了秒杀活动");
          }else{
              System.out.println("小皮同学没有参加上秒杀活动");
          }
      } 
  }
  ```

#### 7.20JDK8时间日期类

> ####  JDK8新增日期类
>

+ LocalDate       表示日期（年月日）  
+ LocalTime       表示时间（时分秒）
+ LocalDateTime    表示时间+ 日期 （年月日时分秒）

> #### LocalDateTime创建方法 

+ 方法说明

  | 方法名                                                    | 说明                                              |
  | --------------------------------------------------------- | ------------------------------------------------- |
  | public static LocalDateTime now()                         | 获取当前系统时间                                  |
  | public static LocalDateTime of  (年, 月 , 日, 时, 分, 秒) | 使用指定年月日和时分秒初始化一个LocalDateTime对象 |

+ 示例代码

  ```java
  public class JDK8DateDemo2 {
      public static void main(String[] args) {
          LocalDateTime now = LocalDateTime.now();
          System.out.println(now);
  
          LocalDateTime localDateTime = LocalDateTime.of(2020, 11, 11, 11, 11, 11);
          System.out.println(localDateTime);
      }
  }
  ```

> #### LocalDateTime获取方法 
>

+ 方法说

  | 方法名                          | 说明                        |
  | ------------------------------- | --------------------------- |
  | public int getYear()            | 获取年                      |
  | public int getMonthValue()      | 获取月份（1-12）            |
  | public int getDayOfMonth()      | 获取月份中的第几天（1-31）  |
  | public int getDayOfYear()       | 获取一年中的第几天（1-366） |
  | public DayOfWeek getDayOfWeek() | 获取星期                    |
  | public int getMinute()          | 获取分钟                    |
  | public int getHour()            | 获取小时                    |

+ 示例代码

  ```java
  public class JDK8DateDemo3 {
      public static void main(String[] args) {
          LocalDateTime localDateTime = LocalDateTime.of(2020, 11, 11, 11, 11, 20);
          //public int getYear()           获取年
          int year = localDateTime.getYear();
          System.out.println("年为" +year);
          //public int getMonthValue()     获取月份（1-12）
          int month = localDateTime.getMonthValue();
          System.out.println("月份为" + month);
  
          Month month1 = localDateTime.getMonth();
  //        System.out.println(month1);
  
          //public int getDayOfMonth()     获取月份中的第几天（1-31）
          int day = localDateTime.getDayOfMonth();
          System.out.println("日期为" + day);
  
          //public int getDayOfYear()      获取一年中的第几天（1-366）
          int dayOfYear = localDateTime.getDayOfYear();
          System.out.println("这是一年中的第" + dayOfYear + "天");
  
          //public DayOfWeek getDayOfWeek()获取星期
          DayOfWeek dayOfWeek = localDateTime.getDayOfWeek();
          System.out.println("星期为" + dayOfWeek);
  
          //public int getMinute()        获取分钟
          int minute = localDateTime.getMinute();
          System.out.println("分钟为" + minute);
          //public int getHour()           获取小时
    
          int hour = localDateTime.getHour();
          System.out.println("小时为" + hour);
      }
  }
  ```

> ####  LocalDateTime转换方法 
>

+ 方法说明

  | 方法名                           | 说明                      |
  | -------------------------------- | ------------------------- |
  | public LocalDate  toLocalDate () | 转换成为一个LocalDate对象 |
  | public LocalTime toLocalTime ()  | 转换成为一个LocalTime对象 |

+ 示例代码

  ```java
  public class JDK8DateDemo4 {
      public static void main(String[] args) {
          LocalDateTime localDateTime = LocalDateTime.of(2020, 12, 12, 8, 10, 12);
          //public LocalDate toLocalDate ()    转换成为一个LocalDate对象
          LocalDate localDate = localDateTime.toLocalDate();
          System.out.println(localDate);
  
          //public LocalTime toLocalTime ()    转换成为一个LocalTime对象
          LocalTime localTime = localDateTime.toLocalTime();
          System.out.println(localTime);
      }
  }
  ```

> ####  LocalDateTime格式化和解析 
>

+ 方法说明

  | 方法名                                                    | 说明                                                        |
  | --------------------------------------------------------- | ----------------------------------------------------------- |
  | public String format (指定格式)                           | 把一个LocalDateTime格式化成为一个字符串                     |
  | public LocalDateTime parse (准备解析的字符串, 解析格式)   | 把一个日期字符串解析成为一个LocalDateTime对象               |
  | public static DateTimeFormatter ofPattern(String pattern) | 使用指定的日期模板获取一个日期格式化器DateTimeFormatter对象 |

+ 示例代码

  ```java
  public class JDK8DateDemo5 {
      public static void main(String[] args) {
          //method1();
          //method2();
      }
  
      private static void method2() {
          //public static LocalDateTime parse (准备解析的字符串, 解析格式) 把一个日期字符串解析成为一个LocalDateTime对象
          String s = "2020年11月12日 13:14:15";
          DateTimeFormatter pattern = DateTimeFormatter.ofPattern("yyyy年MM月dd日 HH:mm:ss");
          LocalDateTime parse = LocalDateTime.parse(s, pattern);
          System.out.println(parse);
      }
  
      private static void method1() {
          LocalDateTime localDateTime = LocalDateTime.of(2020, 11, 12, 13, 14, 15);
          System.out.println(localDateTime);
          //public String format (指定格式)   把一个LocalDateTime格式化成为一个字符串
          DateTimeFormatter pattern = DateTimeFormatter.ofPattern("yyyy年MM月dd日 HH:mm:ss");
          String s = localDateTime.format(pattern);
          System.out.println(s);
      }
  }
  ```

  > #### LocalDateTime修改方法 
  >

  + 方法说明

    | 方法名                                              | 说明                           |
    | --------------------------------------------------- | ------------------------------ |
    | public LocalDateTime withYear(int year)             | 直接修改年                     |
    | public LocalDateTime withMonth(int month)           | 直接修改月                     |
    | public LocalDateTime withDayOfMonth(int dayofmonth) | 直接修改日期(一个月中的第几天) |
    | public LocalDateTime withDayOfYear(int dayOfYear)   | 直接修改日期(一年中的第几天)   |
    | public LocalDateTime withHour(int hour)             | 直接修改小时                   |
    | public LocalDateTime withMinute(int minute)         | 直接修改分钟                   |
    | public LocalDateTime withSecond(int second)         | 直接修改秒                     |

  + 示例代码

    ```java
    /**
     * JDK8 时间类修改时间
     */
    public class JDK8DateDemo8 {
        public static void main(String[] args) {
            //public LocalDateTime withYear(int year)   修改年
            LocalDateTime localDateTime = LocalDateTime.of(2020, 11, 11, 13, 14, 15);
           // LocalDateTime newLocalDateTime = localDateTime.withYear(2048);
           // System.out.println(newLocalDateTime);
    
            LocalDateTime newLocalDateTime = localDateTime.withMonth(20);
            System.out.println(newLocalDateTime);
    
        }
    }
    ```

  ### 

> #### Period 方法
>

+ 方法说明

  | 方法名                                          | 说明                 |
  | ----------------------------------------------- | -------------------- |
  | public static Period between(开始时间,结束时间) | 计算两个“时间"的间隔 |
  | public int getYears()                           | 获得这段时间的年数   |
  | public int getMonths()                          | 获得此期间的总月数   |
  | public int getDays()                            | 获得此期间的天数     |
  | public long toTotalMonths()                     | 获取此期间的总月数   |

+ 示例代码

  ```java
  /**
   *  计算两个时间的间隔
   */
  public class JDK8DateDemo9 {
      public static void main(String[] args) {
          //public static Period between(开始时间,结束时间)  计算两个"时间"的间隔
  
          LocalDate localDate1 = LocalDate.of(2020, 1, 1);
          LocalDate localDate2 = LocalDate.of(2048, 12, 12);
          Period period = Period.between(localDate1, localDate2);
          System.out.println(period);//P28Y11M11D
  
          //public int getYears()         获得这段时间的年数
          System.out.println(period.getYears());//28
          //public int getMonths()        获得此期间的月数
          System.out.println(period.getMonths());//11
          //public int getDays()          获得此期间的天数
          System.out.println(period.getDays());//11
  
          //public long toTotalMonths()   获取此期间的总月数
          System.out.println(period.toTotalMonths());//347
  
      }
  }
  ```

> #### Duration 方法
>

+ 方法说明

  | 方法名                                           | 说明                 |
  | ------------------------------------------------ | -------------------- |
  | public static Durationbetween(开始时间,结束时间) | 计算两个“时间"的间隔 |
  | public long toSeconds()                          | 获得此时间间隔的秒   |
  | public int toMillis()                            | 获得此时间间隔的毫秒 |
  | public int toNanos()                             | 获得此时间间隔的纳秒 |

+ 示例代码

  ```java
  /**
   *  计算两个时间的间隔
   */
  public class JDK8DateDemo10 {
      public static void main(String[] args) {
          //public static Duration between(开始时间,结束时间)  计算两个“时间"的间隔
  
          LocalDateTime localDateTime1 = LocalDateTime.of(2020, 1, 1, 13, 14, 15);
          LocalDateTime localDateTime2 = LocalDateTime.of(2020, 1, 2, 11, 12, 13);
          Duration duration = Duration.between(localDateTime1, localDateTime2);
          System.out.println(duration);//PT21H57M58S
          //public long toSeconds()	       获得此时间间隔的秒
          System.out.println(duration.toSeconds());//79078
          //public int toMillis()	           获得此时间间隔的毫秒
          System.out.println(duration.toMillis());//79078000
          //public int toNanos()             获得此时间间隔的纳秒
          System.out.println(duration.toNanos());//79078000000000
      }
  }
  ```

#### 7.21异常

- 异常的概述

  ​	异常就是程序出现了不正常的情况

- 异常的体系结构

  ![](JavaEE.assets/01_异常体系结构.png)

> #### 编译时异常和运行时异常的区别
>

- 编译时异常

  - 都是Exception类及其子类
  - 必须显示处理，否则程序就会发生错误，无法通过编译

- 运行时异常

  - 都是RuntimeException类及其子类
  - 无需显示处理，也可以和编译时异常一样处理

- 图示

  ![](JavaEE.assets/02_编译时异常和运行时异常.png)

> #### JVM默认处理异常的方式
>

- 如果程序出现了问题，我们没有做任何处理，最终JVM 会做默认的处理，处理方式有如下两个步骤：
  - 把异常的名称，错误原因及异常出现的位置等信息输出在了控制台
  - 程序停止执行

> #### 查看异常信息 
>

控制台在打印异常信息时,会打印异常类名,异常出现的原因,异常出现的位置

我们调bug时,可以根据提示,找到异常出现的位置,分析原因,修改异常代码

![](JavaEE.assets/03_查看异常信息.png)

> #### throws方式处理异常
>

- 定义格式

  ```java
  public void 方法() throws 异常类名 {
      
  }
  ```

- 示例代码

  ```java
  public class ExceptionDemo {
      public static void main(String[] args) throws ParseException{
          System.out.println("开始");
  //        method();
            method2();
  
          System.out.println("结束");
      }
  
      //编译时异常
      public static void method2() throws ParseException {
          String s = "2048-08-09";
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
          Date d = sdf.parse(s);
          System.out.println(d);
      }
  
      //运行时异常
      public static void method() throws ArrayIndexOutOfBoundsException {
          int[] arr = {1, 2, 3};
          System.out.println(arr[3]);
      }
  }
  ```

- 注意事项

  - 这个throws格式是跟在方法的括号后面的
  - 编译时异常必须要进行处理，两种处理方案：try...catch …或者 throws，如果采用 throws 这种方案，在方法上进行显示声明,将来谁调用这个方法谁处理
  - 运行时异常因为在运行时才会发生,所以在方法后面可以不写,运行时出现异常默认交给jvm处理

> #### throw抛出异常 
>

+ 格式

  throw new 异常();

+ 注意

  这个格式是在方法内的，表示当前代码手动抛出一个异常，下面的代码不用再执行了

+ throws和throw的区别

  | throws                                         | throw                                      |
  | ---------------------------------------------- | ------------------------------------------ |
  | 用在方法声明后面，跟的是异常类名               | 用在方法体内，跟的是异常对象名             |
  | 表示声明异常，调用该方法有可能会出现这样的异常 | 表示手动抛出异常对象，由方法体内的语句处理 |

+ 示例代码

  ```java
  public class ExceptionDemo8 {
      public static void main(String[] args) {
          //int [] arr = {1,2,3,4,5};
          int [] arr = null;
          printArr(arr);//就会 接收到一个异常.
                          //我们还需要自己处理一下异常.
      }
  
      private static void printArr(int[] arr) {
          if(arr == null){
              //调用者知道成功打印了吗?
              //System.out.println("参数不能为null");
              throw new NullPointerException(); //当参数为null的时候
                                              //手动创建了一个异常对象,抛给了调用者,产生了一个异常
          }else{
              for (int i = 0; i < arr.length; i++) {
                  System.out.println(arr[i]);
              }
          }
      }
  
  }
  ```

> ####  try-catch方式处理异常
>

- 定义格式

  ```java
  try {
  	可能出现异常的代码;
  } catch(异常类名 变量名) {
  	异常的处理代码;
  }
  ```

- 执行流程

  - 程序从 try 里面的代码开始执行
  - 出现异常，就会跳转到对应的 catch 里面去执行
  - 执行完毕之后，程序还可以继续往下执行

- 示例代码

  ```java
  public class ExceptionDemo01 {
      public static void main(String[] args) {
          System.out.println("开始");
          method();
          System.out.println("结束");
      }
  
      public static void method() {
          try {
              int[] arr = {1, 2, 3};
              System.out.println(arr[3]);
              System.out.println("这里能够访问到吗");
          } catch (ArrayIndexOutOfBoundsException e) {
              System.out.println("你访问的数组索引不存在，请回去修改为正确的索引");
          }
      }
  }
  ```

- 注意

  1. 如果 try 中没有遇到问题，怎么执行？

     会把try中所有的代码全部执行完毕,不会执行catch里面的代码

  2. 如果 try 中遇到了问题，那么 try 下面的代码还会执行吗？

     那么直接跳转到对应的catch语句中,try下面的代码就不会再执行了
     当catch里面的语句全部执行完毕,表示整个体系全部执行完全,继续执行下面的代码

  3. 如果出现的问题没有被捕获，那么程序如何运行？

     那么try...catch就相当于没有写.那么也就是自己没有处理.
     默认交给虚拟机处理.

  4. 同时有可能出现多个异常怎么处理？

     出现多个异常,那么就写多个catch就可以了.
     注意点:如果多个异常之间存在子父类关系.那么父类一定要写在下面

> #### Throwable成员方法
>

- 常用方法

  | 方法名                        | 说明                              |
  | ----------------------------- | --------------------------------- |
  | public String getMessage()    | 返回此 throwable 的详细消息字符串 |
  | public String toString()      | 返回此可抛出的简短描述            |
  | public void printStackTrace() | 把异常的错误信息输出在控制台      |

- 示例代码

  ```java
  public class ExceptionDemo02 {
      public static void main(String[] args) {
          System.out.println("开始");
          method();
          System.out.println("结束");
      }
  
      public static void method() {
          try {
              int[] arr = {1, 2, 3};
              System.out.println(arr[3]); //new ArrayIndexOutOfBoundsException();
              System.out.println("这里能够访问到吗");
          } catch (ArrayIndexOutOfBoundsException e) { //new ArrayIndexOutOfBoundsException();
  //            e.printStackTrace();
  
              //public String getMessage():返回此 throwable 的详细消息字符串
  //            System.out.println(e.getMessage());
              //Index 3 out of bounds for length 3
  
              //public String toString():返回此可抛出的简短描述
  //            System.out.println(e.toString());
              //java.lang.ArrayIndexOutOfBoundsException: Index 3 out of bounds for length 3
  
              //public void printStackTrace():把异常的错误信息输出在控制台
              e.printStackTrace();
  //            java.lang.ArrayIndexOutOfBoundsException: Index 3 out of bounds for length 3
  //            at com.itheima_02.ExceptionDemo02.method(ExceptionDemo02.java:18)
  //            at com.itheima_02.ExceptionDemo02.main(ExceptionDemo02.java:11)
  
          }
      }
  }
  ```

> ####  异常的练习 
>

+ 需求

  键盘录入学生的姓名和年龄,其中年龄为18 - 25岁,超出这个范围是异常数据不能赋值.需要重新录入,一直录到正确为止

+ 实现步骤

  1. 创建学生对象
  2. 键盘录入姓名和年龄，并赋值给学生对象
  3. 如果是非法数据就再次录入

+ 代码实现

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
          if(age >= 18 && age <= 25){
              this.age = age;
          }else{
              //当年龄不合法时,产生一个异常
              throw new RuntimeException("年龄超出了范围");
          }
      }
  
      @Override
      public String toString() {
          return "Student{" +
                  "name='" + name + '\'' +
                  ", age=" + age +
                  '}';
      }
  }
  ```

  测试类

  ```java
  public class ExceptionDemo12 {
      public static void main(String[] args) {
          // 键盘录入学生的姓名和年龄,其中年龄为 18 - 25岁,
          // 超出这个范围是异常数据不能赋值.需要重新录入,一直录到正确为止。
  
          Student s = new Student();
  
          Scanner sc = new Scanner(System.in);
          System.out.println("请输入姓名");
          String name = sc.nextLine();
          s.setName(name);
         while(true){
             System.out.println("请输入年龄");
             String ageStr = sc.nextLine();
             try {
                 int age = Integer.parseInt(ageStr);
                 s.setAge(age);
                 break;
             } catch (NumberFormatException e) {
                 System.out.println("请输入一个整数");
                 continue;
             } catch (AgeOutOfBoundsException e) {
                 System.out.println(e.toString());
                 System.out.println("请输入一个符合范围的年龄");
                 continue;
             }
             /*if(age >= 18 && age <=25){
                 s.setAge(age);
                 break;
             }else{
                 System.out.println("请输入符合要求的年龄");
                 continue;
             }*/
         }
          System.out.println(s);
  
      }
  }
  ```

> #### 自定义异常
>

+ 自定义异常概

  当Java中提供的异常不能满足我们的需求时,我们可以自定义异常

+ 实现步骤

  1. 定义异常类
  2. 写继承关系
  3. 提供空参构造
  4. 提供带参构造

+ 代码实现

  异常类

  ```java
  public class AgeOutOfBoundsException extends RuntimeException {
      public AgeOutOfBoundsException() {
      }
  
      public AgeOutOfBoundsException(String message) {
          super(message);
      }
  }
  ```

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
          if(age >= 18 && age <= 25){
              this.age = age;
          }else{
              //如果Java中提供的异常不能满足我们的需求,我们可以使用自定义的异常
              throw new AgeOutOfBoundsException("年龄超出了范围");
          }
      }
  
      @Override
      public String toString() {
          return "Student{" +
                  "name='" + name + '\'' +
                  ", age=" + age +
                  '}';
      }
  }
  ```

  测试类

  ```java
  public class ExceptionDemo12 {
      public static void main(String[] args) {
          // 键盘录入学生的姓名和年龄,其中年龄为 18 - 25岁,
          // 超出这个范围是异常数据不能赋值.需要重新录入,一直录到正确为止。
  
          Student s = new Student();
  
          Scanner sc = new Scanner(System.in);
          System.out.println("请输入姓名");
          String name = sc.nextLine();
          s.setName(name);
         while(true){
             System.out.println("请输入年龄");
             String ageStr = sc.nextLine();
             try {
                 int age = Integer.parseInt(ageStr);
                 s.setAge(age);
                 break;
             } catch (NumberFormatException e) {
                 System.out.println("请输入一个整数");
                 continue;
             } catch (AgeOutOfBoundsException e) {
                 System.out.println(e.toString());
                 System.out.println("请输入一个符合范围的年龄");
                 continue;
             }
             /*if(age >= 18 && age <=25){
                 s.setAge(age);
                 break;
             }else{
                 System.out.println("请输入符合要求的年龄");
                 continue;
             }*/
         }
          System.out.println(s);
  
      }
  }
  ```


## 