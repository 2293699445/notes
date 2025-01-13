# Java Basic Knowledge

## 1、Basic Syntax

* ### **Data** **Type**

  * (1) <u>computer storage unit</u>

    <img src="D:\snipateImg\Snipaste_2024-10-22_11-02-59.png" style="zoom:50%;" />

    ​	                                                             bit byte kilobyte megabyte gigabyte terabyte

  * (2) <u>data type of java</u>

    * basic type

      * numerical type

        ​	byte short int long float double char 

      * non-numerical type

        ​	boolean

    * reference type

      ​	class interface array	

* ### **Variable** 

  * <u>attention in using variable</u> 

    <img src="C:\Users\19625\AppData\Roaming\Typora\typora-user-images\image-20241022112534495.png" alt="image-20241022112534495" style="zoom:50%;" />

    ​                    "double-->float" may cause precision loss, because the precision and range of "float" is smaller than that of double.

  * <u>some naming conventions</u> 

    * Upper Camel Case: the first letter of each word is capitalized.

      ​	 name of **class**

    * Lower Camel Case:

      ​	name of **variable** and **method**

  * <u>type conversion</u> 

    * automatic conversion
      * a value or variable with a small data range is assigned to a large.
    * forced conversion 
      * a value or variable with a large data range is assigned to a small
      * format: int num1 = (int) num2
      * statement: operation between type of byte,short and char will be conversed to type of int.

* ### **Operator** 

  * <u>"+" operator</u>

    * between value

      ​	the operation result is a value.

    * between char 

      ​	the operation result is a value.

    * between String

      ​	the operation result is a String.(<u>even if "+" operator is used between a value and a string, the result is still a string</u>)

  * ternary operator

    * format: (judgement)?action1:action2

      ​	when the result of judgement is true, action1 will be activated

      ​	when the result of judgement is false, action2 will be activated

* ### **Import Data** 

  * <u>step</u>:

     1. import package

        ​	`import java.util.Scanner `

     2. create object 

        ​	`Scanner sc1 = new Scanner(System.in)`

     3. accept data 

        ​	`int i = sc1.nexInt()`

        ​	the expression mean that the content imputed from keyboard is seem as a int value. 

* ### **Array**

  * initialize array statically 

    ​	format: type[ ] arrayName = new type[ ]{value1,value2,value3}   or   type[ ] arrayName = {value1,value2,value3 } 

  * <u>initialize array dynamically</u>

    ​	type[ ] arrayName = new type[ length] , arrayName[index] = num

* ### **Method**

  * override 
    * 
  * overload
    * different: number,location and type of method 
    * identical: method name, return type 

* ### **Object-Oriented-Base**(create object , use method)

  * encapsulation
    * define: what an object represents, it has to encapsulate the corresponding data and provide the corresponding behaviors of the data.
    * "this" and "the principle of nearness"
    * constructor 
    * standard JavaBean 
      * name(class) 
      * private(member variables)
      * constructor(empty & all)
      * setter and getter method
  * differ between member variables and local
    * location in class
    * initialized value 
    * location in memory 
    * life cycle 
    * scope 
  * keyword: "this" 
    * function: differentiate between member variables and local(the principle of nearness). 
    * theory: the address value of caller of the method where it is located.

* ### **String Class** 

  * two method in creating String object

    * directly assign

      ​	String name="燕双鹰"

    * new String object

      ​	String name = new String() 

      ​	String name = new String("string")

      ​	String name = new String(char[ ] chs)

      ​	String name = new String(byte[ ] chs)

  * StringTable

    * the string object by directly assigning will be saved in StringTable.
    * when assigning directly with double quotation marks, the system will check whether the string exists in the StringTable.
    
  * some operations on the string

    * compare
    * traverse
    * join
    * reverse
    * extract characters
    * replace

