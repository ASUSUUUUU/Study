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
