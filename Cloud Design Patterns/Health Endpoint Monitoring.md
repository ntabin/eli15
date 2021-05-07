# Health Endpoint Monitoring Pattern 

Monitoring of cloud resource. Basically we should not allow customers to report that our app is not available or there is something wrong. Instead we developers should be the first to know when a problem exists in the first place.

Example for a web app, we create an endpoint to check all cloud resources or maybe you want an endpoint specific for microservices or databases. It isn't limited to just microservices and databases.

The problems with this pattern is on how much detailed we should go. Or maybe an attacker on our website can take advantage of this. So the solution to this problem is you can add an _**API key**_ in the request headers and validated it.
