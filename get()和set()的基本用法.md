get()和set()的基本用法


使用前提：当要访问被private封装的属性时
提供访问方式的原因： 之所以用private封装，又对外提供访问方式（set get），是因为可以在访问方式中加入逻辑判断等语句，对访问的数据进行操作，其中操作包括给属性赋值和查看属性，提高代码的健壮性。

``class Student {private int age;`

```java
class Student {
    private int age;
	public int getAge() {//获取private权限下的age//4.
    return age;
}

public void setAge(int a) {//设置age，主函数中的实参传入//3.
    if (a > 0 && a < 200) {//此处判断为了让age满足现实
        age = a;
    } else {
        System.out.println("输入错误");
    }
}
`}`

`public class Test {`
    `public static void main(String[] args) {`
        `Student student = new Student();//1.`
        `student.setAge(18);//2.`
        `System.out.println("年龄： " + student.getAge());//将以传入的实参打印出来//5.`
    `}`
`}`
```



封装性的体现：

属性私有化

不对外暴露私有的方法

单例模式

