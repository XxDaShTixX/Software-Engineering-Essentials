# Table of Content
- [Design Patterns](#design-patterns)
  - [Definition](#definition)
  - [Importance](#importance)
  - [Characteristics](#characteristics)
- [Types of Design Patterns](#types-of-design-patterns)
  - [Creational Design Patterns](#creational-design-patterns)
  - [Structural Design Patterns](#structural-design-patterns)
  - [Behavioral Design Patterns](#behavioral-design-patterns)
- [Deep Dive into Each Design Pattern](#deep-dive-into-each-design-pattern)
  - [Singleton Pattern (Creational)](#singleton-pattern-creational)
  - [Factory Pattern (Creational)](#factory-pattern-creational)
  - [Abstract Factory Pattern (Creational)](#abstract-factory-pattern-creational)
  - [Builder Pattern (Creational)](#builder-pattern-creational)
  - [Prototype Pattern (Creational)](#prototype-pattern-creational)
  - [Object Pool Pattern (Creational)](#object-pool-pattern-creational)
  - [Adapter Pattern (Structural)](#adapter-pattern-structural)
  - [Bridge Pattern (Structural)](#bridge-pattern-structural)
  - [Composite Pattern (Structural)](#composite-pattern-structural)
  - [Decorator Pattern (Structural)](#decorator-pattern-structural)
  - [Facade Pattern (Structural)](#facade-pattern-structural)
  - [Flyweight Pattern (Structural)](#flyweight-pattern-structural)
  - [Proxy Pattern (Structural)](#flyweight-pattern-structural)
  - [Observer Pattern (Behavioral)](#observer-pattern-behavioral)
  - [State Pattern (Behavioral)](#state-pattern-behavioral)
  - [Strategy Pattern (Behavioral)](#strategy-pattern-behavioral)
  - [Template Method Pattern (Behavioral)](#template-method-pattern-behavioral)
  - [Visitor Pattern (Behavioral)](#visitor-pattern-behavioral)
  - [Command Pattern (Behavioral)](#command-pattern-behavioral)
  - [Iterator Pattern (Behavioral)](#iterator-pattern-behavioral)
 
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

## Characteristics
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



## Structural Design Patterns

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





# Deep Dive into Each Design Pattern
Let’s take a look at the previously mentioned design patterns and their implementation in C#. I’ll provide a brief overview, structure, and a simple real-world example for each.

## Singleton Pattern (Creational)
### Purpose: 
Ensures a class has only one instance and provides a global point of access to it.
### Real-world Example:
A printer spooler in an operating system. There should be only one spooler to avoid multiple print commands sent to the printer at the same time.
### Structure:
```
public sealed class Singleton
{
    private static Singleton instance = null;
    private static readonly object padlock = new object();

    Singleton()
    {
    }

    public static Singleton Instance
    {
        get
        {
            lock (padlock)
            {
                if (instance == null)
                {
                    instance = new Singleton();
                }
                return instance;
            }
        }
    }
}
```

## Factory Pattern (Creational)
### Purpose: 
Provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.
### Real-world Example:
A hiring manager is a good example of the Factory Method. The hiring manager is responsible for hiring employees. The basic steps of the hiring process are the same (publish job opening, collect resumes, conduct interviews), but the actual part of creating the employee is not done by the hiring manager, but by the specific departments (factories) which need the employees.
### Structure:
```
public abstract class Product
{
    public abstract void Use();
}

public class ConcreteProductA : Product
{
    public override void Use()
    {
        // Implementation for Product A
    }
}

public class ConcreteProductB : Product
{
    public override void Use()
    {
        // Implementation for Product B
    }
}

public abstract class Factory
{
    public abstract Product CreateProduct();
}

public class ConcreteFactoryA : Factory
{
    public override Product CreateProduct()
    {
        return new ConcreteProductA();
    }
}

public class ConcreteFactoryB : Factory
{
    public override Product CreateProduct()
    {
        return new ConcreteProductB();
    }
}

```

## Abstract Factory Pattern (Creational)
### Purpose: 
Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
### Real-world Example:
An animal factory is a good example of the Abstract Factory pattern. The factory can create different types of animals (like a cat or a dog), and each animal type can have different breeds. The Abstract Factory pattern allows you to create families of related objects without specifying their concrete classes.
### Structure:
```
public abstract class AbstractProductA
{
    public abstract void UseProductA();
}

public abstract class AbstractProductB
{
    public abstract void UseProductB();
}

public abstract class AbstractFactory
{
    public abstract AbstractProductA CreateProductA();
    public abstract AbstractProductB CreateProductB();
}

public class ConcreteProductA1 : AbstractProductA
{
    public override void UseProductA()
    {
        // Implementation for Product A1
    }
}

public class ConcreteProductB1 : AbstractProductB
{
    public override void UseProductB()
    {
        // Implementation for Product B1
    }
}

public class ConcreteFactory1 : AbstractFactory
{
    public override AbstractProductA CreateProductA()
    {
        return new ConcreteProductA1();
    }

    public override AbstractProductB CreateProductB()
    {
        return new ConcreteProductB1();
    }
}
```

## Builder Pattern (Creational)
### Purpose: 
Separates the construction of a complex object from its representation so that the same construction process can create different representations.
### Real-world Example:
Consider a construction of a complex Pizza. The construction process is the same but the parts (toppings, crust type, size etc.) can vary. The Builder pattern allows you to construct the Pizza in steps, and at the end, `GetResult()` gives you the final product.
### Structure:
```
public abstract class Builder
{
    public abstract void BuildPartA();
    public abstract void BuildPartB();
    public abstract Product GetResult();
}

public class ConcreteBuilder : Builder
{
    private Product _product = new Product();

    public override void BuildPartA()
    {
        // Implement part A construction
    }

    public override void BuildPartB()
    {
        // Implement part B construction
    }

    public override Product GetResult()
    {
        return _product;
    }
}

public class Director
{
    public void Construct(Builder builder)
    {
        builder.BuildPartA();
        builder.BuildPartB();
    }
}
```

## Prototype Pattern (Creational)
### Purpose: 
Specifies the kind of objects to create using a prototypical instance, and creates new objects by copying this prototype.
### Real-world Example:
A good example of the Prototype pattern is cloning cells in biology. When a cell divides, it essentially clones itself to create a new cell. In software, you might use the Prototype pattern when creating an object is expensive, and you want to avoid the cost of initialization. Instead, you could clone an existing (prototype) object.
### Structure:
```
public abstract class Prototype
{
    public abstract Prototype Clone();
}

public class ConcretePrototype : Prototype
{
    public override Prototype Clone()
    {
        // Implement deep copy logic here
        return (Prototype)this.MemberwiseClone();
    }
}
```

## Object Pool Pattern (Creational)
### Purpose: 
Reuse and share objects that are expensive to create. It manages a set of instances instead of creating and destroying them on demand.
### Real-world Example:
A common use case for the object pool pattern is in a game application where you need to spawn and destroy many similar objects (like bullets or enemies) frequently. Instead of creating a new object every time one is needed and destroying it after use (which can be costly in terms of memory and performance), you can use the Object Pool pattern to “recycle” these objects.
### Structure:
```
public class ObjectPool<T> where T : new()
{
    private readonly List<T> _available = new List<T>();
    private readonly List<T> _inUse = new List<T>();

    public T Get()
    {
        lock(_available)
        {
            if (_available.Count != 0)
            {
                T obj = _available[0];
                _inUse.Add(obj);
                _available.RemoveAt(0);
                return obj;
            }
            else
            {
                T obj = new T();
                _inUse.Add(obj);
                return obj;
            }
        }
    }

    public void Release(T obj)
    {
        lock(_available)
        {
            _available.Add(obj);
            _inUse.Remove(obj);
        }
    }
}
```

## Adapter Pattern (Structural)
### Purpose: 
Allows classes with incompatible interfaces to work together by wrapping its own interface around that of an already existing class.
### Real-world Example:
Consider a scenario where you have a memory card and a laptop that only accepts USB input. Here, a card reader acts as an adapter. You plug the memory card into the card reader, and the card reader into the laptop. The card reader adapts the interface of the memory card to the USB interface of the laptop.
### Structure:
```
// Existing way requests are implemented
class Adaptee
{
    public void SpecificRequest()
    {
        // ...
    }
}

// New standard for requests
interface ITarget
{
    void Request();
}

// Implementing the new standard in terms of the old
class Adapter : ITarget
{
    private readonly Adaptee _adaptee;

    public Adapter(Adaptee adaptee)
    {
        _adaptee = adaptee;
    }

    public void Request()
    {
        _adaptee.SpecificRequest();
    }
}
```

## Bridge Pattern (Structural)
### Purpose: 
Decouples an abstraction from its implementation so that the two can vary independently.
### Real-world Example:
Consider a device like a TV. The TV could be controlled by several different types of control mechanisms, e.g., a remote control, a joystick, or voice commands. Here, the TV is the abstraction, and the control mechanism is the implementation. Using the Bridge pattern, you can vary the TV independent of the control mechanism and vice versa.
### Structure:
```
// Implementor
public interface IImplementation
{
    void OperationImpl();
}

// Concrete Implementors
public class ConcreteImplementationA : IImplementation
{
    public void OperationImpl()
    {
        // Implementation A
    }
}

public class ConcreteImplementationB : IImplementation
{
    public void OperationImpl()
    {
        // Implementation B
    }
}

// Abstraction
public abstract class Abstraction
{
    protected IImplementation implementation;

    public Abstraction(IImplementation implementation)
    {
        this.implementation = implementation;
    }

    public virtual void Operation()
    {
        implementation.OperationImpl();
    }
}

// Refined Abstraction
public class RefinedAbstraction : Abstraction
{
    public RefinedAbstraction(IImplementation implementation) : base(implementation)
    {
    }

    public override void Operation()
    {
        // Additional behavior
        base.Operation();
    }
}
```

## Composite Pattern (Structural)
### Purpose: 
Composes objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.
### Real-world Example:
Consider a file system, which comprises directories (folders) and files. A directory can contain other directories as well as files, but a file cannot contain anything. Here, ‘Directory’ is the composite class, ‘File’ is the leaf class, and they both inherit from a common interface ‘FileSystemEntity’.
### Structure:
```
// Component
public abstract class Component
{
    public abstract void Operation();
}

// Leaf
public class Leaf : Component
{
    public override void Operation()
    {
        // Leaf operation
    }
}

// Composite
public class Composite : Component
{
    private List<Component> _children = new List<Component>();

    public override void Operation()
    {
        foreach (var child in _children)
        {
            child.Operation();
        }
    }

    public void Add(Component component)
    {
        _children.Add(component);
    }

    public void Remove(Component component)
    {
        _children.Remove(component);
    }
}
```

## Decorator Pattern (Structural)
### Purpose: 
Dynamically adds/overrides behaviour in an existing method of an object. It provides a flexible alternative to subclassing for extending functionality.
### Real-world Example:
Consider a window in a graphical user interface. You can decorate a window with additional behaviors like scrollable, resizable, etc., without changing the window’s code. Each decorator adds some decoration, like a scrollbar or a resize grip, without modifying the underlying object being decorated.
### Structure:
```
// Component
public abstract class Component
{
    public abstract void Operation();
}

// Concrete Component
public class ConcreteComponent : Component
{
    public override void Operation()
    {
        // Original operation
    }
}

// Decorator
public abstract class Decorator : Component
{
    protected Component component;

    public Decorator(Component component)
    {
        this.component = component;
    }

    public override void Operation()
    {
        component.Operation();
    }
}

// Concrete Decorators
public class ConcreteDecoratorA : Decorator
{
    public ConcreteDecoratorA(Component component) : base(component)
    {
    }

    public override void Operation()
    {
        // Additional behavior A
        base.Operation();
    }
}

public class ConcreteDecoratorB : Decorator
{
    public ConcreteDecoratorB(Component component) : base(component)
    {
    }

    public override void Operation()
    {
        // Additional behavior B
        base.Operation();
    }
}
```

## Facade Pattern (Structural)
### Purpose: 
Provides a simplified interface to a larger body of code, such as a class library.
### Real-world Example:
Consider a computer system. Turning on a computer involves initializing the processor, testing memory, loading system files, etc. To make it easy for the user, a “Start” button is provided, which serves as a facade, simplifying a complex process behind a simple interface.
### Structure:
```
// Complex subsystem classes
public class SubsystemClassA
{
    public void OperationA() { /* ... */ }
}

public class SubsystemClassB
{
    public void OperationB() { /* ... */ }
}

// Facade
public class Facade
{
    private SubsystemClassA _a = new SubsystemClassA();
    private SubsystemClassB _b = new SubsystemClassB();

    public void Operation()
    {
        _a.OperationA();
        _b.OperationB();
        // ...
    }
}
```

## Flyweight Pattern (Structural)
### Purpose: 
Provides a simplified interface to a larger body of code, such as a class library.
### Real-world Example:
A common use case for the Flyweight pattern is in a game application where you need to spawn and destroy many similar objects (like bullets or enemies) frequently. Instead of creating a new object every time one is needed and destroying it after use (which can be costly in terms of memory and performance), you can use the Flyweight pattern to share the common parts of the object state among multiple objects.
### Structure:
```
public interface IFlyweight
{
    void Operation(string extrinsicState);
}

public class ConcreteFlyweight : IFlyweight
{
    private string _intrinsicState;

    public ConcreteFlyweight(string intrinsicState)
    {
        _intrinsicState = intrinsicState;
    }

    public void Operation(string extrinsicState)
    {
        // Use _intrinsicState and extrinsicState
    }
}

public class FlyweightFactory
{
    private Dictionary<string, IFlyweight> _flyweights = new Dictionary<string, IFlyweight>();

    public IFlyweight GetFlyweight(string intrinsicState)
    {
        if (!_flyweights.ContainsKey(intrinsicState))
        {
            _flyweights[intrinsicState] = new ConcreteFlyweight(intrinsicState);
        }

        return _flyweights[intrinsicState];
    }
}
```

## Proxy Pattern (Structural)
### Purpose: 
Provides a surrogate or placeholder for another object to control access to it.
### Real-world Example:
A common example of the Proxy pattern is a credit card, which acts as a proxy for a bank account. The credit card defers payments to the bank account and provides controlled access to the bank account’s funds.
### Structure:
```
public interface ISubject
{
    void Request();
}

public class RealSubject : ISubject
{
    public void Request()
    {
        // Real implementation
    }
}

public class Proxy : ISubject
{
    private RealSubject _realSubject;

    public void Request()
    {
        if (_realSubject == null)
        {
            _realSubject = new RealSubject();
        }

        // Control access to the real subject
        _realSubject.Request();
    }
}
```

## Observer Pattern (Behavioral)
### Purpose: 
Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
### Real-world Example:
A news agency. When the agency publishes a new story, all registered outlets (observers) are notified and publish the story.
### Structure:
```
public interface IObserver
{
    void Update();
}

public interface ISubject
{
    void Attach(IObserver observer);
    void Detach(IObserver observer);
    void Notify();
}

public class ConcreteSubject : ISubject
{
    private List<IObserver> _observers = new List<IObserver>();

    public void Attach(IObserver observer)
    {
        _observers.Add(observer);
    }

    public void Detach(IObserver observer)
    {
        _observers.Remove(observer);
    }

    public void Notify()
    {
        foreach (var observer in _observers)
        {
            observer.Update();
        }
    }
}

public class ConcreteObserver : IObserver
{
    public void Update()
    {
        // ...
    }
}
```

## State Pattern (Behavioral)
### Purpose: 
Allows an object to alter its behavior when its internal state changes. The object will appear to change its class.
### Real-world Example:
Consider a traffic light system. The light changes state from green to yellow, yellow to red, and then red to green. Here, each color represents a different state and has different behaviors associated with it.
### Structure:
```
public interface IState
{
    void Handle(Context context);
}

public class ConcreteStateA : IState
{
    public void Handle(Context context)
    {
        // Handle request and set the next state
        context.State = new ConcreteStateB();
    }
}

public class ConcreteStateB : IState
{
    public void Handle(Context context)
    {
        // Handle request and set the next state
        context.State = new ConcreteStateA();
    }
}

public class Context
{
    public IState State { get; set; }

    public Context(IState state)
    {
        this.State = state;
    }

    public void Request()
    {
        this.State.Handle(this);
    }
}
```

## Strategy Pattern (Behavioral)
### Purpose: 
Defines a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from clients that use it.
### Real-world Example:
Consider a map application that provides several methods (or strategies) to go from point A to point B (like fastest route, shortest route, or least busy route). Here, each method represents a different strategy.
### Structure:
```
public interface IStrategy
{
    void AlgorithmInterface();
}

public class ConcreteStrategyA : IStrategy
{
    public void AlgorithmInterface()
    {
        // Implement algorithm A
    }
}

public class ConcreteStrategyB : IStrategy
{
    public void AlgorithmInterface()
    {
        // Implement algorithm B
    }
}

public class Context
{
    private IStrategy _strategy;

    public Context(IStrategy strategy)
    {
        this._strategy = strategy;
    }

    public void ContextInterface()
    {
        _strategy.AlgorithmInterface();
    }
}
```

## Template Method Pattern (Behavioral)
### Purpose: 
Defines the skeleton of an algorithm in a method, deferring some steps to subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm’s structure.
### Real-world Example:
Consider a software development process. The steps (requirements, design, implementation, testing) are the same and occur in the same order for every kind of project. However, the details of each step can vary based on the type of project (web project, mobile project, cloud project). Here, each type of project can be a subclass that implements the steps according to its requirements.
### Structure:
```
public abstract class AbstractClass
{
    public void TemplateMethod()
    {
        PrimitiveOperation1();
        PrimitiveOperation2();
        // ...
    }

    public abstract void PrimitiveOperation1();

    public abstract void PrimitiveOperation2();
}

public class ConcreteClass : AbstractClass
{
    public override void PrimitiveOperation1()
    {
        // Implement operation 1
    }

    public override void PrimitiveOperation2()
    {
        // Implement operation 2
    }
}
```

## Visitor Pattern (Behavioral)
### Purpose: 
Represents an operation to be performed on the elements of an object structure without changing the classes on which it operates.
### Real-world Example:
Consider a tax calculation system. The system can calculate different types of taxes (like income tax, sales tax, etc.) for different types of people (like an employee, a business owner, etc.). Here, each type of tax calculation is a visitor, and each type of person is an element.
### Structure:
```
public interface IElement
{
    void Accept(IVisitor visitor);
}

public class ConcreteElementA : IElement
{
    public void Accept(IVisitor visitor)
    {
        visitor.VisitConcreteElementA(this);
    }
}

public class ConcreteElementB : IElement
{
    public void Accept(IVisitor visitor)
    {
        visitor.VisitConcreteElementB(this);
    }
}

public interface IVisitor
{
    void VisitConcreteElementA(ConcreteElementA concreteElementA);
    void VisitConcreteElementB(ConcreteElementB concreteElementB);
}

public class ConcreteVisitor1 : IVisitor
{
    public void VisitConcreteElementA(ConcreteElementA concreteElementA)
    {
        // Visitor 1's implementation for ConcreteElementA
    }

    public void VisitConcreteElementB(ConcreteElementB concreteElementB)
    {
        // Visitor 1's implementation for ConcreteElementB
    }
}

public class ConcreteVisitor2 : IVisitor
{
    public void VisitConcreteElementA(ConcreteElementA concreteElementA)
    {
        // Visitor 2's implementation for ConcreteElementA
    }

    public void VisitConcreteElementB(ConcreteElementB concreteElementB)
    {
        // Visitor 2's implementation for ConcreteElementB
    }
}
```

## Command Pattern (Behavioral)
### Purpose: 
Encapsulates a request as an object, thereby letting you parameterize clients with different requests, queue or log requests, and support undoable operations.
### Real-world Example:
Consider a remote control for an electronic device (like a TV or Radio). Each button on the remote is a command that encapsulates a request (like turning the power on/off, changing the channel, adjusting the volume). The remote control, the invoker, can execute these commands without knowing the specifics of the device’s operations.
### Structure:
```
public interface ICommand
{
    void Execute();
}

public class ConcreteCommand : ICommand
{
    private Receiver _receiver;

    public ConcreteCommand(Receiver receiver)
    {
        _receiver = receiver;
    }

    public void Execute()
    {
        _receiver.Action();
    }
}

public class Invoker
{
    private ICommand _command;

    public Invoker(ICommand command)
    {
        _command = command;
    }

    public void Invoke()
    {
        _command.Execute();
    }
}

public class Receiver
{
    public void Action()
    {
        // Perform some action
    }
}
```

## Iterator Pattern (Behavioral)
### Purpose: 
The Iterator Pattern provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation. It encapsulates the internal structure of how the items are organized and allows clients to traverse the elements without knowing the underlying details.
### Real-world Example:
A real-world example of the Iterator pattern is a radio station tuner. You can think of each station as an element in a collection. The tuner acts as an iterator that lets you go through the stations one by one without knowing how they are ordered in the frequency spectrum.
### Structure:
```
public interface IIterator
{
    bool HasNext();
    object Next();
}

public interface IAggregate
{
    IIterator GetIterator();
}

public class ConcreteAggregate : IAggregate
{
    private List<object> _items = new List<object>();

    public IIterator GetIterator()
    {
        return new ConcreteIterator(this);
    }

    public int Count
    {
        get { return _items.Count; }
    }

    public object this[int index]
    {
        get { return _items[index]; }
        set { _items.Insert(index, value); }
    }
}

public class ConcreteIterator : IIterator
{
    private ConcreteAggregate _aggregate;
    private int _current = 0;

    public ConcreteIterator(ConcreteAggregate aggregate)
    {
        this._aggregate = aggregate;
    }

    public bool HasNext()
    {
        return _current < _aggregate.Count;
    }

    public object Next()
    {
        return _aggregate[_current++];
    }
}
```
