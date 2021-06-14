# ==100+ Java Interview Questions==

## Q1. Explain JDK, JRE and JVM?

| **JDK**                                                      | **JRE**                                                      | **JVM**                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| It stands for Java Development Kit.                          | It stands for Java Runtime Environment.                      | It stands for Java Virtual Machine.                          |
| It is the tool necessary to compile, document and package Java programs. | JRE refers to a runtime environment in which Java bytecode can be executed. | It is an abstract machine. It is a specification that provides a run-time environment in which Java bytecode can be executed. |
| It contains JRE + development tools.                         | It’s an implementation of the JVM which physically exists.   | JVM follows three notations: Specification, **Implementation,** and **Runtime Instance**. |



## Q2. Explain public static void main(String args[]) in Java.

main() in Java is the entry point for any Java program. It is always written as **public static void main(String[] args)**.

- **public**: Public is an access modifier, which is used to specify who can access this method. Public means that this Method will be accessible by any Class.
- **static**: It is a keyword in java which identifies it is class-based. main() is made static in Java so that it can be accessed without creating the instance of a Class. In case, main is not made static then the compiler will throw an error as **main**() is called by the JVM before any objects are made and only static methods can be directly invoked via the class. 
- **void**: It is the return type of the method. Void defines the method which will not return any value.
- **main**: It is the name of the method which is searched by JVM as a starting point for an application with a particular signature only. It is the method where the main execution occurs.
- **String args[]**: It is the parameter passed to the main method.



## Q3. Why Java is platform independent?

Java is called platform independent because of its **byte codes** which can run on any system irrespective of its underlying operating system.



## Q4. Why Java is not 100% Object-oriented?

Java is not 100% Object-oriented because it makes use of **eight primitive data types** such as boolean, byte, char, int, float, double, long, short which are not objects.



## Q5. What are wrapper classes in Java?

Wrapper classes convert the Java primitives into the **reference types** (objects). Every primitive data type has a class dedicated to it. These are known as wrapper classes because they “wrap” the primitive data type into an object of that class. Refer to the below image which displays different primitive type, wrapper class and constructor argument.



## Q6. What are constructors in Java?

In Java, constructor refers to a block of code which is used to **initialize an object**. It must have the same name as that of the class. Also, it has **no return type** and it is **automatically called** when an **object is created**.

There are two types of constructors:

1. **Default Constructor:** In Java, a default constructor is the one which **does not take any inputs**. In other words, default constructors are the **no argument constructors** which will be created by default in case you no other constructor is defined by the user. Its main purpose is to initialize the instance variables with the default values. Also, it is majorly used for object creation. 
2. **Parameterized Constructor:** The parameterized constructor in Java, is the constructor which is capable of **initializing the instance variables with the provided values**. In other words, the constructors which take the arguments are called parameterized constructors.



## Q7. What is singleton class in Java and how can we make a class singleton?

Singleton class is a class whose **only one instance can be created** at any given time, in one JVM. A class can be made singleton by making its **constructor private**.

