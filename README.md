## Micro-backend-app
Backend system for an imaginary photo-backup app. 

It uses the Spring framework to illustrate an example of a backend system, built with the microservice-approach mindset.


This repository contains only the Docker files used to build / deploy the system.
See the links bellow for each microservice source code.

### How to use it:
* Clone this repository and run `docker-compose up`. 
* You **might need to restart some of the services**,, once the docker compose finishes fetching the images and creating the containers.
* This is **because some services might become available before SpringCloud Configuration Service becomes available**.
* Once all the services have started successfully, use Postman or something similar to create an account.
* Once you created an account, you need to sign in. After authorization, an JWT Token will be created, which will be valid for one day.
* You will have to (manually) include the JWT token in the headers of all your subsequent requests, except the ones targeting the "Create Account" and "Login" endpoints. 
* The users-service is backed up by a MySql database.
* The file-uploader service stores the files in a H2 database.

### Acknowledgement

* This is a bit messy and none of the services contains any tests.
* My focus has been on ilustrating the communication between multiple services and how they come together, when building scalable systems.



![Backend-Diagram drawio](https://user-images.githubusercontent.com/22425017/137919729-cbbfa8ed-cbc5-462c-b0cd-1fcc49e95346.png)



 
### Source code

* [Configuration Server Repository](https://github.com/PetreVane/photo-backend-configServer)
* [Spring Cloud Config-Server](https://github.com/PetreVane/SpringCloud-ConfigService) 
* [Spring Cloud Gateway Service](https://github.com/PetreVane/Backend-gatewayService)
* [Eureka Discovery Service](https://github.com/PetreVane/Backend-DiscoveryService)
* [Users Service](https://github.com/PetreVane/Backend-usersService)
* [File Uploading Service](https://github.com/PetreVane/backend-file-uploader-api)
* [Elastic Stack](https://github.com/PetreVane/docker-elk)

### Login Credentials (username & password)
* RabbitMQ: guest & guest
* Kibana: elastic & changeme
* Eureka dashboard: eureka & dashboard
* MySql: root & root


