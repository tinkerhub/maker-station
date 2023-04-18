## Why learn Lambda ❓

If you checked the GettingStarted section of serverless, you will have read about AWS Lambda.

AWS Lambda is a FaaS (Function as a Service) provided by AWS. The basic idea is that we only have to care about building our application. Running it, maintinaing the underlying infrastructure, scaling it etc. will be handled by AWS.

Lambda allows us to literally pay only when the code is executed. Which means the cost is directly proportional to the popularity of the deployed application. Lambda can work as an API with the help of API Gateway, it can work as a cron job with the help of Event Bridge rules or it can even process data asynchronously with SQS.

This makes Lambda a good solution especially for event driven applications.

---
## 🎓 Take Away Skills

- Working with AWS Lambda
- Understanding how AWS Lambda works under the hood

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

The best way to reduce lambda cost is to code for the least runtime duration and memory usage and the best way to do it is to code in a language that compiles directly into a binary (No runtime needed) like Go, Rust etc.

## 📲 Installation and Setup

- [AWS Account](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html) - An AWS account is needed since we'll be using AWS for the cloud resources, but don't worry, the free tier will be more than enough for learning and it won't cost anything
- [Set up Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html)

---

## 💡 Learning Session

- Theory
    - [AWS Lambda:](https://aws.amazon.com/lambda/getting-started/)
    - [Working with IAM roles (permission)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)
    - [Basics of AWS SDK](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html)

- Project:
    - Setting up a Lambda function to respond hello world

---
## 🔖 Resource Pool

- [AWS serverless repository](https://aws.amazon.com/serverless/serverlessrepo/)
- [AWS Training and certification](https://aws.amazon.com/training/)

### 📄 Articles/Blogs
- [Under the Hood of AWS Lambda](https://d1.awsstatic.com/events/reinvent/2019/REPEAT_1_A_serverless_journey_AWS_Lambda_under_the_hood_SVS405-R1.pdf)

### 📽️ Videos
- [Under the Hood of AWS Lambda](https://www.youtube.com/watch?v=xmacMfbrG28)

### 🗞️ Newsletters (Optional)
- https://serverless.email/

### 🫂 Communities (Optional)
- AWS User groups ([Kochi](https://meetup.com/awsugkochi))

---
## 🚀 Project Pool

- https://github.com/aws-samples/aws-lambda-sample-applications



