# Service Consumer Patterns

## Composite Front-End
This pattern is almost the same as Composite Design Pattern except it is in the UI or Frontend. And this UI also wants to display data from multiple services. The basic idea is that the UI must be composable and each UI component is service-specific. In some Javascript Frameworks like Angular, this is super easy as it is built with components in mind. And we can make each component communicate to a specific service that we want without much coupling.

## Client-Server
A standard Client - Server has 3 parts:

* **Front End** - This is the part that interacts with the users or the part that the users see. It is designed to interact with all existing devices in the market not limited to PC. mobiles, and tablets.
* **Application server** - This is the part where all the software modules are installed. It connects to the database and interacts with users.
* **Database Server** - basically it contains the database.

It works like this:
1. The user makes a request in the front end. **_For example please give me all the orders received within x period._**
2. Then The Application Server gets the request then sends it to the database server. The database server processes the request then sends it to the response to Application Server then the application server sends the response to the front end.

This pattern separates hardware, software and functionalities. Only the front end must be adapted to communicate to different devices.
