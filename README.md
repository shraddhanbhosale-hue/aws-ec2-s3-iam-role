# AWS EC2 S3 IAM Role

## Overview

This project demonstrates how to securely provide an EC2 instance with read-only access to Amazon S3 using an IAM role.

Instead of storing AWS access keys on the EC2 instance, an IAM role was attached to the EC2 instance to provide temporary credentials automatically.

## AWS Services Used

- Amazon EC2
- AWS IAM
- Amazon S3
- AWS CLI

## Implementation

### 1. Created IAM Policy

Created a customer-managed IAM policy:

`EC2-S3-ReadOnly-Policy`

The policy provides read-only access to S3 resources.

### 2. Created IAM Role

Created the role:

`EC2-S3-ReadOnly-Role`

The role was configured to be assumed by the EC2 service.

### 3. Attached Role to EC2

The IAM role was attached to the EC2 instance:

`web-server`

Instance type:

`t3.micro`

### 4. Tested S3 Access

Connected to the EC2 instance using SSH and tested AWS CLI commands.

```bash
aws s3 ls
