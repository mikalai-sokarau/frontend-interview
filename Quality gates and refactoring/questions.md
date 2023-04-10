### What is quality gates?
It is set a of rules and standards that are put in place to ensure that code quality is maintained throughout the development process. These gates can be applied to various stages of the software development lifecycle, including coding, testing, and deployment. Quality gates are designed to help identify and prevent issues early on in the development process, which can save time and money by reducing the number of defects and issues that arise later on in the development cycle.

Examples of quality gates:
Code review.
Automated testing.
Code coverage: The percentage of code covered by automated unit tests.
Branch coverage: A more specific version of code coverage that measures the percentage of execution paths covered by tests.
Code coverage on new code: The same as the first example, but targeting only new code.
Code churn: How soon and often code gets rewritten.

### Quality Attributes
Reliability - ability to properly perform the required actions under predefined conditions for a certain period of time
Testability - how easy to test a piece of code or functionality
Performance efficiency - how fast the system returns a result
Security - how well are the system and its data protected against attacks
Usability - how effectively end users can use, learn, or control the system
Scalability - the ability to meet the demand of increased usage (Black Friday test)
Maintainability - how easy to upgrade and troubleshoot the system
Flexibility - how easy to adapt the system to different environments and configurations
Localization - how will the system detect and display different languages/currencies
Accessibility - how the system is accessible to all types of users
...

The most important quality attributes will depend on the specific needs and goals of the application and the stakeholders. It may be necessary to prioritize some attributes over others depending on the context.

### Refactoring
Refactoring is a systematic process of improving code without creating new functionality that can transform a mess into clean code and simple design.

When to refactor
Rule of Three:

When you’re doing something for the first time, just get it done.
When you’re doing something similar for the second time, cringe at having to repeat but do the same thing anyway.
When you’re doing something for the third time, start refactoring.

### Technical debt
Causes of technical debt:

Time pressure/deadlines
Delayed refactoring
Poor alignment to standards
Insufficient testing
Overly complex technical design
Suboptimal code
Lack of skill
When there is too much tech debt, engineers spend all their time fixing bugs and cannot switch to new, revenue-building functionality. Organizations that don’t take technical debt seriously – and dedicate time to keep it under control – will have a harder time retaining talent, and in the worst cases, a harder time hiring as well. Business doesn't know how to develop applications and ideally shouldn't insist on tight deadlines.

### How to explain the idea of technical debt to non-technical people? Car analogy:
Many people want to buy a car and cannot decide to postpone that purchase for months or years to save up the necessary cash: So they take out a car loan. That means they’re paying extra for the car over time, but they get what they need now. And even if your vehicle is paid in full, you’ve still got maintenance to consider: Ignoring it will likely cause more expensive problems later, including downtime for major repairs.

### How to maintain code quality on the project?
Follow best practices, conventions and principles (codding, commiting, commenting, SOLID, KISS, etc.)
Use automatic tools (linters, prettiers) to keep the codebase consistent (ESLint, JSLint, Prettier, .editorconfig)
Use static code analizators (SonarQube, DeepSource)
Use docker vulnerability scanners (Snyk, Docker Bench)
Use automatic source/dependency checkers (Dependabot, BlackDuck)
Write tests (unit, integration, e2e, etc.)
Use pre-commit/push hook
Use typed version of javascript (TypeScript, Flow)
Adopt continuous integration
Manually review pull requests
Practice pair programming

### Pros and cons of using pre-commit hooks?
Pros:
* Preventing issues: Pre-commit hooks can prevent issues before code is committed, which can save time and effort in the long run.
* Consistency: Pre-commit hooks can enforce consistent code style and formatting across the team.
* Automation: Pre-commit hooks can automate repetitive tasks such as linting and code formatting, freeing up developers' time to focus on more important tasks.
* Early detection: Pre-commit hooks can detect issues early in the development process, allowing them to be fixed before they cause problems downstream.

