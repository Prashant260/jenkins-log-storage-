This project automates the process of uploading Jenkins build logs or artifacts to an AWS S3 bucket using a Jenkins pipeline and shell scripting. It is designed to enhance CI/CD workflows by enabling efficient and secure archival, sharing, or backup of Jenkins-generated files directly to Amazon S3.

Prerequisites
Jenkins Installation

Jenkins should be installed and running on your system.

Java

Jenkins requires Java (preferably OpenJDK 21 or newer). Ensure Java is installed.

AWS CLI

Install AWS CLI to facilitate interactions with AWS services.

bash
sudo apt-get update
sudo apt-get install awscli -y
Or with pip:

bash
pip install awscli
Configure AWS CLI

Set up your AWS CLI with valid credentials.

bash
aws configure
Enter your AWS Access Key ID, Secret Access Key, Default Region, and Output Format.

AWS S3 Bucket

Create an S3 bucket to store your Jenkins files.

bash
aws s3 mb s3://your-unique-jenkins-log-bucket
Replace your-unique-jenkins-log-bucket with your actual bucket name.

IAM User & Permissions

Use an IAM user with sufficient S3 permissions (preferably at least AmazonS3FullAccess).

Configure the AWS credentials in Jenkins.

Jenkins Pipeline: AWS Steps Plugin

Install the Pipeline: AWS Steps plugin from Jenkins’s plugin manager for S3 integration within pipelines.

Shell Script Permissions (if scripting)

If using a shell script for uploads, ensure it has execution rights:

bash
chmod 777 s3upload.sh
With all prerequisites fulfilled, you’re ready to set up Jenkins pipelines that seamlessly upload build logs or artifacts to AWS S3 as part of your CI/CD process.
