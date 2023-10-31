# AWS Storage

Amazon Web Services (AWS) offers a diverse portfolio of storage solutions tailored to efficiently manage data in a secure and scalable manner. These solutions prioritize durability to ensure data backup, archiving, and swift retrieval. Depending on specific requirements such as file, block, or object storage, AWS has a dedicated service.

## Amazon Simple Storage Service (S3)

**Amazon S3** is a highly-scalable, reliable, and low-latency object storage service provided by AWS. It's the go-to solution for a broad spectrum of storage needs, from backups to content delivery and everything in-between.

### Key Features

- **Scalability**:
  - Can store an unlimited amount of data with individual objects ranging in size from 1 byte to 5 terabytes.
  - Built to store and retrieve any amount of data, accommodating growing or fluctuating workloads seamlessly.

- **Security**:
  - Offers features like S3 Object Lock which can enforce retention policies and protect against object deletions.
  - Supports server-side encryption (SSE) for data at rest.
  - Integrates with AWS Identity and Access Management (IAM) for fine-grained access control.
  - Provides tools for logging access and monitoring through AWS CloudTrail and Amazon S3 Server Access Logging.

- **Flexibility**:
  - Supports storage of diverse types of data – from structured to unstructured data.
  - Offers storage class options catering to different access patterns and cost considerations, such as S3 Standard, S3 Infrequent Access, and S3 Glacier.

- **Data Analysis**:
  - Enables in-place analytics with tools like Amazon Athena and Redshift Spectrum without moving the data.
  - Compatible with a broad range of big data analytics and machine learning tools.

- **Integration**:
  - Seamlessly works with a plethora of AWS services, such as AWS Lambda, Amazon CloudFront, and more.
  - Supports event-driven computing with AWS Lambda to build serverless applications.

### Storage Classes

1. **S3 Standard**:
   - Ideal for frequently accessed data.
   - Suited for big data analytics, content distribution, and backup.

2. **S3 Standard-IA (Infrequent Access)**:
   - For long-lived, but infrequently accessed data.
   - Lower storage cost compared to S3 Standard.

3. **S3 One Zone-IA**:
   - Stored in a single availability zone.
   - Suitable for backups or secondary backup copies.

4. **S3 Glacier & S3 Glacier Deep Archive**:
   - For long-term archival storage.
   - S3 Glacier offers retrievals ranging from minutes to hours, while Deep Archive is for retrieval within 12 hours.

### Data Lifecycle Policies

- Use S3 Lifecycle policies to transition objects between storage classes.
- Automatically move to less expensive storage classes or archive and even delete as per defined criteria.

### Use Cases

- Content distribution using integration with Amazon CloudFront.
- Backup and archival solutions.
- Big data, analytics, and data lake scenarios.
- Hosting static websites.
- Mobile, gaming, and app storage needs.

## Amazon Glacier

**Amazon Glacier** is a specialized storage service by AWS, optimized for archiving data and long-term backups. While Amazon S3 provides quick data retrieval, Glacier is tailored for data that is retrieved infrequently but needs to be stored for extended periods.

### Features

- **Cost-Effective**:
  - Offers one of the lowest storage costs in AWS.
  - Suited for data that is accessed infrequently, making it cost-effective for long-term archiving.

- **Security**:
  - All data is encrypted automatically at rest.
  - Supports secure data transit using SSL.
  - Integrates with AWS Identity and Access Management (IAM) to control and monitor who accesses your data.

