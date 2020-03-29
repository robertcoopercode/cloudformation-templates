# Cloudformation Templates

This repo contains the cloudformation templates I used for a web app deployed on AWS ECS.

The following cloudformation templates exist in this repository:

**assets.yml**

Describes AWS infrastructure that will allow for the storage of assets such as images and PDF files. The AWS infrastructure used is S3 buckets and a Cloudfront CDN. It also adds the correct DNS entry to Route 53 to have Cloudfront serve assets from a specific domain name.

**vpc.yml**

Sets up a VPC to be used by ECS in order to have the services accessible from the internet and communicate with each other. Also sets up a cloudwatch log group responsible for aggregating server logs for all the services. 

**backend.yml**

Describes an ECS service for a back-end app and expose it on a VPC. Also adds a DNS entry to Route 53 to allow the back-end to be accessible at a specific domain name.

**frontend.yml**

Describes an ECS service for a front-end app, expose it on the VPC load balancer, make it accessible through the web (at an https address), and create a DNS entry in Route 53 to allow the app to be accessible at a specific domain name.

**prisma.yml**

Describes an ECS service for a prisma server, expose it on the VPC load balancer, make it accessible through the web (at an https address), create a DNS entry in Route 53 to allow it to be accessible at a specific domain name, and create an RDS MySQL DB that the prisma server will be able to read and write to.
