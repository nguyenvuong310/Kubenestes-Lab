# Kubernetes Labs — Step-by-step student guide

This repository contains a sequence of hands-on Kubernetes labs. Each lab folder (lab1, lab2, ...) contains the lab description and example manifests or code. This README gives students a consistent, step-by-step workflow to complete each lab, common checks, and per-lab quick-start instructions.

## Quick start (one-time)

```shell
git clone https://github.com/nguyenvuong310/Kubenestes-Lab.git
cd Kubenestes-Lab
```

## Presentation Content

### 1. Overview — Kubernetes Fundamentals

- What Kubernetes is and its main purpose
- Problems Kubernetes solves in containerized environments
- Core features:
  - Automated deployment
  - Self-healing
  - Horizontal scaling
- High-level Kubernetes architecture:
  - Control Plane components
  - Worker Node components
- Role of the Kubernetes API Server
- Basic Kubernetes objects:
  - Pod
  - Deployment
  - Service
- Differences between:
  - Containers vs Virtual Machines
  - Docker vs Kubernetes

### 2. CI/CD with Kubernetes

- Definition of Continuous Integration (CI)
- Definition of Continuous Deployment / Delivery (CD)
- Why CI/CD is important in Kubernetes-based systems
- Typical CI/CD workflow for Kubernetes applications
- Container image build and registry concepts
- Deployment strategies in Kubernetes:
  - Rolling updates
  - Rollbacks
- CI tools commonly used with Kubernetes:
  - Jenkins
  - GitLab CI
  - GitHub Actions
- CD tools and approaches:
  - kubectl-based deployments
  - Helm charts
  - GitOps and ArgoCD

### 3. Logging in Kubernetes

- Purpose of logging in distributed systems
- Differences between traditional logging and Kubernetes logging
- How Kubernetes handles application logs
- Standard output (stdout) and standard error (stderr) logging
- Centralized logging concepts
- Common logging architectures (e.g. EFK / ELK)
- Log collection tools:
  - Fluentd
  - Filebeat
- Log storage and visualization tools:
  - Elasticsearch
  - Kibana
- Logging best practices:
  - Structured logging
  - Metadata and labels
  - Log retention policies

## 4. Monitoring Kubernetes

- Purpose of monitoring in cloud-native systems
- Difference between monitoring and logging
- Types of metrics in Kubernetes:
  - Node metrics
  - Pod metrics
  - Application metrics
- Prometheus architecture and concepts
- Metrics exposition and scraping
- Grafana dashboards and visualization
- Alerting concepts and Alertmanager
- Health checks and probes:
  - Liveness probes
  - Readiness probes
- How monitoring supports scaling and reliability

## General workflow for each lab

**Lab 1 — Basics / Hello Kubernetes**

Quick intro to kubectl and core primitives (Pod, Service). Deploy a simple app and inspect pods, logs and service endpoints.

**Lab 2 — Multi-component app**

Deploy a multi-component application (frontend + backends). Focus on service-to-service communication, selectors, and basic troubleshooting.

**Lab 3 — Microservices sample**

Explore a small microservice demo: frontend, service-a, service-b. Build or run sample images and apply manifests in k8s-yaml to see inter-service requests and routing.

**Lab 4 — Stateful workloads / MySQL**

Deploy MySQL with PersistentVolume and PersistentVolumeClaim. Practice creating PV/PVC, initializing a database from SQL, and validating persistent storage across pod restarts.

**Lab 5 — Practice deploy Microservices**

Hands-on tasks described in lab5.md — typically configuration validation and applying manifests; read the lab file for exact objectives and exercises.

**Lab 6 — Jenkins CI on Kubernetes**

Deploy Jenkins with a PV/PVC, expose via NodePort, create a Pipeline using the sample Jenkinsfile, run npm test for the sample app, and integrate basic GitHub triggers. Includes sample files under sample.

**Lab 7 — Deploy ArgoCD**

Deploy ArgoCD in a dedicated namespace and expose its web interface using a NodePort service.

**Lab 8 — Cluster logging (EFK stack)**

Deploy Elasticsearch (StatefulSet), Fluent Bit (DaemonSet + ConfigMap) and Kibana in the kube-logging namespace. Verify logs are collected from /var/log/containers and searchable in Kibana.

**Lab 9 — Helm fundamentals**

Learn Helm 3: scaffold a chart (helm create), use values.yaml, render templates, install/upgrade/rollback releases, lint/package charts and use local repos. Exercises scaffold a minimal myweb nginx chart.

**Lab Final**

This final lab consolidates all knowledge and skills from previous labs into a single.
