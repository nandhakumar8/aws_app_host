[Previous: Introduction About Architecture](readme.md)

## 1. DataBase Creation

#### 1. Create DataBase Subnet Group

1. Give Subnet Name and Description
2. Choose VPC.

![alt text](images/dbs1.0.png)

3. Choose Availability Zones and Subnets

![alt text](images/dbs1.1.png)
![alt text](images/dbs1.2.png)

Click **Create**

#### 2. Create DataBase
Create Two DataBase one for production server and another for disaster recovery server

#### For Production Server:
   Goto **RDS**, Click Create DataBase.

1. Creation Method – Standard

2. Choose DataBase Engine - MySQL

![alt text](images/db1.1.0.png)

3. Choose Engine Version

![alt text](images/db1.1.1.png)

4. Template – Free Tier

![alt text](images/db1.1.2.png)

5. DB Instance Identifier - prdb

![alt text](images/db1.1.3.png)

6. Credentials,
 	Master UserName : pradmin
	Password	         : prdb1234


![alt text](images/db1.1.4.png)

7. Choose Instance configuration,

![alt text](images/db1.1.5.png)

8. Enable Storage AutoScaling,

![alt text](images/db1.1.6.png)

9. Choose VPC, DB Subnet Group.

![alt text](images/db1.1.7.png)

10. Public Access : No
    VPC Security Group : **alltraffic**
    Others Kept as defaults.


![alt text](images/db1.1.8.png)
![alt text](images/db1.1.9.png)

11. Additional configuration
    initial database name : prdb


![alt text](images/db1.1.10.png)
![alt text](images/db1.1.11.png)

Click **Create** .

#### For Disaster Recovery

1. **Settings**

   DB instance identifier - drdb

![alt text](images/db1.2.0.png)


2. Credential settings,
	Master UserName : dradmin
	password	       : drdb1234

![alt text](images/db1.2.1.png)

3. Initial DatabaseName : drdb


![alt text](images/db1.2.2.png)


Others same as production.



[Next: 2. IAM Role Creation](iam.md)