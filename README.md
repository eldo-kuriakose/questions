## Basic level interview questions

### Java

#### What is the difference between JVM and JRE?

Java Runtime Environment (JRE) is the implementation of JVM. JRE consists of JVM and java binaries and other classes to execute any program successfully. JRE doesn’t contain any development tools like java compiler, debugger etc. If you want to execute any java program, you should have JRE installed.

#### What is the importance of main method in Java?

main() method is the entry point of any standalone java application. The syntax of main method is 
public static void main(String args[]).

main method is public and static so that java can access it without initializing the class. The input parameter is an array of String through which we can pass runtime arguments to the java program. 

#### What is overloading and overriding in java?

When we have more than one method with same name in a single class but the arguments are different, then it is called as method overloading.

Overriding concept comes in picture with inheritance when we have two methods with same signature, one in parent class and another in child class. We can use @Override annotation in the child class overridden method to make sure if parent class method is changed, so as child class.

#### What are access modifiers?

Java provides access control through public, private and protected access modifier keywords. When none of these are used, it’s called default access modifier.
A java class can only have public or default access modifier

#### What is finally and finalize in java?

finally block is used with try-catch to put the code that you want to get executed always, even if any exception is thrown by the try-catch block. finally block is mostly used to release resources created in the try block.

finalize() is a special method in Object class that we can override in our classes. This method get’s called by garbage collector when the object is getting garbage collected

#### Can we declare a class as static?

We can’t declare a top-level class as static however an inner class can be declared as static. If inner class is declared as static, it’s called static nested class.
Static nested class is same as any other top-level class and is nested for only packaging convenience.

#### What is try-with-resources in java?

One of the Java 7 features is try-with-resources statement for automatic resource management. Before Java 7, there was no auto resource management and we should explicitly close the resource. Usually, it was done in the finally block of a try-catch statement. This approach used to cause memory leaks when we forgot to close the resource.

#### What is Marker interface?

A marker interface is an empty interface without any method but used to force some functionality in implementing classes by Java. Some of the well known marker interfaces are Serializable and Cloneable.

#### What is composition in java?

Composition is the design technique to implement has-a relationship in classes. We can use Object composition for code reuse.

#### What is the benefit of Composition over Inheritance?

* Any change in the superclass might affect subclass even though we might not be using the superclass methods.
* Inheritance exposes all the super class methods and variables to client and if we have no control in designing superclass, it can lead to security holes. Composition allows us to provide restricted access to the methods and hence more secure.
* We can get runtime binding in composition where inheritance binds the classes at compile time

#### How to sort a collection of custom Objects in Java?

We need to implement Comparable interface to support sorting of custom objects in a collection

#### What is inner class in java?

We can define a class inside a class and they are called nested classes. Any non-static nested class is known as inner class. Inner classes are associated with the object of the class and they can access all the variables and methods of the outer class. Since inner classes are associated with instance, we can’t have any static variables in them.

#### What is Classloader in Java?

Java Classloader is the program that loads byte code program into memory when we want to access any class. 

#### What is Garbage Collection?

Garbage Collection is the process of looking at heap memory, identifying which objects are in use and which are not, and deleting the unused objects.

#### What is Serialization and Deserialization?

We can convert a Java object to an Stream that is called Serialization. Once an object is converted to Stream, it can be saved to file or send over the network or used in socket connections.

The object should implement Serializable interface and we can use java.io.ObjectOutputStream to write object to file or to any OutputStream object.

The process of converting stream data created through serialization to Object is called deserialization. 


#### What is difference between Heap and Stack Memory?

* Heap memory is used by all the parts of the application whereas stack memory is used only by one thread of execution.
* Whenever an object is created, it’s always stored in the Heap space and stack memory contains the reference to it. Stack memory only contains local primitive variables and reference variables to objects in heap space.



### Functional Programing

A functional approach involves composing the problem as a set of functions to be executed. A programmer define the input to each function, and what each function returns. Funtions are self-contained and stateless and they do not rely on any external state.

### Scala


#### What are the Scala Features?

* Supports both OOP-style(Imperative-Style) and Functional-Style Programming
* Pure Object-Oriented Programming Language
* Supports all Functional Features
* REPL(Read-Evaluate-Print Loop) Interpreter
* Strong Type System
* Statically-Typed Language
* Type Inference
* Supports Pattern Matching
* Supports Closures
* Supports Persistent Data Structures
* Uses Actor Model to develop Concurrency Applications
* Interoperable with Java

#### Like Java’s java.lang.Object class, what is the super class of all classes in Scala?

As we know in Java, the super class of all classes (Java API Classes or User Defined Classes) is java.lang.Object. In the same way in Scala, the super class of all classes or traits is “Any” class.

Any class is defined in scala package like “scala.Any”.

#### What is default access modifier in Scala? Does Scala have “public” keyword?

In Scala, if we don’t mention any access modifier to a method, function, trait, object or class, the default access modifier is “public”. Even for Fields also, “public” is the default access modifier.

Because of this default feature, Scala does not have “public” keyword.

#### What is trait in Scala?

Traits are collections of fields and behaviors that you can extend or mix into your classes. It’s a component of a class, not a class by itself, so there is no constructor, trait is restricted in comparison to class to prevent multiple inheritance problems.


#### What is difference between map and flatMap ?

Map is a method that apply a function on all elements , it returns the associated value in a Some. Where as flatMap also same, but it returns a sequence for each element in the list.


Eg: val l = List(“Computer”, “Keyboard”, “Mouse”, “Monitor”)
l.map(_.toUpperCase) //Returns COMPUTER, KEYBOARD, MOUSE, MONITOR
l.flatMap(_.toUpperCase) //Returns C,O,M,P,U,T,E,R,K,E,Y,B,O,A,R,D,M,O,U,S,E,M,O,N,I,T,O,R

What is Case Class importance in scala?

Depending on constructor arguments, case class generate an immutable data-holding objects.

 * Case classes can be pattern matched
 * Case classes automatically define hashcode and equals
 * Case classes automatically define getter methods for the constructor arguments.
 
Explain few collections in Scala?

* Array:List same type element, it’s mutable.
* list: List same type elements, its immutable.
* sets: have no duplicates
* tuple: A tuple groups together simple logical collections of items without using a class.