单例模式，属于创建类型的一种常用的[软件设计模式](https://baike.baidu.com/item/软件设计模式/2117635)。通过单例模式的方法创建的类在当前进程中只有一个[实例](https://baike.baidu.com/item/实例/3794138)（根据需要，也有可能一个线程中属于单例，如：仅线程上下文内使用同一个实例）



## Q8. What is the difference between Array list and vector in Java?

| ArrayList                                                    | **Vector**                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Array List is not synchronized.                              | Vector is synchronized.                                      |
| Array List is fast as it’s non-synchronized.                 | Vector is slow as it is thread safe.                         |
| If an element is inserted into the Array List, it increases its Array size by 50%. | Vector defaults to doubling size of its array.               |
| Array List does not define the increment size.               | Vector defines the increment size.                           |
| Array List can only use Iterator for traversing an Array List. | Vector can use both Enumeration and Iterator for traversing. |

## Q9. What is the difference between equals() and == in Java?

- `Equals()` method is defined in Object class in Java and used for checking equality of two objects defined by business logic.
- `“==”` or equality operator in Java is a binary operator provided by Java programming language and used to compare **primitives** and **objects**. *public boolean equals(Object o)* is the method **provided by the Object class**. The default implementation uses `==` operator to compare two objects. For example: method can be overridden like String class. equals() method is used to compare the values of two objects.



## Q10. What are the differences between Heap and Stack Memory in Java?

The major difference between Heap and Stack memory are:

|    **Features**     | **Stack**                                                    | **Heap**                                                     |
| :-----------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|      *Memory*       | Stack memory is used only by **one thread of execution**.    | Heap memory is used by **all the parts of the application**. |
|      *Access*       | Stack memory **can’t** be accessed by **other threads.**     | Objects stored in the heap are **globally accessible.**      |
| *Memory Management* | Follows LIFO manner to free memory.                          | Memory management is based on the generation associated with each object. |
|     *Lifetime*      | Exists until the **end of** execution of the **thread**.     | Heap memory lives from the start till the end of **application execution**. |
|       *Usage*       | Stack memory only contains **local primitive** and **reference variables** to objects in heap space. | Whenever an **object is created**, it’s always **stored** in the **Heap** space. |



## **Q11.** What is a package in Java? List down various advantages of packages.

Packages in Java, are the collection of related classes and interfaces which are bundled together. By using packages, developers can easily modularize the code and optimize its reuse. Also, the code within the packages can be imported by other classes and reused. Below I have listed down a few of its advantages:

- Packages help in avoiding name clashes
- They provide easier access control on the code
- Packages can also contain hidden classes which are not visible to the outer classes and only used within the package
- Creates a proper hierarchical structure which makes it easier to locate the related classes



## Q12. Why pointers are not used in Java?

Java doesn’t use pointers because they are **unsafe** and **increases the complexity** of the program. Since, Java is known for its simplicity of code, adding the concept of pointers will be contradicting. Moreover, since **JVM is responsible** for implicit memory allocation, thus in order to **avoid direct access** to memory by the user, pointers are discouraged in Java.



## **Q13.** What is JIT compiler in Java?

JIT stands for `Just-In-Time` compiler in Java. It is a program that helps in **converting the Java bytecode into instructions that are sent directly to the processor**. By default, the JIT compiler is enabled in Java and is activated whenever a Java method is invoked. The JIT compiler then compiles the **bytecode** of the invoked method into **native machine code**, compiling it “just in time” to execute. Once the method has been compiled, the JVM summons the compiled code of that method directly rather than interpreting it. This is why it is often responsible for the performance optimization of Java applications at the run time.



## Q14. What are access modifiers in Java? 访问修饰符

In Java, access modifiers are special keywords which are used to restrict the access of a class, constructor, data member and method in another class. Java supports four types of access modifiers:

1. *Default*
2. *Private*
3. *Protected*
4. *Public*

| **Modifier**                     | **Default** | **Private** | **Protected** | **Public** |
| -------------------------------- | ----------- | ----------- | ------------- | ---------- |
| *Same class*                     | YES         | YES         | YES           | YES        |
| *Same Package subclass*          | YES         | NO          | YES           | YES        |
| *Same Package non-subclass*      | YES         | NO          | YES           | YES        |
| *Different package subclass*     | NO          | NO          | YES           | YES        |
| *Different package non-subclass* | NO          | NO          | NO            | YES        |



## Q15. Define a Java Class.

A class in Java is a blueprint which includes all your data. A class contains fields (variables) and methods to describe the behavior of an object. Let’s have a look at the syntax of a class.

```java
class Abc {
    member variables // class body
    methods
}
```



## Q16. What is an object in Java and how is it created?

An object is a real-world entity that has a state and behavior. An object has three characteristics:

1. State
2. Behavior
3. Identity

An object is created using the ‘new’ keyword. For example:

`ClassName obj = new ClassName();`



## Q17. What is Object Oriented Programming?

Object-oriented programming or popularly known as `OOPs` is a programming model or approach where the programs are organized around objects rather than logic and functions. In other words, OOP mainly **focuses on the objects** that are required to be manipulated instead of logic. This approach is ideal for the programs large and complex codes and needs to be actively updated or maintained.



## Q18. What are the main concepts of OOPs in Java?

Object-Oriented Programming or OOPs is a programming style that is associated with concepts like:

1. **Inheritance (继承)**: Inheritance is a process where one class acquires the properties of another.
2. **Encapsulation (封装)**: Encapsulation in Java is a mechanism of wrapping up the data and code together as a single unit.
3. **Abstraction (抽象)**: Abstraction is the methodology of hiding the implementation details from the user and only providing the functionality to the users. 
4. **Polymorphism (多态)**: Polymorphism is the ability of a variable, function or object to take multiple forms.
   - 多态是同一个行为具有多个不同表现形式或形态的能力
   - 多态就是同一个接口，使用不同的实例而执行不同操作
   - 多态性是对象多种表现形式的体现



### 多态存在的三个必要条件

- 继承
- 重写
- 父类引用指向子类对象：`Parent p = new Child();`

![img](https://www.runoob.com/wp-content/uploads/2013/12/java-polymorphism-222.png)

### 多态的实现方式

#### 方式一：重写：

这个内容已经在上一章节详细讲过，就不再阐述，详细可访问：[Java 重写(Override)与重载(Overload)](https://www.runoob.com/java/java-override-overload.html)。

#### 方式二：接口

- 生活中的接口最具代表性的就是插座，例如一个三接头的插头都能接在三孔插座中，因为这个是每个国家都有各自规定的接口规则，有可能到国外就不行，那是因为国外自己定义的接口类型。
- java中的接口类似于生活中的接口，就是一些方法特征的集合，但没有方法的实现。具体可以看 [java接口](https://www.runoob.com/java/java-interfaces.html) 这一章节的内容。

#### 方式三：抽象类和抽象方法

详情请看 [Java抽象类](https://www.runoob.com/java/java-abstraction.html) 章节。



## Q19. What is the difference between a local variable and an instance variable?

In Java, a **local variable** is typically used inside a method, constructor, or a **block** and has only local scope. Thus, this variable can be used only within the scope of a block. The best benefit of having a local variable is that other methods in the class won’t be even aware of that variable.

```java
if(x > 100)
{
	String test = "Edureka";
}
```

Whereas, an **instance variable (member variable)** in Java, is a variable which is bounded to its object itself. These variables are declared within a **class**, but **outside a method**. Every object of that class will create it’s own copy of the variable while using it. Thus, any changes made to the variable won’t reflect in any other instances of that class and will be bound to that particular instance only.

```java
class Test{
	public String EmpName;
	public int empAge;
}
```



## Q20. Differentiate between the constructors and methods in Java?

| **Methods**                                         | **Constructors**                                             |
| --------------------------------------------------- | ------------------------------------------------------------ |
| 1. Used to represent the behavior of an object      | 1. Used to **initialize** the state of an object             |
| 2. **Must** have a **return** type                  | 2. Do **not** have any **return** type                       |
| 3. Needs to be invoked explicitly                   | 3. Is invoked implicitly                                     |
| 4. No default method is provided by the compiler    | 4. A **default constructor** is provided by the compiler if the class has none |
| 5. Method name may or may not be same as class name | 5. Constructor name **must** always be the **same as the class name** |



## Q21. What is final keyword in Java?

**final** is a special keyword in Java that is used as a non-access modifier. A final variable can be used in different contexts such as:

### 1. final variable

- When the final keyword is used with a variable then its **value can’t be changed** once assigned. In case the no value has been assigned to the final variable then using only the class constructor a value can be assigned to it.

### 2. final method

- When a method is declared final then it **can’t be overridden** by the **inheriting class**.

### 3. final class

- When a class is declared as final in Java, it **can’t be extended** by any **subclass** class but it **can extend other class**.
- 有爸爸，没儿子



## Q22. What is the difference between break and continue statements?

| **break**                                                    | **continue**                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1. Can be used in **switch** and **loop** (for, while, do while) statements | 1. Can be only used with loop statements                     |
| 2. It causes the switch or loop statements to **terminate** the moment it is executed | 2. It doesn’t terminate the loop but causes the loop to jump to the **next iteration** |
| 3. It terminates the **innermost** enclosing loop or switch immediately | 3. A continue within a loop nested with a switch will cause the next loop iteration to execute |



## Q23.What is an infinite loop in Java? Explain with an example.

An infinite loop is an instruction sequence in Java that loops endlessly when a functional exit isn’t met. This type of loop can be the result of a programming error or may also be a deliberate action based on the application behavior. An infinite loop will terminate automatically once the application exits.



## Q24. What is the difference between this() and super() in Java?

In Java, super() and this(), both are special keywords that are used to call the constructor. 

| **this()**                                                | **super()**                                                  |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| 1. this() represents the **current instance of a class**  | 1. super() represents the **current instance of a parent/base class** |
| 2. Used to call the default constructor of the same class | 2. Used to call the default constructor of the parent/base class |
| 3. Used to access methods of the current class            | 3. Used to access methods of the base class                  |
| 4. Used for pointing the current class instance           | 4. Used for pointing the superclass instance                 |
| 5. Must be the first line of a block                      | 5. Must be the first line of a block                         |



## Q25. What is Java String Pool?

Java String pool refers to a **collection of Strings** which are stored in **heap** memory. In this, whenever a new object is created, String pool first checks whether the object is already present in the pool or not. If it is present, then the same reference is returned to the variable else new object will be created in the String pool and the respective reference will be returned.



## Q26. Differentiate between static and non-static methods in Java.

| **Static Method**                                            | **Non-Static Method**                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1. *The static* keyword must be used before the method name  | 1. No need to use the *s**tatic* keyword before the method name |
| 2. It is called using the class (**className.methodName**)   | 2. It is can be called like any general method               |
| 3. They **can’t access** any **non-static instance variables or methods** | 3. It can access any static method and any static variable without creating an instance of the class |



## Q27. What is constructor chaining in Java?

In Java, constructor chaining is the process of calling one constructor from another with respect to the current object. Constructor chaining is possible only through legacy where a subclass constructor is responsible for invoking the superclass’ constructor first. There could be any number of classes in the constructor chain. Constructor chaining can be achieved in two ways:

1. Within the same class using this()
2. From base class using super()



## Q28. Difference between String, StringBuilder, and StringBuffer.

| **Factor**      | **String**           | **StringBuilder**  | **StringBuffer** |
| --------------- | -------------------- | ------------------ | ---------------- |
| *Storage Area*  | Constant String Pool | Heap Area          | Heap Area        |
| *Mutability*    | Immutable            | Mutable            | Mutable          |
| *Thread Safety* | Yes                  | No                 | Yes              |
| *Performance*   | Fast                 | **More efficient** | Less efficient   |



## Q29. What is a classloader in Java?

The **Java ClassLoader** is a **subset of JVM** (Java Virtual Machine) that is responsible for loading the class files. Whenever a Java program is executed it is first loaded by the classloader. Java provides three built-in classloaders:

1. Bootstrap ClassLoader
2. Extension ClassLoader
3. System/Application ClassLoader



## Q30. Why Java Strings are immutable in nature?

In Java, string objects are immutable in nature which simply means once the String object is created its state cannot be modified. Whenever you try to update the value of that object instead of updating the values of that particular object, **Java creates a new string object**. Java String objects are immutable as **String objects are generally cached in the String pool.** Since String literals are usually shared between multiple clients, action from one client might affect the rest. It enhances security, caching, synchronization, and performance of the application. 



## Q31. What is the difference between an array and an array list?

| Array                                                        | **ArrayList**                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Cannot** contain values of **different data types**        | Can contain values of different data types.                  |
| **Size** must be defined at the time of declaration          | Size can be **dynamically changed**                          |
| Need to specify the index in order to add data               | No need to specify the index                                 |
| Arrays are not type parameterized                            | Arraylists are type                                          |
| Arrays can contain **primitive** data types as well as **objects** | Arraylists can contain **only objects**, **no primitive** data types are allowed |



## Q32. What is a Map in Java?

In Java, Map is an interface of Util package which maps unique keys to values. The Map interface is not a subset of the main Collection interface and thus it behaves little different from the other collection types. Below are a few of the characteristics of Map interface: 

1. Map doesn’t contain duplicate keys.
2. Each key can map at max one value.

The below image shows the complete hierarchy of the Java Collection.

![FrameworkHierarchy - Java Collections - Edureka](https://www.edureka.co/blog/wp-content/uploads/2017/05/Collection-framework-hierarchy.png)



# ==OOPS Java Interview Questions==

## Q1. What is Polymorphism?

Polymorphism is briefly described as “**one interface, many implementations**”. Polymorphism is a characteristic of being able to assign a different meaning or usage to something in different contexts – specifically, to allow an entity such as a variable, a function, or an object to have **more than one form**. There are two types of polymorphism:

![img](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Polymorphism-483x300.png)

1. Compile time polymorphism
   - method overloading
2. Run time polymorphism
   - done using **inheritance** and **interface**.



## Q2. What is runtime polymorphism or dynamic method dispatch?

什么是运行时多态性或动态方法派遣?

- In Java, runtime polymorphism or dynamic method dispatch is a process in which a call to an **overridden** method is resolved at **runtime** rather than at **compile-time**. 

- In this process, an overridden method is called through the reference variable of a superclass. Let’s take a look at the example below to understand it better.

```java
class Car {
    void run(){
        System.out.println(“car is running”); 
    }
}

class Audi extends Car {
    void run(){
    	System.out.prinltn(“Audi is running safely with 100km”);
    }
    public static void main(String args[]){
        Car b= new Audi();    //upcasting
        b.run();
    }
}
```



## **Q3.** What is abstraction in Java?

Abstraction refers to the quality of dealing with ideas rather than events. It basically deals with **hiding the details** and **showing the essential things** to the user. Thus you can say that abstraction in Java is the process of **hiding the implementation details** from the user and revealing only the **functionality** to them. Abstraction can be achieved in two ways:

1. **Abstract Classes** (0-100% of abstraction can be achieved)
2. **Interfaces** (100% of abstraction can be achieved)



## Q4. What do you mean by an interface in Java?

An interface in Java is a **blueprint of a class** or you can say it is a **collection of abstract methods** and **static constants**. In an interface, each method is **public and abstract** but it does **not** contain any **constructor**. Thus, interface basically is a group of related methods with empty bodies.

```java
public interface Animal {
  public void eat();
  public void sleep();
  public void run();
}
```



## Q5. What is the difference between abstract classes and interfaces?

| **Abstract Class**                                           | **Interfaces**                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| An abstract class can provide **complete**, **default code** and/or just the details that have to be overridden | An interface **cannot** provide any **code** at all, just the signature |
| In the case of an abstract class, a class may **extend only one abstract class** | A Class may **implement several interfaces**                 |
| An abstract class can have **non-abstract methods**          | **All methods** of an Interface are **abstract**             |
| An abstract class can have **instance variables**            | An Interface **cannot** have **instance variables**          |
| An abstract class can have any visibility: **public, private, protected** | An Interface visibility **must be public** (or) none         |
| If we add a **new method** to an abstract class then we have the option of **providing default implementation** and therefore all the existing code might work properly | If we add a new method to an Interface then we have to track down all the implementations of the interface and **define implementation** for the new method |
| An abstract class can **contain constructors**               | An Interface **cannot contain constructors**                 |
| Abstract classes are **fast**                                | Interfaces are **slow** as it requires extra indirection to find the corresponding method in the actual class |



## Q6. What is inheritance in Java?

Inheritance in Java is the concept where the properties of **one class can be inherited by the other**. It helps to **reuse the code** and establish a relationship between different classes. Inheritance is performed between two types of classes:

1. Parent class (Super or Base class)
2. Child class (Subclass or Derived class)

A class which inherits the properties is known as Child Class whereas a class whose properties are inherited is known as Parent class.



## Q7. What are the different types of inheritance in Java?

Java supports four types of inheritance which are:

1. **Single Inheritance:** 

   - In single inheritance, one class inherits the properties of another 

   - i.e there will be **only one parent** as well as one child class.

2. **Multilevel Inheritance:** 

   - When a class is derived from a class which is also derived from another class, 
   - i.e. a class having **more than one parent** class but at different levels, such type of inheritance is called Multilevel Inheritance.

3. **Hierarchical Inheritance:** 

   - When a class has **more than one child** classes (subclasses) or in other words, 
   - more than one child classes have the same parent class, then such kind of inheritance is known as hierarchical.

4. **Hybrid Inheritance:** Hybrid inheritance is a combination of two *or more types* of inheritance.



## Q8. What is method overloading and method overriding?

### **Method Overloading :**

- In Method Overloading, Methods of the same class 
  - **shares the same name** but each method must have a
  - **different number of parameters or parameters having different types and order**.
- Method Overloading is to “add” or “extend” more to the method’s behavior.
- It is a **compile-time** polymorphism.
- The methods must have a different signature.
- It may or may not need inheritance in Method Overloading.

```java
class Adder {
    Static int add(int a, int b){
    	return a+b;
    }
    Static double add( double a, double b){
    	return a+b;	
    }
    public static void main(String args[]){
        System.out.println(Adder.add(11,11));
        System.out.println(Adder.add(12.3,12.6));
    }
}
```

### Method Overriding: 

- In Method Overriding, the **subclass** has the **same method** with the **same name** and exactly the **same number and type of parameters** and **same return type** as a superclass.
- Method Overriding is to **“Change” existing behavior** of the method.
- It is a **run time** polymorphism.
- The methods must have the same signature.
- It always requires inheritance in Method Overriding.

```java
class Car {
    void run(){
    	System.out.println(“car is running”); 
    }
    
    Class Audi extends Car{
    	void run(){
        System.out.prinltn("Audi is running safely with 100km");
    }
    
    public static void main( String args[]){
        Car b=new Audi();
        b.run();
    }
}
```



## Q9. Can you override a private or static method in Java?

You **cannot** override a private or static method in Java. If you create a similar method with the same return type and same method arguments in child class then it will **hide the superclass method**; this is known as **method hiding**. Similarly, you cannot override a private method in subclass because it’s not accessible there. What you can do is **create another private method** with the same name in the child class. Let’s take a look at the example below to understand it better.

```java
class Base {
    private static void display() {
        System.out.println("Static or class method from Base");
    }

    public void print() {
        System.out.println("Non-static or instance method from Base");
    }
}
class Derived extends Base {
    private static void display() {
        System.out.println("Static or class method from Derived");
    }

    public void print() {
        System.out.println("Non-static or instance method from Derived");
    }
}

public class test {
    public static void main(String args[]) {
        Base obj = new Derived();
        obj1.display();
        obj1.print();
    }
}
```

## Q10. What is multiple inheritance? Is it supported by Java?

![MultipleInheritance - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/MultipleInheritance-Java-240x300.png)

- If a child class inherits the property from multiple classes is known as multiple inheritance. Java **does not allow** to extend multiple classes.
- The problem with multiple inheritance is that if multiple parent classes **have the same method name**, then at runtime it becomes difficult for the compiler to decide which method to execute from the child class.
- Therefore, Java doesn’t support multiple inheritance. The problem is commonly referred to as Diamond Problem.



## **Q11.** What is encapsulation in Java?

Encapsulation is a mechanism where you bind your data(variables) and code(methods) together as a single unit. Here, the **data is hidden from the outer world** and can be **accessed only via current class methods**. This helps in **protecting the data** from any unnecessary modification. We can achieve encapsulation in Java by:

- Declaring the variables of a class as **private**.
- Providing **public setter and getter methods** to modify and view the values of the variables.



## Q12. What is an association?

Association is a relationship where all object have their own lifecycle and there is no owner. Let’s take the example of Teacher and Student. Multiple students can associate with a single teacher and a single student can associate with multiple teachers but there is no ownership between the objects and both have their own lifecycle. These relationships can be one to one, one to many, many to one and many to many.



## Q13. What do you mean by aggregation?

An aggregation is a specialized form of Association where all object has their own lifecycle but there is ownership and child object can not belong to another parent object. Let’s take an example of Department and teacher. A single teacher can not belong to multiple departments, but if we delete the department teacher object will not destroy. 



## Q14. What is composition in Java?

Composition is again a specialized form of Aggregation and we can call this as a “death” relationship. It is a strong type of Aggregation. Child object does not have their lifecycle and if parent object deletes all child object will also be deleted. Let’s take again an example of a relationship between House and rooms. House can contain multiple rooms there is no independent life of room and any room can not belongs to two different houses if we delete the house room will automatically delete.



## Q15. What is a marker interface?

A Marker interface can be defined as the interface having no data member and member functions. In simpler terms, an empty interface is called the Marker interface. The most common examples of Marker interface in Java are **Serializable**, Cloneable etc. The marker interface can be declared as follows.



## Q16. What is object cloning in Java?

Object cloning in Java is the process of creating an exact copy of an object. It basically means the ability to create an object with a similar state as the original object. To achieve this, Java provides a method **clone()** to make use of this functionality. This method creates a new instance of the class of the current object and then initializes all its fields with the exact same contents of corresponding fields. To object clone(), the marker interface **java.lang.Cloneable** must be implemented to avoid any runtime exceptions. One thing you must note is Object clone() is a protected method, thus you need to override it.



## Q17. What is a copy constructor in Java?

复制一个类

Copy constructor is a member function that is used to initialize an object using another object of the same class. Though there is no need for copy constructor in Java since all objects are passed by reference. Moreover, Java does not even support automatic pass-by-value.

下面执行测试工作。

```java
CopyClass copyClass1 = new CopyClass();
CopyClass copyClass2 = (CopyClass) copyClass1.clone();
copyClass2.setX(5);

System.out.println("Class 1's X value is: " + copyClass1.getX());
System.out.println("Class 2's X value is: " + copyClass2.getX());
```
得到结果：

```
Class 1's X value is: 0
Class 2's X value is: 5
```



## Q18. What is a constructor overloading in Java?

In Java, constructor overloading is a technique of adding any number of constructors to a class each having a different parameter list. The compiler uses the number of parameters and their types in the list to differentiate the overloaded constructors.

```java
class Demo{
    int i;
    public Demo(int a){
    	i=a;
    }
    
    public Demo(int a, int b)
    {
    	//body
    }
}
```



# ==Exception and Thread Java Interview Questions==

## Q1. What is the difference between Error and Exception?

### Error

An error is an **irrecoverable** condition occurring at runtime. Such as **OutOfMemory** error. These JVM errors you **cannot repair them at runtime**. Though error can be caught in the catch block but the execution of application will come to a halt and is not recoverable.

### Exception

While exceptions are conditions that occur because of **bad input or human error** etc. e.g. `FileNotFoundException` will be thrown if the specified file does not exist. Or a `NullPointerException` will take place if you try using a null reference. In most of the cases it is **possible to recover** from an exception (probably by **giving the user feedback** for entering proper values etc.



## Q2. How can you handle Java exceptions?

There are five keywords used to handle exceptions in Java: 

1. try
2. catch
3. finally
4. throw
5. throws



## Q3. What are the differences between Checked Exception and Unchecked Exception?

### Checked Exception

- The classes that **extend `Throwable` class**， except `RuntimeException` and `Error` are known as checked exceptions. 
- Checked exceptions are **checked at compile-time**.
  - **编译器**要检查这类异常
  - 必须处理（try ...catch）的异常
- Example: `IOException`, `SQLException` etc.

### Unchecked Exception （Runtime Exception）

- The classes that **extend `RuntimeException`** are known as unchecked exceptions. 
- Unchecked exceptions are **not checked at compile-time**.
- Example: `ArithmeticException`, `NullPointerException` etc.



## Q4. What purpose do the keywords final, finally, and finalize fulfill? 

### Final:

Final is used to apply restrictions on class, method, and variable. A final class **can’t be inherited**, final **method can’t be overridden** and **final variable value can’t be changed**. Let’s take a look at the example below to understand it better.

```java
class FinalVarExample {
    public static void main( String args[]){
        final int a=10;   // Final variable
        a=50;             //Error as value can't be changed
    }
}    
```

### Finally

Finally is used to place important code, it will be **executed whether the exception is handled or not**. Let’s take a look at the example below to understand it better.

```java
class FinallyExample {
    public static void main(String args[]){
        try {
        	int x=100;
    	}
        catch(Exception e){
        	System.out.println(e);
        }
        finally{
        	System.out.println("finally block is executing");}
        }
	}
}
```

### Finalize

Finalize is used to perform **clean up processing just before the object is garbage collected**. Let’s take a look at the example below to understand it better.

```java
class FinalizeExample {
    public void finalize() {
    	System.out.println("Finalize is called");
    }
    
    public static void main(String args[]){
        FinalizeExample f1=new FinalizeExample();
        FinalizeExample f2=new FinalizeExample();
        f1= NULL;
        f2=NULL;
        System.gc();
    }
}
```



## Q5. What are the differences between throw and throws? 

| **throw keyword** （程序中）                              | **throws keyword** (方法)                                    |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| Throw is used to explicitly throw an exception.           | Throws is used to declare an exception.                      |
| Checked exceptions can not be propagated with throw only. | Checked exception can be propagated with throws.             |
| Throw is followed by an instance.                         | Throws is followed by class.                                 |
| Throw is used within the method.                          | Throws is used with the method signature.                    |
| You cannot throw multiple exception                       | You can declare multiple exception e.g. public void method()throws IOException,SQLException. |



## Q6. What is exception hierarchy in java?

The hierarchy is as follows:

**Throwable** is a parent class of all Exception classes. There are two types of Exceptions: **`Checked exceptions`** and **`UncheckedExceptions` or `RunTimeExceptions`**. Both type of exceptions extends `Exception` class whereas errors are further classified into Virtual Machine error and Assertion error.

![ExceptionHierarchy - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Exception-hierarchy-516x300.png)



## Q7. How to create a custom Exception?

To create you own exception extend the Exception class or any of its subclasses.

- class New1Exception extends Exception { }        // this will create Checked Exception
- class NewException extends IOException { }       // this will create Checked exception
- class NewException extends NullPonterExcpetion { }  // this will create UnChecked exception



## Q8. What are the important methods of Java Exception Class?

Exception and all of it’s subclasses doesn’t provide any specific methods and all of the methods are defined in the base class Throwable.

1. **String getMessage()** – This method returns the message String of Throwable and the message can be provided while creating the exception through it’s constructor.
2. **String getLocalizedMessage(**) – This method is provided so that subclasses can override it to provide locale specific message to the calling program. Throwable class implementation of this method simply use getMessage() method to return the exception message.
3. **Synchronized Throwable getCause()** – This method returns the cause of the exception or null id the cause is unknown.
4. **String toString()** – This method returns the information about Throwable in String format, the returned String contains the name of Throwable class and localized message.
5. **void printStackTrace()** – This method prints the stack trace information to the standard error stream, this method is overloaded and we can pass PrintStream or PrintWriter as an argument to write the stack trace information to the file or stream.



## Q9. What are the differences between processes and threads?

|                   | **Process**                                                  | **Thread**                                                   |
| ----------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Definition**    | An executing **instance of a program** is called a process.  | A thread is a **subset of the process**.                     |
| **Communication** | Processes must use inter-process communication to communicate with sibling processes. | Threads can directly communicate with other threads of its process. |
| **Control**       | Processes can only exercise control over child processes.    | Threads can exercise considerable control over threads of the same process. |
| **Changes**       | Any change in the parent process does not affect child processes. | Any change in the main thread may affect the behavior of the other threads of the process. |
| **Memory**        | Run in separate memory spaces.                               | Run in **shared memory spaces**.                             |
| **Controlled by** | Process is controlled by the operating system.               | Threads are controlled by programmer in a program.           |
| **Dependence**    | Processes are independent.                                   | Threads are dependent.                                       |



## Q10. What is a finally block? Is there a case when finally will not execute?

Finally block is a block which **always executes a set of statements**. It is always associated with a **try** block regardless of any exception that occurs or not. 

Yes, finally will **not be executed** if the program exits either by calling **System.exit(**) or by causing a **fatal error** that causes the process to abort.



## Q11. What is synchronization?

Synchronization refers to **multi-threading**. A synchronized block of code can be **executed by only one thread at a time**. As Java supports execution of multiple threads, two or more threads may access the same fields or objects. Synchronization is a process which keeps all concurrent threads （并发） in execution to be in sync. Synchronization avoids memory consistency errors caused due to inconsistent view of shared memory. When a method is declared as synchronized the thread holds the monitor for that method’s object. If another thread is executing the synchronized method the thread is blocked until that thread releases the monitor. 

![Synchronization - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Synchronization.png)



##  Q12. Can we write multiple catch blocks under single try block? 

Yes we can have **multiple catch blocks** under **single try** block but the approach should be **from specific to general**. Let’s understand this with a programmatic example.

```java
public class Example {
    public static void main(String args[]) {
        try {
            int a[]= new int[10];
            a[10]= 10/0;
        }
        catch(ArithmeticException e){
        	System.out.println("Arithmetic exception in first catch block");
        }
        catch(ArrayIndexOutOfBoundsException e){
        	System.out.println("Array index out of bounds in second catch block");
        }
        catch(Exception e){
        	System.out.println("Any exception in third catch block");
    	}
}
```



## Q13. What are the important methods of Java Exception Class?

Methods are defined in the base class Throwable. Some of the important methods of Java exception class are stated below. 

1. **String getMessage()** – This method returns the message String about the exception. The message can be provided through its constructor.
2. **public StackTraceElement[] getStackTrace() –** This method returns an array containing each element on the stack trace. The element at index 0 represents the top of the call stack whereas the last element in the array represents the method at the bottom of the call stack.
3. **Synchronized Throwable getCause()** – This method returns the cause of the exception or null id as represented by a Throwable object.
4. **String toString()** – This method returns the information in String format. The returned String contains the name of Throwable class and localized message.
5. **void printStackTrace()** – This method prints the stack trace information to the standard error stream. 



## Q14. What is OutOfMemoryError in Java?

`OutOfMemoryError` is the subclass of `java.lang.Error` which generally occurs when our JVM **runs out of memory**.



## Q15. What is a Thread?

A thread is **the smallest piece of programmed instructions which can be executed independently by a scheduler**. In Java, all the programs will have at least one thread which is known as the main thread. This main thread is **created by the JVM** when the program starts its execution. The main thread is used to **invoke the main()** of the program.



## Q16. What are the two ways to create a thread?

In Java, threads can be created in the following two ways:

- By **implementing** the `Runnable` interface.
- By **extending** the `Thread`



## Q17. What are the different types of garbage collectors in Java?

Garbage collection in Java a program which helps in **implicit memory management**. Since in Java, using the `new` keyword you can create objects dynamically, which once created will consume some memory. Once the job is done and there are no more references left to the object, Java using garbage collection destroys the object and relieves the memory occupied by it. Java provides four types of garbage collectors:

- Serial Garbage Collector
- Parallel Garbage Collector
- CMS Garbage Collector
- G1 Garbage Collector



# ==Servlets – Java Interview Questions==

## Q1. What is a servlet?

- Java Servlet is **server-side** technologies to **extend the capability of web servers** by providing support for **dynamic response and data persistence**.
- The `javax.servlet` and `javax.servlet.http` packages provide interfaces and classes for writing our own servlets.
- All servlets must implement the `javax.servlet.Servlet` interface, which defines servlet lifecycle methods. When implementing a generic service, we can extend the GenericServlet class provided with the Java Servlet API. The `HttpServlet` class provides methods, such as `doGet()` and `doPost()`, for handling HTTP-specific services.
- Most of the times, web applications are accessed using HTTP protocol and thats why we mostly extend `HttpServlet` class. Servlet API hierarchy is shown in below image.

![Servlet - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Servlet-Java-340x300.png)

https://blog.csdn.net/qq_39688352/article/details/76794973

## Q2. What are the differences between Get and Post methods?

| **Get**                                                      | **Post**                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Limited amount of data** can be sent because data is sent in header. | **Large amount of data** can be sent because data is sent in body. |
| **Not Secured** because data is exposed in URL bar.          | **Secured** because data is not exposed in URL bar.          |
| Can be bookmarked                                            | Cannot be bookmarked                                         |
| Idempotent                                                   | Non-Idempotent                                               |
| It is more efficient and used than Post                      | It is less efficient and used                                |
| get 是从服务器上获取数据                                     | post 是向服务器传送数据                                      |
| 把参数数据队列加到提交表单的 ACTION 属性所指的 URL 中        | 通过 HTTP post 机制，将表单内各个字段与其内容放置在 HTML HEADER 内一起传送到 ACTION 属性所指的 URL 地址 |
| GET 把参数包含在 URL 中                                      | POST 通过 request body 传递参数                              |

### 标准答案

- GET 在浏览器回退时是无害的，而 POST 会再次提交请求。
- GET产生的URL地址可以被 Bookmark，而POST不可以。
- GET请求会被浏览器主动cache，而POST不会，除非手动设置。
- GET请求只能进行url编码，而POST支持多种编码方式。
- GET请求参数会被完整保留在浏览器历史记录里，而POST中的参数不会被保留。
- GET请求在URL中传送的参数是有长度限制的，而POST么有。
- 对参数的数据类型，GET只接受ASCII字符，而POST没有限制。
- GET比POST更不安全，因为参数直接暴露在URL上，所以不能用来传递敏感信息。
- GET参数通过URL传递，POST放在Request body中。

### 

### 深层次

- GET产生一个TCP数据包
  - 浏览器会把 `http header` 和 `data` 一并发送出去，服务器响应200（返回数据）
- POST产生两个TCP数据包
  - 浏览器先发送 `header`，服务器响应100 continue，浏览器再发送 `data`，服务器响应200 ok

## HTTP中Get、Post、Put与Delete的区别

- https://blog.csdn.net/haif_city/article/details/78333213

1、GET 请求会向数据库发**索取数据**的请求，从而来获取信息，该请求就像数据库的select操作一样，只是用来查询一下数据，不会修改、增加数据，不会影响资源的内容，即该请求不会产生副作用。无论进行多少次操作，结果都是一样的。

2、与GET不同的是，PUT请求是向服务器端发送数据的，从而改变信息，该请求就像数据库的update操作一样，用来修改数据的内容，但是不会增加数据的种类等，也就是说无论进行多少次PUT操作，其结果并没有不同。

3、POST请求同PUT请求类似，都是向服务器端发送数据的，但是该请求会改变数据的种类等资源，就像数据库的insert操作一样，会创建新的内容。几乎目前所有的提交操作都是用POST请求的。

4、DELETE请求顾名思义，就是用来删除某一个资源的，该请求就像数据库的delete操作。

就像前面所讲的一样，既然PUT和POST操作都是向服务器端发送数据的，那么两者有什么区别呢。。。POST主要作用在一个集合资源之上的（url），而PUT主要作用在一个具体资源之上的（url/xxx），通俗一下讲就是，如URL可以在客户端确定，那么可使用PUT，否则用POST。

综上所述，我们可理解为以下：

1、POST /url 创建 
2、DELETE /url/xxx 删除 
3、PUT /url/xxx 更新
4、GET /url/xxx 查看



## Q3. What is Request Dispatcher?

RequestDispatcher interface is used to **forward the request to another resource** that can be HTML, JSP or another servlet in same application. We can also use this to include the content of another resource to the response.

There are two methods defined in this interface:

1. void forward()
2. void include()

![ForwardMethod - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Forward-Method.png)![IncludeMethod - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Include-Method.png)



## Q4. What are the differences between forward() method and sendRedirect() methods?

| **forward() method**                                         | **SendRedirect() method**                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `forward()` sends the **same request** to **another resource**. | `sendRedirect()` method sends **new request** always because it uses the URL bar of the browser. |
| forward() method works at **server side**.                   | sendRedirect() method works at **client side**.              |
| forward() method works within the server only.               | sendRedirect() method works within and outside the server.   |

- **请求转发 forward**（服务器）：

  - 转发做了一次请求，浏览器的地址栏一直是第一次请求的地址。转发是服务器内部 `request/response` 控制权的移交。
  - 转发的源组件与目标组件必须在同一个应用中，两者可以在 `request` 范围内共享数据。
  - 浏览器发出 `http` 求其 --> 服务器接收请求 --> 服务器调用内部的一个方法在容器内完成请求处理和转发动作 --> 将客户所需资源发送到浏览器
  - `request.getRequestDispatcher("test.jsp").forward(request,response);  //转发到test.jsp`

- **重定向 sendRedirect** （客户端）：

  - 重定向行为是做了两次请求，即产生了两个 `request` 对象，重定向会导致request对象信息丢失。
  - web组件可以将请求重定向到任意一个url，而不仅仅是同一个应用。重定向的源组件与目标组件不共用同一个 `HttpServletRequest` 对象，因此不能在 `request` 范围内共享数据。
  - 浏览器发出 `http` 请求 --> 服务器接受请求并发送 `302` 状态码和新的对应的 `url` 到浏览器 --> 浏览器接收响应并自动请求新的 `url` --> 服务器接收请求并寻找客户所需的资源响应到浏览器
  - `response.sendRedirect("test.jsp");  //重定向到test.jsp`

  

## Q5. What is the life-cycle of a servlet?

![LifeCycleServlet - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Life-Cycle-Servlet-300x284.png)

1. Servlet is loaded
2. Servlet is instantiated
3. Servlet is initialized
4. Service the request
5. Servlet is destroyed



## Q6. How does cookies work in Servlets?

- Cookies are text data **sent by server to the client** and it gets **saved at the client local machine**.
- Servlet API provides cookies support through `javax.servlet.http.Cookie` class that implements Serializable and Cloneable interfaces.
- `HttpServletRequest getCookies()` method is provided to **get the array of Cookies from request**, since there is no point of adding Cookie to request, there are no methods to set or add cookie to request.
- Similarly `HttpServletResponse addCookie(Cookie c)` method is provided to **attach cookie in response header**, there are no getter methods for cookie.



## Q7. What are the differences between ==ServletContext vs ServletConfig==?

The difference between ServletContext and ServletConfig in Servlets JSP is in below tabular format.

| **ServletConfig**                                            | **ServletContext**                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Servlet config object represent single servlet               | It represent whole web application running on particular JVM and common for all the servlet |
| Its like local parameter associated with particular servlet  | Its like global parameter associated with whole application  |
| It’s a name value pair defined inside the servlet section of web.xml file so it has servlet wide scope | ServletContext has application wide scope so define outside of servlet tag in web.xml file. |
| getServletConfig() method is used to get the config object   | getServletContext() method is  used to get the context object. |
| for example shopping cart of a user is a specific to particular user so here we can use servlet config | To get the MIME type of a file or application session related information is stored using servlet context object. |



#### 含义

- **ServletConfig** ：
  - Servlet的配置对象，容器在初始化的时候通过它传递信息给 `Servlet`
  - 创建时期：在容器初始化 `Servlet` 的时候，并为其提供上下文初始化参数的名/值对的引用。
  - 作用范围：每个 `JVM` 中每个 `Web` 应用一个`ServletContext`
- **ServletContext**：
  - 上下文对象，提供了一系列方法提供 `Servlet` 与 `Web` 容器交互
  - 创建时期：容器启动的时候，并为其提供 `Servlet` 初始化参数的名/值对的引用
  - 作用范围：每个 `JVM` 中每个Web应用的每个 `Servlet` 一个 `ServletConfig`。



## Q8. What are the different methods of session management in servlets?

Session is a **conversational state between client and server** and it can consists of **multiple request and response** between client and server. Since **HTTP** and **Web Server** both are **stateless** （无状态）, the only way to **maintain** a session is when some unique information about the session (session id) is passed between server and client in every request and response.

Some of the common ways of session management in servlets are:

1. User Authentication
2. HTML Hidden Field
3. Cookies
4. URL Rewriting
5. Session Management API



![SessionManagement - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Session-management.png)



### 起因

Cookie是有大小限制和数量限制的，并且越来越多的Cookie代表客户端和服务器的传输量增加，可不可以每次传的时候不传所有cookie值，而只传一个唯一ID，通过这个ID直接在服务器查找用户信息呢？答案是有的，这就是我们的session。

**Session 是基于 Cookie 来工作的**，同一个客户端每次访问服务器时，只要当浏览器在第一次访问服务器时，服务器设置一个id并保存一些信息(例如登陆就保存用户信息，视具体情况)，并把这个id通过Cookie存到客户端，客户端每次和服务器交互时只传这个id，就可以实现维持浏览器和服务器的状态，而这个ID通常是NAME为JSESSIONID的一个Cookie。

### 核心

**Session** 技术则是**服务端**的解决方案，它是通过服务器来**保持状态**的。

- 首先，我们通常都会把 `Session` 翻译成会话，因此我们可以把客户端浏览器与服务器之间一系列交互的动作称为一个 `Session`。从这个语义出发，我们会提到 `Session` 持续的时间，会提到在 `Session` 过程中进行了什么操作等等
- 其次，`Session` 指的是服务器端为客户端所开辟的存储空间，在其中保存的信息就是用于保持状态。从这个语义出发，我们则会提到往 Session 中存放什么内容，如何根据键值从 `Session` 中获取匹配的内容等。
- `Java` 中是通过调用 `HttpServletRequest` 的 `getSession` 方法（使用 `true` 作为参数）创建的
- 在创建了 `Session` 的同时，**服务器**会为该 `Session` 生成唯一的 **Session id** ，而这个**Session id** 在随后的请求中会被用来 **重新获得已经创建的Session**
- 在 `Session` 被创建之后，就可以调用 `Session` 相关的方法往 `Session` 中增加内容了，而这些内容只会保存在服务器中，**发到客户端的只有 Session id**
- 当客户端再次发送请求的时候，会将这个`Session id`带上，服务器接受到请求之后就会依据 `Session id` 找到相应的 `Session`，从而再次使用
- 客户端每次请求都会把这个 **Session id** 值放到 **http 请求的头部 **发送给 服务端，而这个 `Session id` 值**在客户端会保存**下来，保存的容器就是 **cookie**



### 二者的异同

相同点(有关系的地方)：

- `Session` 和 `Cookie` 都是为了让 `http` 协议有状态而存在
- `Session` 通过 `Cookie` 工作，`Cookie` 传输的 `SessionID` 让 `Session` 知道这个客户端到底是谁

不同点：

- `Session` 将信息保存到**服务器**，`Cookie` 将信息保存在**客户端**



# ==**JDBC – Java Interview Questions**== 

## Q1. What is JDBC Driver?

JDBC Driver is a software component that enables java application to interact with the database. There are 4 types of JDBC drivers:

1. JDBC-ODBC bridge driver
2. Native-API driver (partially java driver)
3. Network Protocol driver (fully java driver)
4. Thin driver (fully java driver)

![img](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/JDBC.png)



## Q2. What are the steps to connect to a database in java?

- Registering the driver class
- Creating connection
- Creating statement
- Executing queries
- Closing connection



## Q3. What are the JDBC API components?

The `java.sql` package contains interfaces and classes for JDBC API.

### **Interfaces:**

- Connection
- Statement
- PreparedStatement
- ResultSet
- ResultSetMetaData
- DatabaseMetaData
- CallableStatement etc.

### **Classes:**

- DriverManager
- Blob
- Clob
- Types
- SQLException etc.



## Q4. What is the role of JDBC DriverManager class?

The DriverManager *class* manages the registered drivers. It can be used to **register and unregister** drivers. It provides factory method that **returns the instance of Connection**.



## Q5. What is ==JDBC Connection== interface?

The Connection interface **maintains a session** with the database. It can be used for **transaction management**. It provides factory methods that returns the instance of Statement, PreparedStatement, CallableStatement and DatabaseMetaData.

![ConnectionInterface - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Connection-interface.png)



## Q6.  What is the purpose of ==JDBC ResultSet== interface?

The ResultSet object represents a row of a table. It can be used to change the cursor pointer and get the information from the database.



## Q7. What is JDBC ResultSetMetaData interface?

The `ResultSetMetaData` interface **returns the information of table** such as `total number of columns, column name, column type` etc.



## Q8. What is JDBC DatabaseMetaData interface?

The `DatabaseMetaData` interface returns the **information of the database** such as `username, driver name, driver version, number of tables, number of views` etc.



## Q9. What do you mean by batch processing in JDBC?

Batch processing helps you to group related SQL statements into a batch and execute them instead of executing a single query. By using batch processing technique in JDBC, you can **execute multiple queries** which makes the performance faster.



## Q10. What is the difference between execute, executeQuery, executeUpdate?

Statement **execute(String query)** is used to execute any SQL query and it returns TRUE if the result is an ResultSet such as running **Select** queries. The output is FALSE when there is no ResultSet object such as running Insert or Update queries. We can use *getResultSet()* to get the ResultSet and *getUpdateCount()* method to retrieve the update count.

Statement **executeQuery(String query)** is used to execute **Select** queries and returns the ResultSet. ResultSet returned is never null even if there are no records matching the query. When executing **select** queries we should use executeQuery method so that if someone tries to execute insert/update statement it will throw java.sql.SQLException with message “executeQuery method can not be used for update”.

Statement **executeUpdate(String query)** is used to execute **Insert/Update/Delete (DML)** statements or DDL statements that returns nothing. The output is int and equals to the row count for SQL Data Manipulation Language (DML) statements. For DDL statements, the output is 0.

You should **use execute() method only when you are not sure about the type of statement** else use **executeQuery** or **executeUpdate** method.



## Q11. What do you understand by JDBC Statements?

JDBC statements are basically the statements which are used to **send SQL commands to the database and retrieve data back from the database** (发送SQL命令到数据库，并从数据库检索数据). Various methods like `execute()`, `executeUpdate()`, `executeQuery()`, etc. are provided by JDBC to interact with the database.

JDBC supports 3 types of statements:

1. *Statement:* Used for general purpose access to the database and executes a static SQL query at runtime.
2. *PreparedStatement:* Used to provide input parameters to the query during execution.
3. *CallableStatement:* Used to access the database stored procedures and helps in accepting runtime parameters.



# ==**Spring Framework – Java Interview Questions**== 

## Q1. What is Spring?

Wikipedia defines the Spring framework as “an application framework and **inversion of control** container for the Java platform. The framework’s core features can be used by any Java application, but there are extensions for building web applications on top of the Java EE platform.” Spring is essentially a lightweight, integrated framework that can be used for developing enterprise applications in java.



## Q2. Name the different modules of the Spring framework.

Some of the important Spring Framework modules are:

- Spring Context – for dependency injection.
- Spring AOP – for aspect oriented programming.
- Spring DAO – for database operations using DAO pattern
- Spring JDBC – for JDBC and DataSource support.
- Spring ORM – for ORM tools support such as Hibernate
- Spring Web Module – for creating web applications.
- Spring MVC – Model-View-Controller implementation for creating web applications, web services etc.

![SpringFramework - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Spring-Framework-Java.png)



## Q3. List some of the important annotations in annotation-based Spring configuration.

The important annotations are:

- @Required
- @Autowired
- @Qualifier
- @Resource
- @PostConstruct
- @PreDestroy



## Q4. Explain Bean in Spring and List the different Scopes of Spring bean.

Beans are objects that **form the backbone of a Spring application**. They are **managed by the Spring IoC container**. In other words, a bean is an object that is instantiated, assembled, and managed by a Spring IoC container.

There are five Scopes defined in Spring beans.

![SpringBean - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Scopes-of-bean.png)

- **Singleton**: Only one instance of the bean will be created for each container. This is the default scope for the spring beans. While using this scope, make sure spring bean doesn’t have shared instance variables otherwise it might lead to data inconsistency issues because it’s not thread-safe.
- **Prototype**: A new instance will be created every time the bean is requested.
- **Request**: This is same as prototype scope, however it’s meant to be used for web applications. A new instance of the bean will be created for each HTTP request.
- **Session**: A new bean will be created for each HTTP session by the container.
- **Global-session**: This is used to create global session beans for Portlet applications.



## Q5. Explain the role of DispatcherServlet and ContextLoaderListener.

**DispatcherServlet** is basically the front controller in the Spring MVC application as it **loads the spring bean configuration file** and **initializes all the beans that have been configured**. If annotations are enabled, it also scans the packages to **configure any bean annotated** with `@Component`, `@Controller`, `@Repository` or `@Service` annotations.

**![DispatcherServlet - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Dispatcher-Servlet.png)ContextLoaderListener,** on the other hand, is the listener to start up and shut down the **WebApplicationContext** in Spring root. Some of its important functions includes tying up the lifecycle of Application Context to the lifecycle of the ServletContext and automating the **creation of ApplicationContext**.

![ContextLoader - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/ContextloaderListener-528x201.png)



## Q6. What are the differences between constructor injection and setter injection?

| **No.** | **Constructor Injection**                         | **Setter Injection**                                         |
| ------- | ------------------------------------------------- | ------------------------------------------------------------ |
| 1)      | No Partial Injection                              | Partial Injection                                            |
| 2)      | Doesn’t override the setter property              | Overrides the constructor property if both are defined.      |
| 3)      | Creates a new instance if any modification occurs | Doesn’t create a new instance if you change the property value |
| 4)      | Better for too many properties                    | Better for a few properties.                                 |



## **Q7. What is autowiring in Spring? What are the autowiring modes?**

Autowiring enables the programmer to **inject the bean automatically**. We don’t need to write explicit injection logic. Let’s see the code to inject bean using dependency injection.

- `<bean id="emp" class="com.javatpoint.Employee" autowire="byName" />`  

The autowiring modes are given below:

| **No.** | **Mode**    | **Description**                                              |
| ------- | ----------- | ------------------------------------------------------------ |
| 1)      | no          | this is the default mode, it means autowiring is not enabled. |
| 2)      | byName      | Injects the bean based on the property name. It uses setter method. |
| 3)      | byType      | Injects the bean based on the property type. It uses setter method. |
| 4)      | constructor | It injects the bean using constructor                        |



