
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

# AWS Storage

Amazon Web Services (AWS) offers a comprehensive portfolio of storage solutions to help you manage data more cost-effectively, securely, and at scale. AWS storage solutions are built for durability, ensuring that data can be backed up, archived, and easily retrieved. Depending on the specific need (like file storage, block storage, or object storage), AWS has a service tailored for that requirement.

Examples of AWS storage services include:
- **Amazon Simple Storage Service (S3)**: Used for object storage.
- **Amazon Elastic Block Store (EBS)**: Provides block storage.
- **Amazon Elastic File System (EFS)**: Designed for file storage.

## FSx

**Amazon FSx** provides fully managed file storage built on popular open-source file systems. It offers two main products:

- **Amazon FSx for Windows File Server**: Tailored for Windows-based applications, this service offers a fully managed native Microsoft Windows file system. This ensures an easy migration of Windows-based applications to AWS. It's fundamentally constructed upon Windows Server and supports the SMB (Server Message Block) protocol.

- **Amazon FSx for Lustre**: This is ideal for high-performance computing, machine learning, and other data-intensive tasks. It's a managed file system that's fine-tuned for compute-intensive operations and it seamlessly integrates with Amazon S3.

For both products, AWS manages all the intricate tasks such as backups, patching, and infrastructure upkeep.

## AWS Backup

**AWS Backup** is a centralized service that makes it straightforward to initiate, manage, and scale backups across AWS services. This encapsulates services like:
- Amazon DynamoDB
- Amazon RDS (Relational Database Service)
- Amazon EFS
- Amazon EC2
- AWS Storage Gateway

With AWS Backup, you can:
- Set up backup policies.
- Monitor backup tasks.
- Control the backup lifecycle, including the transition to cold storage or eventual deletion after a designated period.

## AWS Elastic Disaster Recovery (formerly CloudEndure Disaster Recovery)

**AWS Elastic Disaster Recovery** is a service designed to help businesses recover swiftly from IT disruptions without needing a secondary physical location. This service continuously mirrors your machines (be it on-premises, in AWS, or in another cloud) to a budget-friendly staging area within your AWS account.

In the event of a disaster, it allows you to:
- Promptly launch thousands of your machines on AWS in their pre-configured state.
- Ensure minimal downtime and data loss by offering speedy, dependable recovery of physical, virtual, and cloud-based servers into AWS.

Combined, these AWS Storage services offer a comprehensive and sturdy storage and backup approach to cater to diverse workloads and scenarios.


# AWS Database Services

## 3. Database:

### Neptune

**Amazon Neptune** is a fast, reliable, fully managed graph database service that makes it easy to build and run applications that work with highly connected datasets. 

- **Key Features**:
  - Supports both **Property Graph** and **RDF**.
  - Highly scalable and can handle billions of relationships.
  - Six-way replicas for high availability.
  - Continuous backup to Amazon S3.

### Amazon QLDB

**Amazon Quantum Ledger Database (QLDB)** is a fully managed ledger database. It provides a transparent, immutable, and cryptographically verifiable transaction log, owned by a central authority.

- **Key Features**:
  - **Immutable**: Once data is written, it cannot be changed.
  - **Transparent**: Every data change is recorded with a complete history.
  - Built-in **cryptographic verification**.
  - Serverless and scales to execute 2–3X more transactions than ledgers in common blockchain frameworks.

### Amazon DocumentDB

**Amazon DocumentDB (with MongoDB compatibility)** is a fast, scalable, highly available, and fully managed document database service that supports MongoDB workloads.

- **Key Features**:
  - **MongoDB Compatibility**: Supports MongoDB workloads, drivers, and tools.
  - **Scalable**: Can scale up to 64 TB of data.
  - **Replication**: Provides up to 15 low-latency read replicas.
  - **Backup**: Continuous backups to Amazon S3.

### Amazon Keyspaces

**Amazon Keyspaces (for Apache Cassandra)** is a scalable, highly available, and managed Apache Cassandra-compatible database service.

- **Key Features**:
  - **Cassandra Compatibility**: Easily manage workloads using the same Cassandra application code and developer tools.
  - **Serverless**: Automatically scales tables up and down based on actual application traffic.
  - **Encryption**: Supports AWS Key Management Service.

### Amazon Timestream

**Amazon Timestream** is a fast, scalable, fully managed time series database service for IoT and operational applications.

