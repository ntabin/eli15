# Competing Consumers Pattern

An appplication running in the cloud is expected to be bombarded by multiple request at the same time. We have to make sure that all request will be processed

This pattern explains how a consumer service can compete for requests on same  **_Message Queue_** to process this request simultaneously.

For example, we have a Consumer Service that can process a request at 3 minutes. An Http Request can go timeout. 
By implementing **_Competing Consumers Pattern_**, we can send the request to a **_Message Queue_** then the consumer service will process the request. 
But what will happen if lets say 100 requests? By utilizing this pattern we can scale it horizontally by adding more consumer services.
That way the Message Queue will be empty very quickly. And even if all consumer services are currently working, all request will be queued in Message Queue.
