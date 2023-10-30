# Infrastructure:

The infrastructure set up:

1. VPC
   1. Two public subnets
   2. One private subnet.
2. Autoscaling Group with Load balancer
   1. Minimum of two EC2s.
   2. Desired two EC2s.
   3. Maximum of three.
3. Two web page EC2s in public subnet connecting to database EC2 in private subnet.

Database needs to be running first.

### AMI

```
ami-0136ddddd07f0584f
```

```
#!/bin/bash

cd /home/ubuntu

export DB_HOST=mongodb://10.0.4.196:27017/posts

cd /home/ubuntu/repo/app

sudo npm install

pm2 kill

pm2 start app.js
```