## Q8. How to handle exceptions in Spring MVC Framework?

Spring MVC Framework provides the following ways to help us achieving robust exception handling.

### **Controller Based:**

We can define exception handler methods in our controller classes. All we need is to annotate these methods with `@ExceptionHandler` annotation.

### **Global Exception Handler:**

Exception Handling is a cross-cutting concern and Spring provides `@ControllerAdvice` annotation that we can use with any class to define our global exception handler.

### **HandlerExceptionResolver implementation:** 

For generic exceptions, most of the times we serve static pages. Spring Framework provides `HandlerExceptionResolver` interface that we can implement to create **global exception handler**. The reason behind this additional way to define global exception handler is that Spring framework also provides default implementation classes that we can define in our spring bean configuration file to get spring framework exception handling benefits.



## Q9. What are some of the important Spring annotations which you have used?

Some of the Spring annotations that I have used in my project are:

- **@Controller** – for controller classes in Spring MVC project.
- **@RequestMapping** – for configuring URI mapping in controller handler methods. This is a very important annotation, so you should go through Spring MVC RequestMapping Annotation Examples
- **@ResponseBody** – for sending Object as response, usually for sending XML or JSON data as response.
- **@PathVariable** – for mapping dynamic values from the URI to handler method arguments.
- **@Autowired** – for autowiring dependencies in spring beans.
- **@Qualifier** – with @Autowired annotation to avoid confusion when multiple instances of bean type is present.
- **@Service** – for service classes.
- **@Scope** – for configuring the scope of the spring bean.
- **@Configuration, @ComponentScan and @Bean** – for java based configurations.

