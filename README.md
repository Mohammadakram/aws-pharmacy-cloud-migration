# AWS Pharmacy Cloud Migration

This project designs and implements a cloud-based solution for a medium-sized UK pharmacy chain with four branches. Each branch currently uses local spreadsheets to manage prescriptions and stock, which causes data loss risk, poor stock visibility, and privacy issues.

The goal is to migrate the pharmacy data and workflows to Amazon Web Services (AWS) and create a single, secure, central system. All branches will share one up-to-date inventory and prescription database, with automated backups and strict security controls.

## Architecture Overview

The solution uses a multi-tier architecture inside an Amazon VPC:

- Public subnet with an EC2 instance for the pharmacy web application
- Private subnet with an Amazon RDS MySQL database for prescriptions and stock
- Amazon S3 and S3 Glacier for backups and long-term archiving
- Amazon SQS for reliable transaction handling
- AWS IAM for identity and access management
- Amazon CloudWatch for basic monitoring and alerts

See `docs/cloud-architecture.md` and `diagrams/architecture-diagram.png` for a detailed view.

## Repository Structure

- `docs/` – Project documentation (business problem, requirements, design, costing, reflection)
- `diagrams/` – Architecture diagram and other visual designs
- `screenshots/` – Redacted AWS console screenshots showing the implementation

This repository is intended as a showcase of cloud architecture, design thinking, and AWS implementation skills for a healthcare use case.
