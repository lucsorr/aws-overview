# AWS Cloud Quest Notes

## Policies:

Sample:

```json
{
    "Version": "2012-10-17",
    "Id": "StaticWebPolicy",
    "Statement": [
        {
            "Sid": "S3GetObjectAllow",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::website-bucket-c45b48f0/*"
        }
    ]
}
```


- `Effect` says this policy will Allow access.
- `Principal` defines who has access. In this case, * represents anyone.
- `Action` defines what users can do to objects in the bucket. In this case, users can only retrieve data with `GetObject`.
- `Resource` specifies that this policy applies to only this bucket.
- Generally, to safeguard against unintentional data exposure, we recommend strict S3 bucket permissions in production. 

you can grant permissions to S3 resources via bucket policies and user policies

an Amazon Resource Name (ARN) identifies aws resources

## Launching an EC2 instance

![](assets/2023-12-14-21-43-30.png)

![](assets/2023-12-14-21-45-51.png)

![](assets/2023-12-14-21-47-11.png)

![](assets/2023-12-14-21-48-25.png)

![](assets/2023-12-14-21-49-55.png)

![](assets/2023-12-14-21-52-37.png)

![](assets/2023-12-14-21-54-10.png)

![](assets/2023-12-14-21-55-17.png)