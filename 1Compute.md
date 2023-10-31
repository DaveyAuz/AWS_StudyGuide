# AWS Compute

## AWS Lambda

**AWS Lambda** provides a serverless computing environment, enabling developers to execute code in response to specific events without needing to provision or manage infrastructure. By automatically handling operational aspects such as scaling, patching, and administration, Lambda empowers developers to focus purely on business logic and code.

### What is AWS Lambda?

AWS Lambda is at the heart of the serverless movement in the cloud. "Serverless" does not mean there are no servers, but rather that you, as a developer or a business, don't have to deal with them. The infrastructure is abstracted away, leaving developers free to focus on building applications.

- **Event-Driven Model**: AWS Lambda is designed to use events like changes to data in an Amazon S3 bucket or updates in a DynamoDB table to trigger the execution of code. When the designated event occurs, Lambda executes the function asynchronously.

- **Stateless**: Each function execution is independent. AWS Lambda assumes no retention of state between function executions.

### Key Features

- **Event-driven**:
  - **Built-in Integrations**: AWS Lambda natively supports triggers from over a dozen AWS services, transforming the development of reactive applications.
  - **Custom Triggers**: With the Lambda API or custom integrations, developers can define custom event sources.
  - **Immediate Processing**: React to real-time data modifications, allowing for live responses and analytics.

- **Automatic Scaling**:
  - **Concurrent Executions**: Lambda functions can run code in parallel and process multiple events simultaneously.
  - **Provisioned Concurrency**: For latency-sensitive applications, you can ensure that there's always a warm container waiting to process an event.
  - **State Management**: For stateful processing, you can utilize services like Amazon ElastiCache or Amazon DynamoDB.

- **Serverless Framework**:
  - **Zero Administration**: Lambda takes care of everything required to run and scale code with high availability.
  - **Built-in Fault Tolerance**: Lambda maintains compute capacity and infrastructure reliability, including monitoring, logging via Amazon CloudWatch, and automatic retries.
  - **Resource Specification**: You can set the amount of memory allocated to a Lambda function, and AWS Lambda allocates proportional CPU power, network bandwidth, and disk I/O.

- **Integrated Security Model**:
  - **IAM Roles**: Assign IAM roles to your Lambda functions to control permissions.
  - **VPC Access**: Run Lambda functions within a Virtual Private Cloud (VPC) to access resources in a private environment.
  - **Encryption**: Data can be encrypted at rest and in transit.

### Use Cases

- **Real-time File Processing**: Automatically process, analyze, and route new files added to Amazon S3 buckets.
- **Data Validation**: Validate, filter, and transform data in real-time.
- **Backend for Websites & Mobile Apps**: Use AWS Lambda with Amazon API Gateway to create serverless backends for websites and mobile apps.
- **Chatbots and Virtual Assistants**: Build serverless chatbots and virtual assistants using AWS Lambda with Amazon Lex or integrate with platforms like Slack.
- **IoT Backend**: Process, store, and analyze IoT device data by executing Lambda functions in response to device activity.


## 2. Batch

- **What is it?**  
AWS Batch is designed for developers, scientists, and engineers to easily and efficiently run hundreds of thousands of computing jobs on AWS. It dynamically provisions the optimal quantity and type of compute resources.

- **Key Features**:
  - **Dynamic Scaling**: Ensures that the right amount of compute resources are used, optimizing cost and performance.
  - **Integration**: Use AWS Fargate for serverless compute capacity to run containers without managing underlying instances or clusters.
  - **Scheduling**: Fine-tuned control over job execution using priority, dependencies, and sequencing.

## 3. Serverless Application Repository

- **What is it?**  
This is a curated digital catalog where developers can share and deploy serverless applications. It simplifies the deployment, sharing, and discovery process of serverless apps.

- **Key Features**:
  - **Sharing**: Developers can publish and share their serverless applications, expanding their reach within the AWS community.
  - **Integration**: Incorporates well with AWS services, especially Lambda, to deploy serverless applications with ease.
  - **Discovery**: Helps users find the right serverless solution by browsing different categories and using filters.

