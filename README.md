# ITS 2130 ECA Capstone Project Submission

Polyrepo architecture with Git submodules, implemented with Spring Cloud and deployed on Google Cloud Platform.

## 1. Student Information

| Field | Value |
|---|---|
| Module | ITS 2130 Enterprise Cloud Application |
| Program | HDSE @ IJSE |
| Student Name | <YOUR_NAME> |
| Student ID | <YOUR_ID> |
| Submission Date | 2026-03-22 |
| Main Submission Repository | https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP |

## 2. Project Overview

This project uses Spring Cloud microservices in a polyrepo model.

- Each platform component and business microservice is in its own GitHub repository.
- This main repository contains those repositories as Git submodules.
- The frontend application consumes backend APIs through the API Gateway.
- The full system is deployed on Google Cloud Platform.

## 3. Live Public URLs (Mandatory)

| Component | Public URL |
|---|---|
| Frontend Application | <YOUR_FRONTEND_PUBLIC_URL> |
| API Gateway | <YOUR_API_GATEWAY_PUBLIC_URL> |
| Eureka Dashboard (Mandatory) | <YOUR_EUREKA_DASHBOARD_PUBLIC_URL> |

## 4. Repository Structure (Polyrepo + Submodules)

### 4.1 Main Submodules

| Path | Repository | Purpose |
|---|---|---|
| Platform | https://github.com/Himanthajaga/Capstone-Project-Platform | Platform layer parent repo |
| Services | https://github.com/Himanthajaga/Capstone-Project-Services | Business services parent repo |
| Webapp | https://github.com/Himanthajaga/Capstone-Project-Webapp | Frontend application |

### 4.2 Nested Submodules in Platform

| Path | Repository | Purpose |
|---|---|---|
| Platform/Api-gateway | https://github.com/Himanthajaga/Capstone-Project-Platform-Api-Gateway | API Gateway |
| Platform/Config-Server | https://github.com/Himanthajaga/Capstone-Project-Platform-Config-Server | Spring Cloud Config Server |
| Platform/platform-registry | https://github.com/Himanthajaga/Capstone-Project-Platform-Service-Registry | Eureka Service Registry |

### 4.3 Nested Submodules in Services

| Path | Repository | Purpose |
|---|---|---|
| Services/Student-Service | https://github.com/Himanthajaga/Capstone-Project-Service-Student | Student microservice |
| Services/program-Service | https://github.com/Himanthajaga/Capstone-Project-Service-Program | Program microservice |
| Services/Enrollment-Service | https://github.com/Himanthajaga/Capstone-Project-Service-Enrollment | Enrollment microservice |

## 5. Spring Cloud Components Implemented

- Spring Cloud Config Server
- Spring Cloud Config Client
- Spring Cloud Netflix Eureka Server
- Spring Cloud Netflix Eureka Client
- Spring Cloud API Gateway

## 6. Frontend Requirement Compliance

The frontend is implemented in Next.js and accesses all backend functionality through the API Gateway.
It demonstrates that microservices are reachable and functioning correctly in the deployed cloud environment.

## 7. GCP Infrastructure Evidence

All required cloud resources are deployed and visible in the GCP Console.

| Required Resource | Evidence |
|---|---|
| VM Instance Groups | <EVIDENCE_LINK_OR_NOTE> |
| Virtual Machines (VMs) | <EVIDENCE_LINK_OR_NOTE> |
| VM Instance Templates | <EVIDENCE_LINK_OR_NOTE> |
| Disk Images | <EVIDENCE_LINK_OR_NOTE> |
| Health Checks | <EVIDENCE_LINK_OR_NOTE> |
| Cloud DNS | <EVIDENCE_LINK_OR_NOTE> |
| Load Balancing | <EVIDENCE_LINK_OR_NOTE> |
| Cloud NAT Gateway | <EVIDENCE_LINK_OR_NOTE> |
| Cloud SQL Instances | <EVIDENCE_LINK_OR_NOTE> |
| Firestore | <EVIDENCE_LINK_OR_NOTE> |
| Cloud Storage (Buckets) | <EVIDENCE_LINK_OR_NOTE> |
| Cloud Router | <EVIDENCE_LINK_OR_NOTE> |
| VPC Network | <EVIDENCE_LINK_OR_NOTE> |
| Firewall Rules | <EVIDENCE_LINK_OR_NOTE> |

## 8. Cloud Storage Requirement (Mandatory)

At least one microservice stores files in a Google Cloud Storage bucket.

| Field | Value |
|---|---|
| Service Name | <SERVICE_NAME> |
| API Endpoint | <ENDPOINT> |
| Bucket Name | <BUCKET_NAME> |
| Evidence (API/UI) | <EVIDENCE_LINK_OR_NOTE> |

## 9. High Availability and Auto Scaling (Mandatory)

### 9.1 Microservice Auto Scaling

| Check | Value |
|---|---|
| Horizontal scaling supported | <YES_OR_NO> |
| Autoscaler configuration | <DETAILS> |
| Instance group details | <DETAILS> |

### 9.2 Platform High Availability

| Check | Value |
|---|---|
| Multi-instance deployment | <YES_OR_NO> |
| Multi-zone deployment | <ZONE_1>, <ZONE_2>, <ZONE_3> |
| Fault-tolerance evidence | <EVIDENCE_LINK_OR_NOTE> |

## 10. PM2 Process Management and Auto Restart (Mandatory)

Applications are managed by PM2 because the deployment is non-containerized.

### 10.1 PM2 Verification Commands

```bash
pm2 status
pm2 monit
pm2 startup
pm2 save
```

### 10.2 PM2 Compliance Checklist

| Requirement | Status |
|---|---|
| Applications started and managed by PM2 | <YES_OR_NO> |
| Logs written to correct location | <YES_OR_NO> |
| Auto restart on failure | <YES_OR_NO> |
| PM2 starts on VM reboot | <YES_OR_NO> |

## 11. Eureka Dashboard (Mandatory)

Public Eureka Dashboard URL: <YOUR_EUREKA_DASHBOARD_PUBLIC_URL>

## 12. Screen Recording Submission (Mandatory)

Recording URL: <YOUR_VIDEO_LINK>

Recording includes:

- Navigation through all required GCP resources
- SSH into each VM
- Running pm2 monit on each VM
- Visibility of running PM2 processes
- Matching project IP addresses with GCP resources

## 13. How to Clone This Repository with All Submodules

```bash
git clone --recurse-submodules https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP.git
cd Capstone-Project-Fully-with-GCP
git submodule update --init --recursive
git submodule status --recursive
```

## 14. Final Submission Checklist

- [x] Main repository contains Platform, Services, and Webapp as submodules
- [x] Nested submodules inside Platform and Services are accessible
- [ ] Frontend consumes deployed APIs via API Gateway URL
- [ ] Public Eureka Dashboard URL is included
- [ ] All mandatory GCP resources are demonstrated
- [ ] Cloud Storage bucket usage is demonstrated
- [ ] Auto scaling and high availability are demonstrated
- [ ] PM2 management and automatic restart are demonstrated
- [ ] Screen recording link is included