- **Key Features**:
  - **Serverless**: Scales automatically to support high ingest rates and query loads.
  - **Built-in Analytics**: Analyze data with built-in time series functions.
  - **Archival Storage**: Automatically moves older data to cost-effective storage tiers.

### DynamoDB

**Amazon DynamoDB** is a fully managed NoSQL database service that offers fast and predictable performance with seamless scalability.

- **Key Features**:
  - **Single-digit millisecond latency**.
  - **Scalable**: Handles more than 10 trillion requests per day and supports peaks of more than 20 million requests per second.
  - **Flexible Data Modeling**: Supports both document and key-value data structures.
  - **Global Tables**: Multi-region replication for global availability.

### Amazon MemoryDB For Redis

**Amazon MemoryDB for Redis** is a fully managed, in-memory database built on popular Redis, delivering ultra-fast performance with the simplicity and fault tolerance of Amazon ElastiCache.

- **Key Features**:
  - **Highly Available**: Multi-AZ with auto-failover.
  - **Durable**: Snapshots are automatically taken and backed up to Amazon S3.
  - **Scalable**: Scales automatically to support demanding workloads.
  - **Security**: Supports encryption at rest and in transit.

# AWS Migration & Transfer Services

## 4. Migration & Transfer:

### AWS Transfer Family

**AWS Transfer Family** is a fully managed service that enables the secure transfer of files over the Internet and into and out of Amazon S3 or Amazon EFS.

- **Key Features**:
  - **Protocol Support**: Supports SFTP, FTPS, and FTP.
  - **Integration**: Directly integrates with Amazon S3 and Amazon EFS.
  - **Identity Store**: Easily integrates with existing authentication systems.
  - **End-to-End Encryption**: Ensures data is secured during transfer.

### DataSync

**AWS DataSync** is a data transfer service that makes it easy for users to automate the movement of data between on-premises storage and Amazon S3, Amazon EFS, or Amazon FSx for Windows File Server.

- **Key Features**:
  - **Speed**: Transfers data up to 10 times faster than open-source tools.
  - **Automatic Encryption**: Data is encrypted during transit.
  - **Schedule and Monitor**: Easily schedule data transfers and monitor progress.
  - **Integrations**: Works with NFS, SMB/CIFS, and object storage interfaces.

### AWS Mainframe Modernization

**AWS Mainframe Modernization** is a service that aids businesses in moving their mainframe applications to AWS. This service helps to reduce costs and drive agility.

- **Key Features**:
  - **Automated Refactoring**: Converts legacy applications into Java or .NET.
  - **Data Migration Tools**: Assists in moving mainframe databases to AWS databases.
  - **Performance Optimization**: Ensures the modernized applications perform efficiently.
  - **Training and Support**: Provides resources and support to ensure a smooth migration process.


# AWS Networking & Content Delivery Services

## 5. Networking & Content Delivery:

### AWS App Mesh

**AWS App Mesh** is a service mesh that provides application-level networking, enabling your services to communicate with each other across multiple types of computing infrastructure.

- **Key Features**:
  - **Traffic Controls**: Provides dynamic traffic routing to manage service-to-service communication.
  - **Observability**: Offers insights into performance and the health of applications.
  - **Consistent Communication**: Helps ensure that services are communicating as expected.
  - **Integrated with AWS**: Easily integrates with services like Amazon ECS, Amazon EKS, and AWS Fargate.

### AWS Cloud Map

**AWS Cloud Map** is a cloud resource discovery service. With AWS Cloud Map, you can define custom names for application resources, and it maintains the updated location of these dynamically changing resources.

- **Key Features**:
  - **Service Discovery**: Enables applications to discover the location of cloud resources dynamically.
  - **Health Checking**: Monitors the health of resources, rerouting traffic when appropriate.
  - **Custom Naming**: Allows developers to define custom names for application services.
  - **Integration**: Seamlessly integrates with services like Amazon ECS and AWS Lambda.

### Global Accelerator

**AWS Global Accelerator** improves the availability and performance of applications by using static IP addresses and the AWS global network infrastructure.

- **Key Features**:
  - **Static Anycast IP Addresses**: Provides global IP addresses that route user traffic to the optimal AWS endpoint.
  - **Performance**: Utilizes the AWS global network backbone to optimize the path from your users to your applications.
  - **Reliability**: Increases the availability of your application through endpoint health checks and instant regional failover.
  - **Security**: Integrates with AWS Shield for DDoS protection.

