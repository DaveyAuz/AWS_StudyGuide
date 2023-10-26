# AWS Compute

## 1. Lambda Functions

- **What is it?**  
AWS Lambda is a serverless compute service that allows developers to execute code in response to certain events without the need to provision or manage servers. This service abstracts infrastructure management tasks, like capacity provisioning and patching, and offers seamless scaling and built-in fault tolerance.

- **Key Features**:
  - **Event-driven**: It responds to triggers from AWS services such as Amazon S3, DynamoDB, or API Gateway, as well as custom events you define.
  - **Scaling**: AWS Lambda scales automatically by running code in response to each trigger. Its applications are highly available without additional effort.
  - **Serverless**: No need to think about servers; focus solely on your code.

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
  