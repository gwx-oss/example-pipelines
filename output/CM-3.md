# CM-3
## Addressed by:
 - S3
 - AWS Config
 - Cloud Formation


## CM-3 a
Records of configuration-controlled changes are retained for at least 1 year in accordance with the 18F Configuration Management policy and utilizing the 18F GitHub site and AWS S3 to store all changes requested, approved, disapproved, implemented and pending.




## CM-3 c
- For changes related to the AWS infrastructure, 18F uses AWS Service Catalog, AWS Config, VisualOps and AlienVault USM for AWS for real-time configuration changes which are documented, approved and tracked within GitHub.


## CM-3 a
- 18F uses several version control systems(i.e. AWS Config, AWS Service Catalog) with its templates to know exactly what changes were made, who made them, and when. If at any point 18F needs to reverse changes to infrastructure, you can use a previous version of a template.





- 18F provisions its infrastructure with AWS CloudFormation, the AWS CloudFormation template describes exactly what resources are provisioned and their settings. Because these templates are text files, 18F can simply track differences in these templates to track changes to its infrastructure, similar to the way developers control revisions to source code.
- 18F uses several version control systems(i.e. AWS Config, AWS Service Catalog) with its templates to know exactly what changes were made, who made them, and when. If at any point 18F needs to reverse changes to infrastructure, you can use a previous version of a template.




