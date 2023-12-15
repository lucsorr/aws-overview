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

## Connecting to an EC2 instance; Vertically scaling an EC2 instance

![](assets/2023-12-15-12-46-32.png)

![](assets/2023-12-15-12-47-01.png)

![](assets/2023-12-15-12-47-26.png)
![](assets/2023-12-15-12-47-40.png)
![](assets/2023-12-15-12-47-58.png)
![](assets/2023-12-15-12-48-11.png)


![](assets/2023-12-15-12-53-38.png)

![](assets/2023-12-15-12-55-30.png)

![](assets/2023-12-15-12-55-50.png)
![](assets/2023-12-15-12-56-13.png)
![](assets/2023-12-15-12-56-45.png)
![](assets/2023-12-15-12-57-23.png)

![](assets/2023-12-15-12-57-48.png)

1. To provide root privileges to the current session, in the terminal window, at the command prompt, run the following command (type the command and press Enter):

`sudo -i`

2. To change to the application directory, run: 

`cd ../home/ec2-user/sample_app`

- Be sure to add a space between cd and the ../ command.
- A sample application resides on this instance. 


3. To view the files in the sample_app directory, run: 

`ls`
			 
4. To check the instance log, run: 

`tail -lf aws_compute_solutions.log`
			
5. Go to the next step.

![](assets/2023-12-15-13-00-32.png)

![](assets/2023-12-15-13-03-07.png)
![](assets/2023-12-15-13-03-19.png)

![](assets/2023-12-15-13-03-47.png)
![](assets/2023-12-15-13-04-43.png)

## Networking concepts

- Configure a routing table and attach an internet gateway
- Configure a security group

![](assets/2023-12-15-13-13-34.png)

![](assets/2023-12-15-13-14-03.png)
![](assets/2023-12-15-13-14-21.png)
![](assets/2023-12-15-13-14-33.png)

![](assets/2023-12-15-13-15-19.png)

![](assets/2023-12-15-13-17-23.png)

![](assets/2023-12-15-13-17-48.png)

![](assets/2023-12-15-13-18-49.png)

![](assets/2023-12-15-13-19-46.png)

![](assets/2023-12-15-13-21-40.png)

![](assets/2023-12-15-13-22-03.png)

![](assets/2023-12-15-13-22-49.png)

![](assets/2023-12-15-13-23-16.png)

![](assets/2023-12-15-13-25-17.png)