* ### **Collection**

  * Single Column Collection---"Collection Class"

    * method of Collection

      1. public boolean add(E e): add an element
      2. public void clear(): clear all 
      3. public boolean remove(E e): remove an specified element.
      4. public boolean contains(Object obj): to determine whether an element is contained in the collection.
      5. public boolean is Empty()
      6. public int size(): return the length of the collection.

    * The Way Of Traversing The Collection.

      1. iterator

         * how to get a iterator?

           Iterator<generics> <u>param</u> = collecName.iterator()

         * method of iterator

           boolean hasNext(): to determine whether current location have the element.

           E next(): to obtain the element of current location and move the iterator object to the next location.

      2. enhanced for

         `````` java
         for(String s : list){  //the s stand for each element in collection.
             System.out.println(s);
         }
         ``````

      3. lambda expression

         * Lambda Introduce 

           * function

             simplify writing style of anonymous inner class of functional interface.

           * premise

             must be a anonymous inner class of interface(not class),only possess a abstract method in the interface.

           * benefit

             this way of writing is simpler than the previous one.

           * more simple method of writing 

             1. the parameter type doesn't need to be written.
             2. if there is only a parameter, the parameter type and “()” doesn't need to be written.
             3. if there exists a line in method body in Lambda expression, "{}",";","return" can be ignored. 

         * Lambda traversal

           ``````java
           
           list.forEach(new consumer<String>(){
               public void accept(String t){
                   System.out.println(t);
               }
           }) //the parameter need to be a object of consumer<> class
           
           // lambda expression 
           list.forEach(t->System.out.println(t))
               
           ``````

    * List series:sequential,repeated,indexed

      1. ArrayList
      2. LinkedList

    * Set series:non-sequential,non-repeated,non-indexed

      1. HashSet
      2. TreeSet

  * Double Column Collection---"Map Class"

* ### **Object-Oriented-Advanced**

  * Keyword "static"
    * 1.static variable
      * feature
        * be **shared** by all objects in class.
        * belong to the class not object.
        * static variables exist prior to objects.
      * called way
        * the class name
        * objects name
    * 2.static method
    * 3.notes
      * static methods can only access static variables and methods.
      * non-static methods not only can access static variables and methods, but also non-static.
      * there is no "static" keyword in static methods.  

* API

  * Math

    * static int abs(int a):to gain absolute value of a.
    * static double ceil(double a):round up.
    * static double floor(double a):round down
    * static double round(float a): round 
    * static int max(int a,int b)：to obtain the larger value between the two.
    * static double pow(double a,double b):a to the power of b.
    * static double random():return a value of double,range 0.0 in 1.0(not contain 1.0).

  * System

    * static void exit():kill java virtual machine.
      * usage: System.exit(number) number(0 or 1) 
    * static long currentTimeMillis():return current system time(from 1970/01/01 08:00 to now).
    * static void arrayCopy():copy array.
      * usage: System.arrayCopy(sourceArr,index,targetArr,index,length)

  * Runtime

    * public static Runtime getRuntime(): to obtain an object of runtime.
    * public void exit(int status): kill java virtual machine.
    * public int availableProcessors():to obtain CPU threading number.
    * public long maxMemory(): the maximum memory that can be obtained by the JVM.
    * public long totalMemory(): the total memory obtained by the JVM.
    * public long freeMemory():remaining memory of JVM.
    * public Process exec(String command): run cmd commands.

  * Object

    * toString
    * equals
    * clone

  * Wrapper Class
  
    * define: 
  
    * Interger: 
  
      1. public static Integer valueOf(int i): create an Integer object according to an integer.
      2. public static Integer valueOf(String s): create  an String object according to a string.
      3. public static Integer valueOf(String s, int radix): create  an String object according to a string and radix.
  
      ``````java
      public static void main(String[] args){
          //manual boxing
          Integer i = Integer.valueOf(3);
          //manual unboxing
          int i1 = i.intValue();
      }
      ``````
  
      4. public static int parseInt(String s): convert the string type to integer type.
  
         ``````java
         //for example 
         int i = Integer.parseInt("123");  
         System.out.println(i);
         ``````
  
         
  
    
  
    ​	