# Web Presentation Pattern

## Model View Controller (MVC)
I first get this term when I was working around ASP.Net MVC but it was traditionally used in Desktop Applications. 
Basically, the aim of this pattern is to decouple the User Interface which is the **_View_**, data which is the **_Model_** and application logic which is the **_Controller_**.
This pattern aims to achieve separation of concerns.

Example for websites, when an MVC pattern is implemented, the:
* request is then routed to the **_Controller_**
* then the **_Controller_** works with the **_Model_** to retrieve or process the data depending on the application logic. The **_Controller_** gets also to decide on what **_View_** to return or display including the **_Model_**.
* then the **_View_** renders the final page/UI with the **_Model_**


## Page Controller
Basically it is as simple as one Controller to one Page logic. 
If you have used ASP.Net Webforms before each logical page (.aspx) and the behavior of the page which is in the code behind. 
As contrast to the **_Model View Controller (MVC)_**, **_Page Controller*_* combines both Views and Controllers.

## Front Controller
Basically this pattern redirects all request from a resource will be handled by **_one_** controller only. After that it can be the so called one controller can use some helpers or other means to achieve the desired results.

Advantages:
* Centralized and Simplicity.

Disadvantages:
* It is close to impossible to scale
