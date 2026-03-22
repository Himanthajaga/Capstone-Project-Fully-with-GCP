# ITS 2130 ECA Capstone Project Submission

Polyrepo architecture with Git submodules, implemented with Spring Cloud and deployed on Google Cloud Platform.

## 1. Student Information

| Field                      | Value                                                           |
|----------------------------|-----------------------------------------------------------------|
| Module                     | ITS 2130 Enterprise Cloud Application                           |
| Program                    | GDSE @ IJSE                                                     |
| Student Name               | J.G Himantha                                                    |
| Student ID                 | 2301692032                                                      |
| Submission Date            | 2026-03-31                                                      |
| Main Submission Repository | https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP |
| GCP Project ID             | capstone-project-490416 |

## 2. Project Overview

This project uses Spring Cloud microservices in a polyrepo model.

- Each platform component and business microservice is in its own GitHub repository.
- This main repository contains those repositories as Git submodules.
- The frontend application consumes backend APIs through the API Gateway.
- The full system is deployed on Google Cloud Platform.

## 3. Live Public URLs (Mandatory)

| Component | Public URL                                           |
|---|------------------------------------------------------|
| Frontend Application | 34.21.151.150:80                           |
| Eureka Dashboard (Mandatory) | http://34.126.186.15:9001/,<br/>http://34.124.176.187:9001/,<br/>http://34.158.34.135:9001/ |

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

## 7. High Availability and Auto Scaling (Mandatory)

### 7.1 Microservice Auto Scaling

| Check | Value |
|---|-------|
| Horizontal scaling supported | YES   |
| Autoscaler configuration | YES   |
| Instance group details | YES   |

### 7.2 Platform High Availability

| Check | Value                                                   |
|---|---------------------------------------------------------|
| Multi-instance deployment | YES                                                     |
| Multi-zone deployment | asia-southeast1-a, asia-southeast1-b, asia-southeast1-c |
| Fault-tolerance evidence | YES                                                     |

## 8. PM2 Process Management and Auto Restart (Mandatory)

Applications are managed by PM2 because the deployment is non-containerized.

### 8.1 PM2 Verification Commands

```bash
pm2 status
pm2 monit
pm2 startup
pm2 save
```

### 8.2 PM2 Compliance Checklist

| Requirement | Status |
|---|---|
| Applications started and managed by PM2 | YES |
| Logs written to correct location | YES |
| Auto restart on failure | YES |
| PM2 starts on VM reboot | YES |


## 9. Screen Recording Submission (Mandatory)

Recording URL: https://drive.google.com/file/d/1TTut_W9pE3YNwCrSYm6ChcSIqrO7CIcO/view?usp=sharing

## 10. How to Clone This Repository with All Submodules

```bash
git clone --recurse-submodules https://github.com/Himanthajaga/Capstone-Project-Fully-with-GCP.git
cd Capstone-Project-Fully-with-GCP
git submodule update --init --recursive
git submodule status --recursive
```