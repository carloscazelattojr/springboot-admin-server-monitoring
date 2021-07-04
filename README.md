# Spring Boot Admin Server - App Monitoring Project

Application Monitoring Project with Spring Boot Admin Server


## Project Dependency

- Spring Web


# Authors

codecentric's Spring Boot Admin


<h1 align="center">
    <img alt="codecentric" title="codecentric" src="https://github.com/codecentric/spring-boot-admin/blob/master/images/logo-spring-boot-admin.png"  /><br>
</h1>


https://github.com/codecentric/spring-boot-admin

## Docs

https://codecentric.github.io/spring-boot-admin/2.3.1/


Add Spring Boot Admin Server starter to your dependencies:

File: pom.xml

```
<dependency>
    <groupId>de.codecentric</groupId>
    <artifactId>spring-boot-admin-starter-server</artifactId>
    <version>2.?</version>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>

```

Pull in the Spring Boot Admin Server configuration via adding @EnableAdminServer to your configuration:

```
@Configuration
@EnableAutoConfiguration
@EnableAdminServer
public class SpringBootAdminApplication {
    public static void main(String[] args) {
        SpringApplication.run(SpringBootAdminApplication.class, args);
    }
}

```


Register Client

In the project you want to monitor, add the dependency in pom.xml.

```
<dependency>
    <groupId>de.codecentric</groupId>
    <artifactId>spring-boot-admin-starter-client</artifactId>
    <version>2.3.1</version>
</dependency>
```

Enable the SBA Client by configuring the URL of the Spring Boot Admin Server:

In the project that will be monitored, add in the file: application.properties 

```
spring.boot.admin.client.url=http://localhost:8080  
management.endpoints.web.exposure.include=*  
```



## Tecnologies

`Java` `Spring Boot` `Spring Boot Admin` 
 
 
 
 
 Credits: codecentric's