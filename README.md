# webcv

## Introduction
After more than 7 years in New Zealand, I am planning to move back to Europe in June. I would like to create an alternative platform to showcase my work and personal development through a website created in a public cloud environment. 


## Business Requirements
Currently working in Oceania and aiming to move to the UK this website is aiming to serve UK clients.
Leaning multi-cloud deployment by having the solution
1. What services should the public cloud deployment offer to the customers?
This public cloud deployment should offer access to a simple website showcasing my updated CV/personal portfolio for customers in Europe.
2. How will the users consume those services? Will they use Internet access or will you have to provide a more dedicated connectivity solution?
Users will consume the service over the internet. The website should be publicly hosted in Europe to insure lower latency and to comply with privacy regulation of GDPR (EU).
3. Identify the data needed by the solution you're deploying. What data is shared with other applications? Where will the data reside?
Data will mainly be static and there should be few interactions with other applications. Ideally hot storage should be hosted on a separate database within the same cloud provider as the application but cold storage should be hosted on a different Cloud platform with scheduled archive transfer and journaling solution.
4. What are the security requirements of your application?
* Application will require privileged access for administrators.
*Limit traffic to only required ports/applications, ideally access will also be limited to regional customers (Europe).
*Communication between Cloud deployments will be restricted to specific traffic
*Monitoring and alerting should be in place to pro-actively add security enhancement and quickly identify incidents.
*Ideally if the application is compromised we should be able to delete the virtual environment and recreate it from the scratch using backups and automation
5. What are the high availability requirements?
* Ideally there should be a standby server in a separate availability zone. 
* A DR solution could be put in place into a separate cloud provider using automation/DNS load balancing.
6. Do you have to provide connectivity to your on-premises data centre? If so, how will you implement it?
There is no need for a private connectivity. Only requirement is Administrative access from my workstation which does not require low latency.
7. Do you have to implement connectivity to other (customer) sites? If so, how will you implement it?
Archiving of the data and DR application data transfer can be done over the internet. To optimise the traffic both the cloud provider should be in a close geographical zone.
8. The most important requirement would be for me to learn as much as I can while measuring and effectively managing the cost of the deployment



## Technical Requirements
1. Web site: deploy a simple web site with back-end database running on a database server.
2. Data archive: archive should be hosted locally on the database server and transfered to a cold storage hosted on a different Cloud platform with scheduled archive transfer and journaling solution. ideally there should be a standby server in a separate availability zone that will use the archived storage. A DR solution could be put in place into a separate cloud provider using automation/DNS load balancing.
3. Privileged access management
*User access: geo-restricted, limited to specific type of traffic.
*Web Administrator access: Access through the internet. Two factor authentication with remote secure access the Web Administration application (Apache?).
*Infrastructure Administrator access: access to the cloud infrastructure via two factor authentication (Azure, AWS).
4. Native cloud firewall will be used along with other security features available.

## Time frames Requirements
Need an available public cloud solution deployed by end of April 2022 for me to start looking out for a job.