# Aspect Oriented Programming

Programming Paradigm that increase modular by separation of business logic from **Cross Cutting Concerns**

Cross Cutting Concerns specifies as concerns that interacts with many parts of the program. 

For Example, you might need to  check if the user is authenticated/authorized before allowing them to interact with most parts of the system. You might also want log events when a system calls a method. 

Usually these concerns clogged up the code and cen be scattered and can be a burden in code maintenance.

You could say that Aspect Oriented Programming is somewhat like Decorator Pattern but that is not the case. Aspected Oriented Programming add or modifies behavior on method or class level while decorator pattern on single instance.
