This project automates the process of uploading Jenkins build logs or artifacts to an AWS S3 bucket using a Jenkins pipeline and shell scripting. It is designed to enhance CI/CD workflows by enabling efficient and secure archival, sharing, or backup of Jenkins-generated files directly to Amazon S3.

Prerequisites:

-Jenkins Installation

-Jenkins should be installed and running on your system.

-Java

-Jenkins requires Java (preferably OpenJDK 21 or newer). Ensure Java is installed.

-AWS CLI

-Install AWS CLI to facilitate interactions with AWS services.

-Configure AWS CLI

-Set up your AWS CLI with valid credentials.

  -- your AWS Access Key ID, Secret Access Key, Default Region, and Output Format.

#AWS S3 Bucket

-Create an S3 bucket to store your Jenkins files.


#Shell Script Permissions (if scripting)

If using a shell script for uploads, ensure it has execution rights:


chmod 777 s3upload.sh
With all prerequisites fulfilled, you’re ready to set up Jenkins pipelines that seamlessly upload build logs or artifacts to AWS S3 as part of your CI/CD process.
