[Next: 6. Route53 Setup ](r53.md)

##  7. Server Synchronization

#### Create S3

1. Provide Bucket Name,

![alt text](images/s1.0.png)


2. Enable **Public Access**

![alt text](images/s1.1.png)

![alt text](images/s1.2.png)

![alt text](images/s1.3.png)

Click **Create Bucket**

#### Create Cronjob to synchronize Servers and S3

In **Pr** Instance,


*/2  * * * * aws s3 sync --delete /var/www/html/ s3://nkbuck


In **Dr** Instance,


*/2  * * * * aws s3 sync --delete s3://nkbuck /var/www/html/


dr.vithaivirucham.shop

![alt text](images/r1.9.png)


