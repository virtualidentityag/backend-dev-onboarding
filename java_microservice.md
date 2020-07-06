# 01. Setup Environment
**Complexity Level 0**
## Resources
- [Backend Development Standards](https://collaboration.virtual-identity.com/display/DEV/Standards+for+Backend+Development)

## Challenge
#### Install required software and tools
Install and setup the following tools in your machine:
- [OpenJDK V13](https://openjdk.java.net/)
- [Git](https://git-scm.com/)
- [Intellij](https://www.jetbrains.com/idea/)

# 02. Setup your first project
**Complexity Level 1**
## Resources
- [Boilerplate Application](https://collaboration.virtual-identity.com/display/DEV/1.+Boilerplate+Application)

#### GitHub
If you do not have an account at GitHub already, you will need one so, go to: [https://github.com/join](https://github.com/join) and create one.
Please note that GitHub is a professional social network and choose an appropriate username.
And since you will soon be added to the <i>virtualidenityag</i> organization on GitHub, it's required that you enable two-factor authentication as a extra layer of protection. To do it, got to *settings > security*. There are three methods you can choose from (Authenticator app, Security keys and SMS). Just pick the one you're more comfortable with.

#### SSH
It's also relevant that you know about the SSH protocol. It allows you to connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without using your username and password everytime. You can get all the information about how to create and setup your SSH keys at the [GitHub support page](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).

#### Git clients
Some people prefer to use graphical tools to use git, so if you do not have installed a git client already, find and install a [git client for your local operating system](https://git-scm.com/downloads/guis).
There are a lot of options so feel free to use the one that you enjoy more!

## Challenge
#### Create a example project
Create a own github repository and use the [Boilerplate Template Repository](https://github.com/virtualidentityag/spring-boot-boilerplate) as template.
Please import the project as a Gradle project in your IDE.

#### Build and run the application
Build the application within your IDE. When compilation succeeded, run the project within your IDE.
To check if the application has started successfully, call an already existing endpoint in your browser and see the response.

## Questions
- What is Gradle?
- What is the benefit of using Gradle?
- How can you add dependencies to your java project with Gradle?
- How can you build your project with Gradle?
- Which are the key technologies/libraries used in the boilerplate application?

# 03. Make your first pull request
**Complexity Level 1**
## Resources
- [Git Usage](https://collaboration.virtual-identity.com/display/DEV/2.+GIT)
- [Spring Boot Getting Started Guide](https://spring.io/guides/gs/spring-boot)

## Challenge
#### Create a feature branch from master branch
Switch to that feature branch in your IDE.
According to the Gitflow-Workflow, in a feature branch you have an isolated environment to implement new cool stuff and send pull requests to a reviewer when you have finished your work.

#### Implement a Spring MVC Controller
In swagger api definition file, add a test endpoint. Develop a controller for that endpoint and return a string "Hello VI" as response.
Rebuild your application and rerun it locally to check the newly implemented api response.

#### Create a pull request
Commit and push your changes to them remote feature branch.
Create a pull request from your feature branch to master branch. Assign this pull request to your mentor as a reviewer.

From now on, merging to the master branch should always be done by merging a pull request that is approved by another reviewer.

## Questions
- What's Git?
- What is a repository?
- What is a branch?
- What is a commit?
- What does push mean?
- What does fetch mean?
- What is a pull request?
- What is GitHub?

- What is Spring?
- What ist Spring Boot?

# 04. Adhere to the Coding Guidelines
**Complexity Level 1**
## Resources
- [Java Coding Guidelines](https://collaboration.virtual-identity.com/display/DEV/1.+Java#id-1.Java-CodingGuidelines)

## Challenge
#### Configure Code Formatter
Download the Java Google Style Code Formatter from [here]( https://github.com/google/styleguide/blob/gh-pages/intellij-java-google-style.xml) and make sure it is configured in your IDE.

#### Reformat your code
Check and reformat your code from previous task based on the configured code formatter.
If there is any change on your code, comiit an push it again and create a new pull request.

## Questions
- What are (in your opinion) the most important rules for writing clean code?
- How the compliance with these rules can be enforced?

# 05. Add automated tests
**Complexity Level 2**
## Resources
- [VI Test Guide](https://collaboration.virtual-identity.com/display/DEV/2.+Tests)
- [Spring Boot Web Test Guide](https://spring.io/guides/gs/testing-web/)
- [Spring Web Tests Reference](https://docs.spring.io/spring/docs/current/spring-framework-reference/testing.html#spring-mvc-test-framework)

## Challenge
#### Write an integration test for your controller
The integration test should check that the api implementation (your controller) returns "Hello VI" as response body and  status code 200.
Run your integration test inside your IDE to see that the test is green.

From now on finish all your challenges by creating a pull request.

## Questions
- What is a unit test?
- What is an integration test?
- Which popular java test frameworks for automated tests exist?
- Why are automated tests important?

# 06. Implement a persisted data model
**Complexity Level 3**
## Resources
- [Spring Data Overview](https://spring.io/projects/spring-data)
- [Spring Data JPA Guide](https://spring.io/guides/gs/accessing-data-jpa/)

## Challenge
Let's start creating an application with some "real" logic.
In the onboarding project we will develop the backend for an (very simple) blog software.

With this blog software, it should be possible to manage authors (with a first- and lastname) and blog entries  with a title, a text and a reference to an author.
An author can write multiple entries and an entry could be written by only one author.
When an author is deleted, all entries should be deleted too.

#### Define your data model with entities
Define entities for author and blog entry. You should use JPA annotations.

#### Implement CRUD Services for the entities
For ervery entity implement a service class, which provides create, read, update and delete methods for this entity.
Both entities should be persisted in an in-memory database.

#### Add tests
Implement integration tests for your service classes, that check if your business logic works as expected and all data is persisted correctly in the database.

From now on, write tests for all your challenges.

## Questions
- What is JPA?
- What is Hibernate?
- What is Spring Data?

# 07. REST APIs
**Complexity Level 3**
## Resources
- [HATEOAS](https://martinfowler.com/articles/richardsonMaturityModel.html)
- [HATEOAS a simple explanation](https://www.e4developer.com/2018/02/16/hateoas-simple-explanation/)
- [HAL Specification](http://stateless.co/hal_specification.html)
- [Swagger/OpenAPI](https://swagger.io/docs/specification/about/)
- [Spring MVC Exception Handling](https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc)

## Challenge
So far, we created business and persistence logic for our tiny blogging software. Let's continue by making these services available by a REST API.

#### Specify new endpoints for your services

Please specify new HAL endpoints for all existing CRUD methods of your services in the api.yaml file. Consider meaningful HTTP methods, request models, response codes and response models. Models should be defined in JSON.

Finally rebuild your project with Gradle and check the generated java sources  for your endpoint definitions and response models.

#### Add controller implementations

Implement controller methods for generated controller stubs of your defined endpoints.

Naturally, write integration tests which check the correct behaviour and response structure of your controllers.

#### Add Error Handling

Grant that exceptions and errors in your services and controllers are fetched and handled  in your controllers. to achieve that, extend the API specification for HTTP error codes and add exception handling to the Spring application.

## Questions
- What is REST?
- What is HATOAS?
- What is HAL?
- What is Swagger and OpenAPI?

# 08. Search
**Complexity Level 3**
## Resources
- [Solr](http://lucene.apache.org/solr/)
- [Spring Data Solr](https://spring.io/projects/spring-data-solr)
- [ElasticSearch](https://www.elastic.co/products/elasticsearch)
- [Spring Data ElasticSearch](https://spring.io/projects/spring-data-elasticsearch)
- [Hibernate Search](http://hibernate.org/search/)

## Challenge
Implement a search that makes it possible to search for blog entries within its title, body as well as author first- and lastname. The search should consist of a service and an endpoint with pagination.
Possible Solutions can be based on an embedded Solr or ElasticSearch Server as well as Hibernate Search.

## Questions
- What is the most popular search library in Java?
- What popular java search frameworks and search servers exist?
- What is the difference between searching and filtering?
- What are facets?

# 09. GraphQL Interfaces
**Complexity Level 3**
## Resources
- [GraphQL official website](https://graphql.org/)
- [Spring Boot GraphQL Tutorial](https://www.baeldung.com/spring-graphql)

## Challenge
Let's create another API for our tiny blog application. Why? Actually we want to be flexible with approaches to build APIs for different client types.

#### Specify graphQL schema

Please specify schema to fetch and change author and blog entry data.

#### Add resolver implementations

Implement both query and mutation resolvers of your defined schema.

## Questions
- What is GraphQL?
- In which cases would yo prefer GraphQL over REST?
- Do you observe any problem with error handling regarding different clients? What approach would you choose to resolve it?

# 10. Containers
**Complexity Level 3**
## Resources
- Thousands of websites related to Docker ;-)
- [Spring Boot with Docker](https://spring.io/guides/gs/spring-boot-docker/)

## Challenge
Containerize your application into a Docker image.
Run your application locally with Docker and call your endpoints to test it.

## Questions
- What is containerization and what is Docker?
- What is a Docker image and what is a docker container?
- How are Docker images structured?
- What is the advantage of containerization in relation to deployments?
- In which contexts and on which platforms you can use Docker images?
