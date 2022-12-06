# AWSLambda Function URL

* Create Lambda function URL and change the auth to AWS_IAM.  
* Create the new user app_user as below and grant lambda:InvokeFunctionUrl.  
* From the client (postman – for testing),   
    Use the AccessKey and SecretKey of the AWS app_user.   
    Set the advanced options - Region & ServiceName. eg. Region=us-east-1 & ServiceName=lambda.  Use "execute-api" for API gateway.  