### AWS Private 5G

**AWS Private 5G** is a managed service that lets you set up and scale private 5G mobile networks in your facilities, without the need for telecom expertise.

- **Key Features**:
  - **Simplicity**: Provides an easy-to-use service for deploying private 5G networks.
  - **Scalability**: Allows for rapid scaling based on business needs.
  - **Flexibility**: Supports various use cases like factories, warehouses, and campuses.
  - **Management**: AWS handles the heavy lifting of network management, letting businesses focus on their core competencies.


# AWS Developer Tools

## 6. Developer Tools:

### CodeArtifact

**AWS CodeArtifact** is a fully managed artifact repository service that makes it easier for organizations to securely store, publish, and share software packages used in their development process.

- **Key Features**:
  - **Centralized Repository**: Store and retrieve versioned software artifacts, enabling consistent builds.
  - **Integration with Dev Tools**: Seamlessly integrates with tools like Maven, Gradle, and npm.
  - **Fine-Grained Permissions**: Uses AWS Identity and Access Management (IAM) for access controls.
  - **Artifact Tracking**: Tracks dependencies and references between packages.

### CloudShell

**AWS CloudShell** is a browser-based shell that provides command-line access to AWS resources directly from the AWS Management Console.

- **Key Features**:
  - **Pre-Authenticated Environment**: Automatically authenticates using the credentials of the user logged into the AWS Console.
  - **Scripting Capabilities**: Supports popular scripting languages such as Python, Node.js, and Bash.
  - **Persistent Storage**: Offers 1 GB of storage for scripts, files, and tools.
  - **Integrated AWS CLI**: Comes with the AWS Command Line Interface pre-installed.

### AWS FIS

**AWS Fault Injection Simulator (FIS)** helps you perform controlled experiments on your AWS workloads by injecting faults and monitoring the results. This allows you to understand your system's resilience.

- **Key Features**:
  - **Controlled Experiments**: Introduce faults like latency, error codes, and instance failures.
  - **Built-In Templates**: Offers predefined templates for common fault injection scenarios.
  - **Monitoring**: Integrates with Amazon CloudWatch for real-time monitoring.
  - **Safety Controls**: Provides the ability to set stop conditions to halt experiments when specified thresholds are met.


# AWS Services

## 7. Blockchain:

### Amazon Managed Blockchain

**Amazon Managed Blockchain** is a fully managed service that makes it easy to create and manage scalable blockchain networks using popular open-source frameworks like Hyperledger Fabric and Ethereum.

- **Key Features**:
  - **Easy to Deploy**: Quickly set up blockchain networks with a few AWS Management Console clicks.
  - **Scalable**: Supports thousands of applications and millions of transactions.
  - **Managed**: Takes care of patching, backups, and node maintenance.
  - **Security**: Data is encrypted at rest and in transit. It also integrates with AWS Key Management Service for managed blockchain network encryption keys.
  - **Interoperable**: With the Amazon Managed Blockchain’s support for Ethereum, it allows for easy interoperability with public Ethereum mainnet.
  - **Reliability**: Uses Amazon QLDB to provide an immutable change history of blockchain network activity.

## 8. Quantum Technologies:

### Amazon Braket

**Amazon Braket** is a fully managed quantum computing service that helps researchers and developers start experimenting with computers from quantum hardware providers.

- **Key Features**:
  - **Hybrid Algorithms**: Combines quantum and classical computing resources.
  - **Accessible**: Provides a development environment for you to explore and build quantum algorithms.
  - **Choice of Quantum Processors**: Offers access to quantum computing hardware from multiple providers.
  - **Secure**: All data is encrypted in transit and at rest.
  - **Integrated**: Works with other AWS services to store, analyze, and manage quantum data.
  - **Managed**: AWS handles the heavy lifting of setting up and managing the quantum compute facilities.


# AWS Services: Management & Governance

## 9. Management & Governance:

### AWS AppConfig

**AWS AppConfig** enables application owners to manage, deploy, and validate configurations, ensuring applications receive correct configurations in real time, even as they scale.

- **Key Features**:
  - **Configuration Deployment**: Enables feature toggle management without code deployments.
  - **Deployment Safety**: Monitors application health and can halt poor configurations.
  - **Integration with Systems Manager**: Seamlessly use with Systems Manager Parameter Store or Config for detailed configuration data management.

### Control Tower