AspectJ annotations for configuring aspects and advices , 

- @Aspect
- @Before
- @After
- @Around
- @Pointcut



## Q10. How to integrate Spring and Hibernate Frameworks?

We can use Spring ORM module to integrate Spring and Hibernate frameworks if you are using Hibernate 3+ where SessionFactory provides current session, then you should avoid using HibernateTemplate or HibernateDaoSupport classes and better to use DAO pattern with dependency injection for the integration.

Also, Spring ORM provides support for using Spring declarative transaction management, so you should utilize that rather than going for hibernate boiler-plate code for transaction management. 



## Q11. Name the types of transaction management that Spring supports.

Two types of transaction management are supported by Spring. They are:

1. **Programmatic transaction management:** In this, the transaction is managed with the help of programming. It provides you extreme flexibility, but it is very difficult to maintain.
2. **Declarative transaction management:** In this, transaction management is separated from the business code. Only annotations or XML based configurations are used to manage the transactions.



# ==**Hibernate – Java Interview Questions**==

## Q1. What is Hibernate Framework?

**Object-relational mapping or ORM** is the programming technique to map **application domain model objects** to the **relational database tables**. Hibernate is Java-based ORM tool that provides a framework for mapping application domain objects to the relational database tables and vice versa.

Hibernate provides a reference implementation of Java Persistence API, that makes it a great choice as ORM tool with benefits of **loose coupling**. We can use the Hibernate persistence API for CRUD operations. Hibernate framework provide option to map plain old java objects to traditional database tables with the use of JPA annotations as well as XML based configuration.

