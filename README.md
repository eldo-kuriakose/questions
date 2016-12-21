## Basic level interview questions

### Java

### Functional Programing

A functional approach involves composing the problem as a set of functions to be executed. A programmer define the input to each function, and what each function returns. Funtions are self-contained and stateless and they do not rely on any external state.

### Scala

What is trait in Scala?

Traits are collections of fields and behaviors that you can extend or mix into your classes. It’s a component of a class, not a class by itself, so there is no constructor, trait is restricted in comparison to class to prevent multiple inheritance problems.


What is difference between map and flatMap ?

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

