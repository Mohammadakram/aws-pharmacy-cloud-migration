# Database and Storage Design

## Database

The central pharmacy database uses Amazon RDS for MySQL:

- Instance type: `db.t3.micro`
- Storage: 20 GB
- Deployment: Single Availability Zone
- Hosted in the private subnet to prevent direct public access

This database holds all patient prescriptions and stock information for the four branches.

## Storage and Backups

Amazon S3 and S3 Glacier are used for backups and archiving:

- Daily automated backups are stored in S3.
- A lifecycle rule moves older data to S3 Glacier for long-term storage at a lower price.
- This approach meets legal requirements for retaining medical records over time while controlling costs.