## 4. AWS Outposts

- **What is it?**  
A fully managed service that extends AWS's infrastructure, AWS services, APIs, and tools to virtually any connected site, such as a data center or on-premises facility.

- **Key Features**:
  - **Consistency**: Provides a consistent hybrid experience by offering the same tools, APIs, hardware, and functionality across on-premises and cloud environments.
  - **Local Processing**: Crucial for applications demanding low-latency access to on-premises systems, local data processing, or local data storage.
  - **Hybrid Architecture**: Facilitates diverse scenarios, from data center extensions to disaster recovery and local data processing.

## 5. EC2 Image Builder

- **What is it?**  
It's a service that provides a simple, fast, and reproducible way to create and manage server images (AMIs), ensuring consistent infrastructure across teams and applications.

- **Key Features**:
  - **Automation**: Simplify the process of building and maintaining up-to-date, secure, and standardized OS images.
  - **Validation**: Ensure the image's compliance with established standards before deployment.
  - **Integration**: Seamlessly connects with a wide variety of AWS services, enhancing its functionality and reach.

## 6. AWS App Runner

- **What is it?**  
A service designed for developers who want to build and run containerized web applications and APIs quickly. It abstracts infrastructure management tasks like provisioning, scaling, and configuration.

- **Key Features**:
  - **Simplified Deployment**: Eliminates the manual steps involved in building and deploying containers. Connect directly to source code repositories or container registries.
  - **Scaling**: App Runner manages the scaling behavior, ensuring that applications can handle varying loads.
  - **Integration**: Tight integration with development platforms like GitHub for streamlined workflows.

## 7. AWS Elastic Beanstalk

- **What is it?**  
  **AWS Elastic Beanstalk** is a PaaS (Platform as a Service) offered by Amazon Web Services. It provides developers an orchestrated way to deploy a variety of applications like Java, .NET, PHP, Node.js, Python, Ruby, and Go without worrying about the infrastructure. The service automatically handles deployment details, capacity provisioning, load balancing, and application health monitoring.

- **Key Features**:
  - **Easy Deployment**: Deploy applications from development to production while AWS takes care of the underlying infrastructure.
  - **Auto Scaling**: Elastic Beanstalk automatically scales resources up or down based on the demands of your application.
  - **Managed Platform Updates**: AWS manages and updates the platform, ensuring you have the latest patches, updates, and features.
  - **Integrated Developer Tools**: Offers integration with other AWS services and developer tools for an end-to-end development and deployment experience.
  - **Customization**: Allows for environment configurations and extensions to fit your application needs.

- **Real-world Usage**:
  - **Web Application Hosting**: Quickly deploying and managing web applications and services without infrastructure setup.
  - **API Backend**: Deploying backend services for mobile, web, and other applications.
  - **E-commerce Websites**: Scaling e-commerce platforms during high demand like sales or holiday seasons.

## 8. Amazon Lightsail

- **What is it?**  
  **Amazon Lightsail** is designed to be an easy-to-use cloud platform that offers developers compute, storage, and networking capabilities. It simplifies the process of launching specific software or developer stacks on a virtual server and is designed for simpler workloads, quick deployments, and getting started scenarios.

- **Key Features**:
  - **Simplified Virtual Servers**: Easily set up and manage virtual servers with a fixed monthly plan.
  - **Managed Databases**: Provides fully managed databases, optimized for performance and reliability.
  - **Networking Features**: Comes with built-in networking features like floating IPs, static IPs, and DNS management.
  - **Pre-configured Applications**: Offers blueprints for WordPress, Joomla, LAMP, Node.js, and many more.
  - **Snapshots and Backups**: Take snapshots of your instance or database to keep your data safe and enable easy restoration.

- **Real-world Usage**:
  - **Web Hosting**: Ideal for running small to medium websites or blogs without the complexities of managing the underlying server.
  - **Development and Testing**: Provides an environment for developers to build and test applications without provisioning complex cloud resources.
  - **Personal Projects**: Suitable for hobbyists or individuals wanting to explore or start on a new project without a significant upfront investment.


  [HOME](./README.md)
  