### What is React?
React is a JavaScript library for building user interfaces. It allows to create reusable UI components that update automatically in response to changes in data. React follows a component-based architecture, where the user interface is built as a tree of components, making it easy to manage.

Pros:
* Flexibility: React is a library, not a framework like Angular or Vue, which means it offers more flexibility in terms of how you structure and manage your application.
* Large ecosystem: React has a large and active community, with a rich ecosystem of third-party libraries, tools, and resources. This provides developers with a wide range of options and solutions for common tasks, such as state management, routing, and UI styling, making it easier to build complex applications.
* Learning curve: React has a relatively low learning curve compared to Angular and Vue.
* Good documentation.
* Backward Compatibility.
* Can be used for mobile development.

Cons:
* Manual configuration and integration of additional libraries for required functionality (routing, SSR, state management, i18n).
* JSX Syntax: React uses JSX (JavaScript XML) syntax, which may require developers to learn a new syntax and understand how it works.

### How does React work?
React uses a virtual DOM to keep track of changes in the UI components. It uses a process called "reconciliation" which is an algorithm that compares the current tree of components with the new tree of components and determines what needs to be updated or changed in browser's DOM. React components have lifecycle methods or hooks that allow developers to connect to different stages of a component's life, such as component creation, updates, and destruction.

### What is the difference between class components and functional components in React?
Class components are traditional React components that use class syntax and have access to lifecycle methods. They can have their own state and are typically used for more complex components. On the other hand, functional components are simpler and do not have their own state. They are written as JavaScript functions and are typically used for presentational or stateless components. Functional components can also use hooks to manage state and side effects.

### What is Angular?
Angular is a framework developed by Google. It is based on TypeScript. It has own routing, two-way Data Binding, use Dependency Injection, RxJS and so on.

Pros:
* Angular is a complete solution, it has own routing, SSR, modular system and so on.
* Large ecosystem: Angular has a large and active community, with a rich ecosystem of third-party libraries, tools, and resources, making it easier to build complex applications.
* Native TypeScript and RxJS integration.
* Built-in CLI that provides a set of commands for creating, building, and managing Angular projects.

Cons:
* Steeper learning curve: Angular has a steeper learning curve compared to some other front-end frameworks due to its comprehensive and complex features, especially for developers who are new to TypeScript or have limited experience with front-end frameworks.
* Overhead: Angular may have some overhead in terms of setup and configuration due to its extensive features and tools, which may require additional effort for initial setup and project configuration.
* Flexibility: Angular may have less flexibility compared to React and Vue, as it follows a more prescriptive approach to building applications, which may not be suitable for all projects or development teams with specific requirements.

### How does Angular work?
Angular is based on the concept of zones, which are a set of hooks that intercept and capture asynchronous operations such as promises, timers, and events. Angular uses a mechanism called "change detection" to detect changes in the application's state and update the view accordingly. Angular also uses a declarative approach to building UI components using templates, which are a combination of HTML, CSS, and JavaScript.

### How to choose a technology stack for a new front-end project?
1. Define Project Requirements: Clearly define the requirements of your project, including the expected functionalities, performance, scalability and timeline. Consider factors such as the size and complexity of the project, target audience, business goals and possible integrations.
2. Define existing customer's ecosystem.
3. Consider team expertise, think about newcomers, documentation, knowledge transfer.
4. Consider cost and time of adopting a new technology stack, including the potential costs of training, onboarding, and migration, as well as the estimated time required for development, testing, and deployment.
5. Define project specifics such as the complexity of the UI (SPA or multi-page), the need for server-side rendering, the availability of existing APIs, and integration requirements with other technologies or systems.

### How can we stay updated with the latest versions of libraries and dependencies?
* Regularly check for updates.
* Set up auto-notifications for new versions.
* Create tickets to update dependencies on a regular basis.

