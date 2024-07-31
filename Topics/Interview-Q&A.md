# Table of Content
- [Introduction](#introduction)
- [Behavioral Questions](#behavioral-questions)
- [Software Engineering Concepts](#software-engineering-concepts)
- [Front-End Questions](#front-end-questions)
- [Back-End Questions](#back-end-questions)
- [Coding Problems](#coding-problems)
- [References](#references)

## Introduction
I have compiled a list of questions that either I personally have gone through or have found online as I was preparing for interviews. These questions may or may not be applicable to you based on the stack you are focused on.





## Behavioral Questions

### **Q: Tell me about yourself?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- Where and what degree did you study.
- Describe a summary of your career journey.
- Describe your skills, work experience and your achievements.
- Go over some of your favorite hobbies.



### **Q: Why did you decide to become a Software Engineer?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- When did you decide to become a Software Engineer?
- Do you enjoy solving problems?
- Any genuine interest(s) in compputers, software or IT concepts?
- Do you enjoy creating things and bringing ideas to life?



### **Q: Tell me about a project you completed successfully?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- Give a specific project which you have worked on.
- Was there an issue, worth noting, that you came across? If so, how did you overcome it to complete the project on time?
- Use STAR technique to structure your answer:
  - STAR: **Situation** you faced, **Task** that needed to be done, **Action** you took to complete the task, Result from performing your action.



### **Q: What are the most important skills and qualities needed to be a great Software Engineer?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable:
- What are some important technical, interpersonal and soft skills needed?
  - **Technical**: Coding skills, testing, debugging, problem-solving, critical and logical thinking.
  - **Interpersonal**: Teamwork (and independent work), collaboration, communication, listening, explain complex technical information to non-technical indivduals.
  - **Soft Skills**: Adaptability, time management, creativity, attention to detail, and emotional intelligence.



### **Q: Why should we hire you as a Software Engineer?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- Mention some organizational values which motivate you.
- Knowledge sharing with other team members.
- Your view on self-development and on-going learning.
- Do you have skills that are not typical for Software Engineers that may be a great addition?



### **Q: How would you explain something technical to a non-technical person?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- Assess their technical knowledge. Don't dumb things too much and don't be too technical. Find the sweet spot.
- Make use of visuals, drawings and diagrams.
- Be sincere and welcoming to any follow up questions.
- Happily repeat or rephrase answer if needed.
- Allow other party to ask questions.



  ### **Q: What is your biggest weakness?**
You can answer this question by using the questions below as a guide and adding any relevant information you may think is applicable to you:
- Avoid giving weaknesses that are core requirements for the role you are applying for.
- Example of weaknesses:
  - Difficult to let go of projects.
  - Not good at public speaking or giving presentations.
  - Don't like giving extremely honest feedback because you are non-confrontational.
  - Don't like to immediately ask people for help, but like to research and figure things out yourself first.
  - Too self-critical or hard on yourself.
  - Not good at technical interviews (lol).





## Software Engineering Concepts

### **Q: Can you explain what is Object-Oriented Programming (OOP)?**
Object-Oriented Programming (OOP) is a programming paradigm that uses “objects” - data structures consisting of data fields and methods together with their interactions - to design applications and computer programs.



### **Q: What are the pillars of Object Oriented Programming (OOP)?**
- **Encapsulation**: This principle is about bundling the data, and the methods that operate on this data, into a single unit called a class. This mechanism helps to hide the internal state of an object and protect it from unauthorized access.
- **Abstraction**: Abstraction is about hiding the complexity and only showing the essential features of the object. So in a way, Abstraction means hiding the real implementation and we, as users, knowing only how to use it.
- **Inheritance**: Inheritance is a mechanism in which one object acquires all the properties and behaviors of a parent object. It's an important part of OOPs as it promotes the concept of reusability and is a way to achieve the desired functionality.
- **Polymorphism**: Polymorphism allows methods to do different things based on the object that it is acting upon. This is important for separating and organizing code to make it more flexible and maintainable.
  
The example below covers all four pillars of Object-Oriented Programming (OOP):
```
public class Animal
{
    public virtual void MakeSound()
    {
        Console.WriteLine("The animal makes a sound");
    }
}

public class Cat : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The cat says: Meow");
    }
}

public class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The dog says: Woof");
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        Animal myAnimal = new Animal();
        Animal myCat = new Cat();
        Animal myDog = new Dog();

        myAnimal.MakeSound();  // Outputs: "The animal makes a sound"
        myCat.MakeSound();     // Outputs: "The cat says: Meow"
        myDog.MakeSound();     // Outputs: "The dog says: Woof"
    }
}
```
- **Encapsulation**: The `Animal`, `Cat`, and `Dog` classes are examples of encapsulation. They bundle the data (none in this case) and methods `MakeSound` into a single unit (the class). The internal state of these objects is protected from unauthorized access.
- **Abstraction**: The `MakeSound` method in the `Animal` class is an example of abstraction. It hides the complexity and only shows the essential features of the object. The real implementation of how each animal makes a sound is hidden in the Cat and Dog classes.
- **Inheritance**: The `Cat` and `Dog` classes inherit from the `Animal` class. This is an example of inheritance, where `Cat` and `Dog` acquire all the properties and behaviors of Animal.
- **Polymorphism**: The `MakeSound` method is an example of polymorphism. It does different things based on the object that it is acting upon. For instance, when `MakeSound` is called on a `Cat` object, it outputs “The cat says: Meow”, and when called on a `Dog` object, it outputs “The dog says: Woof”.


### **Q: What is the difference between a class and an object?**
A class is a blueprint or template from which objects are created. An object is an instance of a class.



### **Q: What is a compiler?**
A compiler is a special program that processes statements written in a particular programming language and turns them into machine language or "code" that a computer's processor uses.



### **Q: What is a software library?**
A library in software is a collection of resources used to develop software, these may include pre-written code and subroutines, classes, values or type specifications.



### **Q: What is namespace in C#?**
A namespace is a keyword used to declare a scope that contains a set of related classes and types. It helps organize code into logical groups and provides unique class names. This allows the same class name to be used in different namespaces without conflict.



### **Q: What is a Data Type in programming?**
A data type in programming is an attribute of data which tells the compiler or interpreter how the programmer intends to use the data.



### **Q: Can you explain what is a data structure?**
A data structure is a particular way of organizing and storing data in a computer so that it can be accessed and modified efficiently.



### **Q: What is the difference between Stack and Queue?**
Stack is a LIFO (Last in First out) structure and Queue is a FIFO (First in First out) structure.
![image](https://github.com/user-attachments/assets/90a96789-4aba-4af7-bb23-7499b378f1c8)



### **Q: What is the difference between abstract and interface?**
Here's a summarized comparison of abstract classes and interfaces in C#:

- **Methods**: Abstract classes in C# can have both abstract and non-abstract methods (virtual or concrete), while interfaces can only have method signatures.
- **Variables**: Variables in an abstract class can be non-static and non-readonly, but those in an interface are always static and readonly in nature.
- **Implementation**: An abstract class can provide an implementation of an interface, but an interface can't implement an abstract class.
- **Members**: A C# abstract class can have public, private, and protected members, whereas an interface only has public members.
- **Inheritance**: An abstract class is extended using the ":" keyword, while an interface is implemented using the ":" keyword.

In essence, while both abstract classes and interfaces are used to create reusable and modular code in C#, they have different rules and use-cases.



### **Q: What is an algorithm?**
An algorithm is a step-by-step procedure, which defines a set of instructions to be executed in a certain order to get the desired output.


### **Q: What is the `time complexity` of an algorithm?**
Time complexity of an algorithm quantifies the amount of time taken by an algorithm to run, as a function of the length of the input.



### **Q: What is the `space complexity` of an algorithm?**
Space complexity of an algorithm quantifies the amount of space or memory taken by an algorithm to run, as a function of the length of the input.


### **Q: What is recursion in programming?**
Recursion in programming is a method where the solution to a problem depends on solutions to smaller instances of the same problem.



### **Q: What is a database?**
A database is an organized collection of data stored and accessed electronically. Databases are used to support storage, manipulation, and retrieval of data.



### **Q: What is SQL?**
SQL stands for Structured Query Language. It’s a standard language for interacting with databases. SQL can be used to insert, search, update, and delete database records.



### **Q: What is the difference between SQL and NoSQL databases?**
- **SQL databases** are relational, use structured query language, and are best for structured data with complex queries and transactions.
- **NoSQL databases** are non-relational, can handle various data types (structured, semi-structured, and unstructured), and are designed for scalability, making them ideal for big data and real-time web applications.



### **Q: What is Agile methodology?**
Agile is a philosophy or mindset centered around continuous improvement and flexibility. It’s a set of principles that guide project management and software development, focusing on delivering incremental value, fostering team collaboration, continual planning, and learning.
![image](https://github.com/user-attachments/assets/152fa7c6-58f4-4ffc-9378-fa5127c464f1)
Reference: https://hygger.io/guides/agile/



### **Q: What is Scrum?**
Scrum is a specific framework for implementing Agile. It structures work into short, iterative cycles known as sprints1. Scrum teams commit to shipping work at the end of each sprint and adopt practices and a team structure that helps them achieve this cadence.
![image](https://github.com/user-attachments/assets/8d429009-c218-4b2b-bdd2-17590886a21e)
Reference: https://www.scnsoft.com/software-development/software-development-models



### **Q: What is an API (Application Programming Interface)?**
An API is a set of rules that allow programs to talk to each other. The developer creates the API on the server and allows the client to talk to it.



### **Q: What is a RESTful API?**
A RESTful API is an architectural style for an application program interface (API) that uses HTTP requests to access and use data.



### **Q: What is Git?**
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.



### **Q: What is the difference between Git and GitHub?**
- **Git** is a version control system that lets you manage and keep track of your source code history.
- **GitHub** is a cloud-based hosting service that lets you manage Git repositories.



### **Q: What is a pull request in GitHub?**
A pull request is a method of submitting contributions to an open development project. It occurs when a developer asks for changes committed to an external repository to be considered for inclusion in a project’s main repository.



### **Q: What is Docker?**
Docker is an open-source platform that automates the deployment, scaling, and management of applications. It does this by isolating applications into containers.



### **Q: What is a microservice?**
Microservices - also known as the microservice architecture - is an architectural style that structures an application as a collection of services that are highly maintainable and testable, loosely coupled, independently deployable, organized around business capabilities, and owned by a small team.



### **Q: What is Kubernetes?**
Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications.



### **Q: What is a Full Stack Developer?**
A Full Stack Developer is a developer who can handle all the work of databases, servers, systems engineering, and clients. They are proficient in both front-end and back-end coding.



### **Q: What is a software development life cycle (SDLC)?**
The Software Development Life Cycle (SDLC) is a systematic process that defines the tasks performed during the development of software. It’s a methodology used to ensure that software is developed in a consistent, efficient, and high-quality manner.



### **Q: What is DevOps?**
DevOps is a set of practices that combines software development (Dev) and IT operations (Ops). It aims to shorten the systems development life cycle and provide continuous delivery with high software quality.



### **Q: What is Continuous Integration/Continuous Deployment (CI/CD)?**
CI/CD is a process that happens prior to deployment. It involves merging code changes frequently (Continuous Integration), running automated tests to ensure the application is not broken by the changes (also part of Continuous Integration), and then automatically deploying these changes to a staging or production environment (Continuous Deployment/Delivery).



### **Q: What is Test-Driven Development (TDD)?**
Test-Driven Development (TDD) is a software development process where you write a test before you write your code, and then write the code that makes the test pass.



### **Q: What is a software framework?**
A software framework is a universal, reusable software environment that provides particular functionality as part of a larger software platform to facilitate development of software applications.



### **Q: What is cloud computing?**
Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet (“the cloud”) to offer faster innovation, flexible resources, and economies of scale.



### **Q: What is Big Data?**
Big Data refers to extremely large data sets that may be analysed computationally to reveal patterns, trends, and associations, especially relating to human behaviour and interactions.



### **Q: What is Functional Programming?**
Functional programming is a programming paradigm where programs are constructed by applying and composing functions. It is a declarative type of programming style. Its main focus is on “what to solve” in contrast to an imperative style where the main focus is “how to solve”.



### **Q: What do we mean by data attributes?**
A data attribute is a data field that defines the characteristics or features of a data object. It mostly exists in a table format but can also refer to special values for objects in programming languages. In a word, data attributes are simply data that describe other data.



### **Q: What are the SOLID principals?**
- **[S] - Single-responsibility Principle**: A class should have one and only one reason to change, meaning that a class should have only one job.
- **[O] - Open-closed Principle**: Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.
- **[L] - Liskov Substitution Principle**: Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it.
- **[I] - Interface Segregation Principle**: Clients should not be forced to depend on interfaces they do not use.
- **[D] - Dependency Inversion Principle**: High-level modules should not depend on low-level modules. Both should depend on abstractions.



### **Q: What is the SOA (Service-Oriented Architecture)?**
SOA is an architectural style that focuses on discrete services instead of a monolithic design. It’s a way to make software components reusable and interoperable through service interfaces. Services use common interface standards and an architectural pattern so they can be rapidly incorporated into new applications.



### **Q: What is an EAI (Enterprise Application Integrtion)?**
EAI is the use of software and computer systems’ architectural principles to integrate a set of enterprise computer applications. It’s an integration framework composed of a collection of technologies and services which form a middleware to enable integration of systems and applications across an enterprise.



### **Q: What is an ESB (Enterprse Service Bus)?**
An ESB implements a communication system between mutually interacting software applications in a service-oriented architecture (SOA). It represents a software architecture for distributed computing, and is a special variant of the more general client-server model.



### **Q: What is an EDA (Enterprse Service Bus)?**
EDA is used by data scientists to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods. It helps determine how best to manipulate data sources to get the answers you need, making it easier for data scientists to discover patterns, spot anomalies, test a hypothesis, or check assumptions.



### **Q: What is a DDD (Domain-Driven Design)?**
DDD is a major software design approach, focusing on modeling software to match a domain according to input from that domain’s experts. DDD is against the idea of having a single unified model; instead it divides a large system into bounded contexts, each of which have their own model.



### **Q: What is JIT (Just-in-Time)?**
JIT refers to a type of compilation that happens during the execution of a program, rather than prior to execution. This approach can lead to significant performance improvements by optimizing the program for the specific hardware and conditions at runtime.



### **Q: What is GC (Garbage Collector)?**
Garbage collection is a form of automatic memory management. It’s a process that attempts to reclaim memory occupied by objects that are no longer in use by the program. .NET and .NET Core both have a garbage collector that manages the allocation and release of memory for your applications.



### **Q: .NET vs .NET Core?**
- **.NET Framework**: is a platform for building applications on Windows. It’s a mature framework with a large library base, great for building Windows desktop applications and games, and has excellent support for building web applications through ASP.NET.
- **.NET Core**: is a cross-platform (Windows, Linux, macOS) framework designed for building modern, cloud-based, and internet-connected applications3. It’s open-source and has a modular architecture, meaning you can include only the components needed for your application3. It’s also optimized for high performance and scalability3.



### **Q: How do you ensure code quality and maintainability in your projects?**
- Use consistent **coding standards** and **style guides** across the project.
- Enforce strict linting and **code formatting** using tools like ESLint or Prettier.
- Implement **unit testing** and **integration testing** with **automated testing frameworks**.
- Use **code review** processes to identify and fix issues.
- Utilize **Continuous Integration and Continuous Deployment (CI/CD)** pipelines to maintain quality throughout the development lifecycle.
- Follow **best practices**, like **SOLID principles** and **design patterns**, for better code organization and reusability.



### **Q: What are the different types of software testing?**
- **Unit Testing:** This is a type of testing where individual components of a software are tested. The purpose is to validate that each unit of the software performs as designed. A unit is the smallest testable part of any software. It usually has one or a few inputs and usually a single output. In procedural programming, a unit may be an individual function or procedure.

- **Integration Testing:** Integration testing is a level of software testing where individual units are combined and tested as a group. The purpose of this level of testing is to expose faults in the interaction between integrated units. Test drivers and test stubs are used to assist in integration testing.

- **Functional Testing:** Functional testing is a type of software testing whereby the system is tested against the functional requirements/specifications. Functions (or features) are tested by feeding them input and examining the output. Functional testing ensures that the requirements are properly satisfied by the application.

- **System Testing:** In system testing, the entire system is tested as per the requirements. Black-box type testing that is based on overall requirements specifications, covers all combined parts of a system.

- **Smoke Testing:** Smoke testing is a high-level type of software testing where the critical functionalities of the program are tested to see if they work or not. The result of this testing is used to decide if a build is stable enough to proceed with further testing.

- **Regression Testing:** Regression testing is a type of software testing that ensures that previously developed and tested software still performs the same way after it is changed or interfaced with other software. The purpose of regression testing is to ensure that changes such as those mentioned above have not introduced new faults.

- **Software Performance Testing:** Performance testing is a type of software testing that focuses on how a system running the system performs under a particular load. This is not about finding software bugs or defects. Performance testing measures the quality attributes of the system.

- **Security Testing:** Security testing is a process intended to reveal flaws in the security mechanisms of an information system that protect data and maintain functionality as intended. Due to the logical limitations of security testing, passing security testing is not an indication that no flaws exist or that the system adequately satisfies the security requirements.

- **User Acceptance Testing (UAT):** User acceptance testing (UAT) is the last phase of the software testing process. During UAT, actual software users test the software to make sure it can handle required tasks in real-world scenarios, according to specifications. UAT is one of the final and critical software project procedures that must occur before newly developed software is rolled out to the market.

- **Acceptance Testing:** Acceptance testing is a term used in agile software development methodologies, particularly extreme programming, referring to the functional testing of a user story by the software development team during the implementation phase. The customer specifies scenarios to test when a user story has been correctly implemented.



### **Q: What are the 12 factor principles?**
1. **Codebase**
   - **Explanation**: There should be one codebase tracked in version control, with many deploys (e.g., production, staging).
   - **Example**: A Git repository for a web application that is deployed to both a staging server and a production server.

2. **Dependencies**
   - **Explanation**: Explicitly declare and isolate dependencies.
   - **Example**: Using a `requirements.txt` file in Python to list all dependencies, which can be installed using `pip`.
   - **Example**: Using `dotnet` to add or restore packages / dependencies.

3. **Config**
   - **Explanation**: Store configuration in the environment.
   - **Example**: Using environment variables to store database connection strings instead of hardcoding them in the code.

4. **Backing Services**
   - **Explanation**: Treat backing services (like databases, queues) as attached resources.
   - **Example**: Connecting to a database using a URL stored in an environment variable, allowing the database to be swapped without changing the code.

5. **Build, Release, Run**
   - **Explanation**: Strictly separate build and run stages.
   - **Example**: Using a CI/CD pipeline where the build stage compiles the code, the release stage packages it, and the run stage deploys it.

6. **Processes**
   - **Explanation**: Execute the app as one or more stateless processes.
   - **Example**: A web application where each request is handled by a stateless process, allowing any instance to handle any request.

7. **Port Binding**
   - **Explanation**: Export services via port binding.
   - **Example**: A web server that listens on a port specified by an environment variable, making it easy to run multiple instances on different ports.

8. **Concurrency**
   - **Explanation**: Scale out via the process model.
   - **Example**: Running multiple instances of a web server to handle increased load.

9. **Disposability**
   - **Explanation**: Maximize robustness with fast startup and graceful shutdown.
   - **Example**: A web server that can start up quickly and handle termination signals to gracefully shut down.

10. **Dev/Prod Parity**
   - **Explanation**: Keep development, staging, and production as similar as possible.
   - **Example**: Using Docker to create identical environments for development, staging, and production.

11. **Logs**
   - **Explanation**: Treat logs as event streams.
   - **Example**: Sending log output to `stdout` and `stderr`, which can then be collected and analyzed by a logging service.

12. **Admin Processes**
   - **Explanation**: Run admin/management tasks as one-off processes.
   - **Example**: Running database migrations as a separate command that can be executed on demand.
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
## Front-End Questions

### **Q: What is the difference between LocalStorage, SessionStorage and Cookie?**
1. **LocalStorage:**
   - It's a web storage object that stores data with no expiration date. The data will not be deleted when the browser is closed and is available across browser sessions.
   - It allows for larger amounts of data to be stored (up to 10MB).
   - It provides methods like `setItem()`, `getItem()`, `removeItem()`, and `clear()` to manage the stored data.
2. **SessionStorage:**
   - It's similar to LocalStorage but the data is only available for the duration of the page session. The data gets cleared when the page session ends, i.e., when the browser or tab is closed.
   - It's suitable for storing temporary data during a user's session.
3. **Cookies:**
   - Cookies are small text files stored by the browser that are sent to the server with every request.
   - They are useful for small amounts of data and have options for expiration and domain restrictions.
   - They are supported by older browsers and are often used as a fallback for frameworks that use LocalStorage or SessionStorage.
In summary, LocalStorage, SessionStorage, and Cookies are all client-side storage solutions, each with their own use cases and limitations. LocalStorage is ideal for persistent data, SessionStorage for session-specific data, and Cookies for small amounts of data that need to be sent back to the server.



### **Q: What is the difference between a Function Declaration and a Function Statement in JavaScript?**
- **Function Declaration:**
   - A function declaration, also known as a function statement, declares a function with the `function` keyword[^1^][1][^2^][2].
   - The function declaration must have a function name[^1^][1][^2^][2].
   - Function declarations are hoisted, meaning they are executed before any other code[^1^][1][^2^][2].
   - The function in the function declaration can be accessed before and after the function definition[^1^][1][^2^][2].
   - Syntax: 
     ```javascript
     function functionName(param1, param2) {
       // Set of statements
     }
     ```
- **Function Expression:**
   - A function expression is similar to a function declaration without the function name[^1^][1][^2^][2].
   - Function expressions can be stored in a variable assignment[^1^][1][^2^][2].
   - Function expressions load and execute only when the program interpreter reaches the line of code[^1^][1][^2^][2].
   - The function in the function expression can be accessed only after the function definition[^1^][1][^2^][2].
   - Function expressions are not hoisted[^1^][1][^2^][2].
   - Syntax: 
     ```javascript
     var functionName = function(param1, param2) {
       // Set of statements
     }
     ```



### **Q: What is the difference between `onload` and `ready`?**
- **onload:** This is a standard event in the DOM (Document Object Model) that is triggered when the entire web page has fully loaded. This includes all content such as images, scripts, CSS, etc. It's often used when the script needs to work with the size of images or other resources that need to be fully loaded.

- **ready:** This event is specific to jQuery, a popular JavaScript library. The `ready` event is triggered as soon as the DOM is loaded and ready to be manipulated by script. This means it can be triggered before all images and other resources are fully loaded. It's often used when the script just needs to work with the DOM or CSS properties, and doesn't need to wait for all resources to load.



### **Q: What is the difference between responsive and adaptive design?**
- **Responsive design** is a technique where a website’s layout adjusts to any screen size, ensuring the website functions well on any device. It uses fluid grids to resize and rearrange the layout based on percentage values.
- **Adaptive design**, on the other hand, involves creating multiple layouts, each optimized for a specific screen size or device type. The website detects the user’s device and displays the corresponding layout. This approach requires fixed layout sizes for specific screen dimensions, necessitating developers to create multiple layouts for predefined screen sizes or device capabilities.



### **Q: What is the difference between a static and dynamic website?**
- **Static websites** are built with HTML, CSS, and JavaScript. Their content remains the same for every access, and the server sends HTML files directly to the user’s browser. Examples include personal blogs and small business websites.
- **Dynamic websites** are built using server-side programming languages like Python, Java, PHP, Ruby, etc., and often use databases. When a user requests a page, the server runs code to generate the content, allowing for dynamic content display. Examples include social media platforms and content management systems.



### **Q: Why is RESTful API a popular choice in web development?**
RESTful API is a web development approach that offers several benefits, including being Stateless, Scalable, Performant, and Cacheable.
- **Stateless**: RESTful API is designed to be stateless. This means each request from the client to the server contains all the necessary information for the server to process it. The server doesn't need to maintain client state between requests, simplifying the server's architecture and enhancing scalability.
- **Scalable and Performant**: The stateless nature of RESTful API allows for better load balancing and horizontal scaling. Servers can distribute the workload more easily without coordinating client states, leading to improved performance.
These features make RESTful API a popular choice for enhancing the efficiency and maintainability of web services.



### **Q: What is the box model in CSS?**
The CSS box model is a key concept that defines how elements are rendered on a webpage. It consists of four main components:
- **Content**: The area holding the actual content, like text or images.
- **Padding**: The space between the content and the border.
- **Border**: The line that goes around the padding and content.
- **Margin**: The space between the border and the outside of the element.
Each of these components contributes to the total size of the element, which is crucial to consider during webpage design and layout.



### **Q: What is V8?**
V8 is an open-source JavaScript engine developed by Google, written in C++. It implements JavaScript according to the ECMAScript specification and provides a runtime for executing JavaScript code. It's used in applications like Google Chrome and Node.js.  

A key feature of V8 is its independence from the browser it runs in. This allowed Node.js developers to use V8 to execute server-side JavaScript, contributing to Node.js's popularity.



### **Q: What is hoisting in JavaScript?**
**Hoisting** is a feature in JavaScript that automatically moves variable, function, and class declarations to the top of their containing scope during the code parsing phase, before the code has been executed. This means you can use variables or functions before they are declared in the code.  

However, it's important to note that hoisting only applies to the declarations, not the initializations. If a variable is declared and initialized after using it, the variable will be undefined until it is initialized. This is because only the declaration is hoisted, not the initialization.



### **Q: What is a JavaScript Promise, and what are its different states?**
A **JavaScript Promise** is an object that signifies the eventual completion or failure of an asynchronous operation. It simplifies the management of multiple async operations and provides better error handling than callbacks or events. A Promise object can exist in one of three states:

- **Pending**: This is the initial state. The Promise is neither fulfilled nor rejected.
- **Fulfilled**: This means the operation has completed successfully.
- **Rejected**: This indicates that the operation has failed.

Promises are a powerful tool in JavaScript for managing asynchronous operations, making code easier to read and reason about.



### **Q: How do you handle browser compatibility issues?**
Browsers like Google Chrome, Mozilla Firefox, Safari, Microsoft Edge, etc., interpret web code differently. This can cause a web page or application to look and function differently across browsers. Here are some tips to handle browser compatibility issues:

- **Use a CSS Reset**: Different browsers have different default styles, which can cause layout inconsistencies. A CSS reset can help by setting a common baseline for all browsers.
- **Use Cross-Browser Frameworks and Libraries**: Frameworks and libraries like jQuery, React, or Angular can help developers avoid browser-specific code and provide a consistent interface across different browsers.
- **Test on Multiple Browsers and Devices**: Developers should test their websites or applications on multiple browsers, including popular ones like Chrome, Firefox, Safari, and Edge, to ensure compatibility.

- **Use Polyfills and Shims**: Polyfills and shims are code snippets that provide fallback functionality for web features not supported by some browsers. Libraries like Modernizr, Polyfill.io, or HTML5 Shiv can help fill in gaps in browser support.



### **Q: What do we mean by MEAN Stack?**
**MEAN** is a tech stack that stands for:

- **MongoDB**: A popular NoSQL database that stores data in a flexible, JSON-like format.
- **Express.js**: A back-end web application framework running on top of Node.js.
- **Angular.js**: A front-end web application framework developed by Google.
- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine that allows running JavaScript on the server side.

MEAN is a JavaScript-based stack used for developing cloud-ready applications. It provides a complete solution for building both the front-end and back-end of dynamic websites and applications using a single technology stack. This stack has gained popularity due to its user-friendly nature and open-source availability, which allows for community-driven improvements and updates.



### **Q: What is jQuery, and what are its features?**
jQuery is a fast and lightweight JavaScript library designed to simplify web development by reducing the amount of code needed. It offers several key features:
- **HTML/DOM Manipulation**: Allows easy manipulation of HTML documents and the Document Object Model (DOM).
- **Cross-Browser Compatibility**: Ensures consistent behavior across different web browsers.
- **CSS Manipulation**: Provides methods for changing CSS properties of elements.
- **HTML Event Methods**: Facilitates handling of user interactions through HTML events.
- **Effects and Animations**: Supports various effects and animations to enhance user experience.
- **AJAX Support**: Enables asynchronous web applications with AJAX.
- **Plugins**: Allows extension of jQuery's functionality with plugins.



### **Q: How do you share code between files in JavaScript?**
In JavaScript, code can be shared between files using 'imports' and 'exports'. This allows for modular programming, where code is split into smaller, reusable modules. Here's how it works:

- **ES5 Syntax**: In ES5, we use the `require` statement to import functions, objects or values from another file, and the `module.exports` statement to export them. Here's an example:

```
// File: module.js
export const name = 'JavaScript Module';

// File: main.js
import { name } from './module.js';
console.log(name);  // Outputs: 'JavaScript Module'
```
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
## Back-End Questions

### **Q: Explain the MVC design pattern?**
The Model-View-Controller (MVC) is a design pattern used in software development, particularly in web development. It simplifies complex software development by dividing it into three components:
- **Model**: Represents the application's data and business logic. It manages data, performs calculations, and responds to the controller's requests.
- **View**: Handles the user interface of the application. It displays the model's data to the users and provides a platform for interaction.
- **Controller**: Manages both the Model and View. It handles the application's flow, including data flow within the Model and updates the View whenever data changes.



### **Q: What is the difference between MVC (Model View Controller) and MVP (Model View Presenter)?**
The **MVC** (Model-View-Controller) and **MVP** (Model-View-Presenter) patterns are both architectural design patterns that help in organizing code in a structured manner:

- **MVC Pattern**: In MVC, the code is divided into three components: Model, View, and Controller. The Controller acts as an intermediary between the Model (which represents the data and business logic) and the View (which displays the data to the user). However, the support for unit testing is somewhat limited in the MVC pattern.

- **MVP Pattern**: MVP is an advanced iteration of software architecture, also composed of three components: Model, View, and Presenter. Unlike MVC, an interface in MVP communicates between the View-Presenter and Presenter-Model, making the View and Model completely independent. This separation makes unit testing highly supported in the MVP pattern, as each component can be tested independently.



### **Q: Talk about mock vs. stub.**
Mocks and stubs are two common methods used for unit testing. You can choose one or both, depending on the testing goals. Here is a comparison of mock vs. stub.
![image](https://github.com/XxDaShTixX/Software-Engineering-Essentials/assets/11358087/1bef9819-e570-41eb-a1e9-ed8dd85a3926)



### **Q: How do you ensure data security in your applications?**
Data security is crucial for protecting sensitive information, maintaining trust, complying with regulations, and preventing financial losses. Here are some measures to ensure data security in application development:
- **Secure Coding Practices**: Use secure coding practices like input validation, access controls, and error handling.
- **Data Encryption**: Protect data during transmission and storage in databases using encryption. This can help prevent data breaches and unauthorized access.
- **Strong Authentication**: Implement robust authentication techniques to ensure only authorized users can access sensitive data.
- **Regular Security Testing**: Conduct regular security testing, such as vulnerability assessments and penetration testing, to identify and address potential security risks before they can be exploited.
- **Follow Industry Best Practices**: Adhere to industry best practices and regulatory guidelines to ensure your applications are secure, efficient, and sustainable.



### **Q: What is the difference between unit testing and integration testing?**
- **Unit Testing**: This is a method where individual components or modules of software are tested during the development stage. The goal is to identify and fix errors in the smallest unit of code early in the development process.
- **Integration Testing**: This involves testing multiple units or components together. The purpose is to verify if the individual components function correctly when combined.



### **Q: Can you explain the concept of microservices architecture?**
- Microservices architecture is a design pattern where an application is built as a collection of small, loosely coupled, and independently deployable services. Each service focuses on a specific business capability and can be developed, tested, and deployed independently. This approach enhances scalability and resilience, and enables faster development cycles. 
- However, it also introduces complexity in areas like coordination, service communication, and data synchronization among microservices.



### **Q: Distinguish between Hashtable and HashMap.**
![image](https://github.com/XxDaShTixX/Software-Engineering-Essentials/assets/11358087/6315e9cf-22e5-44c6-9dbc-800eb3f3cc03)



### **Q: What is backtracking, and why do we use it?**
**Backtracking** is an algorithmic strategy that uses recursive calls to find solutions by incrementally building candidates and abandoning a candidate ("backtracks") as soon as it determines that the candidate cannot possibly be extended to a valid solution.

It's considered an improvement over the brute force approach as it eliminates many unnecessary paths in the search tree, thus providing an efficient way to solve problems.

Backtracking can be applied to a variety of problem types:
- **Decision Problems**: Backtracking can be used to find a feasible solution. It explores possibilities until it finds one that satisfies all constraints.
- **Optimization Problems**: Backtracking can be used to find the best solution. It systematically searches the entire solution space for the optimal solution.
- **Enumeration Problems**: Backtracking can be used to find all feasible solutions. It generates all configurations and tests each one to see if it satisfies all constraints.



### **Q: What are the main differences between process and thread?**
![image](https://github.com/XxDaShTixX/Software-Engineering-Essentials/assets/11358087/d9652012-c238-4be7-9367-99801af9e870)




## Coding Problems

### **Q: Implement a reversing linked list in C#**
This code assumes that you have a `Node` class with a `Value` property and a `Next` property.
```
public class Node
{
    public int Value { get; set; }
    public Node Next { get; set; }
}

public Node ReverseLinkedList(Node head)
{
    // Initialize current, previous, and next pointers
    Node current = head;
    Node previous = null;
    Node next = null;

    while (current != null)
    {
        // Store the next node, then update the current node
        next = current.Next;
        current.Next = previous;

        // Move previous and current one step forward
        previous = current;
        current = next;
    }

    return previous; // new head of the reversed list
}
```
This function works by iterating through the linked list, changing the `Next` pointer of each node to point to the previous node. The `previous` variable keeps track of the already reversed part of the list, while the `current` variable keeps track of the node that’s currently being processed. The `next` variable is used to temporarily store the next node in the original list before changing the `Next` pointer of the current node. The function returns the `previous` node, which is the new head of the reversed list.



### **Q: Maximum in Sliding Window Problem**
The “Maximum in Sliding Window Problem” is a common problem in computer science where you are given an array of integers and a window size, and you need to determine the maximum value in each window as the window slides through the array.
```
public class Solution {
    public int[] MaxSlidingWindow(int[] nums, int k) {
        // Check for base case
        if (nums == null || nums.Length == 0) return new int[0];

        // Initialize the result array
        int[] result = new int[nums.Length - k + 1];

        // Create a Double Ended Queue, Deque (in C# it's a LinkedList) 
        // It will store indexes of useful elements in every window
        LinkedList<int> deque = new LinkedList<int>();

        // Process the first k (window size) elements of array
        for (int i = 0; i < nums.Length; i++) {
            // For every element, the previous smaller elements are useless
            // so remove them from deque

            // Remove the elements which are out of this window
            if (deque.Count != 0 && deque.First.Value + k <= i) {
                deque.RemoveFirst();
            }

            // Remove all elements smaller than the currently
            // being added element (remove useless elements)
            while (deque.Count != 0 && nums[deque.Last.Value] < nums[i]) {
                deque.RemoveLast();
            }

            // Add current element at the rear of deque
            deque.AddLast(i);

            // The element at the front of the deque is the largest element of
            // previous window, so add to the result array
            if (i + 1 >= k) {
                result[i + 1 - k] = nums[deque.First.Value];
            }
        }

        return result;
    }
}
```
This code uses a deque to keep track of the maximum element for each window. The deque stores the indices of the elements, not the actual elements. The front of the deque contains the index of the maximum element of the current window, while the rest of the deque contains indices of elements that could become the maximum if the current maximum is removed. These potential maximums are stored in decreasing order in the deque. When we move to the next window, we add the new element to the deque (removing all smaller elements at the end), and remove the front of the deque if it’s outside the window. The front of the deque is then the maximum of the new window. This ensures that we can find the maximum of each window in constant time, making the algorithm very efficient. The time complexity of this algorithm is O(n), where n is the number of elements in the array, and the space complexity is O(k), where k is the size of the window. This is because we store at most k + 1 elements in the deque.



### **Q: Stock Buy Sell Problem**
The “Stock Buy Sell Problem” is a common problem where you’re given an array for which the ith element is the price of a given stock on day i. The goal is to design an algorithm to find the maximum profit. You may complete as many transactions as you like (i.e., buy one and sell one share of the stock multiple times). However, you must sell the stock before you can buy again.
```
public class Solution {
    public int MaxProfit(int[] prices) {
        // Check for edge cases
        if (prices == null || prices.Length <= 1) return 0;

        int maxProfit = 0;

        // Go through each day
        for (int i = 1; i < prices.Length; i++) {
            // If the current price is greater than the previous price,
            // we could get a profit from it by buying at the previous price
            // and selling at the current price
            if (prices[i] > prices[i - 1]) {
                maxProfit += prices[i] - prices[i - 1];
            }
        }

        return maxProfit;
    }
}
```
This code works by iterating through the array of prices and adding to the maximum profit whenever the current price is greater than the previous price. This is because we can always maximize our profit by buying at the lower price and selling at the higher price. The time complexity of this algorithm is O(n), where n is the number of days, and the space complexity is O(1), because we only use a constant amount of space to store the maximum profit.



### **Q: Merge K Sorted Arrays**
The “Merge K Sorted Arrays” problem is a common problem where you are given K sorted arrays and you need to merge them into a single sorted array.
```
public class Node : IComparable<Node>
{
    public int Value { get; set; }
    public int ArrayIndex { get; set; } // Index of array
    public int ElementIndex { get; set; } // Index of next element in array

    public int CompareTo(Node other)
    {
        if (Value > other.Value) return 1;
        if (Value < other.Value) return -1;
        return 0;
    }
}

public class Solution
{
    public List<int> MergeKSortedArrays(List<List<int>> arrays)
    {
        SortedSet<Node> pq = new SortedSet<Node>();
        List<int> result = new List<int>();

        // Initialize the priority queue with the first element from each array
        for (int i = 0; i < arrays.Count; i++)
        {
            if (arrays[i].Count > 0)
            {
                pq.Add(new Node { Value = arrays[i][0], ArrayIndex = i, ElementIndex = 0 });
            }
        }

        // Take the smallest (top) element from the priority queue,
        // add it to the result list, and insert the next element from the same array into the priority queue
        while (pq.Count > 0)
        {
            Node node = pq.Min;
            pq.Remove(node);
            result.Add(node.Value);
            if (node.ElementIndex + 1 < arrays[node.ArrayIndex].Count)
            {
                pq.Add(new Node { Value = arrays[node.ArrayIndex][node.ElementIndex + 1], ArrayIndex = node.ArrayIndex, ElementIndex = node.ElementIndex + 1 });
            }
        }

        return result;
    }
}
```
This code works by maintaining a priority queue of the smallest unprocessed element from each array. The priority queue is initialized with the first element from each array. Then, in each iteration, the smallest element is removed from the priority queue and added to the result list, and the next element from the same array is added to the priority queue. This process continues until the priority queue is empty, at which point all elements have been processed and the result list contains the merged and sorted elements from all arrays. The time complexity of this algorithm is O(N log K), where N is the total number of elements and K is the number of arrays, and the space complexity is O(K), because the priority queue stores at most one element from each array.





## References
- https://www.turing.com/interview-questions/senior-full-stack
- https://www.reddit.com/r/learnprogramming/comments/voet39/interview_questions_for_a_full_stack_position/
- https://atechdaily.com:8443/posts/difference-between-Stack-and-Queue-in-java
