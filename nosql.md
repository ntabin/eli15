# NoSQL (Non-SQL or Not Only SQL)
NoSQL is a type of database wherein it does not use a tabular relations like Relational Databases.

## When to Embed
Embedding is having a sub document in a document. For example:
<pre>
{
  book: {
    name: 'Introduction to Physics',
    author: 'SomeAuthor'
  }
}
</pre>

Embed data when you have a one is to one relationship.

Embed data for easy read access. This is due to only one docment is read.

Embed data if you need to the current details used.
For example you have an order document like this:

<pre>
`{
   "orders": [
      {
         "name": "soap",
         "quantity": 100
      },
      {
         "name": "liquid",
         "quantity": 30
      }
   ],
   "deliveryAddress": "123 AAA St. Philippines",
   "orderedBy": "d6527314-590f-4a33-a51b-fc1663b3e215",
}`
</pre>

Assuming that `orderedBy` property is referenced from `customers` collection and also assume that the customer has its own address.
Of course we will not use the current address of customer in its `deliveryAddress`.

## When to Reference
Reference is when you only assigned the `Id` of the document to a property on that document.
Reference when you have many to many relationship.
Reference when you need consistency. Going back to the above example, if we don't reference the customer on the `orderedBy` property, we will end up like this: 

<pre>
`{
   "orders": [
      {
         "name": "soap",
         "quantity": 100
      },
      {
         "name": "liquid",
         "quantity": 30
      }
   ],
   "deliveryAddress": "123 AAA St. Philippines",
   "orderedBy": {
      "name": "Juana Change",
      "address": "123 Philippine St."
   },
}`
</pre>

Imagine if the customer updated his/her profile specifically the address part. In the program, you have to update all occurences which references to his/her details.

