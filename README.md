## Cost Optimization with AWS Lambda and CloudWatch:
![Configuration Tool](https://github.com/user-attachments/assets/3fa3eb4c-f875-4e82-ba70-961929baff52)

### UseCase: Identifying stale EBS snapshot

We'll create a Lambda function that identifies EBS snapshots no longer associated with active EC2 instances and deletes them to reduce storage costs. The function works by fetching all EBS snapshots owned by the account and retrieving a list of active EC2 instances (both running and stopped). It then checks each snapshot to see if its associated volume is not linked to any active instance. If a stale snapshot is found, the function deletes it, helping to optimize storage costs

Medium article: https://medium.com/@ruchikapatel1096/lets-explore-a-practical-example-of-how-we-can-achieve-cost-optimization-using-aws-services-ee10cbbedcfe