Similarly, hibernate configurations are flexible and can be done from XML configuration file as well as programmatically.



## Q2. What are the important benefits of using Hibernate Framework?

Some of the important benefits of using hibernate framework are:

1. Hibernate eliminates all the boiler-plate code (样板代码) that comes with JDBC and takes care of managing resources, so we can focus on business logic.
2. Hibernate framework provides support for XML as well as JPA annotations, that makes our code implementation independent.
3. Hibernate provides a powerful query language (HQL) that is similar to SQL. However, **HQL is fully object-oriented** and understands concepts like inheritance, polymorphism, and association.
4. Hibernate is an open source project from **Red Hat Community** and used worldwide. This makes it a better choice than others because learning curve is small and there are tons of online documentation and help is easily available in forums.
5. Hibernate is easy to integrate with other Java EE frameworks, it’s so popular that Spring Framework provides built-in support for integrating hibernate with Spring applications.
6. Hibernate supports lazy initialization using proxy objects and perform actual database queries only when it’s required.
7. Hibernate cache helps us in getting better performance.
8. For database vendor specific feature, hibernate is suitable because we can also execute native sql queries.

Overall hibernate is the best choice in current market for ORM tool, it contains all the features that you will ever need in an ORM tool.



## Q3. Explain Hibernate architecture.

