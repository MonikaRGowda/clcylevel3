
# Monika R-Level 3 Report 
## TASK 1: AWS Lambda
AWS Lambda is a serverless compute service that automatically runs code in response to events, without requiring you to manage the underlying infrastructure. It takes out the burden of provisioning, managing, and scaling servers, helping to focus on writing code. Through this task it was possible to understand how AWS lambda helps in making deploying and scaling of projects easier. I created three different lambda functions for connect, disconnect and message sending, API Gateway WebSocket for real time connection between clients and backend server and S3 buckets for static hosting.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/aws_lambda-2.png?token=GHSAT0AAAAAADSDEC7EQVUUZKAY2IOMXPH62LPOHTQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/aws_lambda-2.png?token=GHSAT0AAAAAADSDEC7FDTT57DJ5JSFVQH262LPOIHA)


## TASK 2: CI/CD (Continuous Integration & Continuous Delivery) - Intro to Jenkins
Jenkins is a powerfull tool that automates CI/CD pipelines allowing developers to just implement codes in github whike the rest is handled by Jenkins as it connects with GitHub/GitLab/Bitbucket, runs your build, runs tests and deploys to servers or cloud.
Pipelines- A Jenkinsfile defines CI/CD steps as code, so it’s repeatable and version-controlled.It provides a workflow, including building code, running tests, deploying applications, and more.
Continuous Integration- Jenkins replaces manual pulling, building, and testing and every push is tested in the same environment (agent) and runs your build tool thus developers immediately know if their change broke the system and executes automated tests.
Continuous Delivery- After CI succeeds, the build is packaged and then deployed through target environment.
In this task, I set up and ran a CI/CD pipeline for a java file of tic-tac-toe in Jenkins
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-1.png?token=GHSAT0AAAAAADSDEC7FXSZAOLPS36AUSWIK2LPOOZQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-3.png?token=GHSAT0AAAAAADSDEC7FHAOB2P4HKJAUPHAA2LPOPEQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/jenkins-2.png?token=GHSAT0AAAAAADSDEC7ENXENCA2PDMJZHTFI2LPOO5A)


## TASK 3: SSH
The Secure Shell Protocol is a cryptographic network protocol for operating network services securely over an unsecured network.
In this task, I created two EC2 instances and copied files from source server to destination server so that we can login to source server through the other server.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/ssh-2.png?token=GHSAT0AAAAAADSDEC7FDAXNAG2WANHJRTIS2LPOP6A)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/ssh-1.png?token=GHSAT0AAAAAADSDEC7FTGGIV3WVP2AXWJLM2LPOP2Q)


## TASK 4: Terraform
Terraform is an Infrastructure as Code (IaC) tool. It creates and manages resources on cloud platforms and other services through APIs. It provides automation, consistency, version control, multi-cloud service, scalability. In this task, I built, change, and destroy EC2 using Terraform. 
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-3.png?token=GHSAT0AAAAAADSDEC7E7KJMMBW7HVSWIZSS2LPOT7A)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-4.png?token=GHSAT0AAAAAADSDEC7FZ4WZ55GEUMLXBPEI2LPOUCA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-5.png?token=GHSAT0AAAAAADSDEC7EECKACWRL2GQHA2V42LPOUFA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/terraform-6.png?token=GHSAT0AAAAAADSDEC7FJZ5NCZPTD4ROBXOY2LPOUIA)


## TASK 5: Wireshark
Wireshark is used for network troubleshooting, analysis, software and communications protocol development. It captures data from network interfaces and displays the raw traffic in a readable format.

We captured real network traffic and captured live Wi-Fi traffic using Wireshark. It helped in observing real packets instead of simulated data
Using filters and packet analysis, we detected TCP retransmissions, observed duplicate acknowledgements, identified out-of-order packets and found SYN retransmissions which helped us to see issues like packet loss, network congestion, Wi-Fi instability and connection setup failures.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-2.png?token=GHSAT0AAAAAADSDEC7EPO7TPKD5BDW4BMLI2LPOVLA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-1.png?token=GHSAT0AAAAAADSDEC7ENX7CBCSLWQ5563QO2LPOVHQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-3.png?token=GHSAT0AAAAAADSDEC7F4QZKXEGBF7EWMK2I2LPOVOQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-4.png?token=GHSAT0AAAAAADSDEC7FXVRASV5Q6KBM64AY2LPOVSA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-6.png?token=GHSAT0AAAAAADSDEC7E2UEXXLKVZCN4UMVI2LPOVZA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/wireshark-5.png?token=GHSAT0AAAAAADSDEC7EDAYQKNOXGPCMTV3I2LPOVWA)

