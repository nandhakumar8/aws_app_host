[Previous: 3. EC2 Instance Creation](ec2.md)
## 4. WordPress Configuration

##### Production Server
Ping production machine public ip in browser.
![alt text](images/wpc1.0.png)

##### Disaster Server
Ping disaster recovery machine public ip in browser.
![alt text](images/wpc1.1.png)

Provide production DB details


![alt text](images/wpc1.2.png)

Provide disaster DB details

![alt text](images/wpc1.3.png)

Copy the **php script** and write it to on both linux server like vi **wp-config.php**

 In word press installed path cd **/var/www/html/**

![alt text](images/wpc1.4.png)


![alt text](images/wpc1.5.png)

click **Submit** .


![alt text](images/wpc1.6.png)

![alt text](images/wpc1.7.png)

![alt text](images/wpc1.8.png)

![alt text](images/wpc1.9.png)

![alt text](images/wpc1.10.png)

![alt text](images/wpc1.11.png)

![alt text](images/wpc1.12.png)

![alt text](images/wpc1.13.png)



[Next: 5. Load Balancer Creation](lb.md)