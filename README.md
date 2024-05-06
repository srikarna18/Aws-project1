AWS Cloud Cost Optimization - Identifying Stale Resources (using AWS Lambda)


Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
    The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). 
For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. 
If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

To create lambda function for any services refer the documentation https://boto3.amazonaws.com/v1/documentation/api/latest/index.html

Deleting the empty s3 buckets

The lambda function fetches the s3 buckets with no files or folders(empty buckets) and delets the specific buckets.
If it finds a stale s3 buckets, it deletes it, effectively optimizing storage costs.

Checkout the AWS-Boto3 documentation for reference https://boto3.amazonaws.com/v1/documentation/api/latest/search.html?q=s3+bucket&check_keywords=yes&area=default#
