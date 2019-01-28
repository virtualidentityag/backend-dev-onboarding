# backend-dev-onboarding
This is an onboarding guide for new backend developers at Virtual Identity.
In case of having questions in any steps please do not hesitate to ask from your buddy.

Kindly follow the below steps : 
## 1. Setup Environment
Install and setup following tools in your Laptop/pc : 
    * OpenJDK
    * Maven
    * Git
    * Intellij
    
## 2. Bitbucket
The backend Onboarding project is located in [here](https://git.virtual-identity.com/projects/VI/repos/vi-backend-onboarding). 
For our onboarding project we are using  Gitflow-Workflow. You can read more about it [here](https://teamspace.virtual-identity.com/display/DEV/2.+GIT). 

Please do below steps : 
- Checkout the project
- Create a new branch with your name from development branch.
- Create a feature branch from your branch
- In swagger api defination file a test endpoint has been defined. Develop a controller for that endpoint and return a string "Hello VI" as response.
- clean/build and run the application locally and test your api.
- Send a pull request to your branch and assign your buddy as reviewer.

## 3. Coding guideline 
You can find our coding guidline in [here](https://teamspace.virtual-identity.com/display/DEV/1.+Java#id-1.Java-CodingGuidelines).
Make sure  Java Google Style is configured in your Intellij.
Update your code from previous task based on the guidline and if there is any change on your code, create a pull request.

## 4. Application/Testing
***Note*** : in first steps we use in-memory h2 database for saving data
Kindly implement below tasks. each tasks is a feature branch and after finishing a task send a pull request to your branch and assign your buddy as reviewer.

1. Define and implement a GET enpoint which returns a list of your favorite Color
2. Define a user entity. Add a service for CRUD actions and add endpoint for CRUD actions via using swagger
3. Write Unit Test and Integration Test for your application.
4. Adapt your endpoints to HAL standard which is base on HATEOAS concept.
5. Write Integration Test for your endpoints which check they follow HAL standard.
 
## 6. Security

## 7. Deployment

