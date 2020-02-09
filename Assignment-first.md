## Anonymous array in JAVA
An array in Java without any name is anonymous array. It is an array just for creating and using instantly.

We can create an array without name, such type of nameless arrays are called *anonymous array*.
The main **purpose** of anonymous array is just for instant use (just for one time usage) .
Anonymous array is passed as an argument of method.

Syntax :
new int[] { 1, 2, 3, 4};  //int type anonymous array

An example to illustrate the concept of anonymous array is given below :

class Test { 
    public static void main(String[] args) 
    { 
        sum(new int[]{ 1, 2, 3 });  //anonymous array
    } 
    public static void sum(int[] a) 
    { 
        int total = 0; 
          for (int i : a) { 
            total = total + i; 
         System.out.println("The sum is:" + total); 
    } 
  }
}



## Default method in Interface
Interface could only have abstract method before Java8, so implementation of a new method done in interface have to be provided in implementing class too.So, to overcome the problem,default methods were used. 
For example : <br/>
interface default_interface
{
  public void cube(int a);
  default void show()
  {
    system.out.println ("Default method");
  }
}
class default_class implements default_interface
{
  public void cube(int a)
  {
    System.out.prinln(a * a * a);
  }
  public static void main(String[] a)
  {
    DefaultClass d = new DefaultClass();
    d.cube();
    d.show();
  }
}



## Inheritance in interface
One interface can inherit another by use of the keyword **extends** . The synatx is the same as for inheriting classes. When a class implements an interface that inherits another
interface,it must provide implementations for all methods required by the interface inheritance chain.
For example :
interface InheritA
{
  void M1();
}
interface InheritB
{
  void M2();
}
class sample implements InheritA, InheritB
{
  public void M1()
  {
    System.out.println("Message M1");
  }
  public void M2()
  {
    System.out.println("Message M2");
  }
  public static void main (String[] a)
  {
    sample obj = new sample();
    obj.M1();
    obj.M2();
  }
}



## Nested Interfaces
The interface which is declared inside another interface or a class is known as ""nested interface"".A nested interface can be declared as public, private or protected. This differs from a top-level interface, which must either be declared as public or use the default access level, as previously described. It is used to resolve the namesop by grouping related interface together. When a nested interface is used outside of its enclosing scope, it must be qualified by the name of the class or interface of which it is a member.
For example:
interface NestedA
{
  void dis();
  interface NestedB
  {
    void show();
  }
}
class Test implements NestedA NestedB
{
  void show()
  {
    System.out.println("Nested interface")
  }
  public static void main (String[] args)
  {
    NestedA.NestedB ob = new Test();
    ob.show();
  }
} 



## How to create your own exception class ?
Sometimes we need to design our own exceptions as per the application requirement. This is possible in Java.

All exceptions must be  child of Throwable. If we want to write a checked exception that is automtically enforced by the handle, we need to extend the Exception class. If we want to write a runtime exception, we need to extend the RuntimeException class. We can define our own exception class as below: 

class MyException extends Exception{
}

*Example:*
class NoException extends Exception
{
  NoException (String s)
  {
    super (s);
  }
}
class TestException
{
  static void checkStudent(String college) throws NonException
  {
    if (college != "GCES")
    throw new NonException ("Not a GCES student");
    else
    System.out.println ("Welcome to GCES");
  }
  public static void main (String args[])
  {
    try
    {
      checkStudent( "PEC");
    }
    catch(Exception e)
    {
      System.out.println("Exception occured: "+ e);
    }
    System.out.println("END");
  }
}



## Difficult Questions : 

1. Explain about *Access Protection Mechanism* with suitable example. <br/>
<br/>
2. Write short notes on: *Casting Astract class*.       
       





