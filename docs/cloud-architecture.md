# Cloud Architecture

The pharmacy system uses a multi-tier cloud architecture inside an Amazon Virtual Private Cloud (VPC). The design separates the web application layer from the database layer to improve security and compliance.

Key components:

- **Amazon VPC**  
  Isolated network environment where all pharmacy resources are hosted.

- **Public Subnet + Internet Gateway**  
  Entry point for staff to access the web application running on an EC2 instance.

- **Amazon EC2 (t3.small)**  
  Hosts the pharmacy management application and handles user interactions.

- **Private Subnet + Amazon RDS (MySQL, db.t3.micro)**  
  Stores prescriptions and inventory data in a managed database that cannot be accessed directly from the internet.

- **Amazon SQS**  
  Queues transactions so that no prescription or sale is lost during busy periods.

- **Amazon S3 + S3 Glacier**  
  S3 stores daily backups; S3 Glacier holds long-term archives of medical records at a lower cost.

- **AWS IAM**  
  Controls who can access and manage data and services.

- **Amazon CloudWatch**  
  Monitors system health and provides basic alerts if something goes wrong.
