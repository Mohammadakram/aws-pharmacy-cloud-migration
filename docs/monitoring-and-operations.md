# Monitoring and Operations

Monitoring and operations focus on keeping the pharmacy system reliable and secure over time.

## Monitoring

- Amazon CloudWatch tracks basic metrics such as CPU, memory, and health checks for the EC2 and RDS instances.
- CloudWatch alarms notify the team if performance issues or failures occur.

## Operations and Maintenance

- IAM permissions should be reviewed regularly to ensure only the right staff have access.
- Backups and S3 lifecycle rules should be checked periodically to confirm that data is being retained as expected.
- As the pharmacy chain grows, the system can scale by increasing EC2 and RDS instance sizes or adding more instances.
