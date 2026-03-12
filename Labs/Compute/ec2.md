Introduction to Amazon EC2

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable, pay-as-you-go virtual servers in the cloud. It allows for the rapid deployment of computing capacity without the need for upfront hardware investment, making web-scale computing easier for developers.

Core Capabilities
- On-Demand Scaling: Ability to scale capacity up or down in minutes to meet changing computing requirements.

- Full Administrative Control: Complete access to the instance lifecycle, including choosing the Operating System (Linux/Windows) and resource configuration.

- Cost Efficiency: A "pay-only-for-what-you-use" model that transforms the economics of traditional computing.

- Failure Resilience: Tools to build highly available applications by isolating instances from common hardware failure scenarios.

- Hands-on Labs & Technical Milestones
Instance Deployment: Launched a web server with Termination Protection enabled to prevent accidental deletion of critical infrastructure.

Security Configuration: Modified Security Groups to manage inbound/outbound traffic, specifically enabling HTTP access to make the web server reachable.

Scalability & Elasticity: Performed a Resize of an Amazon EC2 instance to scale compute resources (CPU/RAM) based on performance requirements.

Monitoring & Health: Utilized AWS monitoring tools to track instance performance and resource utilization.

Lifecycle Management: Validated Termination Protection through testing and successfully managed the full instance lifecycle, including the final Termination of resources.

**Project: Amazon EC2 Lifecycle and Administration**


In this lab, I gained hands-on experience managing the full lifecycle of an Amazon Elastic Compute Cloud (EC2) instance. I practiced deploying a web server, configuring network security, monitoring performance, and performing vertical scaling by resizing instance resources.

**Technical Tasks Completed**
Instance Deployment & Automation: * Launched an Amazon Linux 2023 EC2 instance using a t3.micro instance type.

- Automated the deployment of an Apache web server using a User Data bash script to install httpd and initialize a custom HTML landing page upon boot.

- Enabled Termination Protection to prevent accidental deletion of the resource.

- Network Security & Troubleshooting: * Initially restricted all inbound traffic to demonstrate security best practices.

- Identified connectivity issues and resolved them by modifying the Security Group rules to allow inbound HTTP (Port 80) traffic from any source.

<img width="1483" height="382" alt="image" src="https://github.com/user-attachments/assets/77204c68-c72e-4051-ba42-cb9aaf389aeb" />

- Monitoring & Health Checks: * Utilized the EC2 Management Console to monitor System and Instance Status Checks.

- Analyzed performance metrics via Amazon CloudWatch.

- Used the "Get Instance Screenshot" tool to troubleshoot the boot process without requiring SSH access.

<img width="312" height="272" alt="image" src="https://github.com/user-attachments/assets/10c0cbed-c3c5-4776-995a-2a3d3b44173e" />

- Vertical Scaling (Resizing): * Managed the instance state by performing a controlled stop.

- Upgraded the instance type from t3.micro to t3.small to increase available CPU and memory.

- Modified the Elastic Block Store (EBS) root volume, successfully expanding the storage capacity from 8 GiB to 10 GiB.

Resource Cleanup: * Tested the "Termination Protection" safety gate by attempting to delete the instance while protected.

Successfully disabled protection and terminated the instance to clean up the environment and manage costs.

<img width="1292" height="592" alt="image" src="https://github.com/user-attachments/assets/25f5434d-c741-4dcb-949c-53457fd1d4aa" />

Key AWS Services Used
Compute: Amazon EC2

Storage: Amazon Elastic Block Store (EBS)

Security: AWS Security Groups

Monitoring: Amazon CloudWatch

Deployment: User Data Scripts (Bash)
