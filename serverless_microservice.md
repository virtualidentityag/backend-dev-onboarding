# 01. Setup Environment
**Complexity Level 1**
## Resources
- [Backend Development Standards](https://teamspace.virtual-identity.com/display/DEV/Standards+for+Backend+Developoment)

## Challenge
#### Install required software and tools
Install and setup the following tools in your machine: 
- [Node JS](https://nodejs.org/en/) 
- [Docker](https://www.docker.com) 
- [Git](https://git-scm.com/)
- [VSCode](https://code.visualstudio.com)  or [Intellij](https://www.jetbrains.com/idea/)
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)
- [AWS SAM CLI](https://aws.amazon.com/serverless/sam/)

# 02. Setup static website hosted in AWS S3
**Complexity Level 2**

## Challenge
#### Create S3 bucket 
Create an S3 bucket in AWS via AWS console.

#### Upload an simple html to the bucket 
Upload an test html file in the created S3 bucket

#### Setup CLoudFront distribution
Create a CloudFront distribution and point it to the created S3 bucket

#### Test public access to the HTML
Test you can access publicly to the test HTML file via using CloudFront Domain.

## Questions
- What is Region in AWS?
- What is S3 bucket?
- What is bucket policy?
- What is Origin in CloudFront?

# 03. Create AWS Lambda function
**Complexity Level 2**

## Challenge
#### Create Hello World function
Create a simple AWS Lambda function via AWS console and update the code to return "hello world" string in response body (Write the application in Node JS). 

#### Test the function
Create a test event in AWS Lambda console and test the function is working as it is expected 

## Questions
- What is AWS Lambda?
- What is event in Lambda function?
- What is the entry point in AWS Lambda function/How we can set it? 
- What is Execution Role?
- How we can use environment variables?
- What is Maximum memory size we can assign to a Lambda function?
- What are the basic setting that Lambda function has?

# 04. Create an Endpoint in API Gateway and connect it to AWS Lambda function
**Complexity Level 2**

## Challenge
#### Setup API Gateway Endpoint and point to your test Lambda function
- Create an API Gateway endpoint to call the created Lambda function in previous section

#### Test the Endpoint
- In you browser or Postman call the API endpoint and check it returns Lambda function response. 

## Questions
- What are the steps to create GET method in API gateway.
- How we can get public endpoint in API Gateway?
- How we can make sure only we can call the endpoint in API Gateway?
- How we can retrive data in API request into API gateway?

# 05. Lambda function creates HTML file in S3 bucket via calling API Gateway endpoint
**Complexity Level 3**

## Challenge
#### Update Code in your function
Update your lambda function. Your Lambda function should craete an simple html file in your S3 bucket when it has been called via API Gateway. The name of HTML file should retrive from request parameter called 'filename'.
Also in your Lambda function log the filename coming from request. 

#### Test creating html via calling API Gateway Endpoint
Call the Endpoint with a filename and check S3 bucket that has the generated file.

#### Check the Log in Cloudwatch
Check the filename has been logged in Cloudwatch

## Questions
- What is AWS Cloudwatch
- What is IAM?
- How we can have access to other AWS services in our Lambda function?
- How we can limit Lambda function access to some specific AWS services?

# 06. Create SAM Project
**Complexity Level 3**

## Resources
- [AWS SAM](https://teamspace.virtual-identity.com/display/DEV/AWS+SAM)
- [Github Page](https://github.com/awslabs/serverless-application-model)

## Challenge
#### Create project via SAM Template
- Create a sample SAM Project via SAM command. The SAM template should have a test Lambda function and API Gateway endpoint as event

#### Test your project
- Run your SAM project locally and test it.

#### Deploy project to AWS via SAM CLI
- Deploy your project to AWS using SAM Commands.

#### Test Deoloyment
- Make sure your infrastructure has been deployed in AWS.

## Questions
- What is CloudFormation?
- What is CloudFormation stack?
- What are the steps to deploy your SAM project?

# 07. Setup CloudWatch event to trigger Lambda function 
**Complexity Level 2**

## Challenge
#### Add a Schedule trigger for test Lambda function in SAM template
add a CloudWatch event to trigger your function everynight at 11pm.

#### Deploy project to AWS via SAM CLI
Deploy the project to AWS in same CloudWatch Stack as previous.

#### Test CloudWatch event
Check in AWS console that your cloudwatch event has been created.

## Questions
- What is CloudWatch event?
- How a CloudWatch event structure looks like in Lambda function?
- What are the other events that can trigger a Lambda function

