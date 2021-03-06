1. Introduction to AWS Identity and Access Management (IAM)
2. Introduction to Amazon Simple Storage Service (S3)
3. Using Open Data with Amazon S3
4. Introduction to AWS Lambda


# AWS Identity and Access Management 

* Manage users
* Manage security credentials : access keys
* Permissions to control which AWS resourcess users can access

## AWS Identity and Access Management 

* Manage IAM Users and their access 
Create users and assign them individual security credentials ( access keys, passwords and multi factor authentication devices)

* Manage IAM Roles and their permissions 
Similar to User. An AWS Identity with permission policies that determine what identity can and cannot do in AWS

* Manage federated users and their permissions
Enable identity federation to allow existing users in your enterprise to access the AWS Management Console, to call AWS APIs and to access resources, without the need to create an IAM user for each identity 


# Amazon S3

* Object storage service 
* Create Bucket
* Upload to bucket

* Bucket -> Permission -> Block Public Access -> Deselect 
* File -> Permission -> Public Access

## Control access to entire bucket 

* Bucket -> Permission -> Bucket Policy
  1. AWS Policy generator -> copy arn



# AWS Lambda 

* compute service runs code in response to events and manages compute resources






























# AWS Gateway
API Gateway is a managed service provided by AWS that makes creating, deploying and maintaining APIs easy. API Gateway includes features to:

* Transform the body and headers of incoming API requests to match backend systems
* Transform the body and headers of the outgoing API responses to match API requirements
* Control API access via AWS Identity and Access Management
* Create and apply API keys for third-party development
* Enable Amazon CloudWatch integration for API monitoring
* Cache API responses via Amazon CloudFront for faster response times
* Deploy an API to multiple stages, allowing easy differentiation between development, test, production as well as versioning
* Connect custom domains to an API
* Define models to help standardize your API request and response transformations










## Couple Amazon API Gateway and AWS Lambda
A microservice using Amazon API Gateway consists of a defined resource and associated methods (GET,POST,PUT,etc) in API Gateway
as well as the backend target.

### Using an Amazon API Gateway endpoints that invokes an AWS Lambda function.

Backend target will be lambda function or another HTTP endpoint ( 3rd party API or listerning web server), an AWS service proxy
or a mock integration to be used as a placeholder.

### Amazon API Gateway and AWS Lambda Terminology

* **Resource**: Represented as a URL endpoint and path. For example, . You can associate HTTP methods with resources and define different backend targets for each method. In a microservices architecture, a resource would represent a single microservice within your system.

* **Method**: In API Gateway, a method is identified by the combination of a resource path and an HTTP verb, such as GET, POST, and DELETE.

* **Method Request:**  The method request settings in API Gateway store the methods authorization settings and define the URL Query String parameters and HTTP Request Headers that are received from the client.

* **Integration Request:** The integration request settings define the backend target used with the method. It is also where you can define mapping templates, to transform the incoming request to match what the backend target is expecting.

* **Integration Response:**  The integration response settings is where the mappings are defined between the response from the backend target and the method response in API Gateway. You can also transform the data that is returned from your backend target to fit what your end users and applications are expecting.

* **Method Response:** The method response settings define the method response types, their headers and content types.

* **Model:** In API Gateway, a model defines the format, also known as the schema or shape, of some data. You create and use models to make it easier to create mapping templates. Because API Gateway is designed to work primarily with JavaScript Object Notation (JSON)-formatted data, API Gateway uses JSON Schema to define the expected schema of the data.

* **Stage:** In API Gateway, a stage defines the path through which an API deployment is accessible. This is commonly used to deviate between versions, as well as development vs production endpoints, etc.

* **Blueprint:** A Lambda blueprint is an example lambda function that can be used as a base to build out new Lambda functions.


