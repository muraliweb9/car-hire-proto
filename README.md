# Car Records  Proto

## Overview

This is the project that has all the protobuf definitions shared across all the microservices. This project will be a dependency on all other microservices that need the gRPC stubs (methods) and data models.

Include as dependency.

```pom.xml
<!--========= gRPC Stubs ========-->
<dependency>
    <groupId>com.interview.test</groupId>
    <artifactId>car-hire-proto</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <exclusions>
        <exclusion>
            <groupId>*</groupId>
            <artifactId>*</artifactId>
        </exclusion>
    </exclusions>
</dependency>
```

## Spring Boot Admin
This project is a Spring Boot project and will be deployed. It offers no services but will expose the API and will be used to cross check the gRPC stub versions in a deployment.