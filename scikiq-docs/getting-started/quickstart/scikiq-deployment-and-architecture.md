---
hidden: true
icon: sitemap
---

# ScikIQ Deployment & Architecture

## Table of Contents <a href="#id-626uhx3f7cxo" id="id-626uhx3f7cxo"></a>

* Overview
* Goals
* Specifications
* Platform Specifications
* Deployment Specifications
* CI/CD Specifications

## Overview <a href="#toc110008099" id="toc110008099"></a>

* ScikIQ is a PaAS-based data analytics platform developed in Python. The product has capabilities to connect with various data sources and generate rich dashboards/reports for platform users.
* ScikIQ is a true no-code Holistic Business Data Platform that helps large and medium-sized enterprises implement Data Strategy and build Data Fabric without worrying about the complexities and intricacies of the underlying Data landscape and technology, thereby, enabling these corporations to make faster, smarter & confident decisions using Data, AI and ML.
* All this magic happens without writing a single line of code. For Businesses, ScikIQ provides a single source of truth where business teams are empowered to slice and dice the data in a way that helps them with better and faster decision-making.
* We define and Implement Data Strategy to create a Client’s Data Platform that acts as a one-stop shop for all data needs across the enterprise. We helped our clients build a next-generation data platform that solves data challenges such as ingestion, preparation, governance, and transformation while delivering insights and analytics on a real-time self-serve basis.

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252Fg9tT6kDtmWKozDzEPJjy%252Fimage.png%3Falt%3Dmedia%26token%3D7edbf37f-3841-4ecb-9343-30b1c0b5b89f\&width=768\&dpr=4\&quality=100\&sign=3c8a9ae6\&sv=1)

#### Technical Architecture <a href="#technical-architecture" id="technical-architecture"></a>

* If your organization is running a _**Digital Transformation program or building a new information-centric revenue stream**_ you need to invest in Data Integration and an overall Data Management Platform that will make accurate and trusted information accessible and available to business teams and corporate functions in a format that is easy to consume and act upon.
* **ScikIQ Connect is a NO Code Data Integration and Data Transformation Platform** that lets our client teams effortlessly centralize all the data & build a single version of truth thereby enabling them to make faster, smarter & confident decisions using data.
* **Using ScikIQ Connect,** Client teams can build and deploy Data Integration and Data Transformation Pipelines without writing a single line of Code. The engine takes care of all the complexities in the background thereby saving time and engineering effort - hence creating bandwidth for the client team to work on actual value-added activities and making sense of the data.
* Having dealt with the pain of Integrating data across organizational silos and boundaries, we have architected the product so that it is easy to use and achieves a reduction in the _DATA-TO-ACTION_ timeframe from years and months to days. We help our clients save a tremendous amount of time by eliminating the need to build, integrate & maintain complex data pipelines.
* _ScikIQ Connect_ is designed to enable the business team to drive value from the data and focus on business growth rather than worrying about how the data needs to be stitched together.

## **ScikIQ Connect is 3 step process**

1. Connect to Data Store – Relational, Columnar, Big Data, API, Application, SAP, Files or Real Time Streaming data using KAFKA
2. Setup pipelines to migrate Historic Data
3. Ingest Daily/real-time data loads through ETL Pipeline or ScikIQ KAFKA Engine

_**ScikIQ Connect**_ is built using proven open-source technologies and uses a modern container-based architecture that effortlessly connects to any data store hosted on a single cloud, multiple clouds, or on a hybrid environment (on-premises + cloud).

It hosts highly scalable, Cloud-agnostic, and interoperable data integration toolsets for designing and developing complex data workloads through NO Code's easy-to-use, visual, drag-and-drop User Interface.

The proposed solution will prescribe to the below high-level business architecture.

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FkOYPDlE7WfQFkENRFqEC%252F2.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=954c5fc2\&sv=1)Graphical user interface, application Description automatically generated

* Integrate all your data with ScikIQ Connect —a fully managed self-served data integration service. Visually integrate data sources with pre-built-in connectors at no added cost. Unlock business insights by migrating data loads from your legacy and on-premises infrastructure to the Cloud or build your real-time analytics using ScikIQ Connect capabilities.
  1. Acquire and migrate legacy data using No Code Interface
  2. Build & deliver new capabilities by acquiring data onto ScikIQ
  3. Get Real-Time Data Changes for real-time analytics

