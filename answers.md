## C++ Questions

### Introduction

1. What is the history of C++ language?
C++ was developed by Bjarne Stroustrup at Bell Labs in the early 1980s as an extension of the C language. It was originally called "C with Classes" and later renamed to C++. The language was designed to add object-oriented features to C while maintaining its efficiency and flexibility.

2. What is the importance of C++ language?
C++ is important because it combines the power and efficiency of C with object-oriented programming features. It is widely used for system/software development, game development, real-time systems, and applications requiring high performance.

3. What is the use case of a namespace?
A namespace is used to organize code into logical groups and prevent name conflicts, especially when your code base includes multiple libraries.

4. What is namespace std? Explain std:: with its use case.
`std` is the standard namespace in C++ that contains all the classes, objects, and functions of the C++ Standard Library. For example, `std::cout` is used to access the standard output stream.

5. What are the main features of C++?
- Object-oriented programming (OOP)
- Low-level memory manipulation
- Rich library support (STL)
- Portability
- High performance
- Support for both procedural and object-oriented programming

6. What is the difference between C and C++?
C is a procedural programming language, while C++ supports both procedural and object-oriented programming. C++ adds features like classes, inheritance, polymorphism, and templates.

7. What is the role of a compiler in C++?
A compiler translates C++ source code into machine code so that it can be executed by the computer.

### Object Oriented Programming System (OOPs)

1. What is Object Oriented Programming System (OOPs)? Why we should follow it?
OOPs is a programming paradigm based on the concept of objects, which contain data and methods. It helps in organizing complex programs, promotes code reuse, and improves maintainability.

2. Explain the Principles of OOP.
- Encapsulation
- Inheritance
- Polymorphism
- Abstraction

3. What is Class & Object? Explain with examples.
A class is a blueprint for creating objects. An object is an instance of a class.

```cpp
class Car {
public:
    string model;
    void drive() { cout << "Driving"; }
};
Car myCar;
myCar.model = "Toyota";
myCar.drive();
```

4. Describe any 5 real-world examples in context of Class & Objects.
- Car (class) and myCar (object)
- Student (class) and student1 (object)
- BankAccount (class) and account1 (object)
- Book (class) and book1 (object)
- Employee (class) and emp1 (object)

5. What is the difference between a class and a structure in C++?
By default, members of a class are private, while members of a structure are public. Classes support features like inheritance and polymorphism, while structures are mainly used for grouping data.

6. What is a constructor and a destructor?
A constructor is a special function called when an object is created to initialize it. A destructor is called when an object is destroyed to free resources.

### Encapsulation

1. What is Data Encapsulation?
Encapsulation is the bundling of data and methods that operate on that data within a single unit (class), restricting direct access to some of the object's components.

2. Explain the use of setter & getter.
Setters and getters are methods used to set and get the values of private attributes, providing controlled access.

3. Explain the use case of this keyword in detail with example.
`this` is a pointer to the current object. It is used to refer to the object's members, especially when parameter names shadow member names.

```cpp
class Person {
    int age;
public:
    void setAge(int age) { this->age = age; }
};
```

4. What is Array of objects? Explain with example.
An array of objects is a collection of objects of the same class.

```cpp
class Student {
public:
    string name;
};
Student arr[3];
```

5. Why should we create class attributes as private?
To protect data from unauthorized access and modification, ensuring encapsulation.

6. Why should we create setters & getters as public?
To provide controlled access to private data members from outside the class.

7. Explain the use case of static keyword in detail with example.
`static` members are shared by all objects of a class.

```cpp
class Test {
public:
    static int count;
    Test() { count++; }
};
int Test::count = 0;
```

### Inheritance

1. What is inheritance? Explain its types in C++.
Inheritance is the process by which one class acquires the properties and behaviors of another class. Types: single, multiple, multilevel, hierarchical, and hybrid inheritance.

