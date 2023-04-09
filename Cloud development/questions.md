### What is cloud development?
It's a process of building and deploying software applications that run on cloud-based infrastructure, rather than on local servers or personal computers. This involves using cloud computing platforms, such as Amazon Web Services (AWS), Microsoft Azure, or Google Cloud Platform (GCP), to develop, test, and deploy applications.

### Pros and cons of cloud development?
Pros:
1. Scalability: Cloud infrastructure allows developers to easily scale up or down their resources as needed, which can be especially useful for applications that experience spikes in traffic.
2. Cost savings: Cloud infrastructure eliminates the need for companies to invest in and maintain their own physical servers, which can lead to cost savings.
3. Accessibility: Cloud-based tools and resources can be accessed from anywhere with an internet connection, which can increase collaboration and productivity.
4. Security: Cloud providers often have more resources and expertise to devote to security than individual companies, which can lead to improved security.
5. Flexibility: Cloud development allows developers to use a variety of programming languages, tools, and frameworks, which can increase flexibility and innovation.

Cons:
1. Dependence on third-party providers: Companies that rely on cloud providers for their infrastructure are dependent on the reliability and security of those providers.
2. Potential downtime: Cloud infrastructure can experience downtime, which can lead to decreased productivity and lost revenue.
3. Limited control: Companies may have limited control over their infrastructure and may be subject to the policies and limitations of their cloud provider.
4. Data security concerns: Storing data on cloud servers can raise concerns about privacy and data security.
5. Complexity: Cloud development can be more complex than traditional development, requiring specialized knowledge and skills.

### Pros and cons of on premise development?
Pros:
1. Control: Companies have full control over their infrastructure, including security, resources, and software upgrades.
2. Security: With on-premise development, companies have complete control over their security measures, which can be customized and tailored to their specific needs.
3. Compliance: Companies that operate in highly regulated industries may find it easier to maintain compliance with on-premise development, as they have more control over their infrastructure and can more easily demonstrate their compliance.
4. Reliability: On-premise development can be more reliable than cloud-based solutions, as it is not dependent on third-party providers or internet connectivity.
5. Customization: Companies can customize their infrastructure and development environments to their specific needs, without having to rely on preconfigured cloud solutions.

Cons:
1. Cost: On-premise development can be more expensive than cloud-based solutions, as companies must purchase and maintain their own hardware and software infrastructure.
2. Scalability: Companies may face limitations in scaling their infrastructure with on-premise development, as it may be difficult to quickly acquire and set up new servers and hardware.
3. Accessibility: On-premise development can be less accessible than cloud-based solutions, as it requires physical access to servers and hardware.
4. Time-consuming: On-premise development can be time-consuming, as it requires a significant amount of setup and maintenance.
5. Limited collaboration: On-premise development may limit collaboration among teams, as development environments may not be easily accessible to all team members.

### What does serverless development mean?
Serverless development is a cloud computing model in which the cloud provider manages the infrastructure required to run an application, including the servers and operating systems, and customers only pay for the time their code runs.

### What are some important factors to consider when choosing a cloud provider?
* Pricing
* Reliability
* Security
* Scalability
* Ease of use
...

### What are some common cloud computing use cases?
* Website hosting.
* Data storage and backup.
* Application development and testing.
* Big data processing.
* Machine learning.
...

### The most popular services using in cloud?
1. Databases
2. Virtual machines
3. Queues
4. Lambdas
5. Logging / monitoring
6. CI/CD
7. API Gateway / Global distribution / CDN
...

### What primary categories of cloud computing services exist?
1. Infrastructure as a Service (IaaS): This is the most basic level of cloud computing service provided by AWS. It involves renting out virtualized computing resources, such as servers, storage, and networking, to customers who can then deploy and manage their own operating systems, applications, and other software on top of the infrastructure. Examples of AWS IaaS offerings include Amazon Elastic Compute Cloud (EC2), Amazon Simple Storage Service (S3), and Amazon Elastic Block Store (EBS).

2. Platform as a Service (PaaS): This level of cloud computing service builds upon the infrastructure provided by IaaS and offers a more complete development and deployment environment for software applications. With PaaS, customers can focus on building and deploying their applications without having to worry about managing the underlying infrastructure. Examples of AWS PaaS offerings include AWS Elastic Beanstalk, AWS Lambda, and AWS Elastic Container Service (ECS).

