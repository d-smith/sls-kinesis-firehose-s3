# sls-kinesis-firehose-s3

Kinesis to Firehose to S3 using the serverless framework, with a lambda transformer to write the records to individual lines in the output s3 object.

First, create the bucket by hand of name kfs3-dev-kfs3-destination, then deploy, e.g.

For multiregion replication try the s3-repl Jupyter notebook in the sls-sns project.

```
s3api create-bucket 
 aws s3api create-bucket --bucket kfs3-destination-dev --region us-east-1 --create-bucket-configuration LocationConstraint=us-west-2

 env FIREHOSE_DESTINATION_BUCKET=kfs3-west-dest-dev sls deploy --region us-west-2
```
aws kinesis put-record --stream-name kfs3-dev-app-stream --partition-key abc --data eyJmb28iOnRydWV9Cg==
```