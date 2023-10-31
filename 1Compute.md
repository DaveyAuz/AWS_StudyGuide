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


## AWS Batch

**AWS Batch** empowers developers, scientists, and engineers with a platform that simplifies the execution of batch computing workloads on AWS. Instead of manually deploying and managing infrastructure, AWS Batch intelligently handles the complexities of provisioning, monitoring, and scaling based on the requirements of the workload, ensuring that the most efficient compute resources are used.

### What is AWS Batch?

AWS Batch provides a serverless computing environment to handle virtually any batch computing task, regardless of scale. From small-scale tasks like data processing to vast, compute-intensive simulations, AWS Batch can handle them with ease, streamlining the process of managing, scheduling, and executing batch computing jobs.

- **No Infrastructure Management**: AWS Batch manages the compute environments, ensuring that the job queues are efficiently managed, so you don’t have to.
  
- **Cost-Optimized Resource Procurement**: It provisions the most cost-effective set of resources based on the volume and specific requirements of the jobs.

### Key Features

- **Dynamic Scaling**:
  - **Resource Optimization**: AWS Batch adjusts the compute resources in real-time, depending on the job's requirements, ensuring optimal performance and cost.
  - **Spot Integration**: Utilizes Spot Instances to leverage spare AWS compute capacity, which can lead to cost savings.
  - **Array Jobs**: Split a large job into smaller tasks that run in parallel, speeding up processing.

- **Deep Integration**:
  - **AWS Fargate Integration**: Provides serverless compute capacity, enabling you to run containers without managing the underlying instances or clusters.
  - **Seamless AWS Ecosystem Connectivity**: Integrates effortlessly with services like Amazon EC2, Amazon ECS, and AWS Step Functions for extended functionality.
  
- **Scheduling and Execution**:
  - **Priority Queuing**: Control the order of job execution based on priorities you define.
  - **Job Dependencies**: Define and control job sequences, ensuring certain jobs are run only after others complete.
  - **Retry Strategies**: If jobs fail, AWS Batch can be configured to retry them, ensuring tasks are completed even in the face of transient failures.

- **Custom Compute Environments**:
  - **Custom AMIs**: Use your own Amazon Machine Images (AMIs) tailored for specific tasks.
  - **Instance Type Selection**: Choose from a variety of EC2 instance types, from general-purpose to compute-optimized, to best fit your workload.
  
### Use Cases

- **Data Processing and Transformation**: Process vast datasets for analytics, transforming raw data into actionable insights.
- **Simulation & Modeling**: Perform large-scale simulations for research, engineering, or financial modeling.
- **Genomic Analysis**: Run extensive genomics workloads, analyzing DNA sequences and other genomics data.
- **Machine Learning & AI Training**: Train complex machine learning models on large datasets.
- **ETL Jobs**: Extract, Transform, Load (ETL) tasks for data warehousing and analytics.

## AWS Serverless Application Repository

**AWS Serverless Application Repository** acts as a marketplace and storage for serverless applications, facilitating a seamless and simplified experience for developers looking to share, deploy, or discover serverless solutions. With this service, developers can harness the potential of serverless architecture without starting from scratch, and instead leverage pre-built solutions that cater to a myriad of use cases.

### What is the AWS Serverless Application Repository?

The AWS Serverless Application Repository is a managed repository for serverless applications, catering to the AWS community. It offers a curated collection of applications and components for an array of functionalities. By utilizing this service, developers can circumvent the foundational work and focus on customization and implementation.

- **Seamless Deployments**: Enables developers to deploy entire serverless architectures in a few clicks, significantly reducing deployment time.
  
- **Community-Powered**: Encourages a collective approach to serverless development where developers from around the world contribute, share, and leverage each other's work.

### Key Features

- **Application Sharing**:
  - **Publish Applications**: Developers can publish their serverless applications, expanding their reach and impact within the AWS ecosystem.
  - **Private & Public Sharing**: Applications can be shared publicly for the broader AWS community or privately within specific AWS accounts.
  
- **Deep Integration with AWS Services**:
  - **Direct Deployment**: Applications from the repository can be directly deployed into an AWS account, streamlining the setup process.
  - **Lambda Synergy**: Closely integrates with AWS Lambda, allowing developers to easily deploy serverless functions associated with applications in the repository.
  
