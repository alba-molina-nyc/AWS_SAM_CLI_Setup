# AWS SAM CLI

## Instructions/ Setup

### Download AWS CLI

[download AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

![install_AWS_CLI](imgs/01_install_AWS_CLI.png)

### Setting up AWS Configurations

![install_AWS_CLI](/imgs/02_configuring_AWS.png)

### Install Docker

[download Docker](https://docs.docker.com/desktop/install/mac-install/)

![download Docker](/imgs/03_setup_docker.png)

### Install AWS SAM CLI

AWS Serverless Application Model (different from serverless framework - it is a diff paradigm but the same idea)

[Install AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-mac.html)

![Install SAM](imgs/04_install_SAM_CLI.png)

---

## What is AWS

1. What is SAM
2. Benefits of SAM
3. Create First SAM Project
4. Run Locally and Test it
5. Deploy to AWS Cloud

SAM used to define serverless app, uses the same concept as yamp but differences in how the structure of the application is put together. But essentially it is just a `different` way of creating a serverless application

AWS Components:

- `AWS SAM Template Specifications` - where you write properties to a file (just like serverless.yml all the metadata needed for the lambda functions to work) to describe functions, APIs, permissions, timeouts etc.
- `AWS SAM CLI` - invoke packages, deploy, view, run the applications locally, and test them
  
Benefits:

- `single deployment configuration` - AKA deply the whole stack as a single entity. It all comes packaged together when pushed to the cloud or run locally
- `Extention of AWS CloudFormation` - connection with how it is all packaged up, using what AWS cloud already has, not re-inventing the wheel
- Built in best practices as code reviews
- `Local debugging and testing via (docker)` before push to AWS cloud
- `Deep integration` with development tools

---

## Building a Basic SAM Hello World App

- use AWS CLI and SAM CLI to create a serverless project
- Run, test it locally
- Deploy to AWS Cloud
- Create same app using AWS Toolkit
- Run it, test it locally
- Deploy it to AWS Cloud and test it there too

### What the App will do:

creating a simple API using `API Gateway` for the endpoint and `AWS Lambda Function`

- so when send `GET` request to `API Gateway endpoint`, the `Lambda function` is invoked, and then the lambda function will `return` a message
  