---
layout: post
title: /Notes/ Java Beginner Notes
---

_Beginner notes from CompSci 101_

Public:
- Indicates there are no special restrictions on the use of the method.

Methods:
- Every method belongs to some class & is available to objects created from that class. The definition of a method is given in the definition of the class to which it belongs.

Instance variables:
- Data fields belonging to each instance of the class (each object). Instance variables are written differently depending on whether they are within the class (`this.instanceVariable` or `instanceVariable`) or outside of the class (as inside a program that uses the class, i.e. `receivingObject.instanceVariable`)

This:
- Within a method definition, you can use the keyword `this` as a name for the object receiving the method call

Local variables:
- A variable declared within a method. All variables declared in a program's main method are local to main. If you decide to declare a variable within a block, variable is local to the block. So the scope of a local variable extends from its declaration to the end of the block containing the declaration. Formal parameters are local variables.

Precondition:
- States the conditions that must be true before the method is invoked

Postcondition:
- Describes all the effects produced by a method invocation

Public vs private:
- The public modifier, when applied to a class, method, or instance variable, means that any other class can directly use or access the class/method/variable by name.
- public and private are called access modifiers
- When an instance variable is private, its name is not accessible outside of the class definition. But you can still use its name within any method inside the class definition.
- Methods can be private - they cannot be invoked outside the class definition. A private method can still be invoked within the definition of other methods in the same class.

Getters/Setters:
- Getter = get method = accessor
- Setter = set method = mutator

Encapsulation:
- When done correctly, it neatly divides a class definition into two parts: the interface and the implementation
- A class interface tells programmers all they need to know to use the class. Consists of headings for the public methods & public named constants of the class.
- Implementation consists of all the private elements of the class definition, principally the private instance variables, along with definitions of public and private methods.
- When defining a class while using encapsulation, separate the class interface from the implementation conceptually so the interface is a safe and simplified description of the class.