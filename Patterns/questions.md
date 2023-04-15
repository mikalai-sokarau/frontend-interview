### What are design patterns?
Design pattern is a way of organizing and structuring code to solve common problems that arise during software development. It's like a blueprint or a template that describes a proven solution to a particular coding challenge. Design patterns are reusable and provide a standard approach to designing software, making it more efficient and maintainable.

### Why design patterns needed?
Design patterns are important in software development for several reasons:
* Reusability: encapsulate best practices and provide reusable solutions that can be applied in different projects, saving time and effort in reinventing the wheel.
* Maintainability: help in creating code that is easier to understand, modify, and maintain.
* Scalability: help in designing software that can adapt and evolve over time, making it easier to add new features or accommodate increased workload.
* Code quality: promote good coding practices, such as separation of concerns, loose coupling, and high cohesion.
* Communication and Collaboration: provide a common language and vocabulary for developers.
...

### Can you provide an example of a design pattern you have used in a commercial project?
* Singleton: restricts the instantiation of a class to a single instance and provides a global point of access to that instance. (e.g. config containing .env variables, logger class)
* Observer: establishes a one-to-many relationship between objects, where changes in one object are automatically reflected in other objects that depend on it. It could be used in a project where you need to notify multiple objects of changes in a particular object, such as an event handling system or a notification system.
* Adapter: allows objects with incompatible interfaces to work together by providing a common interface that they can both implement. It could be used in a project where you need to integrate existing components or systems that have different interfaces, such as integrating with third-party APIs or legacy systems. (e.g. integration with different front-end frameworks).
* Decorator: allows behavior to be added to an object dynamically without changing its original interface. It could be used in a project where you need to add additional functionality or behavior to objects dynamically (e.g. performance measuring).

These are just a few examples of the many design patterns that can be used. The choice depends on the specific requirements and architecture of the project.

### What patterns are used in modern front-end frameworks?
* Decorator: often used in front-end frameworks to add additional behavior or styling to UI components without modifying their functionality. Used a lot in Angular and Vue.
* Template Method: used in frameworks like Angular and Vue to define reusable templates for UI components.
* Dependency Injection (DI): used in Angular, where dependencies between components are managed and injected by the framework itself.
* Virtual DOM: used in frameworks like React and Vue, where an in-memory representation of the UI is maintained, and changes to the UI are first applied to the virtual DOM, which is then efficiently updated in the actual DOM.
* Command: Redux and actions can be considered an example of the Command pattern, where actions are plain JavaScript objects that represent a specific type of command or action that is dispatched to the Redux store to trigger state changes.
...

### What are potential problems with Singleton pattern?
* Global state: Can introduce global state, as the Singleton instance is globally accessible, which may lead to potential issues with maintainability, debugging, and understanding the flow of data in the application.
* Tight coupling: Can introduce tight coupling between objects, as objects may directly rely on the Singleton instance, making it difficult to switch or mock the Singleton instance during testing or when changing requirements.
* Thread safety: In multi-threaded environments, Singleton pattern may require additional complexity to handle concurrent access to the Singleton instance and ensure thread safety, which can be error-prone and challenging to implement correctly.
...

### GOF patterns:
Creational Patterns:
* Singleton: Ensures a class has only one instance, and provides a global point of access to that instance.
* Factory Method: Defines an interface for creating objects, but allows subclasses to alter the type of objects that will be created.
* Abstract Factory: Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
* Builder: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
* Prototype: Creates new objects by cloning existing ones, and avoids the need for explicit instantiation.

Structural Patterns:
* Adapter: Converts the interface of a class into another interface that clients expect, allowing classes with incompatible interfaces to work together.
* Bridge: Decouples an abstraction from its implementation, allowing them to vary independently.
* Composite: Represents objects in a tree-like structure, allowing clients to treat individual objects and compositions of objects uniformly.
* Decorator: Dynamically adds or modifies behavior of an object by wrapping it with one or more decorators.
* Facade: Provides a simple interface to a complex subsystem, hiding its complexities from clients.
* Flyweight: Shares objects to reduce memory usage, especially for objects with similar or repetitive state.
* Proxy: Represents an object with a substitute object, controlling access to the original object.

Behavioral Patterns:
* Observer: Defines a one-to-many relationship between objects, so that when one object changes state, its dependents are automatically notified and updated.
* Template Method: Defines the skeleton of an algorithm in a method, allowing subclasses to redefine certain steps without changing the overall algorithm's structure.
* Strategy: Defines a family of interchangeable algorithms and encapsulates them, allowing them to be selected at runtime.
* Command: Encapsulates a request as an object, allowing users to parameterize clients with queues, requests, and operations.
* Chain of Responsibility: Allows multiple objects to handle a request in a chain, until one of them handles it.
* State: Represents the state of an object as an object, allowing it to change its behavior based on its internal state.
* Mediator: Defines a mediator object that encapsulates the interaction between objects, allowing them to communicate without knowing each other's details.
* Memento: Captures and restores an object's internal state, without violating encapsulation.
* Iterator: Provides a way to sequentially access elements of a collection, without exposing the underlying representation.
* Visitor: Separates operations on elements from the structure of the elements, allowing new operations to be added without modifying the elements.

### Can you provide an example of the Observer pattern in JavaScript?
For example addEventListener() method used to attach event listeners to DOM elements and receive notifications when events occur.

### What is the difference between currying and partial application of a function?
Currying: transforms a function with multiple arguments into a sequence of functions that take one argument at a time and return a new function after each argument is provided. 
```javascript
// Curried function
const add = (a) => (b) => (c) => a + b + c;

// Usage
const result = add(1)(2)(3);
console.log(result); // Output: 6
```