- **Robust Discovery Tools**:
  - **Categorized Browsing**: Applications are categorized, making it easier for users to navigate and find solutions relevant to their needs.
  - **Advanced Filtering**: Users can filter based on various parameters like author, AWS service used, or specific keyword to refine their search.
  - **Application Details**: Each application comes with a detailed description, including its functionalities, requirements, and setup instructions.

- **Security and Compliance**:
  - **Verified Applications**: AWS verifies the applications for known malicious content, though users are encouraged to review applications before deploying.
  - **IAM Permissions**: Clearly defines the IAM permissions required for each application, ensuring users are aware of the access levels granted to the app.

### Use Cases

- **Rapid Prototyping**: Deploy pre-built applications to test concepts and ideas without building everything from scratch.
- **Operational Tools**: Find tools for monitoring, logging, or security to integrate into serverless architectures.
- **Data Processing**: Implement data transformation, analysis, or ETL tasks using serverless applications available in the repository.
- **Learning & Experimentation**: For those new to serverless, explore and deploy applications to understand best practices and design patterns.



## AWS Outposts

**AWS Outposts** is a unique offering from AWS, extending its infrastructure and services right into on-premises facilities, be it data centers or other connected sites. This pioneering service aims to bridge the gap between cloud and on-premises environments, ensuring a cohesive and consistent experience irrespective of where your applications run.

### What is AWS Outposts?

AWS Outposts is a culmination of AWS’s hardware and software, brought into your on-premises location. It embodies the spirit of hybrid cloud architecture, allowing enterprises to enjoy the flexibility of cloud while addressing data residency and latency-sensitive application requirements.

- **Unified Experience**: While the location of operation changes, the experience doesn't. Users can leverage the same AWS APIs, tools, and infrastructure both in the cloud and on-premises.

- **Customized Solutions**: AWS Outposts can be tailored to suit specific needs, be it computational, memory, or storage requirements. 

- **Seamless Expansion**: As businesses grow, so can their Outpost, ensuring no roadblocks to scaling up or down based on demands.

### Key Features

- **Consistent Hybrid Experience**:
  - **Unified Management**: With AWS Outposts, there's no dichotomy between cloud and on-premises. The same AWS Management Console, CLI, or SDKs are at play.
  - **Standardized APIs**: The APIs you've been using on the AWS cloud remain unchanged, ensuring your applications need no modifications when operated on Outposts.

- **Optimized for Local Processing**:
  - **Low-latency Operations**: Critical applications demanding swift data access or operations, especially in sectors like finance or augmented reality, can thrive with Outposts.
  - **Local Data Residency**: For sectors bound by regulatory constraints on data localization, Outposts can be a lifesaver, ensuring data doesn't leave the facility.

- **Adaptive Hybrid Architectures**:
  - **Data Center Extension**: For businesses not ready to migrate everything to the cloud, Outposts acts as a bridge, ensuring a smooth transition phase.
  - **Disaster Recovery**: By maintaining a consistent environment, businesses can ensure quick recoveries in case of unforeseen events.
  - **Edge Computing**: For operations close to data sources, like in IoT scenarios, Outposts can process data locally, ensuring timely actions.

### Use Cases

- **Healthcare & Life Sciences**: With stringent data localization and privacy regulations, such as GDPR or HIPAA, Outposts ensures data remains on-premises while still leveraging AWS's computational prowess.

- **Telecommunications**: Enhancing the 5G experience demands data processing closer to the source, something Outposts excels in.

- **Manufacturing & Industrial**: Real-time data processing, crucial for IoT devices in industries, is facilitated by Outposts, ensuring timely insights and actions.

- **Financial Services**: In sectors where milliseconds can translate to millions, Outposts ensures ultra-low latency operations for critical financial transactions.

## EC2 Image Builder

**EC2 Image Builder** offers a streamlined solution to the often complex task of building, testing, and maintaining server images. By encapsulating the entire lifecycle of Amazon Machine Images (AMIs), it provides consistency and ensures that the infrastructure remains standardized and up-to-date across the board.

### What is EC2 Image Builder?

