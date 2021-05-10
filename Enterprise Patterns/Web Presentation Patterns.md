# Web Presentation Pattern

## Model View Controller (MVC)
I first get this term when I was working around ASP.Net MVC but it was traditionally used in Desktop Applications. 
Basically, the aim of this pattern is to decouple the User Interface which is the **_View_**, data which is the **_Model_** and application logic which is the **_Controller_**.
This pattern aims to achieve separation of concerns.

Example for websites, when an MVC pattern is implemented, the:
* request is then routed to the **_Controller_**
* then the **_Controller_** works with the **_Model_** to retrieve or process the data depending on the application logic. The **_Controller_** gets also to decide on what **_View_** to return or display including the **_Model_**.
* then the **_View_** renders the final page/UI with the **_Model_**
