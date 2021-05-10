# Onion Architecture

* An architecture wherein the business logic is sealed and protected from technological changes. 
* We define the business logic once and we can change the tech anytime we want without affecting business logic.
* This architecture focuses on separation of concern.
* Dependency Injection is heavily used to implement this architecture.

## Onion Architecture Layers beginning from the inner:

### Domain Layer
* Also know as the business logic.
* This layer includes all business classes.
* Must have no dependencies on other layers.
* Representation of business not tech stack. 
* Includes repository definition not implementation. It is somewhat related to data access. 
* This means that the domain layer doesn't care where the data is coming from. Whether in MSSQL Server, MySQL, Mongo DB or even from a json file. 
It only cares about the definitions defined in contracts (like __**Interfaces**__).
* This layer is like this because we know that business logic seldom changes like for example in stock trading. What the process is for the past 20 years is the same as of this moment. 
We can also say that a business logic is only need to be implemented once. The one that is rapidly changing is the technology stack. 
For example you started to write your app in Angular 2, then after you finish it the Angular 5 is now available. 
Also same with the data access implementation, at first you thought that a RDBMS is the solution but you realize that a NoSql is better.
With this approach it is really easy to change because this layer does not implement the data access but rather just expects the definitions defined in contracts (like __**Interfaces**__).

### Application Layer
* This layer connects Infrastracture Layer to the Domain Layer

### Infrastracture Layer
* This is where repository or the data access is implemented implementation.
* This is also where some third party integrations is implemented.
* In short anything the application access externally is implemented Here

Direction of coupling is from outer to inner