## TASK 6: Docker
Docker enables developers to build, share, and run applications by packaging them into standardized, isolated environments called containers. We learnt what Docker is and how it packages an application and its dependencies into containers for execution across different platforms. Also executed basic Docker commands such as docker run, docker images, and docker ps to manage containers and images.
I was able to successfully ran the hello-world container and run sample containers like Ubuntu and welcome-to-docker to understand container isolation, port mapping, and interaction using Docker Desktop.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/docker-2.png?token=GHSAT0AAAAAADSDEC7EAS5ERONNX2EXIVCG2LPOJ3A)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/docker-3.png?token=GHSAT0AAAAAADSDEC7FVGKKMECLDZIHH26W2LPOKBQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/docker-1.png?token=GHSAT0AAAAAADSDEC7FZY4CDSZ6YXBJLCJC2LPOJUQ)

## TASK 7: Dockerize ( without using yaml file )
In this task, we created Dockerfile for backend application and learnt how to write a Dockerfile to define the environment, dependencies, and execution steps for a backend web application. And also learnt how to build a Docker image from a Dockerfile using the docker build command and to manage and run containers using only Docker CLI commands without using docker-compose or YAML files and how to create and use a custom bridge network to allow communication between backend and database containers. Also understood the importance of Docker volumes for persistent data storage, especially for database containers. 
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/docker-5.png?token=GHSAT0AAAAAADSDEC7F52KPYN6IBRDJSMDO2LPOKIA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/docker-8.png?token=GHSAT0AAAAAADSDEC7ENCDC5HZYC63NEY2O2LPOKWQ)


## TASK 8: Web Scraping and Automation - Flight Ticket Price Analysis
Web Scraping is a technique that helps in process of extracting data or content from websites using various libraries of python.
Throughout the task, the errors were challenging and learning steps like real flight websites failed due to modern SPA design, controlled inputs, and anti-bot mechanisms also issues included city values not storing, search not triggering, wrong data extraction, slow loading, and ChromeDriver misconfiguration but these were solved by inspecting the DOM, fixing ChromeDriver setup, and refining element selectors thus a Selenium-friendly demo site (BlazeDemo) was used to ensure reliable automation and dynamic scraping and learnt the importance of proper environment setup, DOM analysis, and choosing suitable websites for automation tasks. 
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/webscrapping-1.png?token=GHSAT0AAAAAADSDEC7F3DJIVQU62SR3ZTSQ2LPOU6Q)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/webscrapping-2.png?token=GHSAT0AAAAAADSDEC7EIXSKLISQG4H3ZGMS2LPOVDQ)


## TASK 9: Hashing
Hashing refers to the process of generating a fixed-size output from an input of variable size using the mathematical formulas known as hash functions. I used hashlib library to create secure hash values of passwords with algorithm SHA-256, os.urandom() to generate random salt that provides cryptographically secure random bytes which helped in ensuring that even identical passwords generate different hashes.
Hashing is done to protect user passwords and to make sure passwords are never stored in plain text and even if the database is leaked, original passwords cannot be recovered and to prevent unauthorized access by making sure that only during login, passwords are rehashed and compared and no password decoding or retrieval is performed
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/hashing-2.png?token=GHSAT0AAAAAADSDEC7EFHAYAECEZ72C4AXI2LPOLBQ)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/hashing-1.png?token=GHSAT0AAAAAADSDEC7EMF3UE2NZFMQ7TPKG2LPOK5Q)


## TASK 10: NMap
NMap or the Network Mapper scans networks to find live hosts, open ports, running services and operating systems, helping us map networks, find vulnerabilities, and manage services by sending specially crafted packets and analyzing responses. We did various analysis with NMap which includes identifying open ports and running services on a system, detecting the operating system using network behavior and etc.
The Nmap aggressive scan that was taken identified multiple open ports associated with Windows system services and local web applications. Ports 135 and 445 indicate Windows RPC and SMB services, while ports 8080 and 9001 indicate HTTP-based services including a Jetty web server. OS detection successfully identified the host as Microsoft Windows 10. The scan results were saved and analyzed to assess potential security exposure.
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/nmap-2.png?token=GHSAT0AAAAAADSDEC7EXGSEBOGA6MMPRMDO2LPOPUA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/nmap-1.png?token=GHSAT0AAAAAADSDEC7F4OSOIB5CZMTP7KAK2LPOPPA)
![image](https://raw.githubusercontent.com/MonikaRGowda/clcylevel3/refs/heads/main/nmap-3.png?token=GHSAT0AAAAAADSDEC7E4WRRRIQU2NAMY4SS2LPOPXQ)

