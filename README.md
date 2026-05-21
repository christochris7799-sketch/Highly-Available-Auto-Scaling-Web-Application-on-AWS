# Highly-Available-Auto-Scaling-Web-Application-on-AWS# 

This project demonstrates how to deploy a **highly available**, **fault-tolerant**, and **auto-scaling** web application using AWS.  
The infrastructure uses **Application Load Balancer (ALB)**, **Auto Scaling Group (ASG)**, and **Multi-AZ deployment** to ensure continuous availability even during failures or high traffic.

 🎯 Project Goals
- Build a **zero-downtime**, **self-healing** architecture  
- Deploy across **multiple Availability Zones (Multi-AZ)**  
- Automatically scale the number of servers based on demand  
- Distribute traffic using a **Load Balancer**  
- Replace unhealthy servers automatically  
- Demonstrate production-ready AWS deployment

✅ Services Used

- Amazon EC2
- Launch Template
- Auto Scaling Group
- Application Load Balancer
- Target Groups
- Amazon VPC
- Security Groups
- IAM Role
- Amazon CloudWatch
- Route 53
- S3 Bucket

🧱 Architecture Overview

                  ┌─────────────────────────────┐
                  │     Users / Clients          │
                  └─────────────────────────────┘
                               │
                               ▼
                 ┌──────────────────────────────┐
                 │ Application Load Balancer     │
                 └──────────────────────────────┘
                         │                 │
               ┌─────────┘                 └─────────┐
               ▼                                       ▼
    ┌───────────────────┐                  ┌────────────────────┐
    │ Auto Scaling Group│                  │ Auto Scaling Group │
    │  Instance #1      │                  │  Instance #2       │
    └───────────────────┘                  └────────────────────┘
               │                                       │
               └────────────────────────┬──────────────┘
                                        ▼
                        ┌──────────────────────────┐
                        │ Multi-AZ (2 Availability │
                        │       Zones Active)      │
                        └──────────────────────────┘

⭐ Key Features

Multi-AZ distributed deployment, Auto scaling based on CPU load, Self-healing infrastructure, Fault tolerant, Highly available, Zero downtime, Fully production-ready design

📈 Future Enhancements

Add RDS Multi-AZ backend, Implement CI/CD using CodePipeline, Deploy with Terraform or CloudFormation, Add CloudFront CDN, Add AWS WAF security layer

Christopher
