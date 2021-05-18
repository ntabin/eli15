# Service Integration Patterns

## Message Bus

Message bus is there to provice common communication platforms to different services or applications which then can be used to send and receive messages.
In the cloud this Message Bus can provide to different deployed services. 

Pros:
* Same protocols for all communications
* can be prioritize

cons:
* The message bus can get crowded with messages since all services or applications uses this
* There can be security issues if someone connects in the message bus. We should provide an end to end encryption
* The **_Same protocols for all communications_** can be a drawback since all services or applications are force to use this protocols even if it is inefficient

## Message Routing 

Message Routing Pattern determines the recipient/receiver of a message based on certain conditions.

* Content-Based Router - Determines the recipient/receiver of message base on content.

* Routing Slip - Describes a situation wherein a message will be routed to different components.

* Scatter-Gather - Broadcast a message to multiple receivers. Then it uses aggregator to collect the responses fusing them into 1.

* Recipient List - Addresses the solution in the scenario wherein a message is routed to one or more recipients. Recipients can bot be statically or dynamically.

* Splitter - Addresses the solution when a message must be splitted to multiple recipients
