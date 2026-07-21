# Network and Security Design

## Region and Data Centre

The pharmacy data is hosted in an AWS region that keeps medical records within the UK for GDPR compliance. Using a nearby region also reduces latency for staff accessing the system.

## VPC and Subnets

- A dedicated Amazon VPC isolates pharmacy resources from other customers.
- A **public subnet** hosts the EC2 web server and is connected to the internet through an Internet Gateway.
- A **private subnet** hosts the RDS database, which has no direct internet access.

## Security Controls

- **Security groups** restrict inbound and outbound traffic to only what is required (for example, allowing web access to EC2 and database access only from the EC2 instance).
- **IAM roles and policies** ensure that only authorised users and services can access patient and inventory data.
- Data is protected using AWS security best practices suitable for healthcare workloads.
