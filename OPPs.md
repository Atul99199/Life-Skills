#                                                   OBJECT ORIENTED PROGRAMMING


## Introduction:
Object-Oriented Programming (OOP) is a paradigm centered around the idea of organizing software using objects and classes. It encourages the design of software by bundling related properties (data) and behaviors (functions) together. OOP makes complex systems easier to understand, maintain, and extend.

## Class:
A class is a custom data structure defined by the user that contains data members (attributes) and member functions (methods). It is a template for creating objects. A class on its own doesn’t use memory until an object is created from it.

### Example:-
```
class student {
public:
    int id;         // data member
    int mobile;     // data member
    string name;    // data member

    int add(int x, int y) {  // member function
        return x + y;
    }
};
```

## Object:
An object is an instance of a class. When a class is instantiated, it becomes an object that has its own copy of the class's attributes and can call its methods.

### Example:-
```
C++ Syntax (for object):
student s = new student();
```

The four pillars of Object-Oriented Programming (OOP) are Abstraction, Encapsulation, Inheritance, and Polymorphism.

## 1. Inheritance:
Inheritance allows one class (the child or derived class) to inherit members (attributes and methods) from another class (the parent or base class). This promotes reusability and extends functionality.

### Example:
```
C++ Syntax :
class derived_class :: visibility-mode base_class;

visibility-modes = {private, protected, public}
```

## Types of Inheritance:

### a. Single inheritance : 
When one class inherits another class, it is known as single level inheritance.

### b. Multiple inheritance :
 Multiple inheritance is the process of deriving a new class that inherits the attributes from two or more classes.

### c. Hierarchical inheritance : 
Hierarchical inheritance is defined as the process of deriving more than one class from a base class.

### d. Multilevel inheritance : 
Multilevel inheritance is a process of deriving a class from another derived class.

### e. Hybrid inheritance :
Hybrid inheritance is a combination of simple, multiple inheritance and hierarchical inheritance.

## 2. Encapsulation:
Encapsulation means combining data and the functions that operate on that data into a single unit, typically a class. Access to internal data is restricted using access specifiers (private, protected, public). It helps achieve data hiding, which minimizes unintended interference.

## 3. Abstraction:
Abstraction focuses on exposing only the essential features of a system while hiding the complex implementation details. It helps to reduce code complexity and increase maintainability.

### Data binding : 
Data binding is a process of binding the application UI and business logic. Any change made in the business logic will reflect directly to the application UI.

## 4. Polymorphism:
Polymorphism is an object-oriented programming (OOP) concept that allows objects of different classes to be treated as objects of a common superclass. The term "polymorphism" originates from Greek words meaning "many forms." 

## Types of Polymorphism :

### a. Compile Time Polymorphism :
Function overloading allows multiple methods with the same name but different parameter lists within the same class.

* Method Overloading: 
Method overloading is a technique that allows you to have more than one function with the same function name but with different functionality. 

### Example:
```
#include <bits/stdc++.h>
using namespace std;

class Add {
public:
    int add(int a, int b) {
        return (a + b);
    }

    int add(int a, int b, int c) {
        return (a + b + c);
    }
};

int main() {
    Add obj;
    int res1, res2;

    res1 = obj.add(2, 3);      // Calls 2-parameter version
    res2 = obj.add(2, 3, 4);   // Calls 3-parameter version

    cout << res1 << " " << res2 << endl;  // Output: 5 9
    return 0;
}

```

### b. Runtime Polymorphism:
Runtime polymorphism, also known as dynamic polymorphism, is a type of polymorphism. Function overriding is an example of runtime polymorphism. Function overriding means that when the child class contains a method that is already present in the parent class. Hence, the child class overrides the process of the parent class.

### Example:
```
#include <iostream>
using namespace std;

// Base class
class Base {
public:
    virtual void show() {
        cout << "Apni Kaksha base" << endl;
    }
};

// Derived class
class Derived: public Base {
public:
    void show() override {
        cout << "Apni Kaksha derived" << endl;
    }
};

int main() {
    Base* b;         // Base class pointer
    Derived d;       // Derived class object

    b = &d;          // Point base pointer to derived object
    b->show();       // Calls Derived::show() due to virtual function

    return 0;
}
```

## Conclusion:
Object-Oriented Programming (OOPs) is an effective programming approach that enhances code structure, encourages reuse, and simplifies maintenance. By understanding and applying its core concepts—Encapsulation, Abstraction, Inheritance, and Polymorphism—developers can create scalable and maintainable software systems with greater efficiency.