**Control Tower** is a managed service to set up and govern a secure, compliant, multi-account environment or landing zone.

- **Key Features**:
  - **Blueprints**: Provides design patterns and best practices for setting up AWS environments.
  - **Guardrails**: Pre-packaged governance rules for security, operations, and compliance.
  - **Account Factory**: Automated account provisioning.

### AWS License Manager

**AWS License Manager** allows enterprises to manage and govern software licenses, ensuring compliance and preventing overages.

- **Key Features**:
  - **Centralized License Rules**: Define rules based on licensing agreements to prevent license breaches.
  - **Stop non-compliant deployments**: Automatically enforce licensing rules.
  - **Track licenses across multiple AWS accounts**: Monitor and manage all license usage from a single account.

### AWS Well-Architected Tool

**AWS Well-Architected Tool** provides a consistent approach to evaluating AWS architectures, helping you implement designs that scale with application needs over time.

- **Key Features**:
  - **Workload Review**: Compares your workload against AWS best practices.
  - **Milestones**: Records and reviews architectural improvements over time.
  - **Framework**: Covers five pillars: operational excellence, security, reliability, performance efficiency, and cost optimization.

### AWS Health Dashboard

**AWS Health Dashboard** offers real-time information about AWS services, providing transparency into service health and incidents.

- **Key Features**:
  - **Event Notifications**: Alerts on incidents affecting AWS services you use.
  - **Personal Health Dashboard**: Offers visibility into service health tailored to your AWS account.
  - **API Access**: Programmatically access AWS Health Information.

### AWS Chatbot

**AWS Chatbot** facilitates real-time monitoring and interaction with AWS resources from Slack channels and Amazon Chime chat rooms.

- **Key Features**:
  - **Instant Notifications**: Receive alerts directly in your chat rooms.
  - **Interact with AWS**: Use commands to fetch AWS resource status or invoke AWS Lambda functions.
  - **IAM Integration**: Secure permissions management.

### Launch Wizard

**Launch Wizard** identifies appropriate AWS resources for your application, making it easier to set up and deploy third-party applications.

- **Key Features**:
  - **Guided Deployments**: Simplifies deployment of key applications.
  - **Cost Estimates**: Provides a breakdown of infrastructure costs.
  - **Best Practice Compliance**: Ensures resources are set up following AWS best practices.

### AWS Compute Optimizer

**AWS Compute Optimizer** utilizes machine learning to analyze and recommend resources, optimizing performance and reducing costs.

- **Key Features**:
  - **Resource Recommendations**: Recommends optimal AWS resources for your workloads.
  - **Performance Metrics**: Analyzes historical data to predict future resource needs.
  - **Cost Savings**: Identifies under-utilized resources to reduce costs.

### Resource Group & Tag Editor

**Resource Group & Tag Editor** helps in organizing, managing, and locating AWS resources.

- **Key Features**:
  - **Tagging**: Apply metadata to resources to simplify organization and searching.
  - **Resource Group Creation**: Organize resources based on lifecycle, owner, or environment.
  - **Visualize and Manage Resources**: Offers a central dashboard for resource overview.

### Amazon Grafana

**Amazon Grafana** is a managed Grafana-compatible service, enabling you to instantly create, operate, and scale Grafana visualizations for operational insights.

- **Key Features**:
  - **Fully Managed**: Offloads operational overhead, including backups, patching, and scaling.
  - **Data Source Integration**: Connects with several data sources, including AWS, other cloud services, and on-premises data.

### Amazon Prometheus

**Amazon Prometheus** offers compatibility with the popular open-source Prometheus monitoring tool, optimized for container and microservices-based architectures.

- **Key Features**:
  - **Scalable**: Adapts to increasing metric workloads automatically.
  - **Prometheus Query Language**: Utilizes native Prometheus Query Language (PromQL) for metric queries.
  - **Integrated with Amazon Grafana**: Visualize Prometheus metrics with Amazon Grafana seamlessly.

### AWS Proton

**AWS Proton** is an application delivery automation service, ensuring consistent infrastructure and code deployments for serverless and container-based applications.

- **Key Features**:
  - **Templates**: Defines infrastructure and CI/CD configurations for applications.
  - **Managed Deployments**: Handles infrastructure provisioning and code deployments.
  - **Centralized Governance**: Ensures service standards and best practices.

### AWS Resilience Hub

