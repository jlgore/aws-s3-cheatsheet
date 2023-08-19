DEMOS: Uploading / Fetching files
			  Hosting websites
			  S3 Versioning

## S3 Transfer Acceleration Demo:
https://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html

## MAN PAGES:
Manual pages for CLI apps are very common ways of getting help when you start out with a new program. To learn more about what the S3 commands need you can type the following:

``aws s3 help
``aws s3api help

``aws s3`` is a wrapper for many common use cases, `aws s3api` is a way to make all the API calls that S3 allows over REST via CLI.

## Bucket Creation and Deletion
Buckets can only be deleted if they are empty. 

```
aws s3 mb s3://$BUCKET_NAME --region us-east-1 --profile gorecc
aws s3 rb s3://$BUCKET_NAME --region us-east-1 --profile gorecc
aws s3api create-bucket --bucket $BUCKET_NAME --profile gorecc
aws s3api delete-bucket --bucket $BUCKET_NAME --profile gorecc
```

## Moving Objects into S3
```
aws s3 cp $SOURCE_DIR s3://$BUCKET_NAME --recursive
aws s3 sync $SOURCE_DIR s3://BUCKET_NAME --recursive
```

## Removing Objects from S3
```
aws s3 rm $SOURCE_FILE s3://$BUCKET_NAME
```

