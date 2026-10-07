# Module 3: Introduction to Serverless Computing

# INTRODUCTION
- Introduction to Serverless Computing
  - With serverless computing, you run applications without managing the underlying infrastructure. In the following lessons, you learn how to take full advantage of it with powerful compute services. 
  - Key takeaways: Unmanaged and managed services
    - Unmanaged and managed services:
      - unmanaged: With unmanaged compute services like Amazon EC2, AWS takes care of the underlying physical infrastructure, but you're responsible for setting up, securing, and maintaining the operating system, network configurations, and applications on your instances. 
      - managed: Managed services, on the other hand, reduce the amount of infrastructure you need to manage (you still might need to perform some provisioning or configuration, depending on service).
    - Fully-managed services --> Fully-managed services—like serverless ones—take abstraction even further, eliminating the need to provision or manage any servers at all (underlying infrastructure fully managed by AWS).
    -  
    
# AWS SERVERLESS, CONTAINERS, AND SOLUTIONS OVERVIEW
- AWS Lambda
  - Lambda is a serverless compute service that runs code in response to events without the need to provision or manage servers. It automatically manages the underlying infrastructure, scaling resources based on the volume of requests.
  -   You can optimize performance by configuring the appropriate memory size for your function.
    - How Lambda works:
      - Upload code to lambda
      - Set code to trigger from an event source
      - Run code when triggered
      - Pay only for compute time used
    - Lambda use cases:
  - Lambda (demonstration):
- Containers and Orchestration on AWS
- Additional Compute Services

- NEED TO ADD
- # Containers on AWS
 
Containers package an application's code and dependencies into a single portable unit, so it runs the same way on any machine. This makes them a good fit for workloads that need security, reliability, and scalability.
 
## Containers vs. virtual machines
 
| | Containers | Virtual machines |
|---|---|---|
| Isolation | Share the host operating system | Each runs a full, separate OS on a hypervisor |
| Startup | Fast | Slower |
| Resource use | Lightweight | Heavier |
 
## Why containers help deployments
 
When a developer's environment differs from staging or production, deployments fail and are hard to debug. Containers keep the application's environment identical at every stage, which reduces deployment failures and simplifies troubleshooting.
 
## Orchestration
 
A few containers on one host can grow into hundreds or thousands across many hosts. At that scale, handling lifecycle, monitoring, and operations by hand is unsustainable. Orchestration tools automate deployment, scaling, and management.
 
## AWS container services
 
AWS container tooling falls into three categories:
 
| Category | Service | What it does |
|---|---|---|
| Orchestration | Amazon ECS | AWS-native orchestration for running and managing containers (e.g. Docker) |
| Orchestration | Amazon EKS | Fully managed Kubernetes on AWS |
| Registry | Amazon ECR | Stores, manages, and deploys container images |
| Compute | AWS Fargate | Serverless compute engine that hosts containers |
 
### Amazon ECS (Elastic Container Service)
 
A scalable orchestration service for running and managing containers on AWS.
 
- **ECS on EC2**: full control over infrastructure. Suits custom applications that need specific hardware or networking configurations.
- **ECS on Fargate**: serverless, with no servers to manage. Suits small teams and web applications with variable traffic.
### Amazon EKS (Elastic Kubernetes Service)
 
A fully managed service for running open-source Kubernetes on AWS, with support and updates from the wider Kubernetes community.
 
- **EKS on EC2**: full control and deep customization of EC2 instances. Suits complex, large-scale enterprise workloads.
- **EKS on Fargate**: Kubernetes without managing servers. Suits teams that want Kubernetes flexibility with serverless simplicity.
### Amazon ECR (Elastic Container Registry)
 
A registry for container images that follow the Open Container Initiative (OCI) standards. Images are pushed, pulled, and managed with standard container tooling and CLIs.
 
### AWS Fargate
 
A serverless compute engine for containers that works with both ECS and EKS. Fargate is a hosting platform, not an orchestrator: ECS or EKS decides what runs, and Fargate provides the compute to run it.
 
- No servers to provision or manage
- Pay only for the resources your containers use
## Choosing a launch type
 
| | EC2 | Fargate |
|---|---|---|
| **ECS** | Infrastructure control with simpler AWS-native orchestration | Least operational overhead |
| **EKS** | Maximum control and customization with Kubernetes | Kubernetes without server management |

# CONCLUSION