EC2 Image Builder is a service that encapsulates the lifecycle management of server images, giving users a straightforward and automated method to generate, patch, and test OS images. The images created are not just restricted to EC2 instances but are suitable for on-premises scenarios as well.

- **Centralized Management**: From the AWS Management Console, users can seamlessly create and manage images, reducing complexity and increasing productivity.

- **No Additional Costs**: Only pay for the AWS resources used during the image building process. There's no extra charge for the Image Builder service itself.

- **Golden Images**: Establish standardized and pre-approved image templates, known as Golden Images, ensuring a baseline of security and compliance.

### Key Features

- **Automated Image Building**:
  - **Pipeline Creation**: Define and configure automated pipelines that streamline the process of building and testing images.
  - **Scheduled Updates**: Set automated schedules for patching and updating OS and software components, ensuring images are always current.

- **End-to-End Validation**:
  - **Pre & Post Build Testing**: Integrate custom tests or utilize AWS-provided tests to guarantee the image's integrity and functionality.
  - **Compliance Checks**: Before deploying images, ensure they align with the organization's security and compliance benchmarks.

- **Extensive AWS Integration**:
  - **Service Coupling**: EC2 Image Builder can be seamlessly paired with other AWS services like AWS Organizations, Amazon EC2, and AWS Lambda to augment its capabilities.
  - **Cross-Account Image Sharing**: Share custom AMIs across accounts using AWS Resource Access Manager, ensuring standardized images across the organization.

### Use Cases

- **Rapid Deployments**: Accelerate the launch of applications by leveraging pre-built, tested, and compliant images, reducing deployment times.

- **Security & Compliance**: Ensure all instances, be it on AWS or on-premises, operate on compliant, secure, and standardized images, reducing vulnerabilities.

- **Consistent Environments**: By utilizing Golden Images, maintain a consistent environment for development, testing, and production, reducing anomalies and inconsistencies.

## AWS App Runner

**AWS App Runner** was born out of the need for developers to have a simplified and direct approach to deploying web applications and APIs, eliminating the overhead of managing the underlying infrastructure. By seamlessly connecting to existing source code repositories or container registries, App Runner offers a fast track from code to scalable running application in the AWS cloud.

### What is AWS App Runner?

AWS App Runner is a service primarily targeting developers, especially those looking to rapidly deploy web applications or APIs without getting bogged down by the intricacies of provisioning, configuration, or scaling. It's all about speed and simplicity.

- **Infrastructure Abstraction**: No need to get involved with the nuances of server setups, networking configurations, or security settings. App Runner handles it all.

- **Direct Integration**: Whether your code resides in a repository like GitHub or you have a container already built, App Runner connects directly and gets your application up and running.

- **Managed Runtime**: With AWS's expertise behind the scenes, expect a robust, high availability runtime environment for your applications, fully managed and monitored.

### Key Features

- **Effortless Deployment**:
  - **Continuous Deployment**: Whenever you update your code or container image, App Runner can automatically detect the changes and initiate the deployment process.
  - **Build and Deploy**: Just provide your application source code. App Runner will handle the process of building a container and deploying it.

- **Auto-scaling**:
  - **Adaptive Scaling**: Based on incoming traffic and utilization metrics, App Runner dynamically adjusts the number of running instances of your application, ensuring responsiveness while optimizing costs.
  - **Concurrent Requests Handling**: App Runner instances can handle multiple web requests concurrently, ensuring efficient resource utilization.

- **Seamless AWS Integration**:
  - **Developer Tools**: Enjoy tight integration with popular developer platforms like GitHub, making your CI/CD workflows smoother.
  - **Service Coupling**: App Runner works well with other AWS services, amplifying its capabilities. Think AWS Identity and Access Management (IAM) for security or Amazon CloudWatch for monitoring.

### Use Cases

- **Rapid Prototyping**: For developers looking to quickly iterate and test out ideas, App Runner offers a speedy way to get a prototype live.
  
- **Production-ready Web Applications**: Not just for prototypes, App Runner is robust enough to handle production workloads, backed by the reliability of AWS infrastructure.
  
- **API Deployment**: Whether you're deploying a RESTful API, GraphQL endpoint, or any other web service, App Runner is equipped to host and scale it.



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
  