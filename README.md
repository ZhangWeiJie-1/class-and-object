# class-and-object
https://namic.vercel.app/namic/notes/211229/#%E7%B1%BB%E5%92%8C%E5%AF%B9%E8%B1%A1
具有相同性质的对象，我们可以抽象称为类，人属于人类，车属于车类
class 类名{ 访问权限： 属性 / 行为 };
#include<iostream>
using namespace std;
//圆周率
const double PI = 3.14;
//1、封装的意义
//将属性和行为作为一个整体，用来表现生活中的事物

//封装一个圆类，求圆的周长
//class代表设计一个类，后面跟着的是类名
class Circle
{
public:  //访问权限  公共的权限

	//属性
	int m_r;//半径

	//行为
	//获取到圆的周长
	double calculateZC()
	{
		//2 * pi  * r
		//获取圆的周长
		return  2 * PI * m_r;
	}
};
int main() {

	//通过圆类，创建圆的对象(具体的圆)
	// 实例化（通过一个类，创建一个对象的过程）
	// c1就是一个具体的圆
	Circle c1;//创建对象
	c1.m_r = 10; //给圆对象的半径 进行赋值操作

	//2 * pi * 10 = = 62.8
	cout << "圆的周长为： " << c1.calculateZC() << endl;

	system("pause");

	return 0;
}
构造函数和析构函数到底是干嘛的
this指针

赋值运算符重载
c++编译器至少给一个类添加4个函数

默认构造函数(无参，函数体为空)
默认析构函数(无参，函数体为空)
默认拷贝构造函数，对属性进行值拷贝
赋值运算符 operator=, 对属性进行值拷贝
如果类中有属性指向堆区，做赋值操作时也会出现深浅拷贝问题
<img width="452" height="622" alt="image" src="https://github.com/user-attachments/assets/dcc14ad7-bd64-4603-8383-3161acf11abb" />

