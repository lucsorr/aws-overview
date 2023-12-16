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

![Image](assets/2023-12-14-21-43-30.png)

![Image](assets/2023-12-14-21-45-51.png)

![Image](assets/2023-12-14-21-47-11.png)

![Image](assets/2023-12-14-21-48-25.png)

![Image](assets/2023-12-14-21-49-55.png)

![Image](assets/2023-12-14-21-52-37.png)

![Image](assets/2023-12-14-21-54-10.png)

![Image](assets/2023-12-14-21-55-17.png)

## Connecting to an EC2 instance; Vertically scaling an EC2 instance

![Image](assets/2023-12-15-12-46-32.png)

![Image](assets/2023-12-15-12-47-01.png)

![Image](assets/2023-12-15-12-47-26.png)
![Image](assets/2023-12-15-12-47-40.png)
![Image](assets/2023-12-15-12-47-58.png)
![Image](assets/2023-12-15-12-48-11.png)


![Image](assets/2023-12-15-12-53-38.png)

![Image](assets/2023-12-15-12-55-30.png)

![Image](assets/2023-12-15-12-55-50.png)
![Image](assets/2023-12-15-12-56-13.png)
![Image](assets/2023-12-15-12-56-45.png)
![Image](assets/2023-12-15-12-57-23.png)

![Image](assets/2023-12-15-12-57-48.png)

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

![Image](assets/2023-12-15-13-00-32.png)

![Image](assets/2023-12-15-13-03-07.png)
![Image](assets/2023-12-15-13-03-19.png)

![Image](assets/2023-12-15-13-03-47.png)
![Image](assets/2023-12-15-13-04-43.png)

## Networking concepts

- Configure a routing table and attach an internet gateway
- Configure a security group

![Image](assets/2023-12-15-13-13-34.png)

![Image](assets/2023-12-15-13-14-03.png)
![Image](assets/2023-12-15-13-14-21.png)
![Image](assets/2023-12-15-13-14-33.png)

![Image](assets/2023-12-15-13-15-19.png)

![Image](assets/2023-12-15-13-17-23.png)

![Image](assets/2023-12-15-13-17-48.png)

![Image](assets/2023-12-15-13-18-49.png)

![Image](assets/2023-12-15-13-19-46.png)

![Image](assets/2023-12-15-13-21-40.png)

![Image](assets/2023-12-15-13-22-03.png)

![Image](assets/2023-12-15-13-22-49.png)

![Image](assets/2023-12-15-13-23-16.png)

![Image](assets/2023-12-15-13-25-17.png)

## Coonecting VPCs

![Image](assets/2023-12-15-16-23-34.png)

![Image](assets/2023-12-15-16-25-14.png)

![Image](assets/2023-12-15-16-25-36.png)

![Image](assets/2023-12-15-16-26-01.png)

![Image](assets/2023-12-15-16-26-11.png)

![Image](assets/2023-12-15-16-26-26.png)

![Image](assets/2023-12-15-16-26-42.png)

![Image](assets/2023-12-15-16-26-53.png)

![Image](assets/2023-12-15-16-27-05.png)

![Image](assets/2023-12-15-16-27-20.png)

![Image](assets/2023-12-15-16-27-36.png)


![Image](assets/2023-12-15-16-35-03.png)

(If a EC2 instance has no public IP address, this is because it was created in a private subnet.)

![Image](assets/2023-12-15-16-39-19.png)

![Image](assets/2023-12-15-16-39-29.png)

from the EC2 cli, enter `ping <ip>` to check private connection between current and other vpc

![Image](assets/2023-12-15-16-40-45.png)

![Image](assets/2023-12-15-16-42-26.png)

You can identify internet gateways by id `igw-xxx...`

![Image](assets/2023-12-15-16-43-54.png)

![Image](assets/2023-12-15-16-44-25.png)

![Image](assets/2023-12-15-16-46-07.png)

![Image](assets/2023-12-15-16-47-46.png)

![Image](assets/2023-12-15-16-53-01.png)

![Image](assets/2023-12-15-16-53-19.png)

![Image](assets/2023-12-15-16-57-12.png) 
(they remember who came in, and who came out)

![Image](assets/2023-12-15-16-58-25.png)

