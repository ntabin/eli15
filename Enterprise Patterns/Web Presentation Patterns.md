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

## Template View
If you need a to develop a dynamic web page that changes the displayed data for every parameter change then this pattern is very useful to you.
By Definition it is HTML Page with embedded markers.
Basically it is just a HTML template. For example in ASP.Net MVC Razor Page:

```
<html>
  <head>
    <title>Index</title>
  </head>
  <body>
    <div>
      First Name: @FirstName
      Last Name: @LastName
    </div>
  </body>
</html>
```

In the sample above, the `@FirstName` and `@LastName` depending on the passed value.

## Transform View

By definition it is a View that transforms domain data into HTML, XML or JSON. 
As oppose to template view, **_Transaform View_** transforms data element by element. 
A good example of ths is the `JSON.stringify()` in javascript which returns a string containing the JSON representation of the supplied value.

## Two Step view
The problem this pattern solves is when we have a multiple page website, we want the website to have a consistent look on all web pages. With a template view, we duplicate all elements related to attain the consistent look. What we want is to have a way to alter the look globally.

By definition it is transforming of domain data into HTML in two steps. 
1) we separate the process of transforming  model data into a logical representation like a JSON or XML.
2) Then we convert that logical presentation with actual formatting that we desire. 

We can easily to this by:
1) Make the backend response to be JSON.
2) Use Angular, View or ReactJS to render the HTML. This way, the transformation is done by a JS Framework ad not manually.

## Application Controller
Basically this pattern makes the decision for which is the next View or screen to show sort of like the software wizard or setup assistant usually in Web Applications. All request will be directed to just one controller and the controller gets to decide what to do next on the request and on what  View or screen to show based on state. This pattern can be merge with **_Front Controller_** and **_Page Controller_** as both want to handle request on only one place.
