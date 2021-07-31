# sls-kinesis-firehose-s3

Kinesis to Firehose to S3 using the serverless framework, with a lambda transformer to write the records to individual lines in the output s3 object.

```
aws kinesis put-record --stream-name kfs3-dev-app-stream --partition-key abc --data eyJmb28iOnRydWV9Cg==
```