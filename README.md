# Kubernetes Manifests for DevSecOps GitOps Deployment

This repository contains **Kubernetes manifest files** used for deploying a **three-tier MERN stack application** on **AWS EKS** following **GitOps principles**.

The manifests are continuously monitored and synchronized to the Kubernetes cluster using **ArgoCD** as part of an **end-to-end DevSecOps CI/CD pipeline**.

---

## 📌 Repository Purpose

* Acts as the **GitOps source of truth** for Kubernetes deployments
* Stores **declarative YAML manifests** for application components
* Enables **automated deployments** via ArgoCD
* Supports **Stable and Canary deployment strategies**

---

## 🏗️ Architecture Overview

The Kubernetes manifests deploy the following components on AWS EKS:

* **Frontend** – React application
* **Backend** – Node.js & Express API
* **Database** – MongoDB
* **Kubernetes Resources**

- **Deployments** – Application pod definitions and replica management  
- **Services** – Internal and external service exposure  
- **Ingress** – HTTP routing and path-based access  
- **ConfigMaps** – Application configuration management  
- **Secrets** – Sensitive configuration (base64 encoded)  
- **Namespaces** – Logical environment isolation  


---

## 🚀 Deployment Strategy

This repository implements **GitOps-based deployments** using **ArgoCD**:

* **Stable Deployment**

  * Handles production traffic
* **Canary Deployment**

  * Used to validate new application versions
  * Enables controlled traffic rollout

Image versions are **automatically updated** by the Jenkins pipeline and committed to this repository.

---

## 🔄 GitOps Workflow

1. Code changes pushed to the application repository
2. Jenkins builds and scans the application
3. Docker images are pushed to the container registry
4. Jenkins updates Kubernetes manifests with new image tags
5. Changes are committed to this repository
6. ArgoCD detects changes and syncs them to AWS EKS

---

## 🛠️ Tools & Technologies

* **Kubernetes**
* **AWS EKS**
* **ArgoCD (GitOps)**
* **Docker**
* **Jenkins**
* **GitHub**
* **MERN Stack**

---

## 📌 Prerequisites

* AWS EKS cluster
* kubectl configured for the cluster
* ArgoCD installed on EKS
* Docker images available in a container registry

---

##  Observability

* Kubernetes pod health is continuously observed via ArgoCD

---

## 👤 Maintainer

**Muppidi Sai Adithya**
GitHub: [https://github.com/MSAdithya45](https://github.com/MSAdithya45)

---


## 📄 Notes

* This repository is intended for **educational and demonstration purposes**
* Follows **cloud-native best practices** and **GitOps methodology**

---
