# aws-datasync-nfs-migration
Automate AWS DataSync infrastructure with CloudFormation to migrate data across VPCs using NFS and S3—efficient and low-cost

This repository contains AWS CloudFormation templates to migrate ~100 small text files from an NFS server to an Amazon S3 bucket using AWS DataSync, as described in my [LinkedIn article](https://www.linkedin.com/pulse/setting-up-aws-datasync-migration-infrastructure-vladimir-jovanovski-ejm8f/?trackingId=1SHn9jBmlVBXmQEhIgW8Pg%3D%3D). The setup spans two regions: us-east-1 for the source (VPC, NFS server, two DataSync agents) and us-east-2 for the destination (S3 bucket, IAM role).

## Repository Contents

- `source-vpc-template.yaml`: Deploys VPC, subnet, route table, security groups, and three t3.medium EC2 instances (NFS server, two DataSync agents) in us-east-1. ([Link](#))
- `destination-s3-template.yaml`: Creates an S3 bucket and IAM role for DataSync in us-east-2. ([Link](#))
- `README.md`: This file.

## Purpose

This demo, inspired by my AWS SAA recertification, tests AWS DataSync’s capabilities for file migration between regions, using two agents for parallel task execution. See the [LinkedIn article](https://www.linkedin.com/pulse/setting-up-aws-datasync-migration-infrastructure-vladimir-jovanovski-ejm8f/?trackingId=1SHn9jBmlVBXmQEhIgW8Pg%3D%3D) for setup and configuration details.

## Usage

Refer to the [LinkedIn article](https://www.linkedin.com/pulse/setting-up-aws-datasync-migration-infrastructure-vladimir-jovanovski-ejm8f/?trackingId=1SHn9jBmlVBXmQEhIgW8Pg%3D%3D) for instructions on deploying the templates, configuring the NFS server, setting up DataSync tasks, and cleaning up resources to minimize costs (~$0.30 for t3.medium instances).

## License

MIT License (see [LICENSE](LICENSE)).
