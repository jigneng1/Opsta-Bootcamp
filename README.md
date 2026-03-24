# Opsta Bootcamp: Bookinfo Microservices Workshop

This project is part of the **Opsta Bootcamp**, showcasing a complete DevSecOps lifecycle. It involves deploying the polyglot **Bookinfo** application on Google Kubernetes Engine (GKE) using modern CI/CD practices and automated security gates.

> [!IMPORTANT]
> **Status Note:** All services and environments listed below are currently **DOWN**. This repository and the associated URLs serve as a structural **Example** and architectural showcase from the workshop only.

---

## 🏗 System Architecture

The **Bookinfo** application is a microservices-based system consisting of four services and a database backend:

### Services Detail:
* **Product Page (Python):** The entry point for users, aggregating data from other services.
* **Reviews (Java):** Provides book reviews and star ratings.
* **Details (Ruby):** Provides specific information about the book.
* **Ratings (Node.js):** Manages the rating system, persisted in the database.
* **Database (MongoDB):** Stores the rating data.

---

## 🛠 DevSecOps Platform Layer

Our infrastructure is built on **GKE** with a high focus on security, ensuring all services are accessible via **HTTPS**.

### Security & Tooling Compliance
| Tool Name | Function | Architecture |
| :--- | :--- | :--- |
| **Jenkins** | CI/CD Orchestration | on K8S |
| **Gitlab** | Source Code Repository | on SaaS |
| **Harbor** | Container Image Registry | on K8S |
| **Trivy** | Container Image Security | on Pipeline |
| **Dependency Check** | Software Composition Analysis (SCA) | on Pipeline |
| **SonarQube** | Static Application Security Testing (SAST) | on K8S |
| **OWASP Zap** | Dynamic Application Security Testing (DAST) | on Pipeline |
| **KICS** | Infrastructure as Code Security | on Pipeline |

---

## 🌐 Access Links (Status: Offline)

### DevSecOps Tools
| Tool | Access URL |
| :--- | :--- |
| **Jenkins** | [https://cicd-neng.stthi.com](https://cicd-neng.stthi.com) |
| **Harbor** | [https://registry-neng.stthi.com](https://registry-neng.stthi.com) |
| **SonarQube** | [https://sast-neng.stthi.com](https://sast-neng.stthi.com) |

### Application Environments
| Environment | URL |
| :--- | :--- |
| **Production** | [https://bookinfo-neng.stthi.com](https://bookinfo-neng.stthi.com) |
| **UAT** | [https://bookinfo-neng-uat.stthi.com](https://bookinfo-neng-uat.stthi.com) |
| **Dev** | [https://bookinfo-neng-dev.stthi.com](https://bookinfo-neng-dev.stthi.com) |

---

## 🚀 Deployment Pipeline

The pipeline is designed with **Security Gates**:
1. **SCA & SAST:** Check dependencies and code quality using **Dependency Check** and **SonarQube**.
2. **Container Security:** Scan Docker images in **Harbor** using **Trivy**.
3. **IaC Security:** Validate Kubernetes manifests/Helm charts using **KICS**.
4. **Automated Deployment:** Deploy to GKE using **Helm** across Dev, UAT, and PRD.
5. **DAST:** Run dynamic security scans with **OWASP Zap** on the running environment.

---
**Maintainer:** Opsta Bootcamp Student  
**Year:** 2026
