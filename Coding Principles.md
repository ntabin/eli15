# Coding Principles

## KISS (Keep it Simple Stupid)

Also known as Keep it super simple or Keep it simply simple.

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
First lets define **Inheritance**. Inheritance is a technique in Object Oriented Programming to implement an **is-a** relationship. 
For example, when a `PayingCustomer` class inherits from `Customer` class, all properties of `Customer` class can be accessed by `PayingCustomer` class. To further understand the **is-a** relationship, you can do this:

`Customer payingCustomer = new PayingCustomer();`

Second lets define **Composition**. Composition is a technique in Object Oriented Programming to implement an **has-a** relationship between objects.

For example we have 3 classes defined as
<pre><code>
public class Customer {
  public string FullName { get; set; }
}

public class PaymentDetail {
  public string CardToken { get; set; }
}
  
public PayingCustomer : Customer {
  public double TotalAmount { get; set; }
  public PaymentDetail PaymentDetail { get; set; }
}
</pre></code>

Notice that the `PayingCustomer` class **has-a** property called `PaymentDetail`. So this is composition, you compose a class its needed properties or behaviors as oppose to inheritance wherein you get all properties or behaviors.

So why prefer Composition over Inheritance:

1. Creating deep inheritances lead to brittle code, and hard to maintain. You have little problem with this with composition as it is very flexible.

2. In inheritance, there may be instances that the inherited class contains some properties that the child class doesn't need.

So when or what should be the case basis whether to use inheritance or composition:

1. Use **Inheritance** when you need an **is-a** relationship. For example a `PayingCustomer` is-a `Customer`, a `WorkingPerson` is-a `Person`.
2. Use Composition when you need a has-a relationship. For example a `PayingCustomer` has-a `PaymentDetail`, a `WorkingPerson` has-a `Job`.

## YAGNI (You Aren't Gonna Need It)
In a nutshell in terms of software developemt, do not add code/codes that you will not gonna use or need.

This means that whatever is the requirement, stick with it. Do not add some fancy features or stuffs that the user will not gonna use or need.

Do not build a feature now that you will need in the future. Lets say you are working on an application which proceses document and saves it in a file directory. For sure, some time in the future you have to build a feature wherein a user must be able to create or rename a directory. But the important question is does the user need it now? Can the user do the whole system process flow without it? If yes then **You Aren't Gonna Neet It**.

Of course a developer may say _I am in this part and it will be wise to do this as I might need it in the future_. I would say hold on for a while. While it may look cheaper and practical to do it now, you will never know if and when there maybe a change in requirements. And with that, most of the effort will just be wasted.
