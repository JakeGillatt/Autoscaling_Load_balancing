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
