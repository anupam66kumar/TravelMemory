# TravelMemory - Scalable MERN Deployment

This repository contains the full-stack TravelMemory application, deployed on a high-availability AWS infrastructure.

## 🚀 Project Overview
The objective of this project was to deploy a MERN (MongoDB, Express, React, Node.js) application on Amazon EC2, ensuring scalability through Load Balancing and accessibility via a custom domain.

## 🏗️ Architecture
The deployment features:
- **Frontend:** React.js (Served via Nginx)
- **Backend:** Node.js (Managed by PM2)
- **Reverse Proxy:** Nginx (Handling Port 80 to Port 3000)
- **Database:** MongoDB Atlas (Cloud)
- **Infrastructure:** AWS Application Load Balancer (ALB) across multiple Availability Zones.
- **Domain:** Hosted on GoDaddy (`anupam66kumar.xyz`).

## 🛠️ Deployment Steps

### 1. Backend & Proxy Setup
- Cloned the repository and configured `.env` for database connectivity.
- Set up Nginx as a reverse proxy to manage traffic between the web and the Node.js application.

### 2. Frontend Integration
- Updated `urls.js` to link the React frontend to the backend API.
- Generated production builds served via Nginx.

### 3. Scaling & High Availability
- Created an Amazon Machine Image (AMI) for rapid scaling.
- Deployed multiple instances across different AZs.
- Configured an Application Load Balancer to distribute incoming traffic and provide fault tolerance.

### 4. Custom Domain
- Integrated a custom domain using GoDaddy DNS.
- Mapped the ALB endpoint using a CNAME record for seamless user access.

## 📊 Deployment Diagram
The architectural flow (GoDaddy -> AWS ALB -> EC2 Cluster -> MongoDB Atlas) is documented in the repository under `/docs` (or root).

## 👤 Author
**Anupam Kumar** *Senior Technical Support Engineer*
