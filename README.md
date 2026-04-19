# Zabbix + Grafana Monitoring Lab (VM Infrastructure Project)

## Overview

This project consists of building a complete monitoring environment using Zabbix and Grafana on Linux and Windows virtual machines.

The goal was to simulate a production-like scenario focused on observability, network troubleshooting, tool integration, and automated alerting.

---

## Architecture

- Zabbix Server (Linux VM)
- Zabbix Frontend (Web UI)
- Linux Agent (multiple network interfaces)
- Windows Agent
- Grafana (dashboard visualization)
- Integration via Zabbix API
- Email alerts via Zabbix Media Types

---

## Objectives

- Implement centralized infrastructure monitoring
- Collect metrics from Linux and Windows machines
- Create host-separated dashboards in Grafana
- Configure automated email alerts
- Simulate a real observability environment
- Practice network and service troubleshooting

---

## Technologies Used

- Zabbix Server / Zabbix Agent
- Grafana
- Linux (Debian/Ubuntu)
- Windows Server / VM
- Multi-subnet networking
- Zabbix API
- SMTP (email alerts)

---

## Project Screenshots

### System Architecture
![Architecture](images/architecture.png)

### Grafana - Linux Dashboard
![Grafana Linux](images/grafana-linux.png)

### Grafana - Windows Dashboard
![Grafana Windows](images/grafana-windows.png)

### Zabbix Hosts
![Zabbix Hosts](images/zabbix-hosts.png)

### Real-time Metrics (Latest Data)
![Latest Data](images/latest-data.png)

### Email Alerts
![Email Alerts](images/email-alerts.png)

### Communication Test (zabbix_get)
![Terminal](images/terminal-zabbix-get.png)

---

## Issues and Solutions

### 1. Grafana + Zabbix Integration
- Issue: API connection failure
- Cause: incorrect endpoint configuration
- Solution: fixed API URL and authentication settings

---

### 2. EMPTY RESPONSE on Zabbix Agent
- Issue: zabbix_get returned no data
- Cause: mismatch between host IP and interface configuration
- Solution: corrected Server and ServerActive configuration

---

### 3. Network Conflicts
- Issue: multiple subnets (192.168.99.x and 192.168.244.x)
- Cause: routing confusion between network interfaces
- Solution: standardized Zabbix communication IP

---

### 4. Misconfigured Host in Zabbix Frontend
- Issue: agent not responding correctly
- Cause: incorrect interface IP assigned to host
- Solution: fixed host interface configuration

---

### 5. Communication Validation Tools
- zabbix_get
- nc (netcat)
- curl
- ss

---

## Results

- Fully functional monitoring environment
- Real-time metrics collection
- Host-separated Grafana dashboards
- Working email alert system
- Full infrastructure visibility

---

## Learnings

- Monitoring depends on correct communication between all components
- Small network misconfigurations can break the entire system
- CLI troubleshooting is essential for real-world environments
- Networking and interface configuration are critical in distributed systems
- Integration requires precision and validation

---

## Conclusion

This project strengthened my practical experience in infrastructure, monitoring, and troubleshooting in distributed environments.

It helped me develop a deeper understanding of how production-like systems operate and reinforced my skills in Linux, networking, and observability.

---

## Status

Functional project  
Stable environment  
Active monitoring
