# SpringBootProject
Contains a simple project for many uses. Eureka Discovery Channel -> Spring boot gateway -> Spring microservice -> mysqldb

## Eureka Discovery Channel
Spring Boot Project by https://start.spring.io/
  application.properties:
    We must define the server.port, spring.application.name, eureka.client.service-url.defaultZone and do not registerWithEureka.
  Main class:
    Must add the anotation @SpringBootApplication to make this a pring boot application.
  Dependencies:
    <dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
		</dependency>
  Optional:
    Create a controller with @RestController anotation and the @RequestMapping route.
    Create a method with @GetMapping to check the status of the microservice.
    
## Spring Boot Gateway
  application.properties:
    We must define the server.port, spring.application.name, eureka.client.serviceUrl.defaultZone and spring.cloud.gateway.discovery.locator.enabled to register the microservice with eureka discovery server
  Main class:
    Must add the anotation @SpringBootApplication to make this a pring boot application and @EnableEurekaServer to enable this app as an eureka discovery server.
  Dependencies:
    <dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-gateway</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
		</dependency>
  Optional:
    Create a controller with @RestController anotation and the @RequestMapping route.
    Create a method with @GetMapping to check the status of the microservice.
    
## Microservices

This part will contain the definition of the other microservices.


    
    
    
    
    
    
    
    
