# Cost Estimate

An initial monthly cost estimate was created using the AWS Pricing Calculator.

Approximate costs:

- **Compute:** One t3.small EC2 instance for the pharmacy web application.
- **Database:** One db.t3.micro RDS MySQL instance for prescriptions and stock.
- **Storage:** Amazon S3 for daily backups and S3 Glacier for long-term archives.
- **Support:** AWS Business Support Plan for 24/7 access to cloud support engineers.

The estimated monthly cost is around 86.48 USD, with no upfront hardware investment. Network services (VPC, basic CloudWatch, IAM) are included without additional direct charges at this scale.
