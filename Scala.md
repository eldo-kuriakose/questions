### Functional Programing
-------

A functional approach involves composing the problem as a set of functions to be executed. A programmer define the input to each function, and what each function returns. Funtions are self-contained and stateless and they do not rely on any external state.

## Scala
-----

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

#### What is Case Class importance in scala?

Depending on constructor arguments, case class generate an immutable data-holding objects.

 * Case classes can be pattern matched
 * Case classes automatically define hashcode and equals
 * Case classes automatically define getter methods for the constructor arguments.
 
#### Explain few collections in Scala?

* Array:List same type element, it’s mutable.
* list: List same type elements, its immutable.
* sets: have no duplicates
* tuple: A tuple groups together simple logical collections of items without using a class.