## SCIKIQ Data Platform <a href="#toc82080629" id="toc82080629"></a>

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FHaTuZMOxjTynzgzbxtV6%252Fimage.png%3Falt%3Dmedia%26token%3D515fbb8b-abee-4ca0-9934-6ed3060d9e92\&width=768\&dpr=4\&quality=100\&sign=500e62f7\&sv=1)

* **API Router**
  * ScikIQ Data platform uses Django Router for routing requests from the front-end application to back-end services. The router is also responsible for handling authentication of requests using a token-based authentication framework. The router also supports throttling of requests so that each user’s access to features is limited to keep the overall platform performing at an optimum level
* **API Layer**
  * The ScikIQ Data Platform will provide access to data from the data warehouse via queryable Data APIs. The current version of the platform will support REST APIs and future versions will support GraphQL-based queries. The Data APIs can be consumed by 3rd party reporting systems for data visualization purposes. Functional APIs will be used by the Report Designer & ETL Designer modules. Authorization API deals with providing Role Based Access Control (RBAC) and Row Level Security (RLS) for downstream microservices and data warehouses.

## **ScikIQ Data Engine**

* The ScikIQ Data Engine is composed of 3 major modules
  1. ETL Engine which supports the ETL designer and execution of the ETL pipeline
  2. Query Engine which focuses on continuous metadata capture on queries and automated performance monitoring and optimization
  3. Analytics Engine which focuses on providing data science and analytics capabilities within the platform

## **ODS Layer**

The ODS layer is built on top of the Vertica database which follows a multi-node architecture for scalable performance.

**ScikIQ reporting studio**

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FLoFHTeDHhc3THNNgtbpM%252F4.jpeg%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=33461e1d\&sv=1)Graphical user interface, application Description automatically generated

**Reports & Dashboard Designer**

ScikIQ Studio comes with a WYSIWYG designer module for DIY reports and dashboards. It comes with built-in support for 20+ chart types such as Bar, Pie, Line, Maps, Heatmap, etc. Users can drop and drop the chart types and quickly connect to a dataset to create their own metrics and KPIS.

**Reports & Dashboard Viewer**

Once the reports are published, rights can be assigned to users, user groups and roles to access the reports through the ScikIQ portal. The list of published reports will be made available through an API which can be consumed for setting up the downstream mobile application.

**ETL Designer**

The ETL Designer module allows the users to design their ETL flows using a drag and drop editor. Connect to data sources, setup transformations and load the data into the data warehouse.

**Scheduler**

The Scheduler module allows Users to setup of ETL jobs and report jobs on a pre-set schedule and frequency. Reports can be configured to be sent to an FTP location or to specific email addresses.

## High-Level Infrastructure Architecture <a href="#toc82080631" id="toc82080631"></a>

The platform is composed of various components:

1. Public API Gateway for ingress and API Management of publicly accessible APIs , like APIs for mobile devices and web applications
2. Private API Gateway, accessible from a VPC deployed component, like internal Authentication and authorization APIs
3. User pool management and authentication integration using **Auth0**
4. **ScikIQ Web UI**: Python Django-based UI backed by MysqlDB
5. **Casbin Server**: An authorization library deployed as a docker service
6. Backend Microservices:
   1. ScikIQ APIs
   2. ETL and Scheduler
   3. Metadata discovery
   4. Router
7. Databases
   1. ScikIQ Data Store: Azure Database for Mysql
   2. Metadata Store: Neo4J ( Graph Database )
   3. Casbin Server Policy Store: Azure Database for Mysql
8. Operational Data Store
   1. Vertica DB hosted on a Virtual Machine
   2. Object Store
9. Third-party integrations:
   1. Elastic Cloud

**The diagram below depicts the high-level deployment architecture for the integrated solution.**

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FVY5w0wdgS09GZsPA6fYU%252F5.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=45cb410d\&sv=1)Graphical user interface, diagram Description automatically generated

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FzlI6I0oQSfVAXmLWgWZa%252F6.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=4ba5e98d\&sv=1)

ScikIQ is built primarily on Open-Source technologies which enable it to be agile, scalable, and nimble when it comes to technological improvements or even the rollout of new features.

The core of ScikIQ is a host of Python-based microservices that cater to different feature sets in ScikIQ. A Django framework integrated with a MySQL metadata engine completes the back-end. The ScikIQ front-end is built on bespoke HTML and Javascript/jQuery engines and embeds cleanly with the microservices to provide an optimum responsive user interface.

In addition, ScikIQ utilizes the below technologies:

