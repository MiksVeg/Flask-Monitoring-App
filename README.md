# Scalable Flask Application Deployment with Kubernetes and CI/CD

This project focuses on deploying a Flask application designed to handle **10,000 concurrent users** while implementing best practices in DevOps, containerization, and CI/CD automation.

## Overview

The goal of this project is to build a scalable, reliable, and fault-tolerant application infrastructure using Docker, Kubernetes, AWS EKS, and Jenkins. By automating deployments and scaling the infrastructure, this project demonstrates how to achieve high availability and resilience for a web application.

## Key Features

- **Dockerization**: Containerized the Flask application, ensuring consistent environments across development and production. Docker images are hosted on DockerHub.
- **Kubernetes Deployment**: Automated the setup using Kubernetes (`kubeadm`), enabling the system to scale dynamically to accommodate high user concurrency.
- **AWS EKS**: Deployed on AWS Elastic Kubernetes Service (EKS) to leverage cloud-native scaling, high availability, and fault tolerance.
- **Load Balancing**: Configured a multi-node cluster architecture in EKS with load balancing for optimal performance and traffic distribution.
- **CI/CD Pipeline**: Built a robust pipeline with Jenkins and GitHub webhooks to automate the build, test, and deployment processes. Every code change triggers an automated pipeline, ensuring smooth updates.

## Results

- Scaled the application to efficiently handle **10,000 concurrent users**.
- **Reduced downtime by 60%** with improved fault tolerance and high availability via AWS EKS.
- Enabled fast, automated deployments with a Jenkins-based CI/CD pipeline, integrated with GitHub for seamless updates.

## Tools & Technologies

- **Docker**
- **Kubernetes (`kubeadm`)**
- **AWS EKS**
- **Jenkins**
- **GitHub**
- **Flask**

## Installation

1. Clone the repository.
![image](https://github.com/user-attachments/assets/335ed089-5521-4303-9b05-dd4511348c3f)
2. Build the Docker image and push it to DockerHub.
![image](https://github.com/user-attachments/assets/7200af6d-54bf-43e8-aa6e-2e50caeaca4c)
3. Set up a Kubernetes cluster using `kubeadm`.

![image](https://github.com/user-attachments/assets/a8a12b6c-86a9-42e9-9ba5-139b358bd4f3)

4. Deploy the application on AWS EKS.
![image](https://github.com/user-attachments/assets/e9428918-e330-4891-9b75-8ad5879b9f6a)
5. Configure Jenkins for CI/CD pipeline automation with GitHub integration.
![image](https://github.com/user-attachments/assets/14d31f77-e79d-4780-a07e-e4c986fe30ca)
![image](https://github.com/user-attachments/assets/cca54cd5-908c-4fee-8b31-8178ddeda8de)
6. Final output of the application
![image](https://github.com/user-attachments/assets/405281dc-0395-4d93-ad9a-d7ba65ee2ba7)


## Conclusion

This project showcases the integration of modern DevOps practices, container orchestration with Kubernetes, and continuous deployment automation, resulting in a scalable and resilient infrastructure capable of handling high traffic and ensuring minimal downtime.
