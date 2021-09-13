# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.5.4/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.5.4/maven-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.5.4/reference/htmlsingle/#boot-features-developing-web-applications)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/2.5.4/reference/htmlsingle/#using-boot-devtools)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.5.4/reference/htmlsingle/#boot-features-jpa-and-spring-data)
* [OAuth2 Resource Server](https://docs.spring.io/spring-boot/docs/2.5.4/reference/htmlsingle/#boot-features-security-oauth2-server)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

####  Client part

1) Download and Install the node.js from https://nodejs.org/en/download/ as per your operating system and check if the installation is successful using the command ‘node -v’ which will print the current installed version.
2) Run the command ‘npm install -g @angular/cli’ to install Angular CLI.
3) (Optional) Download the visual code using the link https://code.visualstudio.com/ and import the angular project provided.
4) unpack ./static/client-app-ui.zip into some folder
5) Navigate to the folder, inside the project where package.json is present and run the command ‘npm install’ by opening a terminal. This will install all the dependencies inside the new folder created with the name ‘node_modules’
6) Run the command ‘ng serve’ and it will start the application at ‘http://localhost:4200/’ by default.

#### Client UI important files
1) src/environments.ts
    rooturl : 'http://localhost:8080' -- has to point onto web site (API)
2) src/app/app.module.ts

      config: {
        url: 'http://localhost:8082/auth'  --- has point onto keycloak

     pkceMethod: 'S256',
     redirectUri: 'http://localhost:4200/dashboard'  -- web app entry point


### Keycloak entities

    Client id: eazypublicclient
    access type: public
    valid Redirect URI: http://localhost:4200/dashboard
    web Origins: *

 
    User: accounts
    email: accounts@eazybytes.com
    password: 12345
    With roles: "USER", "ADMIN"