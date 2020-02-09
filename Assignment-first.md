## Anonymous array in JAVA
An array in Java without any name is anonymous array. It is an array just for creating and using instantly.

We can create an array without name, such type of nameless arrays are called *anonymous array*.
The main **purpose** of anonymous array is just for instant use (just for one time usage) .
Anonymous array is passed as an argument of method.

Syntax :
new int[] { 1, 2, 3, 4};  //int type anonymous array

An example to illustrate the concept of anonymous array is given below :

class Test { <br/>
    public static void main(String[] args) <br/>
    { </br>
        sum(new int[]{ 1, 2, 3 });  //anonymous array
    } </br>
    public static void sum(int[] a) <br/>
    { <br/>
        int total = 0; <br/>
          for (int i : a) { <br/>
            total = total + i; <br/>
         System.out.println("The sum is:" + total); <br/>
    } <br/>
  }


## Default method in Interface
Interface could only have abstract method before Java8, so implementation of a new method done in interface have to be provided in implementing class too.So, to overcome the problem,default methods were used. 
For example : <br/>
<br/>
interface default_interface <br/>
{ <br/>
  public void cube(int a); <br/>
  default void show() <br/>
  { <br/>
    system.out.println ("Default method"); <br/>
  } <br/>
} <br/>
class default_class implements default_interface <br/>
{ <br/>
  public void cube(int a) <br/>
  { <br/>
    System.out.prinln(a * a * a); <br/>
  } <br/>
  public static void main(String[] a) <br/>
  { <br/>
    DefaultClass d = new DefaultClass(); <br/>
    d.cube(); <br/>
    d.show(); <br/>
  } <br/>
} <br/>



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
For example:<br/> 
<br/>
interface NestedA <br/>
{ <br/>
  void dis(); <br/>
  interface NestedB <br/>
  { <br/>
    void show(); <br/>
  } <br/>
} <br/>
class Test implements NestedA NestedB <br/>
{ <br/>
  void show() <br/>
  { <br/>
    System.out.println("Nested interface"); <br/>
  } <br/>
  public static void main (String[] args) <br/>
  { <br/>
    NestedA.NestedB ob = new Test(); <br/>
    ob.show(); <br/>
  } <br/>
} <br/>



## How to create your own exception class ?
Sometimes we need to design our own exceptions as per the application requirement. This is possible in Java.

All exceptions must be  child of Throwable. If we want to write a checked exception that is automtically enforced by the handle, we need to extend the Exception class. If we want to write a runtime exception, we need to extend the RuntimeException class. We can define our own exception class as below: <br/> 
<br/>
class MyException extends Exception{ <br/>
} <br/>
<br/>
*Example:* <br/>
class NoException extends Exception <br/>
{ <br/>
  NoException (String s) <br/>
  { <br/>
    super (s); <br/>
  } <br/>
} <br/>
class TestException <br/>
{ <br/>
  static void checkStudent(String college) throws NonException <br/>
  { <br/>
    if (college != "GCES") <br/>
    throw new NonException ("Not a GCES student"); <br/>
    else <br/>
    System.out.println ("Welcome to GCES"); <br/>
  } <br/>
  public static void main (String args[]) <br/>
  { <br/>
    try <br/>
    { <br/>
    checkStudent( "PEC"); <br/>
    } <br/>
    catch(Exception e) <br/>
    { <br/>
      System.out.println("Exception occured: "+ e); <br/>
    } <br/>
    System.out.println("END"); <br/>
  } <br/>
} <br/>



## Difficult Questions : 

1. Explain about *Access Protection Mechanism* with suitable example. <br/>
2. Write short notes on: *Casting Astract class*. 
       





