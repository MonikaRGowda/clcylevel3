
# Monika R-Level 3 Report 
## TASK 1: AWS Lambda
AWS Lambda is a serverless compute service that automatically runs code in response to events, without requiring you to manage the underlying infrastructure. It takes out the burden of provisioning, managing, and scaling servers, helping to focus on writing code. Through this task it was possible to understand how AWS lambda helps in making deploying and scaling of projects easier. I created three different lambda functions for connect,disconnect and message sending, API Gateway WebSocket for real time connection between clients and backend server and S3 buckets for static hosting.

![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/aws_lambda-2.png?token=GHSAT0AAAAAADJXOF3HKXE4MNUWKEW7XLEK2FXCEKQ)
![image]([https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/aws_lambda-1.png?token=GHSAT0AAAAAADJXOF3GRMSQN6CIVRQGWADQ2FXCEHA](https://github.com/MonikaRGowda/clcylevel3/blob/main/aws_lambda-1.png?raw=true))


## TASK 2: CI/CD (Continuous Integration & Continuous Delivery) - Intro to Jenkins
Jenkins is a powerfull tool that automates CI/CD pipelines allowing developers to just implement codes in github whike the rest is handled by Jenkins as it connects with GitHub/GitLab/Bitbucket, runs your build, runs tests and deploys to servers or cloud.
Pipelines- A Jenkinsfile defines CI/CD steps as code, so it’s repeatable and version-controlled.It provides a workflow, including building code, running tests, deploying applications, and more.
Continuous Integration- Jenkins replaces manual pulling, building, and testing and every push is tested in the same environment (agent) and runs your build tool thus developers immediately know if their change broke the system and executes automated tests.
Continuous Delivery- After CI succeeds, the build is packaged and then deployed through target environment.
In this task,I set up and ran a CI/CD pipeline for a java file of tic-tac-toe in Jenkins
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-1.png?token=GHSAT0AAAAAADJXOF3GODPZZLRBQ73ROXEK2FXCEPA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-3.png?token=GHSAT0AAAAAADJXOF3GWAFI64XLFZUZETP42FXCEUQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-2.png?token=GHSAT0AAAAAADJXOF3GTD5ZYRU6IFU77EBK2FXCERA)


## TASK 3: SSH
The Secure Shell Protocol is a cryptographic network protocol for operating network services securely over an unsecured network.
In this task, I created two EC2 instances and copied files from source server to destination server so that we can login to source server through the other server.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/ssh-2.png?token=GHSAT0AAAAAADJXOF3HXWMWNGBIGMGXSWTK2FXCHBA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/ssh-1.png?token=GHSAT0AAAAAADJXOF3GYJAZ3KKUMKJTY7UO2FXCG7A)


## TASK 4: Terraform
Terraform is an Infrastructure as Code (IaC) tool.It creates and manages resources on cloud platforms and other services through APIs. It provides automation, consistency, version control, multi-cloud service, scalability.In this task, I built, change, and destroy EC2 using Terraform. 
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-3.png?token=GHSAT0AAAAAADJXOF3GIDUYZK7JNES2BGTW2FXCISQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-4.png?token=GHSAT0AAAAAADJXOF3GSPSKQDZIYM7RFQWS2FXCIWQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-5.png?token=GHSAT0AAAAAADJXOF3H6TL3ZC437IY46NHU2FXCI6A)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-6.png?token=GHSAT0AAAAAADJXOF3GN6VQBSBPHWVY5M2Y2FXCJDQ)
