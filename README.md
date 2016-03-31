# docker-api-gateway-example

This project is a simple example of API Gateway pattern for [microservices](http://microservices.io/patterns/apigateway.html) implemented in Node.js.

It's **not production-ready** service and its sole purpose is to demonstrate usage of **node-docker-monitor** and **http-proxy** npm modules.

Service reacts on Docker events and as Docker containers go up and down it creates or removes HTTP routing rules for them. 
To indicate that container to be handled by the gateway it must have label **api_route** defining URL prefix for that container 
plus it must EXPOSE port that containerised service listens on. 

![Routing HTTP requests with API Gateway](docker-api-gateway.png)