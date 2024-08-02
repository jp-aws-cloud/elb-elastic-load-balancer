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

> There is a key difference in how the load balancer types are configured. With `Application Load Balancers`, `Network Load Balancers`, and `Gateway Load Balancers`, instances are registered as targets with a `target group`, and you route traffic to the target group. 

> With `Classic Load Balancers`, instances are registered directly with the load balancer.

## Application Load Balancer
Routes and load balances at the application layer (HTTP/HTTPS), and supports path-based routing. An Application Load Balancer can route requests to ports on one or more registered targets, such as EC2 instances, in your virtual private cloud (VPC).

## Network Load Balancer
Routes and load balances at the transport layer (TCP/UDP Layer-4), based on address information extracted from the Layer-4 header. Network Load Balancers can handle traffic bursts, retain the source IP of the client, and use a fixed IP for the life of the load balancer.

## Gateway Load Balancer
Distributes traffic to a fleet of appliance instances. Provides scale, availability, and simplicity for third-party virtual appliances, such as firewalls, intrusion detection and prevention systems, and other appliances. Gateway Load Balancers work with virtual appliances that support the GENEVE protocol. Additional technical integration is required, so make sure to consult the user guide before choosing a Gateway Load Balancer.

## Classic Load Balancer
Routes and load balances either at the transport layer (TCP/SSL), or at the application layer (HTTP/HTTPS).