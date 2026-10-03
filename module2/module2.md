# Module 2: Compute in the Cloud

## INTRODUCTION

- Introduction to Amazon EC2

## COMPUTE IN THE CLOUD

- Amazon EC2 Instance Types: General purpose, Compute optimized, Memory optimized, Accelerated computing, Storage optimized   
- How to Provision AWS Resources
- Demo: Launching an Amazon EC2 Instance
- Amazon EC2 Pricing
  - On-Demand Instances: Pay only for the compute capacity you consume with no upfront payments or long-term commitments required.
  - Reserved Instances: Get a savings of up to 75 percent by committing to a 1-year or 3-year term for predictable workloads using specific instance families and AWS Regions.
  - Spot Instances: Bid on spare compute capacity at up to 90 percent off the On-Demand price, with the flexibility to be interrupted when AWS reclaims the instance.
  - Savings Plans: Save up to 72 percent across a variety of instance types and services by committing to a consistent usage level for 1 or 3 years.
  - Dedicated Hosts: Dedicated Hosts:
Reserve an entire physical server for your exclusive use. This option offers full control and is ideal for workloads with strict security or licensing needs.
  - Dedicated Instances: Dedicated Instances:
Pay for instances running on hardware dedicated solely to your account. This option provides isolation from other AWS customers.  

## AUTO SCALING AND LOAD BALANCING

- Scaling Amazon EC2
  - Scalability is about a system’s potential to grow over time, whereas elasticity is about the dynamic, on-demand adjustment of resources.
  - You can **scale up** by adding more power to existing machines, or you can **scale out** by adding more machines. Scalability focuses on long-term capacity planning to make sure that the system can grow and accommodate more users or workloads as needed.
  - Elasticity is the ability to automatically scale resources up or down in response to real-time demand.
  - **Amazon EC2 Auto Scaling**: automatically adjusts the number of EC2 instances based on changes in application demand, providing better availability. 
    - Dynamic scaling: adjusts in real time to fluctuations in demand
    - Predictive scaling: preemptively schedules the right number of instances based on anticipated demand
  - Auto Scaling groups: collections of EC2 instances that can scale in or out to meet your application’s needs. 3 types (below):
    - minimum capacity --> defines the least number of EC2 instances required to keep the application running.
    - desired capacity --> the ideal number of instances needed to handle the current workload, which Auto Scaling aims to maintain
    - maximum capacity --> sets an upper limit on the number of instances that can be launched, preventing over-scaling and controlling costs.
- Directing Traffic with Elastic Load Balancing
  - Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple resources, such as EC2 instances, to optimize performance and reliability.
  - Serves as the single point of contact for all incoming web traffic to an Auto Scaling group.
  - Although ELB and Amazon EC2 Auto Scaling are distinct services, they work in tandem to enhance application performance and ensure high availability.
  - ELB main benefits:
    -  Efficient traffic distribution --> evenly distributes traffic across EC2 instances, preventing overload on any single instance
    -  Automatic scaling --> scales with traffic and automatically adjusts to changes in demand for a seamless operation.
    -  Simplified management --> decouples front-end and backend tiers and reduces manual synchronization. Also handles maintenance, updates, and failover to ease operational overhead.
  -  Routing methods (4):
    - Round Robin --> Distributes traffic evenly across all available servers in a cyclic manner.
    - Least Connections --> Routes traffic to the server with the fewest active connections, maintaining a balanced load.
    - IP Hash --> Uses the client’s IP address to consistently route traffic to the same server.
    - Least Response Time --> Directs traffic to the server with the fastest response time, minimizing latency.
- Messaging and Queuing
  - Decoupling services: Monolithic applications (tightly coupled) vs. Microservices architecture (loosely coupled)
  - **Amazon EventBridge**, **Amazon SNS**, and **Amazon SQS** are AWS services that help different parts of an application communicate effectively in the cloud. These services support building event-driven and message-based systems.
    - EventBridge --> serverless service that helps connect different parts of an application **using events**, helping to build scalable, event-driven systems.
    - Amazon SQS --> application places messages into a queue, and a user or service retrieves the message, processes it, and then removes it from the queue.
    - Amazon SNS --> a publish-subscribe service that publishers use to send messages to subscribers through SNS topics. Subscribers can include web servers, email addresses, Lambda functions, and various other endpoints.

## Module 2: CONCLUSION