3. Software as a Service (SaaS): This is the highest level of cloud computing service provided by AWS, and involves delivering software applications over the internet as a fully managed service. With SaaS, customers can access and use software applications without having to install or maintain any software on their own devices. Examples of AWS SaaS offerings include Amazon WorkSpaces, Amazon Chime, and Amazon QuickSight.

### What does infrastructure as a code mean?
Infrastructure as Code (IaC) is a concept allowing to define and manage infrastructure resources through code, using high-level programming languages or configuration files, which can be version controlled, tested, and deployed like any other software code.

### What tools can be used for logging, alerting and monitoring in cloud?
1. AWS CloudWatch / GCP Stackdriver / Azure monitor for collecting logs.
2. AWS X-ray for tracing.
3. Grafana / NewRelic for visualization, real-time monitoring and alerting.
4. Splunk / ELK for searching and analyzing.
5. PagerDuty for notifications.

### Pros and cons of using VPC?
Pros:
1. Enhanced Security: VPC provides a high level of security by allowing users to create isolated networks that are not accessible from the public internet. It also provides features such as network ACLs (access control lists) and security groups to control traffic flow.
2. Customizable Networking: VPC allows users to customize their network configuration, including IP address ranges, subnets, and routing tables, to suit their specific needs.
3. Easy to Scale: VPC can be easily scaled up or down to meet changing business needs. Users can add or remove resources, such as EC2 instances, without affecting other resources in the network.

Cons:
1. Complex Setup: Setting up VPC can be complex, especially for users who are not familiar with networking concepts. Users need to have a good understanding of IP addressing, routing, and network security to create a functional VPC.
2. Requires Maintenance: VPC requires ongoing maintenance to ensure that it is functioning properly. This includes monitoring network traffic, managing security groups, and updating routing tables.
3. Difficult to Troubleshoot: Troubleshooting network issues in VPC can be difficult, especially for users who are not familiar with networking concepts. Users need to have a good understanding of network troubleshooting tools and techniques to resolve issues.

### What does cloud development mean?
Cloud development refers to the practice of developing, deploying, and maintaining applications and services in cloud computing environments, such as Amazon Web Services (AWS), Microsoft Azure, or Google Cloud Platform. Instead of deploying and managing applications on local servers, cloud development allows developers to use remote infrastructure to create and scale applications.

### Cloud
Pros:
* Scalability: the ability to easily and quickly scale up or down resources to meet demand.
* Availability: cloud services are typically designed with high availability and redundancy, ensuring that services remain available even in the event of hardware failures.
* Maintenance: cloud providers typically handle hardware maintenance and software updates, allowing customers to focus on their applications rather than infrastructure.
* Flexibility: cloud solutions offer the ability to quickly spin up and deploy new applications or services, without needing to procure and configure hardware.
* Low initial costs.

Cons:
* Security: there is a risk of data breaches or other security vulnerabilities when using cloud services.
* Cost: while cloud solutions offer flexibility, they can also be more expensive than on-premise solutions in certain situations, particularly for long-term usage.
* In most cases it will be vendor lock-in, migration will be difficult if needed.
* Engineers must have cloud skill set.

### On premise
Pros:
* Full control of the system (even without Internet connection), physical access to it, low latency.
* Full customization based on project's requirements.
* Maybe a good choice if the project owns secret/critical data (government, banks).

Cons:
* High initial investment, underutilized resources are financially wasteful.
* May be difficult to set up complicated functionality such as quantum calculations, speech recognition, etc.
* Necessity to spend time and efforts on scalability, security, licensing, administration, back-ups, etc.