![Image](assets/2023-12-15-17-04-08.png)

## Databases in practice

![Image](assets/2023-12-16-01-25-46.png)

...

![Image](assets/2023-12-16-01-26-13.png)

![Image](assets/2023-12-16-01-26-28.png)

![Image](assets/2023-12-16-01-26-39.png)

![Image](assets/2023-12-16-01-26-54.png)

![Image](assets/2023-12-16-01-27-06.png)

![Image](assets/2023-12-16-01-27-22.png)

![Image](assets/2023-12-16-01-28-37.png)

![Image](assets/2023-12-16-01-29-32.png)

![Image](assets/2023-12-16-01-30-02.png)

![Image](assets/2023-12-16-01-30-27.png)

![Image](assets/2023-12-16-01-30-52.png)

![Image](assets/2023-12-16-01-32-39.png)

![Image](assets/2023-12-16-01-33-01.png)

![Image](assets/2023-12-16-01-34-28.png)

## NoSQL Databases

![Image](assets/2023-12-16-01-54-57.png)

![Image](assets/2023-12-16-01-55-14.png)

![Image](assets/2023-12-16-01-55-52.png)

![Image](assets/2023-12-16-01-56-07.png)

![Image](assets/2023-12-16-01-56-20.png)

![Image](assets/2023-12-16-01-56-33.png)

![Image](assets/2023-12-16-01-56-47.png)

![Image](assets/2023-12-16-01-56-57.png)

![Image](assets/2023-12-16-01-57-36.png)

![Image](assets/2023-12-16-01-58-04.png)

![Image](assets/2023-12-16-01-58-27.png)

![Image](assets/2023-12-16-02-00-20.png)

![Image](assets/2023-12-16-02-01-24.png)

![Image](assets/2023-12-16-02-02-29.png)

![Image](assets/2023-12-16-02-03-57.png)

![Image](assets/2023-12-16-02-04-09.png)

![Image](assets/2023-12-16-02-05-16.png)

![Image](assets/2023-12-16-02-05-58.png)

![Image](assets/2023-12-16-02-06-17.png)

## File systems in the cloud

![Image](assets/2023-12-16-15-00-51.png)

![Image](assets/2023-12-16-15-01-03.png)

![Image](assets/2023-12-16-15-01-14.png)

![Image](assets/2023-12-16-15-01-23.png)

![Image](assets/2023-12-16-15-01-33.png)

![Image](assets/2023-12-16-15-06-15.png)

![Image](assets/2023-12-16-15-07-35.png)

![Image](assets/2023-12-16-15-08-11.png)

![Image](assets/2023-12-16-15-08-55.png)

![](assets/2023-12-16-15-14-07.png)

![](assets/2023-12-16-15-14-58.png)

![](assets/2023-12-16-15-16-19.png)

![](assets/2023-12-16-15-17-07.png)

![](assets/2023-12-16-15-18-57.png)

![](assets/2023-12-16-15-31-16.png)

![](assets/2023-12-16-15-31-30.png)

![](assets/2023-12-16-15-32-17.png)

![](assets/2023-12-16-15-32-52.png)

![](assets/2023-12-16-15-34-07.png)

(Remember:)
![](assets/2023-12-16-15-34-45.png)

![](assets/2023-12-16-15-35-31.png)

![](assets/2023-12-16-15-38-19.png)

![](assets/2023-12-16-15-38-38.png)

![](assets/2023-12-16-15-39-26.png)

![](assets/2023-12-16-15-40-12.png)

![](assets/2023-12-16-15-41-00.png)

![](assets/2023-12-16-15-41-44.png)

![](assets/2023-12-16-15-44-32.png)

## Auto-Healing and Scaling Applications

![](assets/2023-12-16-15-57-48.png)

![](assets/2023-12-16-16-11-53.png)

![](assets/2023-12-16-16-12-05.png)

![](assets/2023-12-16-16-12-28.png)

![](assets/2023-12-16-16-12-45.png)

![](assets/2023-12-16-16-12-57.png)

![](assets/2023-12-16-16-13-06.png)

![](assets/2023-12-16-16-13-23.png)

![](assets/2023-12-16-16-13-33.png)

![](assets/2023-12-16-16-14-10.png)




















