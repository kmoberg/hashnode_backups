## AWS Can Be Confusing: Where should I run my crap?

AWS has over 180 different services with a myriad of different names and it can be incredibly hard to figure out where you should run your applications. In this post, my goal is to make it a bit easier for you to get started with AWS, and know what services you should consider researching moving forward.

## Basic Services
Well start with a quick introduction of some of AWS most popular and well known services, just to get a brief understanding on what services we are going to be talking about later:

- [Amazon EC2](https://aws.amazon.com/ec2/ "Amazon EC2") - The backbone and arguably one of AWS most famous services. EC2 is AWS Virtual Machines. You select how much CPU, RAM and disk space you need, then what operating system to run. You can pick from a myriad of Linux distributions, Windows Server and Desktop and even macOS (special rates and restrictions apply). You’re billed by the second you have the virtual machine running.
- [Simple Storage Service (S3)](https://aws.amazon.com/s3/) - Amazons unlimited object storage, making it easy to store files for access by other AWS services or serving them to the internet (although you might want to put a cache such as Amazon CloudFront in front if you chose this last service).
- [Amazon Elastic Cloud Service (ECS)](https://aws.amazon.com/ecs/ "Amazon ECS") - Have you containerized your application and need somewhere to run them, but don’t want to deal with the complexity of Kubernetes? ECS is for you. Amazons ECS service is a fully managed container orchestration service making it easier for you by abstracting away most of the complexity that comes with container orchestration.
- [Amazon Elastic Kubernetes Service (EKS)](https://aws.amazon.com/eks/ "Amazon EKS") - A managed container service to run and scale Kubernetes applications in the cloud **or on-premises** with EKS anywhere!
- [AWS App Runner](https://aws.amazon.com/apprunner/ "AWS App Runner") - Just want to run a stupid simple container, and not have to worry about it? Try out App Runner. It connects directly to a code repository, or to a container registry then builds the application on the fly for you. Whenever you push changes, App Runner reacts, rebuilds and republish the application. 
- [Amazon Relational Database Service (RDS)](https://aws.amazon.com/rds/ "Amazon RDS") - Databases are a mess to maintain on your own, so why do it yourself when Amazon can take care of it for you? Pick a database engine, MySQL, PostgreSQL, Oracle or even SQL Server, select how much CPU, memory and how you want to store the data, and Amazon takes care of the rest for you.
- [AWS Lambda](https://aws.amazon.com/lambda/ "AWS Lambda") - Serverless computing! Lambda is a serverless, event-driven compute service that lets you run code for virtually any type of application or backend service without provisioning or managing servers. At all. You can trigger Lambda functions from most AWS Services, or your own code. 
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/ "AWS CloudWatch") - Collect, access, and correlate data on a single platform from across all your AWS resources, applications, and services. 


## Flow Diagram
For a quick and dirty suggestion to where you can run your application, here is a quick flow diagram:




![Flow Diagram](https://cdn.hashnode.com/res/hashnode/image/upload/v1652694922583/a_ffp1aSD.png)



## What are you trying to run?
With the services primer in place, the question becomes "What are you actually trying to run?" and "how do you want to run it"?

- If you’re migrating a work load directly from an on-premise virtual machine, without the ability to containerize or refactor the application, [Amazon EC2](https://aws.amazon.com/ec2/ "Amazon EC2") is probably the right choice for you. You pick the number of CPU cores and how much memory you need, and you can use [Amazon Application Migration Service (AWS MGN)](https://aws.amazon.com/application-migration-service/) to automate the migration for you!
- Got a brand new application you’re building, with limited dependencies? Consider going a brand new direction, where you don’t have to worry about servers, or infrastructure. Serverless compute, using services such as [AWS Lambda](https://aws.amazon.com/lambda/ "AWS Lambda") and [Amazon API Gateway](https://aws.amazon.com/api-gateway/ "Amazon API Gateway") lets you build applications and run them only when you need them, and only pay for when the functions are executed - and the cost is dirt cheap. Fractions of what it would cost to run code in any other service. I recommend checking out how a company such as “A Cloud Guru” [runs their entire video training platform on AWS Lambda and Serverless](https://siliconangle.com/2017/08/15/a-cloud-guru-uses-lambda-and-api-gateway-to-build-serverless-company-awssummit/). This architecture requires you to rethink how you’re building your application, but it’s not very complicated, and you can save a significant amount of energy and money.

### Containers

![Containers Header](https://cdn.hashnode.com/res/hashnode/image/upload/v1652694924611/-Zeq0IXFO.png)

- When you have containers to run, you have multiple choices depending on how much control you want over the the orchestration of the containers themselves. 
	- If you just have a simple container, with minimal dependencies, [AWS App Runner](https://aws.amazon.com/apprunner/ "AWS App Runner") is a great way to run your container. 
	- Alternatively if you do not expect to get much traffic to the application, [Amazon Lightsail](https://aws.amazon.com/lightsail/ "Amazon Lightsail") is a dirt cheap way to run containers too, just don’t expect too much integration with other AWS Services.
	- Want container orchestration, with automatic scaling out and in, using load balanced solutions, but don’t want to maintain it? [Amazon Elastic Container Service (Amazon ECS)](https://aws.amazon.com/ecs/ "Amazon Elastic Container Service (Amazon ECS)") on [Fargate](https://aws.amazon.com/fargate/ "AWS Fargate") is perfect! Running on [Fargate](https://aws.amazon.com/fargate/ "AWS Fargate") you have no servers to maintain or have to worry about provisioning capacity, AWS takes care of it all for you, including scaling, load balancing, and maintaining the control plane. It’s simple to configure, and integrates very well with other tools such as [CodePipeline](https://aws.amazon.com/codepipeline/ "AWS CodePipeline"), [CodeBuild](https://aws.amazon.com/codebuild/ "AWS CodeBuild") and [CodeCommit](https://aws.amazon.com/codecommit/ "AWS CodeCommit").
	- [Kubernetes](https://kubernetes.io "Kubernetes") is an amazing technology allowing for incredible scaling and expandability thanks to its open source nature, but it can be complicated to set up, and especially to maintain in the long run. [Amazon EKS](https://aws.amazon.com/eks "Amazon EKS") works to solve a lot of the complicated parts of running a Kubernetes cluster by delivering a managed control plane, across multiple data centers for high availability and taking care of availability and scaling, as well as automatically detecting and replacing unhealthy control plane nodes. EKS gives you the flexibility of Kubernetes, without necessarily requiring an entire infrastructure team to manage your cluster. It also makes it much easier to integrate and authenticate with other AWS services.

### Databases

![Databases Header](https://cdn.hashnode.com/res/hashnode/image/upload/v1652694926411/gYPJ1zSte.png)

- In most cases, you not only need a compute service, you also need somewhere to store your data. Amazon provides multiple database services depending on your needs:
	- After having spent a number of years working with databases in AWS, I cannot emphasize enough how much I recommend [Amazon Aurora](https://aws.amazon.com/rds/aurora/ "Amazon Aurora") if you’re running MySQL or PostgreSQL in production. Amazon Aurora takes the concept of a managed database to the next level, and automates replication across multiple availability zones, or regions, distributed storage, and has incredible performance. No longer do you have to worry about scaling out, or increasing database storage - Aurora takes care of it all. For production, we’d go for Aurora in 10/10 cases.
	- For smaller projects, development, or if you need OracleDB, MSSQL or even some custom databases, [Amazon RDS](https://aws.amazon.com/rds/ "Amazon RDS") is a managed database service, abstracting away the need to maintain the database server itself, and making it incredibly easy to maintain a database. You still need to provision capacity and monitor it, but it is still an amazing service in order to avoid having to maintain a database server.
	- The last half a decade has also seen the meteoric rise of NoSQL databases. AWS offers a fantastic managed, Key-Value NoSQL database service known as [DynamoDB](https://aws.amazon.com/dynamodb/ "DynamoDB"). It features single-digit millisecond performance with nearly unlimited throughput **and** storage. It has encrypted data at rest, backup and restore and automatic multi-region replication. The storage is cheap, and is well worth a shot for projects that work well in NoSQL databases.
	- Another good alternative for NoSQL workloads is [Amazon DocumentDB](https://aws.amazon.com/documentdb/ "Amazon DocumentBD") with MongoDB compatibility. Built upon Amazon Aurora, and supporting MongoDB 3.6 and 4.0 APIs, DocumentDB allow you to manage your database in JSON with incredible performance and AWS tooling support.

On top of all the traditional database types, AWS also has a number of other databases such as Amazon ElastiCache with support for Redis and Memcached, graph databases with Amazon Neptune, data warehouses with AWS Redshift and more. All of these are well documented and often require some special use case, so I’m not spending much time on them.

## Thoughts about Vendor Lock-in
![Vendor lock-in Head](https://cdn.hashnode.com/res/hashnode/image/upload/v1652694928368/5r0cBuWF4.png)

A lot of these services mentioned in this post are Amazon proprietary software, and a question we get _a lot_ when working with cloud, is customers being worried about being locked into a vendor and not being able to move to a different cloud vendor at a later point if needed. 

This is very much a valid concern that the business needs to consider when building their cloud infrastructure, and I’ll provide a few observations from my years working with all three major cloud vendors. 

- As long as you’re working with a cloud vendor, you will always have a lot of features that you are required to use, that are cloud proprietary. Examples of this include IAM and account provisioning, VPC design, database design (unless you run your own database as a VM - and if you do that: why are you in the cloud, and not just in a datacenter…) (also note, this does not include data!) and a lot more. 
- Making sure you’re declaring **all** of your cloud infrastructure in a cloud agnostic IaC language will mitigate a lot of these issues.
- Your **data** is almost never locked in, but how you manage that data might be to some degree or another. However: no matter what cloud you use, and what service you use in that cloud, migrating that data OUT of any cloud vendor, will be **insanely expensive** if you have more than a few TB of data. We’re talking tens if not hundreds of thousands of dollars in data egress cost depending on how much data you got. Most cloud vendors, including AWS, have migration tools you can use, to very easily migrate data into their service, meaning your data is safe. There are some caveats: AWS Lambda isn’t directly transferrable to Azure Cloud Functions without a rather large refactor. Moving from Google Kubernetes Engine to Amazon EKS will require you to refactor how your Kubernetes cluster integrates with other services, but migrating from an Azure managed MySQL database to a Google managed MySQL database, is not complicated - at all. 
- Very, VERY few companies ever migrate to another cloud vendor. I’ve seen companies build their infrastructure, avoiding the use of any cloud vendor native solution, but instead managing it themselves, to be cloud agnostic, yet never ever actually investigate migrating their infrastructure. Instead, they are paying many, many times more for their infrastructure than they need to. Managed infrastructure is often cheaper, and is absolutely cheaper when you start counting the amount of hours of maintenance they require.
- Having a **plan** for what you need to do **if** you wish to migrate, is **extremely important**. It’s a plan B, incase AWS goes under, or Azure decides they no longer want you on their platform. Having spent a few hours thinking through, and writing down a sketch of what you need to do, in case you need to migrate, is extremely helpful. Additionally, writing down the reasons **why** you picked your cloud provider in the first place, can also help ease the doubts you might have later on, and reduce the stress of “what if we want to switch” years down the road. 

For a vast majority of companies, a migration will be a costly job no matter how you design your infrastructure, including just using non-propriatorey solutions, so for most, it is much easier just to use the services you need to, in the first place and deal with it, if it ever becomes a problem. Trust me, your engineers will be much happier.

## Conclusion
Amazon Web Services consist of a vast web of interconnected services, and with over 200 different services with confusing sounding names, it can be a very complicated and confusing area to get into. Starting with the basic services mentioned in this post, can be a great starter for a lot of users that are just getting into cloud computing. As with most AWS services, all the services listed here integrate very well with the rest of AWS and allow you to keep expanding on and further build your infrastructure. 

Additionally, if you want to try out most of these services (EKS not included), AWS has a very [generous free-tier](https://aws.amazon.com/free/ "AWS Free Tier") allowing you to try out most services for free, without paying anything. 

If you have recently started using AWS and want to know where to go from here, I highly recommend looking into the study materials for some of the AWS certifications. You don’t need to take the certifications if you don’t want to, but the materials for certifications such as the [AWS Certified Developer - Associate](https://aws.amazon.com/certification/certified-developer-associate/ "AWS Certified Developer - Associate") give you a great introduction to a vast number of services in a short amount of time.

And if you're ever in need of help picking a service, or have questions about how you should run your crap - feel free to reach out to me!