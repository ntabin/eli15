# Circuit Breaker Pattern

Basically this pattern detect failure and prevents recurring failure. 

This pattern acts in the same principle as a circuit breaker. In a circuit breaker when a fault is detected it immediately opens the breaker same with this pattern.

In this pattern if one or more of our dependent services is down or unreachable, our system shouldn't try to complete the transaction hence the principle **_Fail Fast_** in software engineering.

This pattern has 3 states, Closed, Open and Half Open.

a) Closed: The program/system should allow the transaction. This is when the system is up and running fine. No problems.

b) Open: The program/system shall not the transaction. The sytem detects that 1 or more of its resources is unreachable so it prevents transaction to go hence there will be no recurring errors.

c) Half Open: For a limited time, a limited number of transactions will be allowed and if those transactions proceeded without error/s then it is assumed that the system is complete and it goes to **_Closed State_**.
If that is not the case wherein there are errors in the transactions, then it goes back to **_Open State_**
