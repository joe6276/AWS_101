# Firewalls

![image_73.png](image_73.png)

If you application is running on port 443 then we need to make sure that we only allow traffic from that port
and not from other ports. That's where firewalls comes in  


Firewalls monitor traffic and only allow traffic permitted by a set of predefined rules.

Firewalls rules are broken down into  inbound and outbound rules.

**Inbound rules** - are a set of rules that defines what traffic is allowed from the internet into the resources protected by the firewall

**Outbound rules** - are a set of rules that define the traffic allowed to the internet 

## Stateless Firewalls

a Stateless firewall is configured to allow both inbound & outbound traffic.

![image_74.png](image_74.png)


## Stateful Firewalls
Stateful firewalls are intelligent enough to understand which request and response are part of the same direction.

If a request is permitted the response is automatically permitted as well in a stateful firewall.

![image_75.png](image_75.png)

## Network Access Control List (NACL)

NACls filter traffic entering and leaving a subnet.

NACLs do not filter traffic within a subnet ( If you have two server on one subnet they can talk to each other)

NACs are stateless firewalls so rules must be set for both inbound and outbound traffic.

![image_76.png](image_76.png)

## Security Groups

Security groups acts as a firewall for individual resources (EC2, LB, RDS)

Security groups are stateful so only the request needs to be allowed.

### NACLS VS Security Groups
![image_77.png](image_77.png)


Her is like the whole picture of Networking
![image_78.png](image_78.png)