1. Create S3 Images storage and add the following to bucket policy:
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::<bucket-name>/<folder>/*"
        }
    ]
}
    ** Upload some images having number 0-9 as filename and extension name "jpg" 


2. Copy the ssh key file to webapp/modules/aws_ec2/
3. in tf_aws directory >>

3. Run: terraform init
4. Run: terraform apply

5. change directory to 'webapp'
6. Run: terraform init
7. Run: terraform plan
8. Run: terraform apply
9. Open the load balancer DNS name





3. To reload module
  - terraform init -upgrade
  - 
  4. To show traffic behind load balancer
  
Go to aws_ec2 directory || sudo chmod 400 shubhamkey.pem|| Copy key to Bastion Public IP > scp -i shubhamkey.pem shubhamkey.pem ec2-user@50.16.98.253:
|| ssh to bastion > ssh -i shubhamkey.pem ec2-user@50.16.98.253 (Public IP of Bastion)
From bastion SSH to load balancer instance unamed.
sudo su
cd /var/log/httpd/
tail -f access_log

5. To show autoscaling, Go to Load balancer and then auto scaling group.
6. To deploy staging,prod and dev, uncomment the required one in aws_vpc2 >> variables.tf