Cons:
* Slower development: Pre-commit hooks can slow down development by adding additional steps and checks before code can be committed.
* Limited rules: Not all rules may be covered by pre-commit hooks, so some issues may still slip through.
* --no-verify

### What is a code smell?
Code smells are characteristics or patterns in code that indicate potential problems or weaknesses in its design. These smells can make the code harder to read, maintain, or extend, and can lead to bugs or other issues. Some examples of code smells include duplicated code, long methods, unused variables, and complex conditional statements.

### What metrics can be obtained from SonarQube?
* Code coverage: This metric measures the percentage of code that is covered by automated tests.
* Code duplications: This metric measures the amount of duplicated code in the project.
* Code complexity: This metric measures the complexity of the code, such as the number of lines of code, the number of methods, and the number of parameters.
* Code smells: This metric identifies any coding practices that might indicate potential problems in the code, such as long methods, large classes, and duplicated code.
* Security vulnerabilities: This metric identifies any security vulnerabilities in the code, such as SQL injection, cross-site scripting, and buffer overflows.
* Maintainability: This metric evaluates the ease with which the code can be maintained, such as the code readability, documentation, and the number of bugs.
...

### What unit tests best practices do you know?
* Test only one thing: Each unit test should test a single behavior of a function or a class.
* Keep it simple: Unit tests should be simple and straightforward, focusing on the functionality being tested without extraneous code.
* Test edge cases: Unit tests should include tests for edge cases to ensure the code handles unexpected input and conditions.
* Use meaningful names: Name your tests clearly and descriptively to make it easy to understand the intent of the test.
* Isolate dependencies: Use mocks, stubs, or fakes to isolate the code being tested from its dependencies.
* Run tests often: Run your unit tests frequently to catch regressions early in the development cycle.
* Keep tests independent: Unit tests should be independent of each other, meaning that the failure of one test should not cause other tests to fail.
* Test both positive and negative cases: Unit tests should include tests for both valid and invalid input to ensure the code behaves correctly in both cases.
* Use a testing framework: Use a testing framework to organize and run your tests and to provide helpful output when tests fail.
* Test for performance: If your code has performance requirements, include tests that measure performance to ensure that the code meets those requirements.

### What is testing pyramid?
The testing pyramid is a visual representation / testings strategy of the different types of tests that should be included in a software testing strategy. The pyramid is made up of three layers, each representing a different type of test, with the largest layer at the bottom of the pyramid and the smallest layer at the top. The layers, from bottom to top, are:
* Unit Tests: These tests are at the bottom of the pyramid and make up the largest layer. They are automated tests that focus on testing individual units or components of the code in isolation. Unit tests are typically written by developers and are used to ensure that each individual unit of code is working as expected.
* Integration Tests: The middle layer of the pyramid is made up of integration tests. These tests focus on testing how the different units or components of the code work together. Integration tests are used to ensure that the different units of code can work together as expected and that there are no issues or bugs in the interactions between them.
* End-to-End Tests: At the top of the pyramid is the smallest layer, which is made up of end-to-end tests. These tests focus on testing the entire system or application, from the user interface down to the database. End-to-end tests are used to ensure that the application works as expected from a user's perspective and that all the different components work together seamlessly.

### What alternatives does the test pyramid have?
* The testing trophy: The testing trophy is a testing strategy that emphasizes end-to-end testing. It has a base of unit tests, followed by integration tests, API tests, UI tests, and end-to-end tests.
* The diamond model: The diamond model is a testing strategy that places equal emphasis on unit tests, integration tests, and end-to-end tests, with fewer API tests and no UI tests.
* The ice cream cone model: The ice cream cone model is a testing strategy that emphasizes end-to-end testing. It has a small number of unit tests, followed by a larger number of integration tests, API tests, and UI tests, and finally, a large number of end-to-end tests.
* The hourglass model: The hourglass model is a testing strategy that starts with unit tests, then moves to a small number of integration tests, followed by a large number of end-to-end tests.