# Cost-Optimization-AWS
Cost Optimization script for AWS using boto3 

This is a Lambda function written in Python using the Boto3 library to interact with AWS services. The purpose of this script is to identify and delete unused EBS snapshots to optimize costs.

Here's a breakdown of what the script does:

1.It uses the Boto3 library to create an EC2 client.
2.It retrieves a list of EBS snapshots owned by the current AWS account.
3.It retrieves a list of active EC2 instances.
4.It iterates through each snapshot and checks if it is attached to any volume or if the volume is attached to a running instance.
5.If a snapshot is not attached to any volume, it is deleted.
6.If a snapshot is attached to a volume, it checks if the volume still exists. If not, it deletes the snapshot.
7.The script prints information about each deleted snapshot for logging purposes.
