# TravelMemory - Scalable MERN Deployment

This repository contains the full-stack TravelMemory application, deployed on a high-availability AWS infrastructure.

## 🏗️ Deployment Architecture
![Architecture Diagram](https://github.com/anupam66kumar/TravelMemory/raw/5d36438d4a392d406305e9f506b486b4dd44c50b/Architecture%20Diagram%20TravelMemory.drawio.png)

## 🚀 Project Overview
The objective of this project was to deploy a MERN (MongoDB, Express, React, Node.js) application on Amazon EC2, ensuring scalability through Load Balancing and accessibility via a custom domain.

## 🛠️ Infrastructure Details
- **Frontend:** React.js (Served via Nginx)
- **Backend:** Node.js (Managed by PM2)
- **Reverse Proxy:** Nginx (Handling Port 80 to Port 3000)
- **Database:** MongoDB Atlas (Cloud)
- **High Availability:** AWS Application Load Balancer (ALB) across multiple Availability Zones.
- **Domain:** Hosted on GoDaddy (`anupam66kumar.xyz`).

## 📋 Deployment Steps

### 1. Backend & Proxy Setup
- Cloned repository and configured `.env` with MongoDB Atlas URI.
- Set up Nginx as a reverse proxy to manage traffic flow to the Node.js application.

### 2. Frontend Integration
- Updated `urls.js` to link React frontend to the backend API.
- Generated production builds served via Nginx.

### 3. Scaling & High Availability
- Created an Amazon Machine Image (AMI) for rapid scaling.
- Deployed multiple instances across different AZs.
- Configured an Application Load Balancer to distribute traffic and provide fault tolerance.

### 4. Custom Domain
- Integrated a custom domain using GoDaddy DNS.
- Mapped the ALB endpoint using a CNAME record.

## 👤 Author
[cite_start]**Anupam Kumar** 
[cite_start]*Senior Technical Support Engineer*