* Elastic platform for Logging
* Rabbit MQ for Orchestration and Message queuing
* Elastic Search as Metadata Search engine
* Neo4j for Relationship stores
* Python for all the ML/AI features
* Vertica as the Data Lake/Analytics Cluster

## Option A – Setup on AWS and/or Azure <a href="#toc103601838" id="toc103601838"></a>

Deployment of ScikIQ Platform on AWS cloud account

**Pre- Requisites**

* AWS Account IAM user credentials for ScikIQ devops team with required access to deploy above infrastructure along-with VPC peering access
* Networking policy which defines the cases to isolate deployment at AWS VPC Level
* Network CIDR for existing VPCs as to avoid peering conflict with new VPC

#### Proposed Cloud Infrastructure High Level Diagram for AWS: <a href="#toc103601839" id="toc103601839"></a>

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252Fafgb2zmd4ypVkA3BjMXh%252F7.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=4e716bc5\&sv=1)

#### Proposed Cloud Infrastructure High Level Diagram for Azure: <a href="#toc103601840" id="toc103601840"></a>

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FXxSO4dWyYXanmLIuBrB6%252F8.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=8f3b3041\&sv=1)

## Scope Of Work for AWS Setup <a href="#toc103601841" id="toc103601841"></a>

* Configure Infrastructure networking - VPC/Subnets, VPC peering, Security Groups, NAT Gateways
* Setup UAT Environment on EC2
* Setup and configure ODS on EC2 and Metadata DB on RDS
* Configure Production application on EC2 servers and routing using Application load balancers & Configure Autoscaling for production environment to handle dynamic user load
* Setup release pipeline on Jenkins to deploy changes to UAT and Prod
* Setup Monitoring scripts and send metrics to AWS CloudWatch. Setup AWS CloudWatch dashboard, alarms and AWS SNS notification topics
* Deploy AWS Lambda functions to schedule stop/start of UAT environment for cost savings & miscellaneous work

## Deployment Specs <a href="#feyuterpidu0" id="feyuterpidu0"></a>

## **UAT Environment:**

1. 1 X 4vCPU 16 GB RAM Centos 7 VM to host ScikIQ web/API/router/ETL Scheduler
2. 1 X 4vCPU 16 GB RAM VM for Vertica (ODS)
3. Scheduled ON/OFF for UAT environment. Business hours to be defined for this operation

## **Production Environment:**

1. 2 X 2vCPU 8GB RAM Centos 7 VM to host ScikIQ Web + Autoscaling
2. 2 X 2vCPU 8GB RAM Centos 7 VM to host ScikIQ API + Autoscaling
3. 2 X 2vCPU 4GB RAM Centos 7 VM to host ScikIQ Router + Autoscaling
4. 1 X 8vCPU 32GB RAM Centos 7 VM to host ScikIQ ETL Scheduler
5. 1 X 2vCPU 4GB RAM AWS RDS Mysql instance with Multi AZ enabled
6. 1 X 8vCPU 32GB RAM VM to host ODS over Vertica
7. 1 X Internet facing Application Load Balancer for ScikIQ Web
8. 1 X internal Application Load Balancer for non-internet-facing ScikIQ HTTP endpoints
9. Cloud certificate for the DNS entries to be used for ScikIQ WEB and other HTTP endpoints

**Release pipeline:**

* Deploy UAT on manual trigger
* Zero downtime Production deployment on manual approval of UAT deployment

**Monitoring and Backups:**

* AWS Cloudwatch for monitoring critical server metrics
* AWS SNS for sending email alerts on crossing a certain threshold
* AWS Lambda to trigger snapshots backup of vertical
* AWS RDS backup service to backup metadata DB

**Note: The above production configuration is generic, based on certain assumptions. This is supposed to improve on performance and feedback of the UAT environment**

## CI/CD Specifications <a href="#toc110008104" id="toc110008104"></a>

Source code hosting: AWS Codecommit (git-based DVCS)

Git Branching Strategy: Git Flow

No. of environments/stages:

* 1 X development
* 1 X Staging
* 1 X Production

Build notifications: **Email and Slack**

**Not** covered in current scope :

* Multiple DEV/QA environment ( dynamic review or always running )
* Unit testing
* Code coverage analysis and Static code analysis
* Build Quality Gate
* Mobile APP’s release pipeline

CI/CD flow and Git branching strategy ( depicted on next page )

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252F8hVow76GtidY4dQAhYFK%252F9.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=c7d18afd\&sv=1)
