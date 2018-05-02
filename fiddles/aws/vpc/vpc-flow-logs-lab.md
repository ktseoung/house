<img src="https://i.imgur.com/4x1VSb6.png" height="100" title="AWS VPC" />


VPC Flow Logs Lab
======

4 minute lecture / lab on VPC Flow Logs.  For this one, I just took notes.
 
  
## Video Link

[![acloud.guru lecture](https://i.imgur.com/OM6IIGp.png)](https://acloud.guru/course/aws-certified-solutions-architect-associate/learn/vpc/49df150b-19b2-2fcd-a077-edb27dae6201/watch)

*Note - You will need an [acloud.guru](acloud.guru) account.*


## What are VPC Flow logs?

VPC Flow logs is a feature that enables you to capture information about the IP traffic going to and from 
your network interface in your VPC. Flow log data is stored using Amazon CloudWatch logs.  After you've 
created a flow log, you can view and retrieve data in the Amazon CloudWatch Logs.

Flow logs can be created at 3 levels:

* VPC 
* Subnet
* Network Interface Level


## Exam Tips

What did we learn?

* You cannot enable flow logs for VPCs that are peered with your VPC unless the peer VPC is in your account
* You cannot tag a flow log
* After you created a flow log, you cannot change its configuration; for example you can't associate a 
  different IAM role with the flow log
* Not all IP Traffic is monitored, including:
  * Traffic generated by instances when they contact the Amazon DNS server. _Note - If you use your own DNS server, then
    all traffic to that DNS server is logged_
  * Traffic generated by a Windows instance for Amazon Windows license activation 
  * Traffic to and from 169.254.169.254 for instance metadata
  * DHCP traffic
  * Traffic to the reserved IP address for the default router
     
   
### Review Questions

1.  What is a flow log?
2.  What type of traffic can it capture? (3 types)
3.  Before you can create a flow log using the VPC wizard, what must you do?
4.  How can flow logs be integrated with Lambda?
5.  What constraint is there on enabling flow logs for peered VPCs?
6.  Can flow logs be tagged?
7.  Once configured can a flow log be easily reconfigured?


### Answers

1.  IP traffic log tied to a VPC.
2.  Accepted / Rejected / All
3.  Create a Log Group in CloudWatch
4.  In CloudWatch you select to "stream the log to Lambda"
5.  They must be under your account
6.  No
7.  No

 
## 

**[Previous Lab/Lecture](vpc-load-balancer-lab.md) | [AWS (root)](../readme.adoc) | [Next Lab/Lecture](vpc-nat-vs-bastion.md)**







