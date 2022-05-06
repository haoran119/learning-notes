# 学习笔记之Cloud Computing

* [Cloud computing - Wikipedia](https://en.wikipedia.org/wiki/Cloud_computing)
* [Cloud computing - 随笔分类 - 浩然119 - 博客园](https://www.cnblogs.com/pegasus923/category/1186049.html)
* [learning-notes/学习笔记之AWS(Amazon Web Services) at main · haoran119/learning-notes](https://github.com/haoran119/learning-notes/tree/main/%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E4%B9%8BAWS(Amazon%20Web%20Services))
* [learning-notes/学习笔记之Docker at main · haoran119/learning-notes](https://github.com/haoran119/learning-notes/tree/main/%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E4%B9%8BDocker)
* [learning-notes/学习笔记之Kubernetes at main · haoran119/learning-notes](https://www.cnblogs.com/pegasus923/p/8656046.html)

## RESOURCES

* [漫画：什么是公有云、私有云和混合云？](https://mp.weixin.qq.com/s/teupOz1wPeADRJY6G_Rqdw)
* [虚拟化技术发展编年史](https://mp.weixin.qq.com/s/wuQ8-pwqb9qXfOt4w3Zviw)
  * https://blog.csdn.net/Jmilk/article/details/99675664
  * https://www.ibm.com/developerworks/cn/linux/l-cn-vt/index.html
* [全面讲解OpenStack技术知识](https://mp.weixin.qq.com/s/toUgYy609GhzBJXrTKiM5g)
* [Spark面试题](https://mp.weixin.qq.com/s/Z9JpqTUKfcqddffDUbXtuw)

## [AWS](https://aws.amazon.com/?nc2=h_lg)

* Amazon Web Services (AWS) - Cloud Computing Services
* [Amazon Web Services - Wikipedia](https://en.wikipedia.org/wiki/Amazon_Web_Services)
  * Amazon Web Services (AWS) is a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments, on a metered pay-as-you-go basis. These cloud computing web services provide a variety of basic abstract technical infrastructure and distributed computing building blocks and tools. One of these services is Amazon Elastic Compute Cloud (EC2), which allows users to have at their disposal a virtual cluster of computers, available all the time, through the Internet. AWS's version of virtual computers emulates most of the attributes of a real computer, including hardware central processing units (CPUs) and graphics processing units (GPUs) for processing; local/RAM memory; hard-disk/SSD storage; a choice of operating systems; networking; and pre-loaded application software such as web servers, databases, and customer relationship management (CRM).
  * The AWS technology is implemented at server farms throughout the world, and maintained by the Amazon subsidiary. Fees are based on a combination of usage (known as a "Pay-as-you-go" model), hardware, operating system, software, or networking features chosen by the subscriber required availability, redundancy, security, and service options. Subscribers can pay for a single virtual AWS computer, a dedicated physical computer, or clusters of either. As part of the subscription agreement,[10] Amazon provides security for subscribers' systems. AWS operates from many global geographical regions including 6 in North America.[11]
  * Amazon markets AWS to subscribers as a way of obtaining large scale computing capacity more quickly and cheaply than building an actual physical server farm.[12] All services are billed based on usage, but each service measures usage in varying ways. As of 2017, AWS owns a dominant 33% of all cloud (IaaS, PaaS) while the next two competitors Microsoft Azure and Google Cloud have 18%, and 9% respectively, according to Synergy Group.[13][14]

### [Amazon Aurora](https://aws.amazon.com/rds/aurora/?nc1=h_ls)

* Fully MySQL and PostgreSQL Compatible Managed Database Service | Amazon Aurora | AWS
* Designed for unparalleled high performance and availability at global scale with full MySQL and PostgreSQL compatibility
* [What is Amazon Aurora? - Amazon Aurora](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)
  * Amazon Aurora (Aurora) is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. You already know how MySQL and PostgreSQL combine the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases. The code, tools, and applications you use today with your existing MySQL and PostgreSQL databases can be used with Aurora. With some workloads, Aurora can deliver up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications.
  * Aurora includes a high-performance storage subsystem. Its MySQL- and PostgreSQL-compatible database engines are customized to take advantage of that fast distributed storage. The underlying storage grows automatically as needed. An Aurora cluster volume can grow to a maximum size of 128 tebibytes (TiB). Aurora also automates and standardizes database clustering and replication, which are typically among the most challenging aspects of database configuration and administration.
  * Aurora is part of the managed database service Amazon Relational Database Service (Amazon RDS). Amazon RDS is a web service that makes it easier to set up, operate, and scale a relational database in the cloud. If you are not already familiar with Amazon RDS, see the [Amazon Relational Database Service User Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html).

### [Amazon DocumentDB](https://aws.amazon.com/documentdb/)

* (with MongoDB compatibility)
* Scale JSON workloads with ease using a fully managed document database service
* [What Is Amazon DocumentDB (with MongoDB Compatibility) - Amazon DocumentDB](https://docs.aws.amazon.com/documentdb/latest/developerguide/what-is.html)
  * Amazon DocumentDB (with MongoDB compatibility) is a fast, reliable, and fully managed database service. Amazon DocumentDB makes it easy to set up, operate, and scale MongoDB-compatible databases in the cloud. With Amazon DocumentDB, you can run the same application code and use the same drivers and tools that you use with MongoDB.
  * Before using Amazon DocumentDB, you should review the concepts and features described in How It Works. After that, complete the steps in Get Started Guide.
* [Amazon DocumentDB - Wikipedia](https://en.wikipedia.org/wiki/Amazon_DocumentDB)
  * Amazon DocumentDB is a fully managed proprietary NoSQL database service that supports document data structures and MongoDB workloads. As a document database, Amazon DocumentDB makes it easy to store, query, and index JSON data. Amazon DocumentDB is currently available in 14 AWS regions of AWS.[2][3]

### [Amazon ECS](https://aws.amazon.com/ecs/?nc1=h_ls)

* Fully Managed Container Solution – Amazon Elastic Container Service (Amazon ECS) - Amazon Web Services
* Run highly secure, reliable, and scalable containers
* Launch thousands of containers across the cloud using your preferred continuous integration and delivery (CI/CD) and automation tools.
* Optimize your time with AWS Fargate serverless compute for containers, which eliminates the need to configure and manage control plane, nodes, and instances.
* Save up to 50 percent on compute costs with autonomous provisioning, auto-scaling, and pay-as-you-go pricing.
* Integrate seamlessly with AWS management and governance solutions, standardized for compliance with virtually every regulatory agency around the globe.
* How it works
  * Amazon ECS is a fully managed container orchestration service that makes it easy for you to deploy, manage, and scale containerized applications.
* Introduction to Amazon ECS
  * Amazon ECS is a fully managed container orchestration service that helps you easily deploy, manage, and scale containerized applications. It deeply integrates with the rest of the AWS platform to provide a secure and easy-to-use solution for running container workloads in the cloud and now on your infrastructure with Amazon ECS Anywhere.
* Use cases
  * Deploy in a hybrid environment
    * Build container-based applications on-premises or in the cloud with Amazon ECS Anywhere and enjoy consistent tooling, management, workload scheduling, and monitoring across environments.
  * Support batch processing
    * Plan, schedule, and execute batch computing workloads across the full range of AWS services, including Amazon Elastic Compute Cloud (EC2), Fargate, and Amazon EC2 Spot Instances.
  * Scale web applications
    * Automatically scale and run web applications in multiple Availability Zones with the performance, scale, reliability, and availability of AWS.
* [Gentle Introduction to How AWS ECS Works with Example Tutorial | by Tung Nguyen | BoltOps | Medium](https://medium.com/boltops/gentle-introduction-to-how-aws-ecs-works-with-example-tutorial-cea3d27ce63d) 
  * Tutorial Example
    * In this tutorial example I will create a small Sinatra web service that prints the meaning of life: 42.
      * Create ECS Cluster with 1 Container Instance
      * Create a Task Definition
      * Create an ELB and Target Group to later associate with the ECS Service
      * Create a Service that runs the Task Definition
      * Confirm Everything is Working
      * Scale Up the Service to 4 Tasks.
      * Clean It All Up

### [Amazon FSx](https://aws.amazon.com/fsx/)

* Amazon FSx | Feature-Rich & Highly-Performant File Systems | Amazon Web Services
* Launch, run, and scale feature-rich and highly-performant file systems with just a few clicks
* Amazon FSx makes it easy and cost effective to launch, run, and scale feature-rich, high-performance file systems in the cloud. It supports a wide range of workloads with its reliability, security, scalability, and broad set of capabilities. Amazon FSx is built on the latest AWS compute, networking, and disk technologies to provide high performance and lower TCO. And as a fully managed service, it handles hardware provisioning, patching, and backups -- freeing you up to focus on your applications, your end users, and your business.
* You choose the file system that powers your Amazon FSx file storage, with full access to each file system's feature sets, performance profiles, and data management capabilities. You can choose between three widely-used file systems: NetApp ONTAP, Windows File Server, and Lustre.
* [Getting Started – Amazon FSx for Windows File Server – AWS](https://aws.amazon.com/cn/fsx/windows/getting-started/)
  * [Introduction to Amazon FSx for Windows File Server](https://www.youtube.com/watch?v=7ThyV2IP27A)

### [AWS Lambda](https://aws.amazon.com/lambda/)

* Serverless Computing - AWS Lambda - Amazon Web Services
* Run code without thinking about servers or clusters
* AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code as a ZIP file or container image, and Lambda automatically and precisely allocates compute execution power and runs your code based on the incoming request or event, for any scale of traffic. You can set up your code to automatically trigger from over 200 AWS services and SaaS applications or call it directly from any web or mobile app. You can write Lambda functions in your favorite language (Node.js, Python, Go, Java, and more) and use both serverless and container tools, such as AWS SAM or Docker CLI, to build, test, and deploy your functions.
* [AWS Lambda – Getting Started](https://aws.amazon.com/lambda/getting-started/)
  * Here you will find tutorials and documentation on how to get started building serverless applications with AWS Lambda. You will also learn about Serverless Application Developer Tools like the AWS Serverless Application Model (SAM) or AWS Cloud9.
  * Another easy way to get started is with the AWS Serverless Application Repository, which enables you to quickly deploy pre-built applications.
  * To dive deeper into specific use cases, you will find resources for web app development, data processing, mobile backend development, and edge computing.
* [AWS Lambda - Wikipedia](https://en.wikipedia.org/wiki/AWS_Lambda)
  * AWS Lambda is an event-driven, serverless computing platform provided by Amazon as a part of Amazon Web Services. It is a computing service that runs code in response to events and automatically manages the computing resources required by that code. It was introduced in November 2014.[1]
  * Node.js, Python, Java, Go,[2] Ruby,[3] and C# (through .NET) are all officially supported as of 2018. In late 2018, custom runtime support[4] was added to AWS Lambda.
  * AWS Lambda supports running native Linux executables via calling out from a supported runtime such as Node.js.[5] For example, Haskell code can be run on Lambda.[6]
  * AWS Lambda was designed for use cases such as image or object uploads to Amazon S3, updates to DynamoDB tables, responding to website clicks, or reacting to sensor readings from an IoT connected device. AWS Lambda can also be used to automatically provision back-end services triggered by custom HTTP requests, and "spin down" such services when not in use, to save resources. These custom HTTP requests are configured in AWS API Gateway, which can also handle authentication and authorization in conjunction with AWS Cognito.
  * Unlike Amazon EC2, which is priced by the hour but metered by the second, AWS Lambda is metered by rounding up to the nearest millisecond with no minimum execution time.
  * In 2019, at AWS' annual cloud computing conference (AWS re:Invent), the AWS Lambda team announced "Provisioned Concurrency", a feature that "keeps functions initialized and hyper-ready to respond in double-digit milliseconds."[7] The Lambda team described Provisioned Concurrency as "ideal for implementing interactive services, such as web and mobile backends, latency-sensitive microservices, or synchronous APIs."[8]

### Resources

* [还不知道 AWS 是什么？这 11 个重点带你认识 AWS ！ (qq.com)](https://mp.weixin.qq.com/s/E7nkDxM3KbnXhqto0ZbkyQ)
  * [A Sneak Peek Into Amazon Web Services Cloud (AWS) - DZone Cloud](https://dzone.com/articles/a-sneak-peek-into-amazon-web-services-cloud-aws)
* [AWS Cheat Sheet - Amazon Web Services Quick Guide [2022]](https://intellipaat.com/blog/tutorial/amazon-web-services-aws-tutorial/aws-cheat-sheet/)
* [Exploring the Basics of AWS: AWS Cheat Sheet - Whizlabs Blog](https://www.whizlabs.com/blog/aws-cheat-sheet/#:~:text=%20AWS%20Cheat%20Sheet%20%201%20Definition%20of,is%20the%20AWS%20regions.%20These%20entries...%20More%20)
