# python-aws

This repository contains Python scripts and AWS automation code for managing EC2 instances, Lambda functions, EventBridge rules, and IAM roles/policies.

## Contents

- **ec2-auto-start.py**: Python script to automatically start EC2 instances at scheduled times.
- **ec2-auto-stop.py**: Python script to automatically stop EC2 instances to save costs.
- **Lambda Function Code**: AWS Lambda function(s) for automating EC2 instance management or handling AWS events.
- **EventBridge Code**: Configuration and automation code for AWS EventBridge rules to trigger automation (such as Lambda functions or scripts) based on schedules or AWS events.
- **IAM Code**: IAM roles and policy definitions required for Lambda functions and scripts to interact with EC2 and other AWS services securely.

## Usage

1. **ec2-auto-start.py / ec2-auto-stop.py**
   - Configure your AWS credentials (`aws configure` or environment variables).
   - Edit the instance IDs or tags within the scripts as needed.
   - Run the scripts manually or deploy them as Lambda functions.

2. **Lambda Functions**
   - Deploy the Lambda code using the AWS CLI, AWS Console, or infrastructure-as-code tools.
   - Assign necessary IAM roles/policies (provided in this repo).

3. **EventBridge Rules**
   - Use the provided code/templates to set up EventBridge rules to trigger Lambda functions or automation scripts at specific times (for instance, start EC2 every morning, stop EC2 every evening).

4. **IAM Roles/Policies**
   - Apply the IAM roles/policies to your Lambda functions or users as required for least-privilege AWS access.

## Example Scenario

- Automatically start EC2 instances every weekday morning and stop them every evening using EventBridge scheduled rules linked to Lambda functions that run the included Python scripts.
- All required IAM permissions for EC2 and Lambda are provided.

## Prerequisites

- AWS account with access to EC2, Lambda, EventBridge, and IAM.
- Python 3.x
- AWS CLI (optional but recommended)
- Permissions to create IAM roles/policies, Lambda functions, and EventBridge rules.

## Setup Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/BharathKumarReddy2103/python-aws.git
   cd python-aws
   ```

2. Install Python dependencies (if any):
   ```bash
   pip install -r requirements.txt
   ```

3. Review and update configuration in the scripts (instance IDs, region, etc).

4. Deploy Lambda functions and EventBridge rules using AWS Console or CLI.

5. Attach IAM roles/policies as needed.

## License

This project is licensed under the MIT License.

## Author

[BharathKumarReddy2103](https://github.com/BharathKumarReddy2103)
