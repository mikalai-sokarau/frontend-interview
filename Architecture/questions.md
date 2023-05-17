### What is software architecture?
Software architecture is the process of designing the fundamental structure of a software system. It involves making high-level decisions about how the different components of a software system should interact with each other and with the external world.

The purpose of software architecture is to ensure that the system is well-organized, modular, and scalable, and that it meets the requirements of its users. A good software architecture should be flexible enough to accommodate changes and additions to the system over time, and it should be designed to be robust and reliable.

### What is a difference between functional and non-functional requirements?
Functional requirements describe what a system or product is supposed to do or how it should behave. They specify the features, functions, and capabilities that a product must have to satisfy the users' needs. Non-functional requirements, on the other hand, describe how the system or product should perform or behave, including its performance, usability, reliability, security, and other quality characteristics.
In other words, functional requirements define what the system or product should do, while non-functional requirements define how well it should do it.

### What are the most important types of non-functional requirements in your opinion?
* Performance: Performance requirements specify how fast the software system should respond to user requests and process data. They are typically defined in terms of response time, throughput, and resource utilization.
* Usability: Usability requirements specify how easy it is to use the software system. They are typically defined in terms of user interface design, accessibility, and user experience.
* Security: Security requirements specify how the software system should protect against unauthorized access, data breaches, and other security threats. They are typically defined in terms of authentication, authorization, encryption, and data privacy.
* Reliability: Reliability requirements specify how dependable and available the software system should be. They are typically defined in terms of uptime, fault tolerance, and disaster recovery.
* Scalability: Scalability requirements specify how the software system should handle increasing volumes of data, users, and requests. They are typically defined in terms of load balancing, horizontal scaling, and vertical scaling.
* Maintainability: Maintainability requirements specify how easy it is to maintain and modify the software system. They are typically defined in terms of code quality, documentation, and modularity.
* Interoperability: Interoperability requirements specify how well the software system should work with other systems and technologies. They are typically defined in terms of data exchange formats, protocols, and standards.

### How quality attributes related to non-functional requirements?
Quality attributes are a type of non-functional requirement that describe the overall characteristics or properties of a system, rather than specific behaviors or features. Non-functional requirements, in general, describe the aspects of a system that are not related to its functional behavior or features.
Quality attributes are a subset of non-functional requirements that specifically address the quality or performance characteristics of a system. Examples of quality attributes include reliability, scalability, availability, maintainability, and security.
For example:
Non-functional requirement - the system has to be available 99.99% of time.
Quality attribute - availability.

### What approaches to separate an application do you know?
There are several approaches to separating an application, depending on the requirements and constraints of the system. Here are a few examples:
* Monolithic architecture: In this approach, the entire application is developed as a single, self-contained unit. All components and modules are tightly coupled, and the application is typically deployed on a single server or set of servers. This approach is simple to develop and deploy but can become unwieldy and difficult to scale as the application grows.
* Service-oriented architecture (SOA): In this approach, the application is separated into a set of loosely-coupled, independent services. Each service performs a specific function or task and communicates with other services through well-defined interfaces. This approach can provide greater flexibility and scalability but can also be complex to develop and manage.
* Microservices architecture: This is an extension of SOA that breaks down the application into even smaller, independent services that can be developed, deployed, and scaled independently. Each microservice typically runs in its own container or process, and communicates with other microservices through APIs. This approach can provide even greater flexibility and scalability, but also requires additional development and management overhead.
* Modular architecture: In this approach, the application is divided into modules, each of which performs a specific function or task. The modules can be developed independently and assembled into a cohesive application at runtime. This approach can provide greater flexibility and maintainability, but can also be complex to design and implement.

### What tools are used to measure coverage of non-functional requirements in front-end projects?
* SonarQube - security, maintainability, reusability, testability, supportability.
* BlackDuck - security.
* Lighthouse - performance.
* ESLint - code consistency.

### What types of deployment exist?
* All at once (in-place deployment)
* Rolling deployment
* Blue/green deployment
* Canary deployment
...

### What architecture level do you know?
* Enterprise architecture - this level deals with the overall structure and organization of an entire enterprise, including its business processes, information systems, and technology infrastructure.
* Application architecture - this level deals with the design and organization of individual applications, including their components, modules, and interfaces.
* Domain architecture - this level deals with the design and organization of specific domains within an application or system, including their business logic, data models, and interfaces.
* Component architecture - this level deals with the design and organization of individual components or modules within an application, including their functionality, interfaces, and dependencies.
* Technical architecture - this level deals with the design and organization of the underlying technology infrastructure that supports an application or system, including hardware, software, and network components.

### What an architect does on the project?
A software architect is responsible for the design and overall technical direction of a software project. Their main role is to create a blueprint of the software system that describes how different components and modules will work together to meet the functional and non-functional requirements of the system.

### What does micro frontend approach mean?
Micro frontends is an architectural pattern where a front-end application is divided into smaller, self-contained and loosely-coupled micro-applications, each responsible for a specific part of the user interface. These micro-applications can be developed, deployed, and maintained independently, allowing for flexibility and scalability in front-end development.

Pros:
* Scalability and flexibility: Micro frontends allow for independent development and deployment of smaller, self-contained components, enabling teams to work independently and at their own pace. This can result in improved scalability, flexibility, and faster development cycles.
* Reusability and maintainability: Micro frontends can promote reusability of components and UI elements across multiple applications, reducing duplication of code and efforts. This can lead to improved maintainability and easier updates and bug fixes.
* Team autonomy: Micro frontends allow for separation of concerns, enabling different teams to work independently on different parts of the front-end application. This can lead to better team autonomy, ownership, and productivity.
* Technology diversity: Micro frontends allow for the use of different technologies and frameworks for different micro-applications, providing flexibility in technology choices based on the specific requirements of each micro-app. This can be advantageous in scenarios where different teams have different technology expertise or when integrating with legacy systems.

Cons:
* Increased complexity: Micro frontends introduce additional complexity in terms of managing multiple micro-applications, coordinating communication and state management between them, and handling cross-cutting concerns such as authentication, performance optimizations, and error handling.
* Overhead and setup costs: Setting up and managing a micro frontends architecture requires additional effort in terms of tooling, infrastructure, and deployment pipelines. There may be overhead costs associated with managing multiple micro-applications, coordinating their development and deployment, and ensuring consistency across them.
* Potential performance impact: Micro frontends may introduce additional overhead in terms of network requests, as each micro-application may require separate loading and execution of its own resources. This can impact performance and increase load times, especially in scenarios where multiple micro-applications are loaded on the same page.
* Complexity in cross-cutting concerns: Managing cross-cutting concerns such as authentication, state management, and UI consistency can be challenging in a micro frontends architecture, as these concerns may need to be addressed separately for each micro-app. This can add complexity and increase development efforts.



### Examples of non-functional requirements on your project and how to test / improve them on the project?