2. What is the difference between public, private, and protected inheritance?
- Public: public members remain public in derived class.
- Protected: public and protected members become protected.
- Private: public and protected members become private.

3. What is multiple inheritance? How is it implemented in C++?
Multiple inheritance is when a class inherits from more than one base class.

```cpp
class A {};
class B {};
class C : public A, public B {};
```

4. What is the diamond problem in C++?
It occurs when two classes inherit from the same base class and a fourth class inherits from both, causing ambiguity. Solved using virtual inheritance.

### Polymorphism

1. What is polymorphism? Explain its types.
Polymorphism allows functions or objects to behave differently in different contexts. Types: compile-time (function/operator overloading) and runtime (virtual functions).

2. What is function overloading and operator overloading?
Function overloading: multiple functions with the same name but different parameters.
Operator overloading: redefining the way operators work for user-defined types.

3. What is virtual function? Explain with example.
A virtual function in C++ is a member function declared within a base class and is redefined by a derived class. It enables runtime polymorphism.

```cpp
class Base {
public:
    virtual void show() { cout << "Base"; }
};
class Derived : public Base {
public:
    void show() override { cout << "Derived"; }
};
Base* b = new Derived();
b->show(); // Output: Derived
```

4. What is pure virtual function and abstract class?
A pure virtual function is a function with no implementation in the base class and is declared by assigning 0. A class containing at least one pure virtual function is called an abstract class and cannot be instantiated.

```cpp
class Shape {
public:
    virtual void draw() = 0; // Pure virtual function
};
```

### Abstraction

1. What is abstraction in C++?
Abstraction is the concept of hiding complex implementation details and showing only the necessary features of an object.

2. How is abstraction implemented in C++?
Abstraction is implemented using abstract classes and interfaces (pure virtual functions), and by providing public methods to interact with private data.

### Memory Management

1. What is the difference between stack and heap memory?
Stack memory is used for static memory allocation and is managed automatically. Heap memory is used for dynamic memory allocation and must be managed manually using `new` and `delete`.

2. How is dynamic memory allocated in C++?
Dynamic memory is allocated using `new` (for single objects or arrays) and deallocated using `delete`.

```cpp
int* p = new int; // allocation
* p = 10;
delete p; // deallocation
```

3. What is a memory leak? How can it be avoided?
A memory leak occurs when dynamically allocated memory is not deallocated, causing wasted memory. It can be avoided by always using `delete` or smart pointers after `new`.

4. What is smart pointer?
A smart pointer is a C++ object that manages the lifetime of a dynamically allocated object, automatically releasing memory when it is no longer needed. Examples: `std::unique_ptr`, `std::shared_ptr`.

### C++ Standard Library

1. What is the Standard Template Library (STL)?
STL is a collection of C++ template classes for common data structures and algorithms like vectors, lists, stacks, queues, and algorithms.

2. What are containers in STL? Name a few.
Containers are objects that store data. Examples: `vector`, `list`, `deque`, `set`, `map`.

3. What is an iterator in STL?
An iterator is an object that points to elements in a container and allows traversal of the container.

4. What is the difference between vector and list in STL?
`vector` is a dynamic array with fast random access but slow insertions/deletions except at the end. `list` is a doubly linked list with fast insertions/deletions anywhere but slow random access.

5. What is vector? Explain with examples.
A `vector` in C++ is a dynamic array provided by the STL that can grow or shrink in size automatically. It allows fast random access, efficient insertion/removal at the end, and stores elements in contiguous memory locations.

**Example:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> v; // create an empty vector
    v.push_back(10); // add elements
    v.push_back(20);
    v.push_back(30);
    cout << "Vector elements: ";
    for (int i = 0; i < v.size(); ++i) {
        cout << v[i] << " ";
    }
    return 0;
}
```

**Output:**
```
Vector elements: 10 20 30
```

You can also initialize a vector with values:
```cpp
vector<int> v = {1, 2, 3, 4};
```

Vectors are widely used due to their flexibility and ease of use.
