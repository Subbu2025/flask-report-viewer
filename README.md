# Flask Application with Docker

## Overview

This project is a Flask-based web application that has been containerized using Docker. The application serves as a dynamic platform for rendering reports and static content. The containerized application is accessible using your website domain [http://example.com/](http://example.com/) via AWS Route53.

---

## Features

- **Dynamic Rendering**: The application dynamically renders reports using Power BI.
- **Static Pages**: Home and About pages for general information.
- **Containerization**: Built and deployed using Docker.

---

## Table of Contents
- [Prerequisites](#prerequisites)
- [Build and Run the Docker Image](#build-and-run-the-docker-image)
- [Access the Application](#access-the-application)
- [Stop and Remove the Container](#stop-and-remove-the-container)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## Prerequisites

Ensure the following are installed on your system:
1. **Docker**: To build and run the containerized application.
2. **AWS EC2 Instance**: For hosting the application (if deploying to the cloud).
3. **Route53**: For domain name configuration.

---

## Build and Run the Docker Image

### 1. Clone the Repository
Clone the project repository to your local machine:
```bash
git clone https://github.com/Subbu2025/flask-report-viewer.git
cd flask-report-viewer
```
### 2. Build the Docker Image
Build the Docker image using the provided Dockerfile:
```bash
docker build -t flask-report-viewer:v1 .
```
- flask-report-viewer:v1: Name and tag of the Docker image.

### 3. Verify the Docker Image
List all available Docker images:
```bash
docker images
```
### 4. Run the Docker Container
Start a container using the built image:
```bash
docker run -d -p 80:80 --name flask-report-viewer flask-report-viewer:v1
```
- -d: Runs the container in detached mode.
- -p 80:80: Maps port 80 of the host to port 80 of the container.
- --name finapp: Assigns the container a name (finapp).

### 5. Verify Running Containers
Check if the container is running:
```bash
docker ps
```
## Access the Application
Local Access:
Open a browser and navigate to:
```
http://localhost
```

Hosted Access:
If deployed to an EC2 instance and mapped with AWS Route53, access the application at:
```
http://example.com/
```

## Stop and Remove the Container
Stop the Container:
```bash
docker stop flask-report-viewer
```
Remove the Container:
```bash
docker rm flask-report-viewer
```
## Future Enhancements
- Optimize Docker Image: Use multi-stage builds to reduce image size.
- CI/CD Integration: Automate image builds and deployments using Jenkins or GitHub Actions.
- HTTPS Support: Configure SSL/TLS for secure access.
- Scalability: Deploy using Kubernetes for better scalability and management.
# Flask Application

## Screenshots

### Docker Image and Container
![Docker Image and Container](images/Docker-Image-Container.png "Docker Image and Container")

### Route53 A Record Configuration
![Route53 A Record](images/Route53-A-Record.png "Route53 A Record Screenshot")

### Home Page
![Home Page](images/HomePage.png "Home Page Screenshot")

### About Page
![About Page](images/About.png "About Page Screenshot")

### Reports:

#### Healthcare Analysis Report
![Healthcare Analysis Report](images/Report-Heathcare-Ananlysis.png "Healthcare Analysis Report")

#### Financial Analytics Report
![Financial Analytics Report](images/Report-Financial%20Analytics.png "Financial Analytics Report")

#### Balance Sheet Report
![Balance Sheet Report](images/Report-BalanceSheet.png "Balance Sheet Report")


#### HR Analytics Report
![HR Analytics Report](images/Report-HR%20Analytics.png "HR Analytics Report")

#### Retail Insights Report
![Retail Insights Report](images/Report-RetailInsights.png "Retail Insights Report")







