# Deploying a Hello World application

(https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html)

  

This app implements an API backend. When we send a get request, lambda function will be triggered and return a simple `hello world` message.

  

## Steps

  

1. `sam init`

2. `cd sam-app-name`

3. `sam build`

4. `sam deploy --guided`

  
### 1- Downloading SAM

- Follow these prompts for <font color='blue'>  `sam init`:

	- `AWS Quick Start Templates`
	- `Zip` 
	- `Hello World Example`
###  2- Building my app
- Change directory to your app folder `cd my-app` where `template.yaml`resides.
- Now it's time to build our application.
- Run <font color='blue'>  `sam-build`. 

With this command, SAM builds any dependencies our application have and copies source code to be uploaded to Lambda.

### 3- Deploying my app to AWS
- Run <font color='blue'> `sam deploy --guided`
- `Enter` to accept default options.
- Answer `Y` to the following prompt `HelloWorldFunction may not have authorization defined, Is this okay? [y/N]`
Now all my packages are uploaded to an **S3** bucket and my app is deployed with AWS CloudFormation. 
-After a succesfull deployment, what I see is:
`{"message": "hello world"}`

## RECAP
- I downloaded, builded and deployed a serverless Hello World app using SAM. 
- Sam implemented a basic API backend using Amazon API Gateway and AWS Lambda function. 