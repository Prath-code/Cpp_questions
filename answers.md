## C++ Questions

### Introduction

1. What is the history of C++ language?
   - C++ was developed by Bjarne Stroustrup at Bell Labs in the early 1980s as an extension of the C language. It introduced object-oriented features to C, initially called "C with Classes," and was later renamed C++ in 1983. Over time, it evolved with new standards (C++98, C++03, C++11, C++14, C++17, C++20) to support modern programming needs.
2. What is the importance of C++ language?
   - C++ is important because it combines the efficiency and control of C with object-oriented features, making it suitable for system/software development, game engines, real-time simulations, and performance-critical applications.
3. What is the use case of a namespace?
   - Namespaces prevent name conflicts by grouping related identifiers (classes, functions, variables) under a unique name. This is especially useful in large projects or when integrating multiple libraries.
4. What is namespace std? Explain std:: with its use case.
   - `std` is the standard namespace in C++ that contains all the classes, functions, and objects of the C++ Standard Library (like `cout`, `cin`, `vector`). For example, `std::cout` is used to print output to the console.

### Object Oriented Programming System (OOPs)

1. What is Object Oriented Programming System (OOPs)? Why we should follow it?
   - OOP is a programming paradigm based on the concept of objects, which encapsulate data and behavior. It promotes code reusability, modularity, and easier maintenance.
2. Explain the Principles of OOP.
   - The main principles are:
     - Encapsulation
     - Inheritance
     - Polymorphism
     - Abstraction
3. What is Class & Object? Explain with examples.
   - A class is a blueprint for creating objects. An object is an instance of a class.
     Example:
     ```cpp
     class Car { public: string model; };
     Car myCar; myCar.model = "Toyota";
     ```
4. Describe any 5 real-world examples in context of Class & Objects.
   - Car (class), myCar (object)
   - Student (class), student1 (object)
   - BankAccount (class), accountA (object)
   - Book (class), book1 (object)
   - Employee (class), emp1 (object)

### Encapsulation

1. What is Data Encapsulation?
   - Encapsulation is the bundling of data and methods that operate on that data within a single unit (class), restricting direct access to some components.
2. Explain the use of setter & getter.
   - Setters and getters are methods used to set and get the values of private attributes, providing controlled access.
3. Explain the use case of this keyword in detail with example.
   - `this` is a pointer to the current object. It is used to distinguish between class attributes and parameters with the same name.
     Example:
     ```cpp
     class A { int x; public: void setX(int x) { this->x = x; } };
     ```
4. What is Array of objects? Explain with example.
   - An array of objects is a collection of objects of the same class.
     Example:
     ```cpp
     Car cars[3];
     ```
5. Why should we create class attributes as private?
   - To protect data from unauthorized access and modification, ensuring encapsulation.
6. Why should we create setters & getters as public?
   - To provide controlled and safe access to private attributes from outside the class.
7. Explain the use case of static keyword in detail with example.
   - `static` members belong to the class, not to any object. They are shared among all objects.
     Example:
     ```cpp
     class A { static int count; };
     ```
