# SC-7
## Addressed by:
 - Access Control List
 - Sophos UTM
 - Amazon Elastic Compute Cloud
 - Amazon Virtual Private Cloud
 - Application Security Groups


## SC-7 a
- ACLs, or traffic flow policies, are established on each managed interface, which manage and enforce the flow of traffic.





## SC-7 a
- Sophos UTM 9 for AWS is deployed and configured on all instances


## SC-7 b
- Sophos UTM 9 Endpoint Protection is deployed and configured on all instances.





## SC-7 a
- Man in the Middle (MITM) Attacks. All of the AWS APIs are available via SSL-protected endpoints which provide server authentication. Amazon EC2 AMIs automatically generate new SSH host certificates on first boot and log them to the instance’s console. 18F can then use the secure APIs to call the console and access the host certificates before logging into the instance for the first time. 18F uses SSL for all interactions with AWS.
- IP Spoofing. Amazon EC2 instances cannot send spoofed network traffic. The AWS-controlled, host-based firewall infrastructure will not permit an instance to send traffic with a source IP or MAC address other than its own.
- Amazon EC2 provides a complete firewall solution; this mandatory inbound firewall is configured in a default deny-all mode and Amazon EC2 customers must explicitly open the ports needed to allow inbound traffic. The traffic may be restricted by protocol, by service port, as well as by source IP address (individual IP or Classless Inter-Domain Routing (CIDR) block).





## SC-7 b
- 18F utilizes the AWS Virtual Private Cloud (VPC), which provides a private subnet within the AWS cloud. Each VPC is configured to utilize Routing Rules, Subnet Rules, and Security Group Rules. Each of these controls must have appropriate rules and routes in-place before any external service is able to reach a host within AWS.
  - Each VPC is configured to utilize Routing Tables, and Security Groups.  Each of these controls must have appropriate rules and routes in-place before any external service is able to reach a host within Cloud Foundry.
  - Sophos UTM 9 Endpoint Protection is deployed and configured on all instances.
  - Host Based Firewall rules are enforced to provide security in depth
  - Each Amazon VPC is a distinct, isolated network within the cloud; network traffic within each Amazon VPC is isolated from all other Amazon VPCs





## SC-7 a
- Cloud Foundry implements network traffic rules using Linux iptables on the component VMs. Operators can configure rules to prevent system access from external networks and between internal components, and to restrict applications from establishing connections over the DEA network interface.
- Cloud Foundry recommends that you use Cloud Foundry ASGs to specify egress access rules for your applications. This functionality enables you to more securely restrict application outbound traffic to predefined routes.
- Spoofing: If an IP, MAC, or ARP spoofing attack bypasses the physical firewall for the deployment, Cloud Foundry network traffic rules help prevent the attack from accessing application containers. Cloud Foundry uses application isolation, operating system restrictions, and encrypted connections to further mitigate risk.




