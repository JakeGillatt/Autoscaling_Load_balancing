# Auto Scaling & Load Balancing
#
# What are Load balancers?

a load balancer is a service that helps distribute incoming network traffic across multiple servers or instances. The purpose of a load balancer is to ensure that all the instances in a group receive roughly equal amounts of traffic and prevent any single instance from becoming overwhelmed and causing a bottleneck.

#
# What is Auto Scaling?

One of the purposes of Auto scaling is to terminate broken instances and re-load fresh instances in their place. The load balancer can then re-direct traffic from the broken instance to the new instance. Another reason auto scaling is used, is to moniter the current load of an instance and create further instances if neccissary. For example, if the CPU load of an instance reaches 50% or greater, a new instance can be created, and traffic will then be diverted there via the load balancer. They can also shut down instances if they are not required. This process can save a company money by only keeping the instances that are required at any one time, in operation.

#
# Auto Scaling Diagram:

![autoscale-diagram](https://user-images.githubusercontent.com/129315605/234577796-89096561-7401-4b83-80b5-d324c37a610f.png)

#
# Launching two instances with Auto scaling and Load balancing

1. On AWS in the EC2 dashboard, select 'Launch templates' then 'Create launch template'
- Name the template
- Tick provide guidance
- Select the AMI
- Select the Key-Pair
- Select the security group
- Edit the user data and add the following:
```
HAS NOT BEEN VERIFIED YET
```
- Create the template
2. On the EC2 dashboard select 'Auto scaling groups' and 'Create auto scaling group'
- Name the group
- Leave the vpc as default or select a vpc if using one
- Select the regions you reuire, e.g - 1a, 1,b ,1c
- Select a new load balancer with HTTP/S
- Select Internet facing
- Create a target group
- Tick Elastic load balancing
- Health grace can be 300
- Select Next
- Set the desired, min and max instances you want
- Tick target tracking monitering CPU load, 50%
- Select Next two pages over
- Add tags: Key=Name - 'Jake-tech221-asg-alb'
- Select Create ASG
