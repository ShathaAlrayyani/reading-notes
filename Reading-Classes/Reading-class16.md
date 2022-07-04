## What is serverless?
Serverless is a cloud computing application development and execution model that enables developers to build and
run application code without provisioning or managing servers or backend infrastructure.

Serverless lets developers put all their focus into writing the best front-end application code and business 
logic they can. All developers need to do is write their application code and deploy it to containers 
managed by a cloud service provider. The cloud provider handles the rest, provisioning the cloud infrastructure 
required to run the code and scaling the infrastructure up and down on demand as needed. 
The cloud provider is also responsible for all routine infrastructure management and maintenance such as operating 
system updates and patches, security management, capacity planning, system monitoring and more.

## Serverless does not mean 'no servers'
The name notwithstanding, there are most definitely servers in serverless computing. 
'Serverless' describes the developer’s experience with those servers—they are invisible to the developer, 
who doesn't see them, manage them, or interact with them in any way.

Today every leading cloud service provider offers a serverless platform including Amazon Web Services (AWS Lambda), 
Microsoft Azure (Azure Functions), Google Cloud (Google Cloud Functions) and IBM Cloud (IBM Cloud Code Engine). 
Together serverless computing, microservices and containers form a triumvirate of technologies typically considered 
to be at the core of cloud-native application development.

Serverless is more than just FaaS
Function-as-a-service, or FaaS, is a cloud computing service that enables developers to run code or containers in response to specific events or requests, without specifying or managing the infrastructure required to run to code.

FaaS is the compute model central to serverless, and the two terms are often used interchangeably. 
But serverless is much more than FaaS. 
Serverless is an entire stack of services that can respond to specific events or requests, 
and scale to zero when no longer in use—and for which provisioning, management and billing are handled by the cloud 
provider and invisible to developers. In addition to FaaS, these services include:

- **Serverless databases and storage**: Databases (SQL and NoSQL) and storage (particularly object storage) are the foundation of the data layer. A serverless approach to these technologies involves transitioning away from provisioning “instances” with defined capacity, connection and query limits, and moving toward models that scale linearly with demand in both infrastructure and pricing.

- **Event streaming and messaging**: Serverless architectures are well-suited for event-driven and stream-processing workloads most notably the open source Apache Kafka event streaming platform.

- **API gateways**: API gateways act as proxies to web actions and provide HTTP method routing, client ID and secrets, rate limits, CORS, viewing API usage, viewing response logs, and API sharing policies.

## Pros and cons of serverless
### Pros
Given all the preceding, it should be no surprise that serverless computing offers a number of technical 
and business benefits to individual developers and enterprise development teams.

- Improved developer productivity
- Pay for execution only
- Develop in any language
- Streamlined development/DevOps cycles.
- Cost-effective performance.
- Usage visibility. 
### cons
With so much to like about serverless, organizations are using it for a wide variety of applications
But there are drawbacks—some of which are related to specific applications, and others which are universal.

- Unacceptable latency for certain applications.
- Higher costs for stable or predictable workloads.
- Monitoring and debugging issues.
- Vendor lock-in.

for more info visit this link [Here](https://www.ibm.com/cloud/learn/serverless)