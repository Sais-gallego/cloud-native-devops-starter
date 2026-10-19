# ☸️ Cloud-Native DevOps Reference Architecture

[![CI/CD Pipeline](https://github.com/Sais-gallego/cloud-native-devops-starter/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/Sais-gallego/cloud-native-devops-starter/actions/workflows/ci-cd.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.28%2B-326CE5.svg)](https://kubernetes.io/)
[![Docker](https://img.shields.io/badge/Docker-Multi--Stage-2496ED.svg)](https://www.docker.com/)

Production-grade, enterprise-ready reference architecture and templates for deploying secure, resilient, and scalable microservices on Kubernetes and Cloud Native infrastructure.

Authored by **Sergio Andrés Ipuz Saavedra** ([@Sais-gallego](https://github.com/Sais-gallego)), Full Stack & DevOps Specialist with certifications in Kubernetes (University of Helsinki), Docker, and AWS Cloud.

---

## 🏛️ Architecture Overview

```
[ Ingress Nginx + TLS (Cert-Manager) ]
                │
         (NetworkPolicy)
                ▼
[ Pod Replicas (HPA 3-10) Non-Root ] ◄──► [ Prometheus & Grafana ]
                │
         (Private Subnet)
                ▼
[ StatefulSet PostgreSQL 16 & Redis 7 ]
```

---

## 📦 What's Included

* **🐳 Hardened Dockerfiles:** Multi-stage, distroless, non-root user execution (`Node.js`, `Python`, `Go`).
* **☸️ Kubernetes Production Manifests:**
  * Deployments with fine-grained `securityContext` (`readOnlyRootFilesystem`, `drop: ["ALL"]`).
  * Automated Zero-Trust `NetworkPolicy` rules.
  * Ingress with automated Let's Encrypt SSL/TLS via `cert-manager`.
  * Horizontal Pod Autoscaling (HPA) policies.
* **⚓ Helm 3 Chart:** Standardized parameters for staging and production deployments.
* **🚀 GitHub Actions CI/CD:** Automated manifest validation and multi-arch build testing.

---

## 📄 License
Released under the [MIT License](LICENSE).