**AWS Resilience Hub** enables you to understand, improve, and track your AWS workload resilience.

- **Key Features**:
  - **Resilience Summary**: Aggregated view of resilience across workloads.
  - **Improvement Recommendations**: Suggests architectural and operational enhancements.
  - **Workload Monitoring**: Tracks changes to resilience over time.

### Incident Manager

**Incident Manager** ensures timely response and resolution of critical incidents, reducing Mean Time To Recovery (MTTR).

- **Key Features**:
  - **Incident Plans**: Prepare for incidents with defined response plans.
  - **Automated Mobilization**: Alerts and mobilizes the right resources.
  - **Post-Incident Analysis**: Analyzes root causes and tracks action items to improve incident response over time.


# AWS Services: Media Services

## 10. Media Services:

### MediaConnect

**AWS MediaConnect** is a high-quality transport service for live video. It's designed to help broadcasters and content creators reliably ingest, transmit, and distribute live video streams.

- **Key Features**:
  - **Secure & Reliable**: Provides a highly reliable and encrypted stream.
  - **Flexibility**: Adapts to varying bandwidth, latency, and network conditions.
  - **Integration**: Easily integrates with other AWS media services for broader media workflows.
  - **Zixi Protocol**: Supports the Zixi protocol and the RIST standard for high-quality video transport.

### Elemental Appliances & Software

**AWS Elemental Appliances & Software** offer on-premises media solutions to process and deliver broadcast and over-the-top (OTT) video.

- **Key Features**:
  - **Versatility**: Processes live and file-based video content.
  - **End-to-End Workflow**: Supports encoding, packaging, storage, and delivery.
  - **Adaptive Bitrate Streaming**: Ensures optimal viewer experience.
  - **High-Quality Video Processing**: 4K/UHD, HDR processing with high-speed file-based transcoding.

### Amazon Interactive Video Service (IVS)

**Amazon IVS** is a managed service that makes it easy to set up, create, and manage interactive and low-latency live video streams for web and mobile applications.

- **Key Features**:
  - **Ultra-Low Latency**: Delivers video in less than 3 seconds of real-world latency.
  - **Interactivity**: Integrates with interactive features like polls, trivia, and Q&A.
  - **Built-in Monetization**: Enables pay-per-view, subscription, and ad-insertion.
  - **SDKs**: Offers Software Development Kits to build custom video experiences.

### Nimble Studio

**AWS Nimble Studio** empowers creative studios to produce visual effects, animations, and interactive content entirely in the cloud, with the scale and flexibility of AWS.

- **Key Features**:
  - **On-demand Rendering**: Quickly scales rendering workloads without upfront infrastructure investment.
  - **Virtual Workstations**: Provides high-performance virtual machines, suitable for artists and editors.
  - **Shared File Systems**: Enables collaborative workflows with high-speed, scalable shared storage.
  - **Built-in Content Library**: Offers a library of 3D assets and software licenses.


# AWS Services: Analytics

## 11. Analytics:

### Amazon Redshift

**Amazon Redshift** is a fully managed, petabyte-scale data warehouse service in the cloud. It's designed for high-performance analysis of large datasets using sophisticated query optimization and columnar storage.

- **Key Features**:
  - **Performance**: Uses machine learning, massively parallel processing (MPP), and columnar storage for fast query performance.
  - **Scalability**: Starts small and scales up as your needs grow, going up to a petabyte or more.
  - **Concurrency**: Offers Concurrency Scaling to support thousands of concurrent queries.
  - **RA3 Nodes**: Allows you to scale compute and storage separately and also supports automatic workload management for fair allocation of resources.
  - **Integration**: Seamlessly integrates with popular business intelligence tools and integrates well with other AWS services.
  - **Data Sharing**: Share live data across Redshift clusters without data movement or copying.

### AWS Data Exchange

**AWS Data Exchange** is a service that makes it easier for AWS customers to securely exchange and use third-party data within the cloud.

- **Key Features**:
  - **Vast Catalog**: Access to a vast catalog of third-party data from category-leading brands.
  - **Real-time Updates**: Automatically receive updates to subscribed datasets.
  - **Integrated**: Use data directly in AWS analytics and machine learning services.
  - **Control**: Providers retain control and transparency over who is subscribing and how data is used.
  - **Data Subscription Costs**: Transparent data subscription costs, directly through AWS billing.

### AWS Lake Formation

