# Data Source Architectural Patterns

## Row Data Gateway
Row Data Gateway is a pattern in which an object acts as a gateway to a single row in database. The object can also perform update and inserts into the database. This object can be accessed with a common programming mechanism. This is essential to use because business logic coupled with database access logic can be quite complicated and mess up so to sort it out, we need it separated or decoupled.

## Table Data Gateway
Table Data Gateway is a pattern in which an object acts as a gateway to a single table or view in a database. The object can also perform update and inserts into the database. The idea is that 1 Table Data Gateway is to be used per table. This is essential to use because business logic coupled with database access logic can be quite complicated and mess up so to sort it out, we need it separated or decoupled.
Basically this object has some methods like find, findByName, update, insert, delete much like SQL operations.

## Active Record
Active Record is a pattern in which an object instance is tied to a single row in the table. When this objects properties are updated, it will also persist in the database. Active Record is usually used by Object relational Mappers as this objects are usually generated automatically by them. Some people view this as an anti-pattern due to a violation in Single Responsibility Principle(SRP) as every class will have a method and properties for insert, update, delete, save, validation and so on so forth. This pattern is good if you have a business logic next to none but that is rare in software development world.