Partial Application: proves some arguments of a function to create a new function with fewer arguments that can be invoked with the remaining arguments.
```javascript
// Function with multiple arguments
const greet = (greeting, name, age) => {
  console.log(`${greeting}, ${name}! You are ${age} years old.`);
};

// Partially applied function
const greetHello = greet.bind(null, 'Hello'); // Fixing the first argument

// Usage
greetHello('John', 25);
// Output: Hello, John! You are 25 years old.
```

### What is memoization?
It's a technique used in computer programming to optimize the execution time of a function by caching the results of its computations for a given set of inputs, so that if the function is called again with the same inputs, the cached result can be returned instead of re-computing the result.

### Why immutability is important?
It is important because it ensures that once a value is assigned, it cannot be changed, leading to less complex code and fewer unexpected side effects. Immutable data also enables safer concurrent and parallel processing, as it eliminates the need for locks or other synchronization mechanisms, making programs more scalable.

### Functional programming best practices?
* Use pure functions: Pure functions do not have side effects and always produce the same output for the same input, making them predictable and easy to test. Avoid mutable state and global variables within functions.
* Use immutability: Prefer immutability in data structures and avoid modifying data in place. Instead, create new objects or copies when needed to ensure that data remains immutable.
* Use recursion: Take advantage of recursion, which is a natural fit for functional programming, to solve problems in a concise and elegant way.
* Avoid shared mutable state: In functional programming, shared mutable state can lead to complex and hard-to-debug issues. Minimize or eliminate shared mutable state and prefer immutable data structures and functional techniques like recursion and higher-order functions.
* Use higher-order functions: Higher-order functions are functions that take one or more functions as arguments or return a function as a result.
...

### What is separation of concerns?
It is a software engineering principle that advocates for dividing a complex system into smaller, more manageable parts, each responsible for a specific aspect of functionality. This helps to reduce complexity, improve maintainability, and promote modularity in software development.

### What is low coupling?
Low coupling means that components within a software system have minimal dependencies on each other. They are loosely connected and can function independently without relying heavily on each other. Changes in one component have minimal impact on other components, making the system more flexible and easier to maintain.

### What is high cohesion?
High cohesion means that the elements within a module or component work closely together, with a clear and focused purpose. They are tightly related and work towards achieving a single, well-defined goal. This makes the module or component easier to understand, test, and maintain, as it has a clear and cohesive purpose without unnecessary complexity or unrelated functionality.

### What is the purpose of dividing an application into different layers or responsibilities?
It helps with separation of concerns, making the application more maintainable and easier to understand. It allows different teams or developers to work on different parts of the application independently.

### What are some common software architecture patterns?
Model-View-Controller (MVC):
* Model: Represents the data and business logic of the application.
* View: Displays the user interface to the user.
* Controller: Handles user input, updates the Model and View accordingly, and manages the interaction between the Model and View.

Model-View-Presenter (MVP):
* Model: Represents the data and business logic of the application.
* View: Displays the user interface to the user.
* Presenter: Acts as an intermediary between the Model and View, handles user input, updates the Model and View accordingly, and separates the business logic from the user interface.

Model-View-ViewModel (MVVM):
* Model: Represents the data and business logic of the application.
* View: Displays the user interface to the user.
* ViewModel: Exposes the data and commands that the View needs to display the user interface, communicates with the Model to update the data, and separates the View from the business logic.

### Can you provide examples of how these patterns are used in real projects with current technologies?
* MVC, MVP, MVVM, and NVM patterns are widely used in various projects and technologies. For example, MVC is commonly used in web development frameworks like Ruby on Rails and Spring MVC.
* MVP is used in older versions of Angular (AngularJS) and some iOS app architectures.
* MVVM is used in modern front-end frameworks like Angular, React, and Vue.

### How does the controller/presenter/component in these patterns interact with the view and model?
The controller in MVC, presenter in MVP, and view-model in MVVM act as mediators between the view and model, handling user interactions, updating the model, and updating the view. They facilitate communication and coordination between the view and model components.

### What is Redux?
Redux is a pattern commonly used with frameworks like React. It provides a predictable and centralized way to manage application state, making it easier to handle complex state interactions, debug state changes, and build scalable applications.

Pros:
* Centralized State Management: Redux provides a single source of truth for the application state, which makes it easier to manage and debug the state changes in a large application with complex state interactions.
* Predictable State Updates: Redux follows a strict unidirectional data flow, making state updates more predictable and traceable, which helps to reduce bugs and improve code maintainability.
* Time Travel Debugging: Redux allows for time travel debugging, enabling developers to replay and inspect state changes at different points in time, which can be a powerful tool for debugging and troubleshooting.

Cons:
* Learning Curve: Redux has a learning curve, especially for developers who are new to the concepts of state management, immutability, and functional programming, which may require some upfront investment in learning and understanding the Redux ecosystem.
* Boilerplate: Redux can introduce some additional boilerplate code, such as actions, reducers, and store configurations, which may increase development time and effort compared to other state management solutions.
* Overkill for Small Applications: Redux may be overkill for small-scale applications with simple state requirements, and using Redux in such cases may introduce unnecessary complexity and overhead.

### What are 3 main concepts of Redux?
* Single source of truth​ The global state of your application is stored in an object tree within a single store.
* State is read-only​ The only way to change the state is to emit an action, an object describing what happened.
* Changes are made with pure functions​.

### What are 3 core parts of Redux?
* Store: The store is a single source of truth that holds the entire state of the application. It is responsible for managing the state and providing methods to access, update, and subscribe to the state.
* Actions: Actions are plain JavaScript objects that represent the intention to change the state. They are dispatched to the store to trigger state updates.
* Reducers: Reducers are pure functions that handle actions and update the state of the store. They take the current state and an action as input and return a new state, without modifying the original state. Reducers are responsible for handling different actions and producing the next state of the application.

