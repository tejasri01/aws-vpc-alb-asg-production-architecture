#VPC setup 

1.Created VPC to host the project resources.

2.Configured public and private subnets across two Availability Zones for high availability.


<img width="1906" height="890" alt="Screenshot 2026-02-11 003812" src="https://github.com/user-attachments/assets/ca5d9f9d-3a5c-439c-8806-8cd909125ed9" />


3.Deployed an Internet Gateway for internet access to public resources.

4.Set up a NAT Gateway to allow private subnets to access the internet securely.


#Created Auto Scaling Group in Private Subnets

<img width="1894" height="920" alt="Screenshot 2026-02-11 003955" src="https://github.com/user-attachments/assets/2d7d3e56-38a1-43eb-95e8-96ec4db71aab" />


1.Created an Auto Scaling Group (ASG) to automatically manage application instances.

2.Configured the ASG to launch instances based on a launch template.

3. Ensured high availability and scalability across two Availability Zones.

#Created Bastion Host and Deployed HTML Application

<img width="906" height="737" alt="Screenshot 2026-02-11 000334" src="https://github.com/user-attachments/assets/54f418e2-d7c7-468b-a34d-04f9cff43d1f" />

1.Launched a Bastion Host to securely access EC2 instances.

2.Logged into the two EC2 instances through the Bastion Host.

3.Created an index.html file on both instances.

4.Added basic HTML code to the file to display a simple web page

#Created Load Balancer and Target Groups


<img width="1916" height="920" alt="Screenshot 2026-02-11 004037" src="https://github.com/user-attachments/assets/77eecb06-b3ac-4082-ab43-55f55e7272f7" />



<img width="1569" height="405" alt="Screenshot 2026-02-11 004023" src="https://github.com/user-attachments/assets/fe8e7258-67bc-4ac3-92f2-eb6f715f9e14" />




1.Created an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances.

2.Configured Target Groups and registered the EC2 instances so the ALB could forward traffic correctly.
<img width="1902" height="783" alt="Screenshot 2026-02-11 004056" src="https://github.com/user-attachments/assets/89ee0872-8067-4795-a429-5dec6f26d876" />


3.Set up health checks to monitor the status of the instances and ensure traffic is only sent to healthy instances.

#Verified Application via Load Balancer

<img width="1915" height="901" alt="Screenshot 2026-02-11 004445" src="https://github.com/user-attachments/assets/8ea8b584-0a9d-4667-b2b6-2bc4b52b20dd" />

4.Accessed the application using the Application Load Balancer (ALB) DNS in a web browser.

5.The HTML page hosted on the EC2 instances was displayed successfully.

6.Observed that refreshing the browser sometimes displayed the page from different instances, demonstrating that the ALB was distributing traffic across multiple instances.

<img width="1912" height="987" alt="Screenshot 2026-02-11 004128" src="https://github.com/user-attachments/assets/b230962c-baac-414b-b509-2da48099db0a" />

7.This behavior confirmed the load balancing and high availability functionality of the setup.

#Conclusion

The project successfully demonstrated the deployment of a simple HTML web application on AWS using core cloud services. Key achievements include:

Network Setup: Configured a custom VPC with public and private subnets, Internet Gateway, and NAT Gateway.

Scalable Compute: Used an Auto Scaling Group to manage application instances across two Availability Zones for high availability.

Secure Access: Implemented a Bastion Host to securely access EC2 instances.

Load Balancing: Deployed an Application Load Balancer with Target Groups to distribute traffic efficiently and ensure continuous availability.

Application Deployment: Successfully hosted a basic HTML page on multiple EC2 instances and verified load balancing functionality.

Overall, this project provided practical experience with AWS networking, compute, security, and load balancing services, and demonstrated how to deploy a highly available and scalable web application in the cloud.





