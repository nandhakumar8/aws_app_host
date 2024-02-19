[Previous: 4. WordPress Configuration](wp.md)

## 5. Create Classic Load Balancer

1. Give Load Balancer Name
![alt text](images/clb1.0.png)

2. Select **VPC and AZ** 

![alt text](images/clb1.1.png)

3. Choose **alltraffic** Security Group 

![alt text](images/clb1.2.png)

4. Change health check html file name as **healthy.html**

![alt text](images/clb1.3.png)

5. Add **pr** instance

![alt text](images/clb1.4.png)

Similarly, Create another Classic Load Balancer for **dr** instance





[Next: 6. Route53 Setup](r53.md)