Hibernate has a **layered architecture** which helps the user to operate without having to know the underlying APIs. Hibernate makes use of the database and configuration data to provide persistence services (and persistent objects) to the application. It includes many objects such as persistent object, session factory, transaction factory, connection factory, session, transaction etc.

![HibernateArchitecture - Java Interview Questions - Edureka](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/04/Hibernate-Architecture.png)

The Hibernate architecture is categorized in four layers.

- Java application layer
- Hibernate framework layer
- Backhand API layer
- Database layer



## Q4. What are the differences between get and load methods?

The differences between `get()` and `load()` methods are given below.

| **No.** | **get()**                                                    | **load()**                                                  |
| ------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| 1)      | Returns null if object is not found.                         | Throws ObjectNotFoundException if an object is not found.   |
| 2)      | get() method always **hit the database**.                    | load() method doesn’t hit the database.                     |
| 3)      | It returns a real object, not a proxy.                       | It returns a proxy object.                                  |
| 4)      | It should be used if you are not sure about the existence of instance. | It should be used if you are sure that the instance exists. |



## Q5. What are the advantages of Hibernate over JDBC?

Some of the important advantages of Hibernate framework over JDBC are:

1. Hibernate removes a lot of boiler-plate code that comes with JDBC API, the code looks cleaner and readable.
2. Hibernate supports **inheritance, associations, and collections**. These features are not present with JDBC API.
3. Hibernate implicitly provides **transaction management**, in fact, most of the queries can’t be executed outside transaction. In JDBC API, we need to write code for transaction management using commit and rollback. 
4. JDBC API throws SQLException that is a checked exception, so we need to write a lot of try-catch block code. Most of the times it’s redundant in every JDBC call and used for transaction management. Hibernate wraps JDBC exceptions and throw **JDBCException** or HibernateException un-checked exception, so we don’t need to write code to handle it. Hibernate built-in transaction management removes the usage of try-catch blocks.
5. **Hibernate Query Language (HQL)** is more **object-oriented** and close to Java programming language. For JDBC, we need to write native SQL queries.
6. Hibernate supports caching that is better for performance, JDBC queries are not cached hence performance is low.
7. Hibernate provides option through which we can create database tables too, for JDBC tables must exist in the database.
8. Hibernate configuration helps us in using JDBC like connection as well as JNDI DataSource for the connection pool. This is a very important feature in enterprise application and completely missing in JDBC API.
9. Hibernate supports JPA annotations, so the code is independent of the implementation and easily replaceable with other ORM tools. JDBC code is very tightly coupled with the application.

