# Spring-Boot Camel XML REST + Swagger QuickStart

This example demonstrates how to configure Camel routes in Spring Boot via
a Spring XML configuration file that both expose a REST API and provide a
dynamic Swagger definition.

The application utilizes the Spring [`@ImportResource`](http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/ImportResource.html) annotation to load a Camel Context definition via a [camel-context.xml](src/main/resources/spring/camel-context.xml) file on the classpath.

### Building

The example can be built with

    mvn clean install

### Running the Quickstart standalone on your machine

You can also run this booster as a standalone project directly:

Obtain the project and enter the project's directory
Build the project:

    mvn clean package
    mvn spring-boot:run 

### Testing Available APIs

To access the Swagger doc, use the following URL: [`http://localhost:8080/camel/api-docs`](http://localhost:8080/camel/api-docs)

To access the "Hello" REST GET operation, use the following URL: [`http://localhost:8080/camel/hello/{NAME}`](http://localhost:8080/camel/hello/NAME)

You can also use the 'curl' command: `curl -X GET http://localhost:8080/camel/hello/{NAME}`

Replace `{NAME}` with the name you want output. For example: `http://localhost:8080/camel/hello/BOB` should output "Hello BOB!"
