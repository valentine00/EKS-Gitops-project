# EKS-Gitops-project
## Overview

This project demonstrates the deployment and automation of a Java/Tomcat application on Amazon EKS using modern DevOps and GitOps practices.  
It implements an end-to-end workflow covering infrastructure provisioning, continuous integration, containerization, image management, GitOps-based Kubernetes deployment, application monitoring, visualization, and alerting.

The objective was to build a production-style DevOps platform that demonstrates the integration of industry-standard tools and practices, including GitHub Actions, Amazon EKS, ArgoCD, Helm, Prometheus, Grafana, and the Prometheus JMX Exporter. 
This repository serves as a practical demonstration of deploying, operating, monitoring, and maintaining containerized applications on Kubernetes using GitOps principles and cloud-native tools.


## Architecture

Below is the architetural diagram of the application

<img width="1789" height="843" alt="VprofileArchitucture (5) drawio" src="https://github.com/user-attachments/assets/6ae8f92c-4049-4520-9de1-d278d34cb7c1" />



## Technologies used

- Amazon EKS
- Kubernetes
- Docker
- Helm
- ArgoCD
- GitHub Actions
- Amazon ECR
- Terraform
- Prometheus
- Grafana
- Prometheus JMX Exporter
- AWS Load Balancer Controller
- Java
- Apache Tomcat

## Project components
The project is organized across three repositories representing the major components of the platform:

### Application Repository

Contains the Java/Tomcat application and Docker configuration used to build the application container image.

Key components include:

- Java/Tomcat application
- Dockerfile
- JMX Exporter integration
- JVM metrics configuration

### Infrastructure Repository
Contains the infrastructure and automation required to provision and manage the AWS environment.

Key components include:

- Terraform configuration
- Amazon EKS infrastructure
- GitHub Actions workflows
- AWS configuration
- Infrastructure automation

### Helm / GitOps Repository
Contains the Kubernetes application configuration deployed through ArgoCD.

Key components include:

- Helm chart
- Kubernetes Deployments
- Kubernetes Services
- Ingress configuration
- ServiceMonitor
- Application configuration
- ArgoCD deployment configuration

Github actions is used to automate the application delivery process.  
ArgoCD is used to implement GitOps-based deployment to Amazon EKS.  
The application runs on Amazon EKS using Kubernetes resources managed through Helm.  
For monitoring and observability, I use Prometheus and Grafana. Data is scraped with promethus and Grafana allows for Visualization of the data. Alerting is also implemeted. JMX exporter is used to enable prometheus scrape the core application data.

## Screenshots 
The screenshots below demonstrate the working platform.  
### Github actions  
<img width="944" height="735" alt="succeful infra1" src="https://github.com/user-attachments/assets/2a3a687c-5e0b-4868-afa1-28084f59ed27" />
<img width="913" height="698" alt="succeful infra2" src="https://github.com/user-attachments/assets/5f973663-c401-4890-bc7c-58633e774b7d" />
<img width="932" height="664" alt="succesful app1" src="https://github.com/user-attachments/assets/786b1100-4466-48d1-b574-c44f25392222" />
<img width="926" height="657" alt="succesful app2" src="https://github.com/user-attachments/assets/78afaa12-b2dc-4ae3-857a-0bb948fb421e" />  

### ArgoCD  
<img width="942" height="587" alt="argocd" src="https://github.com/user-attachments/assets/6aa57daf-25ea-4536-adb7-8d17ff631746" />  

<img width="1893" height="991" alt="argocdlive" src="https://github.com/user-attachments/assets/f13a4535-2053-48dc-9ca9-cfb1d7e35e11" />  

### Amazon EKS   
<img width="777" height="453" alt="EKS workloads" src="https://github.com/user-attachments/assets/9482b603-0acb-41ed-92a6-c72d27932e10" />  

### Vprofile Prometheus Target  
<img width="1877" height="191" alt="service monitor UP" src="https://github.com/user-attachments/assets/837ced42-841d-498c-b21a-b136dbe246cf" />  

### Grafana

<img width="1902" height="986" alt="Screenshot 2026-06-23 171428" src="https://github.com/user-attachments/assets/9faef0e8-2953-452e-a4fe-788e07bf1745" />  

<img width="1882" height="990" alt="Screenshot 2026-06-23 171411" src="https://github.com/user-attachments/assets/7084f376-a3a7-4044-8f3b-188853609641" />  

<img width="1872" height="793" alt="application monitoring" src="https://github.com/user-attachments/assets/9fa14ba2-5055-4366-9e5d-0789844d0e4a" />  

<img width="1836" height="990" alt="namespacemonitoring" src="https://github.com/user-attachments/assets/8cc87eb2-9737-4f9f-b14a-2c0b482d525c" />  

<img width="1850" height="987" alt="nodeMonitoringDetails" src="https://github.com/user-attachments/assets/0c199f98-171d-4a4e-bebd-2aaffb7bbae9" />  

<img width="1902" height="987" alt="monitoringDashboard1" src="https://github.com/user-attachments/assets/751e701a-4698-465e-a5b8-e7bc92f42c38" />

<img width="1912" height="952" alt="monitoringDashboard" src="https://github.com/user-attachments/assets/176527bf-58b9-47c3-998a-00426fb87bcd" />

### Alerting










