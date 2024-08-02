# Use Elastic Load Balancing

to distribute incoming application traffic in your Auto Scaling group.

ELB(Elastic Load Balancing) automatically distributes your incoming application traffic across all the EC2 instances that you are running. 

`Elastic Load Balancing` helps to manage incoming requests by optimally routing traffic so that no one instance is overwhelmed.

> To use Elastic Load Balancing with your `Auto Scaling group`, attach the load balancer to your Auto Scaling group.

> This registers the group with the `load balancer`, which acts as a single point of contact for all incoming web traffic to your Auto Scaling group.

## Contents
- Elastic Load Balancing types
- repare to attach a load balancer
- Attach a load balancer
- Configure a load balancer
- Verify the attachment status
- Add Availability Zones
- AWS CLI examples for working with Elastic Load Balancing

# Elastic Load Balancing types

Elastic Load Balancing provides four types of load balancers that can be used with your Auto Scaling group: 
1. Application Load Balancers
2. Network Load Balancers
3. Gateway Load Balancers
4. Classic Load Balancers.