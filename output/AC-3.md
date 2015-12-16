# AC-3
## Addressed by:
 - Application Security Groups
 - Identity and Access Management


- Within the CF PaaS, Cloud Foundry uses security groups to act as firewalls to control outbound applications in the deployment. 18F uses Cloud Foundry ASGs to specify egress access rules for its applications. This functionality enables 18F to securely restrict application outbound traffic to predefined routes.       
- Cloud Foundry evaluates security groups and other network traffic rules in a strict priority order. Cloud Foundry returns an allow, deny, or reject result for the first rule that matches the outbound traffic request parameters, and does not evaluate any lower-priority rules
- Cloud Foundry implements network traffic rules using Linux iptables on the component VMs. Operators can configure rules to prevent system access from external networks and between internal components, and to restrict applications from establishing connections over the DEA network interface.





- 18F follows and implements AWS IAM  best practices by implementing the majority of the following&colon;
  - Create individual accounts for anyone that requires access to the AWS infrastructure or APIs or use IAM federation from enterprise identity management system
  - Use groups or roles to assign permissions to IAM users
  - Enable multi factor authentication for all IAM users
  - Use roles for applications that run on EC2 instances
  - Delegate by using roles instead of sharing credentials
  - Rotate credentials regularly




