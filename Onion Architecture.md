# Onion Architecture

An architecture wherein the business logic is sealed and protected from technological changes. We define the business logic once and we can change the tech anytime we want without affecting business logic.

## Onion Architecture Layers beginning from the inner:

### Domain Layer
* Also know as the business logic.
* This layer includes all business classes.
* Must have no dependencies on other layers.
* Representation of business not tech stack. 
* Includes repository definition not implementation. It is somewhat related to data access. 
* This means that the domain layer doesn't care where the data is coming from. Whether in MSSQL Server, MySQL, Mongo DB or even from a json file. 
It only cares about about the return types of data (like __**Interfaces**__) .
* This layer is like this because we know that business logic seldom changes like for example in stock trading what the process is for the past 20 years is the same as of this moment. 
We can also say that a business logic is only need to be implemented once. The one that is rapidly changing is the technology stack. 
For example you started to write your app in Angular 2, then after you finish it the Angular 5 is now available. 
Also same with the data access implementation, at first you thought that a RDBMS is the solution but you realize that a NoSql is better.
With this approach it is really easy to change because this layer does not implement the data access but rather just expects the return value (like __**Interfaces**__) .


### API Layer
* This is not Rest API.
* It is an API that will be used by Infrastracture layer to communicate in Domain Layer

### Infrastracture - repository implementation

Direction of coupling if from outer to inner
