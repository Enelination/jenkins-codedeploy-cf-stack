# Jenkins-codedeploy-cf-stack
This stack tool that creates the following resources:
## Installation

Amazon S3 bucket—Stores the GitHub repository files and the CodeBuild artifact application file that CodeDeploy uses.

IAM S3 bucket policy—Allows the Jenkins server access to the S3 bucket.

JenkinsRole—An IAM role and instance profile for the Amazon EC2 instance for use as a Jenkins server. This role allows Jenkins on the EC2 instance to access the S3 bucket to write files and access to create CodeDeploy deployments.

CodeDeploy application and CodeDeploy deployment group.

CodeDeploy service role—An IAM role to enable CodeDeploy to read the tags applied to the instances or the EC2 Auto Scaling group names associated with the instances.

CodeDeployRole—An IAM role and instance profile for the EC2 instances of CodeDeploy. This role has permissions to write files to the S3 bucket created by this template and to create deployments in CodeDeploy.

CodeBuildRole—An IAM role to be used by CodeBuild to access the S3 bucket and create the build projects.

Jenkins server—An EC2 instance running Jenkins.

CodeBuild project—This is configured with the S3 bucket and S3 artifact.

Auto Scaling group—Contains EC2 instances running Apache and the CodeDeploy agent fronted by an Elastic Load Balancer.

Auto Scaling launch configurations—For use by the Auto Scaling group.

Security groups—For the Jenkins server, the load balancer, and the CodeDeploy EC2 instances.
