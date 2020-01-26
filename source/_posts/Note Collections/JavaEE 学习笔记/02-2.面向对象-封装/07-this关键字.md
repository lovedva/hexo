## this关键字  
package com.itheima_07;  
/*  
 * 学生类  
 *  
 * 起名字我们要求做到见名知意。  
 * 而我们现在的代码中的n和a就没有做到见名知意，所以我要改进。  
 *  
 * 如果有局部变量名和成员变量名相同，在局部使用的时候，采用的是就近的原则。  
 *  
 * 我们有没有办法把局部变量的name赋值给成员变量的name呢?  
 * 有。  
 *  
 * 什么办法呢?  
 * 		用this关键字就可以解决这个问题  
 *  
 * this:代表所在类的对象引用  
 * 		方法被哪个对象调用，this就代表那个对象  
 *  
 * 使用场景：  
 * 		局部变量隐藏成员变量  
 */  
public class Student {  
	private String name;  
	private int age;  

	public void setName(String name) { //"林青霞"  
		//name = name;  
		this.name = name;  
	}  

	public String getName() {  
		return name;  
	}  

	public void setAge(int age) {  
		//age = age;  
		this.age = age;  
	}  

	public int getAge() {  
		return age;  
	}  
}  


package com.itheima_07;  
/*  
 * 学生类的测试类  
 */  
public class StudentDemo {  
	public static void main(String[] args) {  
		//创建对象  
		Student s = new Student();  
		System.out.println(s.getName()+"---"+s.getAge());  

		s.setName("林青霞");  
		s.setAge(28);  
		System.out.println(s.getName()+"---"+s.getAge());  
	}  
}  
