## private关键字    

package com.itheima_05;    
/*    
 * 学生类    
 *     
 * 通过对象直接访问成员变量，会存在数据安全问题    
 * 这个时候，我们就想能不能不让外界的对象直接访问成员变量呢?    
 * 能。    
 * 如何实现呢?    
 * 		private关键字    
 *     
 * private:    
 * 		是一个修饰符    
 * 		可以修饰成员变量，也可以修饰成员方法    
 * 		被private修饰的成员只能在本类中被访问    
 *     
 * 针对private修饰的成员变量，我们会相应的提供getXxx()和setXxx()用于获取和设置成员变量的值,方法用public修饰    
 */    
public class Student {    
	String name;    
	//int age;    
	private int age;    

	public void setAge(int a) {    
		if(a<0 || a>200) {    
			System.out.println("你给的年龄有误");    
		}else {    
			age = a;    
		}    
	}    

	public int getAge() {    
		return age;    
	}    

	public void show() {    
		System.out.println("姓名是："+name+",年龄是："+age);    
	}    
}    


package com.itheima_05;  
/*  
 * 学生类的测试类  
 */  
public class StudentDemo {  
	public static void main(String[] args) {  
		//创建学生对象  
		Student s = new Student();  
		s.show();  

		s.name = "林青霞";  
		//s.age = 28;  
		//s.age = -28;  
		//s.setAge(-28);  
		s.setAge(28);  
		s.show();  
	}  
}  
