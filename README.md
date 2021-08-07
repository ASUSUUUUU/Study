# Study
1.调用无参构造函数创建对象的时候，无能加括号。
  Person p;   正确 -------- Person p(); 错误
  
2.在构造函数里面是不能直接调用其他构造函数的，否则回被认为是创建了一个新的临时对象

3.给字符数组赋值时一定要注意赋值的方式，不然打印出来的东西很可能乱码
  字符可以直接减去数字，得到数字
  （直接把数字赋值给字符是可以的，这样相当于把ASCII赋值给字符了）
  
4.类的成员函数后面加 const，表明这个函数不会对这个调用该函数类对象的数据成员（准确地说是非静态数据成员）作任何改变。 
本质上其实这个const是修饰了this指针——————————而返回值加const，则表明不能返回的对象的数据成员做任何修改。在成员函数返回局部对象的情况下是常用的

5.const对象只能调用const成员函数，无法调用非const成员函数

6.一个函数的参数是一个引用。例如void func(C & a); 那么你不能把一个没有名字的临时对象传给他，引用的作用是给变量起别名。若连一个基础得到名字都没有，何谈别名？


	class MyCmp
	{
	public:
	    bool operator()(int num1, int num2)
	    {
		return num1 > num2; //真的东西排在前面
	    }
	}
	sort(arr, arr + N，MyCmp());
	sort(arr, arr + N，greater<int>());//STL内建仿函数

7.int和int的运算，得到的还是int，就算你用double接收，也还是会将int/int得到的int结果给double。所以你如果真的想保留小数值必须先将int强转成double

8.贪心算法解决问题的重要基础方法
lower_bound( begin,end,num)：从数组的begin位置到end-1位置二分查找第一个大于或等于num的数字，找到返回该数字的地址，不存在则返回end。通过返回的地址减去起始地址begin,得到找到数字在数组中的下标。

9.upper_bound( begin,end,num)：从数组的begin位置到end-1位置二分查找第一个大于num的数字，找到返回该数字的地址，不存在则返回end。
通过返回的地址减去起始地址begin,得到找到数字在数组中的下标
10.upper_bound( begin,end,num)：从数组的begin位置到end-1位置二分查找第一个大于num的数字，找到返回该数字的地址，不存在则返回end。
通过返回的地址减去起始地址begin,得到找到数字在数组中的下标

