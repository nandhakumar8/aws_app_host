[Previous: 2. IAM Role Creation](ec2.md)

## 3. EC2 Instance Creation

##### Security Group:

	Name         : alltraffic
	Inbound Rule : alltraffic
##### EC2 Creation

1. CREATE TWO EC2 WITH
    IAM Role : **fullaccess**
	Security Group: **alltraffic**
    ADD **USER DATA** UNDER ADVANCED SECTION

**User Data:**

```sh

#!/bin/bash
yum install httpd php8.1 php8.1-mysqlnd.x86_64 -y
cd /var/www/html
echo "healthy" > healthy.html
wget https://wordpress.org/latest.tar.gz
tar -xzf latest.tar.gz
cp -r wordpress/* /var/www/html/
rm -rf wordpress
rm -rf latest.tar.gz
chmod -R 755 wp-content
chown -R apache:apache wp-content
chkconfig httpd on
service httpd start

```


[Next: 4. WordPress Configuration](wp.md)