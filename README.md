# Insurance Data Lake ETL Pipeline on AWS

A comprehensive ETL (Extract, Transform, Load) pipeline built on AWS for processing and managing insurance data at scale.

## Project Overview

This project implements a robust data lake architecture on Amazon Web Services (AWS) to handle insurance data processing. The pipeline automates the extraction, transformation, and loading of data from various sources into a centralized data lake, enabling analytics, reporting, and data-driven decision making.

## Architecture

The solution leverages the following AWS services to create a scalable, secure, and maintainable data pipeline:

- **AWS S3** - Data lake storage and staging areas
- **AWS Glue** - ETL jobs and data catalog
- **AWS Lambda** - Serverless event-driven triggers and orchestration
- **AWS RDS/DynamoDB** - Source and target databases
- **AWS CloudWatch** - Monitoring and logging
- **AWS IAM** - Security and access control
- **AWS EventBridge** - Event-driven workflows

## Data Pipeline Workflow

1. **Ingestion** - Data from insurance systems is ingested into S3 staging buckets
2. **Validation** - Lambda functions validate data quality and format
3. **Transformation** - AWS Glue jobs transform and enrich the data
4. **Storage** - Processed data is stored in the data lake (S3)
5. **Cataloging** - Data Catalog maintains metadata and schema information
6. **Analytics** - Data is made available for analysis and reporting

## Getting Started

### Prerequisites

- AWS Account with appropriate permissions
- AWS CLI configured with credentials
- Python 3.8+
- Terraform (for infrastructure as code)

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/ShubhayuMallick1997/Insurance-Data-Lake-ETL-Pipeline-on-AWS-Project.git
cd Insurance-Data-Lake-ETL-Pipeline-on-AWS-Project
```

2. Configure AWS credentials:
```bash
aws configure
```

3. Deploy infrastructure:
```bash
terraform init
terraform plan
terraform apply
```

4. Deploy ETL jobs:
```bash
python deploy_glue_jobs.py
```

## Project Structure

```
.
├── src/
│   ├── glue_jobs/          # AWS Glue ETL job scripts
│   ├── lambda_functions/   # Lambda function code
│   └── utilities/          # Helper functions and utilities
├── terraform/              # Infrastructure as Code
├── config/                 # Configuration files
├── tests/                  # Unit and integration tests
├── docs/                   # Documentation
└── README.md              # This file
```

## Key Features

- **Scalability** - Handles large volumes of insurance data
- **Automation** - Event-driven triggers minimize manual intervention
- **Data Quality** - Built-in validation and error handling
- **Security** - IAM policies and encryption for data protection
- **Monitoring** - CloudWatch dashboards and alerts
- **Cost Optimization** - Efficient resource utilization with serverless architecture

## Configuration

Configuration settings can be found in `config/` directory:
- `config.yaml` - Main configuration file
- `aws_config.json` - AWS-specific settings
- `.env` - Environment variables (not committed to version control)

## Monitoring and Logging

Monitor pipeline execution through:
- **CloudWatch Logs** - Application and job logs
- **CloudWatch Dashboards** - Real-time metrics and KPIs
- **AWS Glue Dashboard** - Job status and performance metrics

## Contributing

Contributions are welcome! Please follow these steps:

1. Create a new branch for your feature
2. Make your changes and add tests
3. Submit a pull request with a clear description

## Troubleshooting

For common issues and solutions, please refer to [TROUBLESHOOTING.md](./docs/TROUBLESHOOTING.md)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or support, please contact the project maintainer or open an issue on GitHub.

## References

- [AWS Glue Documentation](https://docs.aws.amazon.com/glue/)
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/)
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)
- [AWS Data Lake Best Practices](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/data-lake-overview.html)
