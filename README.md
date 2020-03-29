# Cloudformation Templates

This repo contains the cloudformation templates I used for a web app previously deployed on AWS ECS. I've saved the cloudformation templates in this repository as a reference for specifying AWS infrastructure using Cloudformation.

The following cloudformation templates exist in this repository:

**assets.yml**

- S3 bucket
- Cloudfront CDN
- DNS entry in Route 53 allowing Cloudfront assets to be accessible from a custom domain

**vpc.yml**

- VPC
- Load balancer
- Cloudwatch log group that aggragates all server logs

**backend.yml**

- ECS service
- Configure load balancer to expose service internally and externally
- DNS entry in Route 53

**frontend.yml**

- ECS service
- Configure load balancer to expose service internally and externally
- DNS entry in Route 53

**prisma.yml**

- ECS service
- Configure load balancer to expose service internally and externally
- DNS entry in Route 53
- RDS MySQL DB that the prisma service will be able to reade and write to
