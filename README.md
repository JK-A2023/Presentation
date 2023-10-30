# Infrastructure:

The purpose of my project was to create a publicly accessible webpage. I wanted it to request data, while shielding the database. I wanted protection in the case the webpage virtual machines were to fail or grow unhealthy for any reason. And so I made the autoscaling group would spin up another machine in this case. I've made a load balancer that would then spread the traffic out evenly between the remaining healthy machines, and the newly spun up machine.

## Setup:

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

## Blockers:

1. Outdated NodeJS application on Ubuntu 20.04 LTS.
2. Requiring at least 2 Public Subnets for ASG.