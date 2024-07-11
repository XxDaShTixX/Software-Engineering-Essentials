# Table of Content
- [Database Management Systems (DBMS)](#database-management-systems-dbms)
  - [Database Management Systems (DBMS)](#database-management-systems-dbms-1)
  - [Relational Databases](#relational-databases)
  - [SQL (Structured Query Language)](#sql-structured-query-language)
  - [NoSQL Databases](#nosql-databases)


 
# Design Patterns
Design patterns are reusable solutions to common problems that arise during software development. 
They are templates for solving recurring design issues and provide a way to create flexible, scalable, and maintainable software systems.

## Definition
Design patterns are best practices to solve common software design problems. They fall into three categories: creational, structural, and behavioral. 
They improve code readability and testability. Examples include Singleton, Factory, Decorator, and Observer patterns. Use them appropriately.

## Importance
Explains why we use design patterns and how they benefit the development process, such as improving communication, increasing efficiency, and promoting code reusability and maintainability:
- <ins>**Efficiency**</ins>: They provide tested, proven solutions to common problems, saving developers from having to reinvent the wheel.
- <ins>**Communication**</ins>: They offer a common language to conceptualize repeated problems and solutions when discussing system design.
- <ins>**Code Reusability and Maintainability**</ins>: They make the code more organized, reusable, and easy to maintain.
- <ins>**Best Practices**</ins>: They encapsulate the experience of software professionals into a standard solution. Remember, the key is to use them where appropriate. Misuse can lead to unnecessarily complicated designs.

## Key Characteristics
Describe the inherent properties or features of design patterns. They define what design patterns are, such as their:
- <ins>**Standardization**</ins>: Design patterns provide solutions that can be reused across different projects, reducing redundancy in code.
- <ins>**Communication**</ins>: They offer a standard terminology and are universally recognized by developers, improving communication and understanding.
- <ins>**Efficiency**</ins>: By providing proven solutions to common problems, they increase development speed and efficiency.
- <ins>**Flexibility**</ins>: Design patterns often provide flexibility for future changes and enhancements by ensuring that a class or system is easily extendable.





# Types of Design Patterns
Design patterns are typically divided into three types:
- <ins>**Creational Patterns**</ins>: These deal with object creation mechanisms, trying to create objects in a manner suitable to the situation. Examples include Singleton, Factory, and Builder patterns.
- <ins>**Structural Patterns**</ins>: These concern class and object composition. They provide a simple way to realize relationships between entities. Examples include Adapter, Decorator, and Proxy patterns.
- <ins>**Behavioral Patterns**</ins>: These are specifically concerned with communication between objects. They identify common communication patterns and realize these patterns. Examples include Observer, Strategy, and Command patterns.

## Creational Design Patterns

### Purpose:
Creational design patterns are concerned with the way of creating objects. They help make a system independent of how its objects are created, composed, and represented.

### Types and Use Case:
- <ins>**Singleton**</ins>: Ensures a class has only one instance and provides a global point of access to it. It’s often used for things like database connections or logging where you typically want one instance.
- <ins>**Factory Method**</ins>: Provides an interface for creating objects, but allows subclasses to alter the type of objects that will be created. It’s useful when there’s some generic processing in a class, but the required subclass is dynamically decided at runtime.
- <ins>**Abstract Factory**</ins>: Provides an interface for creating families of related or dependent objects without specifying their concrete classes. It’s often used in systems that need to be independent from how its products are created, composed, and represented.
- <ins>**Builder**</ins>: Separates the construction of a complex object from its representation so that the same construction process can create different representations. It’s useful when you need to create an object with lots of possible configuration options.
- <ins>**Prototype**</ins>: Specifies the kind of objects to create using a prototypical instance and creates new objects by copying this prototype. It’s useful when instantiation of a class is expensive or complicated, and you want to avoid the cost of building a class hierarchy of factories.



## Creational Design Patterns

### Purpose:
Structural design patterns are about organizing different classes and objects to form larger structures and provide new functionality.

### Types and Use Case:
- <ins>**Adapter**</ins>: Allows classes with incompatible interfaces to work together by wrapping its own interface around that of an already existing class. It’s often used to make existing classes work with others without modifying their source code.
- <ins>**Bridge**</ins>: Decouples an abstraction from its implementation so that the two can vary independently. It’s useful when you want to avoid a permanent binding between an abstraction and its implementation.
- <ins>**Composite**</ins>: Composes objects into tree structures to represent part-whole hierarchies. It’s useful when you want to treat individual objects and compositions of objects uniformly.
- <ins>**Decorator**</ins>: Dynamically adds/overrides behaviour in an existing method of an object. It provides a flexible alternative to subclassing for extending functionality.
- <ins>**Facade**</ins>: Provides a simplified interface to a larger body of code. It’s often used when a system is very complex or difficult to understand because the system has a large number of interdependent classes or its source code is unavailable.
- <ins>**Flyweight**</ins>: Reduces the cost of creating and manipulating a large number of similar objects. It’s often used when you need to spawn a large number of objects of a class, which are not too dissimilar.
- <ins>**Proxy**</ins>: Provides a surrogate or placeholder for another object to control access to it. It’s often used when you want to add a layer of security to the original object or to reduce the memory footprint of a large object.



## Behavioral Design Patterns

### Purpose:
Behavioral design patterns are about identifying common communication patterns between objects and realize these patterns.

### Types and Use Case:
- <ins>**Observer**</ins>: Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically. It’s often used in event handling systems.
- <ins>**State**</ins>: Allows an object to alter its behavior when its internal state changes. It’s useful when an object’s behavior depends on its state and it must change its behavior at run-time depending on that state.
- <ins>**Strategy**</ins>: Defines a family of algorithms, encapsulates each one, and makes them interchangeable. It’s often used when you need to provide multiple ways to solve a problem.
- <ins>**Template Method**</ins>: Defines the skeleton of an algorithm in a method, deferring some steps to subclasses. It’s useful when you want to let subclasses redefine certain steps of an algorithm without changing the algorithm’s structure.
- <ins>**Visitor**</ins>: Represents an operation to be performed on the elements of an object structure without changing the classes on which it operates. It’s often used when you need to perform an operation across a disparate set of objects.
- <ins>**Command**</ins>: Encapsulates a request as an object, thereby letting you parameterize clients with queues, requests, and operations. It’s often used in menu systems and for implementing callback functions.
- <ins>**Iterator**</ins>: Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation. It’s often used when you need a standard way to iterate over a collection and don’t want to expose its underlying representation.




