# 1.if语句(else的写法与C格式略有区别)
格式：
```java
if (关系表达式1) {
    语句体1;	
} else if (关系表达式2) {
    语句体2;	
} else if(关系表达式3){
	语句体3;	
} else {
    语句体n+1;
}
```
# 2.switch语句（与C一致，注意穿透）

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

- switch在JDK12的新特性
```java
int number = 10;  
switch (number) {  
    case 1 -> System.out.println("一");  
    case 2 -> System.out.println("二");  
    case 3 -> System.out.println("三");  
    default -> System.out.println("其他");  
}

switch (week) {
    case 1, 2, 3, 4, 5 -> System.out.println("工作日");
    case 6, 7 -> System.out.println("休息日");
    default -> System.out.println("没有这个星期");
}
```
# 3.循环语句（与C完全一致）
无限循环while（true）
# 4. Random

Random跟Scanner一样，也是Java提前写好的类，我们不需要关心是如何实现的，只要直接使用就可以了。

### 使用步骤：
```java
//1.导包  
import java.util.Random;  
​  
public class RandomDemo1 {  
    public static void main(String[] args) {  
        //2.创建对象  
        Random r = new Random();  
        //3.生成随机数  
        int number = r.nextInt(100);//包左不包右，包头不包尾  
        //0 ~ 99  
        System.out.println(number);  
​  
    }  
}
```
## 5.数组
## 5.1数组格式
数据类型 [] 数组名

比如：int [] array
## 5.2初始化
静态初始化：int[] arr = {1,2,3,4,5}; 
//长度内容提前写死

动态初始化：int[] arr = new int[3];
//数组内容待定，甚至长度也可以填入参数，等运行时再决定
## 5.3访问长度
arr.length可以直接取出长度
![[Pasted image 20260723172206.png]]
！！！快速遍历一个数组（仅限于遍历，打印，查找，求和），j不是取的下标，而是每一个值
！！！此法无法改变原数组。
## 5.4 二维数组
### 5.4.1静态初始化
![[Pasted image 20260726172600.png]]
### 5.4.2 动态初始化
![[Pasted image 20260726172850.png]]
### 5.4.3遍历
![[Pasted image 20260726172655.png]]
可以用arr[i].length得到内部小数组的长度
### 5.4.4二维数组内存
![[Pasted image 20260726173329.png]]
# 6方法
## 6.1方法的通用格式

- 格式：
    public static 返回值类型 方法名(参数) {  
       方法体;   
       return 数据 ;  
    }
- 注意：方法不能嵌套
- 调用方法时的注意：
	- void类型的方法，直接调用即可
	- 非void类型的方法，推荐用变量接收调用
## 6.2方法重载
- 就是在**同一个类**里，可以定义**多个同名的方法**，但它们**参数列表必须不同**
- 比如Add函数，功能就是把给的所有数相加，你为了考虑所有类型的输入，给每一种情况都写了一个方法，每个方法都很相近，只是参数的类型有变化
- 你不需要为类似的功能起不同的名字，比如 `addTwoInts`、`addThreeInts`、`addDoubles`。一个统一的 `add` 方法名，屏蔽了底层实现的差异，让API变得更简洁。