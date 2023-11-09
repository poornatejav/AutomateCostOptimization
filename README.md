Identifying the unused EBS Snapshots
with the code created a Lambda function that checks for EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.
The Lambda function fetches all EBS snapshots owned by the same account and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a un attached snapshot, it deletes it, for better optimization of storage costs
