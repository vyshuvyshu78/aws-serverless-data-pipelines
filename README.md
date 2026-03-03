# AWS Serverless Data Pipeline

## Overview
This project demonstrates a scalable serverless data pipeline built using AWS services.

## Architecture Flow
1. CSV file uploaded to Amazon S3
2. S3 event triggers AWS Lambda
3. Lambda starts AWS Glue Job
4. Glue processes and stores transformed data back to S3

## Technologies Used
- Amazon S3
- AWS Lambda
- AWS Glue
- Python (boto3)
- CloudWatch

## Features
- Event-driven architecture
- Automated ETL trigger
- Serverless design
- Scalable and cost-efficient

## Future Enhancements
- Add Glue ETL script
- Add infrastructure as code (Terraform/CloudFormation)
- Add monitoring alerts
