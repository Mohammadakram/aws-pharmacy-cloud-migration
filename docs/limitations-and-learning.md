# Limitations and Learning

## Limitations

- The implementation uses an AWS sandbox environment, which has region and service limits. For example, resources were created in a different region where some London region services were not available.
- The RDS database is deployed in a single Availability Zone, so it does not yet provide automatic multi-AZ failover.
- Monitoring is kept basic to avoid extra costs, and more detailed logging could be added later.

## Learning and Future Improvements

Through this project, several lessons emerged:

- Cloud migration for healthcare needs strong focus on data privacy, region choice, and network isolation.
- Multi-tier architectures inside a VPC help separate the web and database layers and reduce risk.
- Using S3 lifecycle rules and Glacier can significantly lower long-term storage costs for medical records.

Future improvements could include:

- Adding multi-AZ support for RDS to increase resilience.
- Introducing more detailed monitoring and alerting.
- Automating infrastructure using tools like Terraform or AWS CloudFormation.
