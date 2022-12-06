# AWS Lambda Function URL

* Create Lambda function URL and change the auth to AWS_IAM.  
* Create the new user app_user as below and grant lambda:InvokeFunctionUrl.  
* From the client (postman – for testing),   
    Use the AccessKey and SecretKey of the AWS app_user.   
    Set the advanced options - Region & ServiceName. eg. Region=us-east-1 & ServiceName=lambda.  Use "execute-api" for API gateway.  
    

## Python code to invoke Lambda URL from client

* Use boto auth, awsrequest and credentials
* Sig4 authentication with app_user credentials
* There is payload format to be used for Lambda URL (which is taken care by boto3)
* Refer Sample code xURLauth.ipynb  

Ref:
https://stackoverflow.com/questions/63154781/generate-the-aws-http-signature-from-boto3  
https://github.com/boto/botocore/issues/1784  
https://gist.github.com/rhboyd/1e01190a6b27ca4ba817bf272d5a5f9a  