### Hybrid
Pros:
* May be used for storing important but not critical data, such as back-ups; own capacities can be used more efficiently.
* Allows to own the most critical data on premise but delegate some safe part of work to cloud (e.g. add more cloud servers in case if own capacity isn't enough at peak load).

Cons:
* Transferring large amounts of data between cloud and on premise infrastructure can be ineffective.
* Knowledge of engineers working with both approaches should be high.

### What is IAAS?
IaaS stands for Infrastructure as a Service. It is a type of cloud computing service that provides users with virtualized computing resources over the internet. This includes access to servers, storage, networking, and other computing infrastructure components. Examples of popular IaaS providers include Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform.

### What is SAAS?
SaaS stands for "Software as a Service". It is a model of cloud computing where software applications are provided and managed remotely over the internet by third-party providers. In this model, users do not have to install and maintain software on their own devices, but rather access them through a web browser or other interface provided by the service provider. Examples: Firebase, DynamoDB, GitHub enterprise.

### Can you be sure that an on-premise solution will be more reliable than a cloud provider?
It's not possible to say that an on-premise solution will be more reliable than a cloud provider in all cases. Cloud providers have more resources and different availability zones to ensure high reliability, while on-premise solutions require a significant investment to set up the correct infrastructure and network for reliability. However, there may be some specific cases where an on-premise solution is preferred, such as data security concerns or if a cloud provider cannot provide a specific feature or service.

###  Which approach will be less or more expensive, cloud or on-premise?
In general, on-premise solutions require a larger upfront investment in hardware and infrastructure, as well as ongoing maintenance and upgrades. This can make them more expensive in the long run, especially if the organization needs to scale up its operations.

On the other hand, cloud solutions typically have lower upfront costs and are often offered on a subscription-based pricing model, allowing organizations to pay only for the resources they use. This can make cloud solutions more cost-effective for smaller organizations or those with fluctuating demand for resources.

### What are some specific things that cloud providers cannot provide, which may require on-premise solutions?
* Regulatory compliance: Some industries, such as healthcare and finance, are subject to strict regulatory requirements for data privacy and security. In some cases, on-premise solutions may be necessary to meet these regulations.
* Legacy applications: Some businesses may have legacy applications or systems that are not compatible with cloud environments. Migrating these systems to the cloud can be difficult and costly.
* Custom hardware: Certain applications may require specialized hardware that is not available in the cloud. In these cases, an on-premise solution may be necessary to support the hardware.
* Limited internet connectivity: In areas where internet connectivity is limited or unreliable, cloud solutions may not be feasible. In these cases, on-premise solutions may be necessary to ensure reliable access to critical applications and data.
* Large-scale data processing: For organizations that need to process large amounts of data quickly and frequently, an on-premise solution may be more cost-effective than using cloud resources. Cloud providers charge for data egress (transferring data out of their network), which can be expensive for large-scale data processing tasks.

### What does serverless mean?
Serverless stands for computing model where developers write code and set up the entire infrastructure in a configuration file, and the cloud provider builds and manages the infrastructure for them.

Pros:
Faster development.
Testability.

Cons:
Complexity.
Vendor lock-in.
Debugging.

### Difference between IaC and serverless?
IaC is a way to manage infrastructure as code, while serverless is a model of cloud computing where infrastructure management is abstracted away from developers.

### How does networking in the cloud work?
Virtual networks in the cloud can be divided into subnets, which allow for more granular control over traffic flow and access. Access to the virtual network can be controlled through security groups, which act as firewalls, controlling inbound and outbound traffic. Load balancers can also be used to distribute traffic across multiple instances or resources to improve performance and reliability.

Networking in the cloud also involves the use of specialized services and tools, such as content delivery networks (CDNs), domain name system (DNS) management, and elastic IP addresses, to optimize network performance, security, and availability.

### What are the core services that a cloud provider should have?
* Compute: This service provides virtual machines or containers that allow users to run their applications or workloads in the cloud.
* Storage: This service provides various types of storage options such as object storage, block storage, and file storage to store and manage data.
* Networking: This service provides networking capabilities such as virtual networks, load balancers, and firewalls to enable communication between resources in the cloud and with external networks.
* Database: This service provides database solutions such as SQL and NoSQL databases to manage and store data.
* Identity and Access Management (IAM): This service provides authentication and authorization capabilities to control user access and manage permissions for cloud resources.
* Security: This service provides various security solutions such as encryption, threat detection, and compliance to ensure the security of cloud resources.
* Monitoring and Management: This service provides tools to monitor and manage the performance and availability of cloud resources.
