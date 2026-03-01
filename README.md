# Auto Scaling and Security using GCP Compute Engine

## Course
M.Tech - Virtualization in Cloud Computing  
IIT Jodhpur

---

## Project Objective

This project demonstrates virtualization, auto scaling, and security implementation using Google Cloud Platform (GCP).

The following cloud concepts are implemented:

- Virtual Machine provisioning
- Managed Instance Group
- CPU-based Auto Scaling
- VPC Firewall configuration
- IAM Role-based Access Control

---

## Architecture Overview

The system architecture consists of:

- Compute Engine Virtual Machines
- Instance Template (VM blueprint)
- Managed Instance Group
- Autoscaler (CPU Utilization > 60%)
- VPC Firewall Rules
- IAM Security Policies

---

## Implementation Details

### 1. Virtual Machine
- Machine Type: e2-medium
- OS: Ubuntu 22.04 LTS
- Region: Asia South (Mumbai)
- Web Server: Apache

### 2. Instance Template
Used as blueprint for auto-provisioning VM instances.

### 3. Managed Instance Group
Initial size: 1  
Maximum size: 5  

### 4. Auto Scaling Policy
- Metric: CPU Utilization
- Target: 60%
- Cooldown period: 60 seconds

### 5. Security Configuration

Firewall Rules:
- Custom firewall rules
- Allow HTTP (Port 80)
- Allow HTTPS (Port 443)
- Allow SSH (Port 22)
- Deny Telnet (port 23)

IAM:
- Owner role
- Compute Engine service account
- IAM Viewer role for least privilege

---

## Testing

CPU load was generated using:
- stress --cpu 8 --timeout 600


During high CPU utilization, VM instances automatically scaled from 1 to 5.

---

## Virtualization Concepts Demonstrated

- Hardware Virtualization
- Resource Isolation
- Elastic Scaling
- On-demand Provisioning
- Identity-based Security
- Network Segmentation

---

## Author
Sourabh Tyagi  
M.Tech(DE) - IIT Jodhpur

