ITS 2130 ECA Capstone Project Submission (Polyrepo with Git Submodules)
Student Information
Module: ITS 2130 Enterprise Cloud Application
Program: HDSE @ IJSE
Student Name: <YOUR_NAME>
Student ID: <YOUR_ID>
Submission Date: 2026-03-22
Main Submission Repository: https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP
Project Overview
This project is implemented using Spring Cloud microservices with a polyrepo architecture and deployed on Google Cloud Platform.
All platform components and business services are maintained in separate repositories and connected through Git submodules in this main submission repository.

Live Public URLs (Mandatory)
Frontend Application URL: <YOUR_FRONTEND_PUBLIC_URL>
API Gateway Public URL: <YOUR_API_GATEWAY_PUBLIC_URL>
Eureka Dashboard Public URL (Mandatory): <YOUR_EUREKA_DASHBOARD_PUBLIC_URL>
Repository Structure (Polyrepo with Submodules)
Main Submodules
Path	Repository	Purpose
Platform	https://github.com/Himanthajaga/Capstone-Project-Platform	Platform layer parent repo
Services	https://github.com/Himanthajaga/Capstone-Project-Services	Business services parent repo
Webapp	https://github.com/Himanthajaga/Capstone-Project-Webapp	Frontend application
Nested Submodules Inside Platform
Path	Repository	Purpose
Platform/Api-gateway	https://github.com/Himanthajaga/Capstone-Project-Platform-Api-Gateway	API Gateway
Platform/Config-Server	https://github.com/Himanthajaga/Capstone-Project-Platform-Config-Server	Spring Cloud Config Server
Platform/platform-registry	https://github.com/Himanthajaga/Capstone-Project-Platform-Service-Registry	Eureka Service Registry
Nested Submodules Inside Services
Path	Repository	Purpose
Services/Student-Service	https://github.com/Himanthajaga/Capstone-Project-Service-Student	Student microservice
Services/program-Service	https://github.com/Himanthajaga/Capstone-Project-Service-Program	Program microservice
Services/Enrollment-Service	https://github.com/Himanthajaga/Capstone-Project-Service-Enrollment	Enrollment microservice
Spring Cloud Components Implemented
Spring Cloud Config Server
Spring Cloud Config Client
Spring Cloud Netflix Eureka Server
Spring Cloud Netflix Eureka Client
Spring Cloud API Gateway
Frontend Application Requirement
The frontend is implemented in Next.js and consumes backend APIs through the API Gateway.
It demonstrates that all deployed microservices are reachable and functioning through one gateway endpoint.

GCP Cloud Infrastructure Evidence
The following resources are deployed and visible in GCP Console:

VM Instance Groups: <EVIDENCE_LINK_OR_NOTE>
Virtual Machines (VMs): <EVIDENCE_LINK_OR_NOTE>
VM Instance Templates: <EVIDENCE_LINK_OR_NOTE>
Disk Images: <EVIDENCE_LINK_OR_NOTE>
Health Checks: <EVIDENCE_LINK_OR_NOTE>
Cloud DNS: <EVIDENCE_LINK_OR_NOTE>
Load Balancing: <EVIDENCE_LINK_OR_NOTE>
Cloud NAT Gateway: <EVIDENCE_LINK_OR_NOTE>
Cloud SQL Instances: <EVIDENCE_LINK_OR_NOTE>
Firestore: <EVIDENCE_LINK_OR_NOTE>
Cloud Storage Buckets: <EVIDENCE_LINK_OR_NOTE>
Cloud Router: <EVIDENCE_LINK_OR_NOTE>
VPC Network: <EVIDENCE_LINK_OR_NOTE>
Firewall Rules: <EVIDENCE_LINK_OR_NOTE>
Cloud Storage Requirement (Mandatory)
At least one microservice stores files in Google Cloud Storage Bucket.

Service Name: <SERVICE_NAME>
API Endpoint: <ENDPOINT>
Bucket Name: <BUCKET_NAME>
Evidence (API response/UI screenshot): <EVIDENCE_LINK_OR_NOTE>
High Availability and Auto Scaling (Mandatory)
Microservices Auto Scaling
Deployment method supports horizontal scaling: <YES/NO>
Autoscaler configuration: <DETAILS>
Instance group details: <DETAILS>
Platform High Availability
Platform components run on multiple instances across multiple zones: <YES/NO>
Zones used: <ZONE_1>, <ZONE_2>, <ZONE_3>
Fault tolerance evidence: <EVIDENCE_LINK_OR_NOTE>
PM2 Process Management and Auto Restart (Mandatory)
PM2 is used to manage non-containerized processes with automatic restart on failure and startup on VM reboot.

PM2 Verification Commands
pm2 status
pm2 monit
pm2 startup
pm2 save
PM2 Expectations Covered
Applications are started by PM2: <YES/NO>
Logs are written correctly: <YES/NO>
Auto restart on failure: <YES/NO>
PM2 starts on VM reboot: <YES/NO>
Eureka Dashboard Requirement (Mandatory)
Public Eureka Dashboard URL: <YOUR_EUREKA_DASHBOARD_PUBLIC_URL>

Screen Recording Submission (Mandatory)
Recording URL: <YOUR_VIDEO_LINK>

Recording includes:

Navigation through all required GCP resources
SSH into each VM
Running pm2 monit on each VM
Visible proof of running processes
Matching IP addresses between GCP and project setup
How to Clone This Submission with All Submodules
git clone --recurse-submodules https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP.git
cd Capstone-Project-Fully-with-GCP
git submodule update --init --recursive
git submodule status --recursive
Final Submission Checklist
Main repo contains Platform, Services, Webapp as submodules
Nested submodules inside Platform and Services are accessible
Frontend consumes APIs through API Gateway
Eureka public URL is included in this README
All mandatory GCP resources are visible
Cloud Storage bucket usage is demonstrated
Auto scaling and high availability are demonstrated
PM2 process management and auto restart are demonstrated
Screen recording link is included