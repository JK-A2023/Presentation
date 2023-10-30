# Infrastructure:

I have set up the following infrastructure:

1. Virtual Private Cloud:
   1. Two public subnets
   2. One private subnet.
2. Autoscaling Group with Load balancer
   1. Minimum of two EC2s.
   2. Desired two EC2s.
   3. Maximum of three.
3. Two web page EC2s in public subnet.
4. EC2 in private subnet.

The purpose of this infrastructure it to create a publically accessible webpage, while shielding the database. If the webpage virtual machines were to fail or grow unhealthy for any reason, the autoscaling group would spin up another machine. The load balancer would then drive spread the traffic out evenly between the remaining healthy machines, and the newly spun up machine.