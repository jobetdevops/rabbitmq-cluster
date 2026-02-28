# 🐇 RabbitMQ High-Availability Cluster for Symfony Microservices

![RabbitMQ](https://img.shields.io/badge/RabbitMQ-4.2.3-orange)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04_LTS-E95420)
![DigitalOcean](https://img.shields.io/badge/Infrastructure-DigitalOcean-blue)
![Security](https://img.shields.io/badge/Security-Zero_Trust-success)
![Monitoring](https://img.shields.io/badge/Monitoring-Prometheus_|_Grafana-informational)

---

## 📌 Overview

This project documents the design and deployment of a **3-node RabbitMQ cluster** built to support **10 staging Symfony-based PHP servers** handling **thousands of microservice messages** within a website stack.

### 🎯 Objectives

- High Availability (HA)
- Secure-by-design architecture
- Private network isolation
- Zero publicly exposed services
- Full observability and alerting

The platform provides a resilient, production-grade messaging backbone for distributed application components in staging environments.

---

# 🏗 Architecture

## Infrastructure Provider
- **DigitalOcean**

## Hardware Configuration

| Component | Specification |
|------------|--------------|
| Nodes | 3 Droplets |
| CPU | 2 vCPU (AMD) |
| RAM | 4 GB DDR5 |
| Network | Private VPC |

All nodes are deployed inside the same **private network** as the 10 staging Symfony application servers.

---

# 🧱 Software Stack

| Layer | Technology |
|--------|------------|
| OS | Ubuntu 24.04 LTS |
| Message Broker | RabbitMQ 4.2.3 |
| Monitoring | Prometheus |
| Visualization | Grafana |
| Alerting | AlertManager |

---

# 🔐 Security Architecture

Security was a **primary design requirement**, not an afterthought.

---

## 🛡 OS Hardening

- CIS Benchmark hardening for Ubuntu 24.04
- Kernel live patching enabled
- Cloud provider firewalls configured
- SSH hardening (key-based authentication, restricted access)
- Minimal attack surface configuration

---

## 🔒 Zero-Trust Secure Access

🚫 **No public ports are exposed**

Secure administrative access is achieved using:

- Cloudflare Zero Trust Tunnels
- Encrypted SSH access via Cloudflare
- Encrypted Web UI access via Cloudflare
- Identity-aware access policies

### ✅ Security Benefits

- No public IP exposure
- End-to-end encryption
- Controlled administrative access
- Reduced attack surface
- Zero Trust access model

---

# 🧩 High Availability Design

The 3-node RabbitMQ cluster ensures:

- Node redundancy
- Automatic failover
- Data replication across nodes
- Clustered message queues for resilience

The staging Symfony servers connect through the private network, ensuring:

- Low latency
- Secure communication
- Isolated message traffic

---

# 📊 Monitoring & Observability

A full observability stack has been implemented:

- Prometheus for metrics scraping
- System exporters for node metrics
- RabbitMQ metrics integration
- Grafana dashboards for visualization
- AlertManager configured to forward alerts via:
  - Slack
  - Email
  - Pager

### 📈 Monitored Metrics

- Node health
- Queue depth
- Memory usage
- CPU utilization
- Cluster status
- Service availability

This enables proactive monitoring and rapid incident response.

---

# 🚀 Use Case

This infrastructure supports:

- Asynchronous processing
- Microservices communication
- Event-driven architecture
- Scalable backend operations
- Reliable staging validation before production

---

# 🏆 Key Achievements

- Designed and deployed a secure HA RabbitMQ cluster
- Integrated Zero Trust access model
- Eliminated publicly exposed infrastructure
- Implemented full monitoring and alerting stack
- Enabled scalable microservices communication for Symfony applications
- Built production-grade architecture within staging environment

---

# 🏁 Conclusion

This project demonstrates:

- Advanced DevOps architecture expertise
- Secure-by-design infrastructure mindset
- High-availability clustering implementation
- Observability engineering
- Zero Trust network architecture
- Enterprise-grade messaging platform deployment

---

## 👤 Author

Senior DevOps Engineer | Cloud & Kubernetes Architect | AI Infrastructure & Security Enthusiast

---
