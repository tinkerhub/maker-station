## Why learn Serverless ❓

The purpose of human scientific inquiry is the creation of processes to have a better understanding of everything around us and make the human life and life as a whole a bit easier.
Serverless might not be as big of an invention as the wheel but it does make the entire SDLC (Software Development Life Cycle) much more easier and hence makes it more relevant if you are working in the IT field.

Serverless is not the absence of servers. It is about offloading the responsibility of managing a server to the CSP (Cloud Service Provider) and we can concentrate completely on building the application with the exact business logic that is needed. Before serverless, when you had to deploy a web application, you had to set up a VM (Virtual Machine) instance in the cloud, configure it, scale it for the load, maintain it with security patches and updates, do user inventory, etc. which ends up with you having to handle all that operational overhead with less resources to focus on actually building the application.

Thus Serverless technology has a huge relevance since the object of all engineering is to provide the best outcome with the least utilisation of resources in a cost effective way.

The future of SDLC will inevitably be closely coupled with cloud solutions, and since Serverless is one of the biggest technological achievement on the consumption of compute capacity in the cloud, it will be the platform on which the present applications are running and the future applications will run.

Serverless is mostly connected to FaaS (Functions as a Service) but it is much more than that. Serverless functions are provided by AWS called Lambda and Azure called Functions but there are databases like DynamoDB, API solutions like API management and API Gateway, Serverless container running platforms like AWS Fargate, Azure container apps etc.

Serverless can be implemented in web apps, data processing, IoT, Analytics etc.

---
## 🎓 Take Away Skills

- Understanding about Serverless deployments
- Working with Serverless resources
- Cost considerations

---
## 🛠️ Prerequisites

 It can be divided into two categories **Programming Knowledge** and **Installation and Setup**

## 🧑🏻‍💻 Programming Knowledge 

Any popular programming language like
- Python
- Go
- JavaScript
- Java
etc.

Since Python is the most popular, we'll go with that, but I would recommend Go for production workloads since it compiles to machine code and is much faster.

## 📲 Installation and Setup

We'll consider that you are using Ubuntu 22.04 and base the procedure on that. Also We'll be using AWS serverless resources.

- [Python](https://www.python.org/downloads/) - Python is installed by default on Ubuntu 22.04 but you can check out the Python website to download it.
- [VSCode](https://code.visualstudio.com/) - We'll use VSCode as the IDE
- [AWS SAM](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html) - We'll use AWS SAM to deploy serverless resources easily
- [AWS Account](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html) - An AWS account is needed since we'll be using AWS for the cloud resources, but don't worry, the free tier will be more than enough for learning and it won't cost anything

---

## 💡 Learning Session

- Theory
    - [AWS Lambda:](https://aws.amazon.com/lambda/getting-started/)
        - [Introduction to Functions as a Service](https://www.ibm.com/in-en/topics/faas#:~:text=FaaS%20(Function%2Das%2Da%2DService)%20is%20a,building%20and%20launching%20microservices%20applications.)
        - [Working with IAM roles (permission)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)
        - [Basics of AWS SDK](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html)
    - [API Gateway:](https://aws.amazon.com/api-gateway/getting-started/)
        - [Introduction to REST API](https://aws.amazon.com/what-is/restful-api/#:~:text=RESTful%20API%20is%20an%20interface,applications%20to%20perform%20various%20tasks.)
        - [Basics of building APIs (resources, methods, formats etc.)](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html)
    - [DynamoDB:](https://aws.amazon.com/dynamodb/getting-started/?refid=1e5631f8-a3e1-45eb-8587-22803d0da70e)
        - [Introduction to Key Value DB](https://aws.amazon.com/nosql/key-value/#:~:text=A%20key%2Dvalue%20database%20is,objects%20to%20complex%20compound%20objects.)
        - [Working with DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)
    - [AWS SAM (Serverless Application Model)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html)

- Project:
    - Setting up a Lambda function to send you an email with a joke every 10 minutes:
        - Practical applications of AWS Lambda
        - Working with [external APIs](https://sv443.net/jokeapi/v2/)
        - Working with Amazon EventBridge
        - Working with Amazon SNS
    - Setting up an API to get some pre-existing data in DynamoDB:
        - Working with API Gateway
        - Working with DynamoDB

---
## 🔖 Resource Pool

- [AWS serverless repository](https://aws.amazon.com/serverless/serverlessrepo/)
- [AWS Training and certification](https://aws.amazon.com/training/)

### 📄 Articles/Blogs
- [AWS Serverless blogs](https://aws.amazon.com/blogs/serverless/)

### 📽️ Videos
- [This is my architecture](https://www.youtube.com/watch?v=hnMQFnTGr3I&list=PLhr1KZpdzukdeX8mQ2qO73bg6UKQHYsHb)

### 📚 Books (Optional)
- https://www.amazon.in/Distributed-Serverless-Architectures-AWS-Implement/dp/1484291581

### 🗞️ Newsletters (Optional)
- https://serverless.email/

### 🫂 Communities (Optional)
- AWS User groups ([Kochi](https://meetup.com/awsugkochi))

---
## 🚀 Project Pool

- https://github.com/claudiajs/claudia



