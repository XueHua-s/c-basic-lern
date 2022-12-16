# 常见C编译器
    GCC、MSVC、Clang
# 代码编译器
    VS2019 - 集成开发环境, 集成了MSVC编译器
# 新建源文件
    xxxx.c - 为源文件
    xxxx.h - 为头文件
# 入门
## 入口函数
    int main() {
    }
    // C语言的代码是从入口函数的第一行开始执行的
    // int返回值类型的函数, return 返回值必须为整数
## 打印
    // 导入包
    #include <stdio.h>
    // 打印
    printf("比特");

    // 打印转换数据格式,将第二个参数的0显示为字符串打印
    printf("%d", 0);
    // 第一个参数为格式也就是模板
## 基础数据类型
    char 字符 - max 1byte
    short 短整 - max 2byte
    int 整型 - max 4byte
    long 长整型 - max 4byte
    long long 更长整形 - max 8byte
    float 单精度浮点数 - max 4byte
    double 双精度浮点数 - max 8byte

    sizeof() 操作符 用于计算类型或者变量所占字节的大小
## 变量声明格式
    int a = 0
## 求和函数
    scanf("%d%d", &d, &d)
## 作用域
    局部变量仅仅限于函数与代码块内

    全局变量的作用域是整个工程
### 引用全局变量
    // 如果在别的文件声明了全局变量,可以通过这个样子导入过来
    extern int g_val
## 生命周期
    变量的声明周期: 变量的生命周期就是创建和销毁之间的时间段
## 常量的声明
### const声明
    常变量通过 const 修饰符进行声明。
    不等同于常量, 数组和对象的下标只能够使用常量来取。
### 标识符常量
    #define 标识符常量
    #define MAX 123
### 枚举常量
    enum Sex {
      MALE = 1,
      FAMALE
    };
    // 枚举给所在位置一个默认值，别的值会依次向下底层
    // 如果没有默认值，会从0依次向下递增
## 字符串
### 描述
    字符串就是一串字符的意思
    用 "" 括起来的一串字符, 就是字符串
### 字符数组
    char name[] = "艾达王";
	  // 字符串在结尾的位置隐藏了一个\0的字符
    // 标志着字符串的结束
### 求字符串长度
    #include <string.h>
    strlen()
    // 这个函数求字符串长度，不算做 \0 字符串结束符号。
## 转义符
    %d 表示数字模板
    %c 表示字符模板
    $s 表示字符串模板格式
    \n 表示空格
    \\ 转义 \ 
    \a 转义声音, 警告字符

    转义阿斯科编码,参考网上阿斯科编码
## 注释
    ctrl + k, ctrn + c 注释
    ctrl + k, ctrn + u 取消注释
## 常见关键字
    register int num = 100; // 建议num的值存放在寄存器中
    signed 有符号的
    unsigned 无符号的
    static 静态属性
    struct 结构体
    union 联合体
    void 无,无返回值
    volatile
    typedef 类型重命名
### static
    static声明的静态属性。
    只会被声明一次，不会被销毁。
### extern
    声明外部符号
## 常量和宏
### define
    define 是一个预处理指令
    #define MAX 1000
### 定义宏
    #define ADD (X, Y) X + Y

    宏是用来替换的，不是函数返回值
    4 * ADD(2, 3)
    
    #define ADD (X, Y) (X + Y)