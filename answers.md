## C++ Questions

### Introduction

1. What is the history of C++ language?
2. What is the importance of C++ language?
3. What is the use case of a namespace?
4. What is namespace std? Explain std:: with its use case.
5. What are the main features of C++?
6. What is the difference between C and C++?
7. What is the role of a compiler in C++?

### Object Oriented Programming System (OOPs)

1. What is Object Oriented Programming System (OOPs)? Why we should follow it?
2. Explain the Principles of OOP.
3. What is Class & Object? Explain with examples.
4. Describe any 5 real-world examples in context of Class & Objects.
5. What is the difference between a class and a structure in C++?
6. What is a constructor and a destructor?

### Encapsulation

1. What is Data Encapsulation?
2. Explain the use of setter & getter.
3. Explain the use case of this keyword in detail with example.
4. What is Array of objects? Explain with example.
5. Why should we create class attributes as private?
6. Why should we create setters & getters as public?
7. Explain the use case of static keyword in detail with example.

### Inheritance

1. What is inheritance? Explain its types in C++.
2. What is the difference between public, private, and protected inheritance?
3. What is multiple inheritance? How is it implemented in C++?
4. What is the diamond problem in C++?

### Polymorphism

1. What is polymorphism? Explain its types.
2. What is function overloading and operator overloading?
3. What is virtual function? Explain with example.
A virtual function in C++ is a member function declared within a base class and is redefined by a derived class. It enables runtime polymorphism. Example:

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
