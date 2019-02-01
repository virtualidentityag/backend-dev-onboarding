# 1. Setup Environment
## Resources
- [Backend Development Standards](https://teamspace.virtual-identity.com/display/DEV/Standards+for+Backend+Developoment)

## Challenge
#### Install required software and tools
Install and setup the following tools in your machine: 
- [OpenJDK](https://openjdk.java.net/) 
- [Maven](https://maven.apache.org/) 
- [Git](https://git-scm.com/)
- [Intellij](https://www.jetbrains.com/idea/) 
    
# 2. Setup your first project
## Resources
- [Boilerplate Application](https://teamspace.virtual-identity.com/display/DEV/1.+Boilerplate+Application)

## Challenge
#### Checkout the backend onboarding example project
The project is located in [Bitbucket](https://git.virtual-identity.com/projects/VI/repos/vi-backend-onboarding)
Please import the project as a Maven project in your IDE.

#### Build and run the application
Build the application within your IDE. When compilation succeeded, run the project within your IDE.
To check if the application has started successfully, call the already existing root endpoint in your browser and see the response. 

## Questions
- What is Maven?
- What is the benefit of using Maven?
- How can you add dependencies to your java project with Maven?
- How can you build your project with Maven? 

# 3. Make your first pull request
## Resources
- [Git Usage](https://teamspace.virtual-identity.com/display/DEV/2.+GIT)

## Challenge
#### Create a new branch with your name from development branch.
You can do that in the Web UI of Bitbucket.
This branch will be your personal development branch for the onboarding project.

#### Create a feature branch from your personal development branch
Switch to that feature branch in your IDE. 
According to the Gitflow-Workflow, in a feature branch you have an isolated environment to implement new cool stuff and send pull requests to a reviewer when you have finished your work.

#### Implement a Spring MVC Controller
In swagger api defination file a test endpoint has been defined. Develop a controller for that endpoint and return a string "Hello VI" as response.
Rebuild your application and rerun it locally to check the newly implemented api response.

#### Create a pull request 
Commit and push your changes to them remote feature branch.
Create a pull request from your feature branch to your personal development branch in the Web UI of Bitbucket. Assign this pull request to your buddy as a reviewer.

## Questions
- What's Git?
- What is a repository?
- What is a branch?
- What is a commit?
- What does push mean?
- What does fetch mean?
- What is a pull request?

# 4. Adhere to the Coding Guidelines
## Resources
- [Java Coding Guidelines](https://teamspace.virtual-identity.com/display/DEV/1.+Java#id-1.Java-CodingGuidelines)

## Challenge
#### Configure Code Formatter
Download the Java Google Style Code Formatter from [here]( https://github.com/google/styleguide/blob/gh-pages/intellij-java-google-style.xml) and make sure it is configured in your IDE.  

#### Reformat your code
Check and reformat your code from previous task based on the configured code formatter.
If there is any change on your code, comiit an push it again and create a new pull request.

## Questions
- What are (in your opinion) the most important rules for writing clean code?
- How can the compliance with these rules can be enforced?

# 5. Application/Testing
## Resources

## Challenge

## Questions

***Note*** : in first steps we use in-memory h2 database for saving data
Kindly implement below tasks. each tasks is a feature branch and after finishing a task send a pull request to your branch and assign your buddy as reviewer.

1. Define and implement a GET enpoint which returns a list of your favorite Color
2. Define a user entity. Add a service for CRUD actions and add endpoint for CRUD actions via using swagger
3. Write Unit Test and Integration Test for your application.
4. Adapt your endpoints to HAL standard which is base on HATEOAS concept.
5. Write Integration Test for your endpoints which check they follow HAL standard.
 
# 6. Security
## Resources

## Challenge

## Questions

# 7. Deployment
## Resources

## Challenge

## Questions

