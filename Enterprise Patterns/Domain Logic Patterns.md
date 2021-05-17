# Domain Logic Patterns

## Transaction Script

By definition, transaction script organizes business logic by procedures wherein each procedure handles a single request from the presentation.

Basically transaction script is:
* super simple as you have to write the procedure in one location
* just write the procedures sequentially and you are all set.
* Transaction script is best in non complext procedures. 
* because of this, transactione may be viewed as not OOP but rather Procedural.

## Domain Model
Well basically it is the object model of the domain with both behavior and data. This pattern creates interconnected objects wherein each object represents meaningful individual. This pattern leverages the full power of Object Oriented Programming as we think through entities and behaviors as oppose to properties. The mortal enemy of this pattern is the relational database as this databases usually returns a data that is not hierarchical but this problem is addressed by ORM's as this ORM's can may database select query returns easily or automatically.