- **Durability**:
  - Designed for 99.999999999% (11 9's) durability annually.
  - Distributes data across multiple facilities and on multiple devices within each facility.

- **Immutable Storage**:
  - Supports WORM (Write Once, Read Many) capability.
  - This ensures that data cannot be altered or deleted for a user-defined period.

- **Integration with S3**:
  - Allows for seamless data lifecycle transitions from S3 to Glacier.
  - Set up policies in S3 to automatically transition data to Glacier after a certain period.

### Retrieval Options

1. **Expedited**:
   - For urgent access.
   - Retrieves data in 1-5 minutes.

2. **Standard**:
   - Default option.
   - Retrieves data in 3-5 hours.

3. **Bulk**:
   - Designed for large-scale requests.
   - Retrieves data in 5-12 hours.

### Use Cases

- Archiving offsite backups.
- Storing historical data for regulatory compliance.
- Preserving digital media assets.
- Research and scientific study data storage.

## Amazon Elastic Block Store (EBS)

**Amazon EBS** provides persistent, block-level storage volumes for use with Amazon EC2 instances. Designed for both throughput and transaction-intensive workloads, EBS volumes are automatically replicated within their Availability Zone, offering high availability and durability.

### Key Features

- **Durability & Availability**:
  - Data is automatically replicated across multiple servers within a single Availability Zone.
  - Offers high durability, ensuring protection against component failures.
  - Provides the ability to attach a single volume to multiple EC2 instances with EBS Multi-Attach (specific volume types).

- **Performance**:
  - Delivers a consistent baseline performance with the ability to burst to higher levels.
  - Offers both SSD (Solid State Drive) and HDD (Hard Disk Drive) based volumes to cater to diverse needs.
    - **General Purpose (gp3 and gp2)**: SSD-based and suited for a broad range of workloads.
    - **Provisioned IOPS (io1 and io2)**: SSD-based for I/O-intensive applications like databases.
    - **Throughput Optimized (st1)**: HDD-based ideal for big data, log processing, etc.
    - **Cold HDD (sc1)**: HDD-based for less frequently accessed workloads.
    - **Magnetic (standard)**: Legacy HDD volume type.

- **Backup**:
  - Ability to create point-in-time snapshots of volumes, which are stored in Amazon S3.
  - Snapshots can be used for backups, creating new volumes, or copying across regions.
  - Supports incremental backups, which means only the blocks that have changed since the last snapshot are saved.

- **Encryption**:
  - Offers data encryption at rest using keys from AWS Key Management Service (KMS).
  - All data moving between instances and volumes is encrypted, ensuring security in transit.
  - Encryption and decryption are handled transparently and do not require any additional action from the user.

### Flexibility

- **Resizable**: Volumes can be increased in size or modified to a different volume type on-the-fly.
- **Snapshot Mobility**: Snapshots can be copied across AWS regions, aiding in disaster recovery, migration, or data duplication tasks.

### Use Cases

- Boot volumes for EC2 instances.
- High-performance databases and transactional systems using Provisioned IOPS.
- Data warehousing and analytics using Throughput Optimized HDD.
- Archival storage or infrequent access scenarios with Cold HDD.
- General-purpose storage with balanced cost and performance using General Purpose SSD.

## Amazon Elastic File System (EFS)

**Amazon EFS** is a managed file storage service designed to be used with AWS Cloud services and on-premises resources. It offers a simple, scalable, and fully managed elastic NFS that can be used concurrently by thousands of different AWS resources and on-premises servers.

### Key Features

- **Compatibility**:
  - Provides a standard file system interface and semantics (NFSv4 protocol).
  - Easily integrates with existing applications and tools that run on Linux-based systems.
  - Can be mounted on an Amazon EC2 instance or an on-premises server.

- **Scalability**:
  - Built to automatically scale up or down as files are added or removed, with no need to provision storage in advance.
  - Supports petabyte-scale storage and can handle large numbers of connections simultaneously.
  - Delivers consistent performance regardless of the amount of data or number of files.

- **Durability & Availability**:
  - Automatically and synchronously replicates data across multiple Availability Zones (AZs) for high availability and durability.
  - Designed to provide 99.999999999% (11 9's) durability over a given year.
  - If a failure occurs, EFS automatically shifts traffic to healthy AZs, ensuring continuous availability.

- **Performance**:
  - Offers two performance modes: 
    - **General Purpose**: Suited for most file systems, balancing latency and throughput.
    - **Max I/O**: Optimized for parallel access patterns, suitable for big data and analytics workloads.
  - Provides the option for provisioned throughput to match specific performance needs, guaranteeing a set level of throughput regardless of the amount of data stored.
  - Infrequent access storage class helps reduce storage costs for older data that's accessed less often.

### Security

- **Access Control**:
  - Integrates with AWS Identity and Access Management (IAM) for access control.
  - Supports POSIX permissions and user and group IDs.

- **Encryption**:
  - Supports encryption at rest using AWS Key Management Service (KMS) keys.
  - Allows encryption in transit using Transport Layer Security (TLS).

- **VPC Integration**:
  - Can be accessed within an Amazon Virtual Private Cloud (VPC) for secure and isolated access.

### Use Cases

- Content repositories and CMS.
- Development environments including build, staging, and production.
- Data analytics applications with shared data sets.
- Home directories for enterprise applications.
- Backup and archival solutions.

## Amazon FSx

**Amazon FSx** provides fully managed third-party file systems optimized for a variety of specific use-cases and integrated with other AWS services. These file systems can easily be used with both AWS Cloud resources and on-premises environments.

### Amazon FSx for Windows File Server

Designed for Windows-based applications requiring shared file storage, it's built on Windows Server and offers native support for Windows file system features.

- **Compatibility**:
  - Supports industry-standard SMB (Server Message Block) protocol, suitable for Windows-based applications.
  - Integrates with Active Directory (AD) allowing users to access the file systems using their domain credentials.
  - Features DFS (Distributed File System) namespaces, a role service in Windows Server that enables grouping shared folders on different servers.

- **Durability & Availability**:
  - Data is automatically backed up daily and is stored durably across multiple Availability Zones.
  - Supports Microsoft Volume Shadow Copy Service (VSS) enabling users to restore previous versions of files.

- **Performance & Storage**:
  - Supports SSD and HDD storage for fast access times and lower-cost options.
  - Uses data deduplication to identify and remove duplicated data blocks, optimizing storage usage and cost.
  - Allows concurrent access from thousands of compute instances without performance degradation.

### Amazon FSx for Lustre

Optimized for high-performance and compute-intensive tasks, Lustre is an open-source, parallel file system designed for applications like machine learning, high performance computing (HPC), and video processing.

- **Compatibility**:
  - Provides a POSIX-compliant file system, making it suitable for Linux-based applications.
  - Seamlessly integrates with Amazon S3, allowing users to associate a Lustre file system with an S3 bucket. This enables data to be ingested from or written back to S3 seamlessly.

- **Performance**:
  - Designed for rapid I/O operations with SSD-based storage ensuring low-latency data access.
  - Can scale to hundreds of GB/s of throughput and millions of IOPS.

- **Durability & Data Processing**:
  - Data is stored across multiple Availability Zones for high durability.
  - Supports high-speed data processing tasks by allowing users to process data directly on FSx for Lustre, and then save processed results back into S3.

### Use Cases

- **FSx for Windows File Server**:
  - Enterprise IT applications.
  - Home directories for users.
  - Content management and rich media workflows.

- **FSx for Lustre**:
  - High-performance computing (HPC) applications.
  - Machine learning and deep learning workloads.
  - Financial simulations and reservoir simulations.

## AWS Backup

**AWS Backup** offers a unified, centralized solution for backing up data across AWS services in both the cloud and on-premises environments. It simplifies the process of backup management and enables organizations to meet their business and regulatory backup compliance requirements.

### Key Features

- **Automation**:
  - **Backup Plans**: Create data protection policies known as backup plans that can be applied to AWS resources.
  - **Backup Selection**: Define what data to back up by assigning resources directly or using tags to include or exclude resources.
  - **Scheduled Backups**: Set backups to be taken on a daily, weekly, or monthly basis, ensuring data is protected at regular intervals.

- **Monitoring & Auditing**:
  - **Dashboard**: Provides a centralized view of backup activity, allowing users to quickly understand their backup and restore status.
  - **Events & Metrics**: Monitor backup and restore events using Amazon CloudWatch metrics.
  - **Audit and Compliance**: Log backup activity with AWS CloudTrail to audit backup and restore operations.

- **Lifecycle Management**:
  - **Transition to Cold Storage**: Automatically transition backups to a colder storage tier, such as Amazon Glacier, to save costs.
  - **Retention Management**: Define how long backups should be retained, from days to years, based on business and compliance needs.
  - **Automated Deletion**: Set rules to automatically delete outdated backups, reducing management overhead and cost.

- **Flexibility & Integration**:
  - **Cross-Region Backup**: Copy backups across AWS regions to ensure data durability and availability.
  - **Support for Multiple Services**: Integrated with services like Amazon EBS, Amazon RDS, Amazon DynamoDB, Amazon EFS, and AWS Storage Gateway.
  - **Hybrid Environments**: Use AWS Backup with AWS Storage Gateway to back up on-premises data, providing a unified backup solution.

- **Security**:
  - **Encryption**: Backups are encrypted at rest and in transit, ensuring data is protected against unauthorized access.
  - **Access Control**: Use AWS Identity and Access Management (IAM) to define who can perform backup and restore operations.

### Use Cases

- **Disaster Recovery**: Quickly restore data in the event of outages or unexpected data corruption.
- **Data Archiving**: Store backups for long-term retention in compliance with industry regulations.
- **Migration**: Use backups to move data between AWS accounts or regions.
- **Operational Tasks**: Restore data to a specific point in time, aiding in tasks like testing or data analysis.



## AWS Elastic Disaster Recovery

Previously known as **CloudEndure Disaster Recovery**, **AWS Elastic Disaster Recovery** provides organizations with a robust and cost-effective solution for business continuity. It ensures that mission-critical workloads remain accessible and operational following IT disruptions such as hardware failures, human errors, ransomware attacks, and natural disasters.

### Key Features

- **Continuous Data Replication**:
  - **Block-Level Replication**: By replicating data at the block level, Elastic Disaster Recovery ensures an up-to-date copy of your source disks in the target AWS Region.
  - **Low Latency**: Replicates changes with minimal lag time ensuring almost real-time data mirroring.
  - **Consistency**: Ensures that applications remain in a consistent state during replication, making them fully operational after recovery.

- **Fast Recovery**:
  - **Sub-Second RPO**: Ensures data integrity with a recovery point objective (RPO) of seconds.
  - **Rapid RTO**: Enables recovery time objectives (RTO) of minutes, ensuring swift recovery post-disruption.
  - **Automation**: Utilizes fully automated machine conversion and orchestration to eliminate manual processes during recovery.

- **Cost-effective**:
  - **Eliminate Secondary DR Site**: Removes the need for dedicated disaster recovery data centers, resulting in significant cost savings.
  - **Pay-As-You-Go**: No need for upfront investments; pay only for what you use, which further optimizes costs.
  - **Storage Flexibility**: Utilize low-cost storage options like Amazon S3 for storing replicated data, thereby optimizing costs.

- **Security and Compliance**:
  - **Encryption**: All replicated data, both at rest and in transit, is encrypted, ensuring data security.
  - **Isolation**: Recovery environments are isolated from source environments, ensuring a separation of concerns.
  - **Audit Trails**: Integrate with AWS CloudTrail to provide a history of API calls for security analysis, resource change tracking, and compliance auditing.

### Use Cases

- **Business Continuity**: Ensure business operations continue even in the face of IT disruptions.
- **Ransomware Mitigation**: Recover quickly from ransomware attacks by restoring from a clean, uncompromised backup.
- **Data Center Outages**: Maintain operations during unplanned data center outages or planned maintenance.
- **Migration and Testing**: Use replicated data for workload migration or testing without impacting production environments.



In summation, AWS's suite of storage services offers holistic solutions tailored for a myriad of storage and backup needs, ensuring data integrity and availability for diverse workloads.





[HOME](./README.md)