**AWS Lake Formation** is a service that simplifies the process of setting up, securing, and managing data lakes. A data lake allows you to store, secure, and analyze data in diverse formats, and scale to petabyte-size.

- **Key Features**:
  - **Data Preparation**: Makes it easy to prepare data for analytics and machine learning with integrated partner and open-source data processing tools.
  - **Centralized Access & Security**: Provides centralized control over permissions, ensuring that policies are consistently enforced across analytics and machine learning services.
  - **Granular Data Access**: Offers table and column-level access controls.
  - **Blueprints**: Allows for automated setup and ingestion, turning raw data into query-ready datasets.
  - **Integration**: Integrates seamlessly with Amazon S3, Redshift, Athena, Glue, and more.

# AWS Services: Security, Identity & Compliance

## 12. Security, Identity & Compliance:

### Resource Access Manager (RAM)

**Resource Access Manager (RAM)** is a service that enables you to easily and securely share AWS resources with any AWS account or within your AWS Organization.

- **Key Features**:
  - **Share Resources**: Share resources like Subnets, Transit Gateways, or License configurations across accounts.
  - **Consolidate Resources**: Avoid duplicating resources, helping you reduce operational overhead.
  - **Control**: Retain resource ownership and maintain control, including who can access and manage those shared resources.

### IAM Identity Center

**IAM Identity Center** is the central location to manage users and their access.

- **Key Features**:
  - **Central Management**: View and manage your AWS IAM resources in a centralized location.
  - **Access Analyzer**: Identify any resources that are shared with external entities.
  - **Visualizations**: View visual summaries of IAM entity details and relationships.

### Cognito

**Amazon Cognito** lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.

- **Key Features**:
  - **User Directories**: Maintain a persistent user directory that can scale to hundreds of millions of users.
  - **Social & SSO Logins**: Support for social identity providers and SAML-based SSO.
  - **Sync**: Synchronize data across devices so that the app experience remains consistent.
  - **Enhanced Security**: Provides user authentication challenges if suspicious activity is detected.

### IAM (Identity and Access Management)

**IAM** lets you manage access to AWS services and resources securely.

- **Key Features**:
  - **Fine-grained Access Control**: Provides granular permissions to AWS services/resources.
  - **Roles for Apps**: Allow applications to make AWS service requests without credential distribution.
  - **MFA**: Add two-factor authentication for privileged accounts.
  - **Identity Federation**: Link IAM with external identity systems like Google or Microsoft Active Directory.

### Key Management Service (KMS)

**AWS Key Management Service (KMS)** is a managed service that makes it easy to create and manage cryptographic keys and control their use across AWS services and in applications.

- **Key Features**:
  - **Centralized Control**: Control the cryptographic keys used to encrypt your data.
  - **Integrated with AWS Services**: Integrated with other AWS services to encrypt data you store in these services.
  - **Auditable**: View logs of key usage to help meet your regulatory and compliance needs.

### Security Hub

**AWS Security Hub** provides a comprehensive view of your security alerts and compliance status across AWS accounts.

- **Key Features**:
  - **Centralized View**: Consolidate security alerts and automate compliance checks.
  - **Integrated**: Integrated with AWS services and third-party products.
  - **Customizable**: Customize the standard findings and create your own.

### Detective

**Amazon Detective** makes it easy to analyze, investigate, and identify the root cause of potential security issues or suspicious activities.

- **Key Features**:
  - **Visualizations**: Provides an interactive view of your AWS resources.
  - **Analysis**: Uses machine learning to analyze and visualize security data.

### AWS Signer

**AWS Signer** is a fully managed code-signing service to ensure the trust and integrity of your code.

- **Key Features**:
  - **Secure**: Centralize and secure your code-signing process.
  - **Integrate with ACM**: Use private keys stored securely in AWS Certificate Manager.

### AWS Network Firewall

**AWS Network Firewall** is a managed service that makes it easy to deploy essential network protections for all of your Amazon VPCs.

- **Key Features**:
  - **Protection**: Provides protection against common web exploits, malicious IPs, and more.
  - **Scalability**: Automatically scales with traffic volume.

### AWS Audit Manager

**AWS Audit Manager** simplifies the process of auditing AWS usage to prove compliance with policies and regulations.

- **Key Features**:
  - **Continuous Auditing**: Continuously audits AWS usage to ensure that it aligns with internal policies.
  - **Automated Evidence Collection**: Automates evidence collection for easier audits.

