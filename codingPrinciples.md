# Coding Principles

## KISS (Keep it Simple Stupid)

Also known as Keet it super simple or Keep it simply simple.

Write code as simple as possible.

`if(payingCustomer)` is easier to read than `if(customer.paymentCustomerId != null)`

For function make it super simple, if the name of the function is `save()`, it should only save.

Use existing libraries/tools to simplify a task. Do not reinvent the wheel unless it's necessary.

For variable names avoid hungarian notation for example:
`isAuthorized` is easier to read than `m_isAuthorized`

## Write DRY(Don\'t Repeat Yourself Code)
If you\'ve copied code from one place to another, then the code you\'ve copied should be refactored to a common function to avoid duplication.

In this manner, if you have to update/change the code logic, it will only be in one and only place.

## Composition Over Inheritance
First lets define Inheritance. Inheritance is a technique in Object Oriented Programming to implement an **is-a** relationship. 

For example, when a `PayingCustomer` class inherits from `Customer` class, all properties of `Customer` class can be accessed by `PayingCustomerClass`. To further understand the **is-a** relationship, you can do this:

`Customer payingCustomer = new PayingCustomer();`
