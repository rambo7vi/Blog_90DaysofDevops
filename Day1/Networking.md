| Layer | Purpose | Real-World Example |
|-------|---------|---------------------|
| **7. Application** | Interfaces with software apps | **HTTP** for web pages, **SMTP** for email |
| **6. Presentation** | Data translation & encryption | **SSL/TLS** encrypts data for HTTPS |
| **5. Session** | Starts & maintains connections | **Remote login session** using **SSH** |
| **4. Transport** | Reliable data transfer | **TCP** ensures full message delivery |
| **3. Network** | Routes data packets | **IP** assigns addresses and routes traffic |
| **2. Data Link** | Error detection, frame delivery | **Ethernet, Wi-Fi MAC** addresses |
| **1. Physical** | Transmits raw bits | **Cables, switches, wireless signals** |

| TCP/IP Layer | Corresponding OSI Layers | Real-World Example |
|--------------|--------------------------|---------------------|
| **Application** | OSI Layers 5–7 | **HTTP**, **DNS**, **SSH**, etc. |
| **Transport** | OSI Layer 4 | **TCP**, **UDP** |
| **Internet** | OSI Layer 3 | **IP**, **ICMP** |
| **Network Access** | OSI Layers 1–2 | **Ethernet**, **Wi-Fi** |

Browser uses HTTP (Layer 7)

HTTP request is encrypted via TLS (Layer 6)

Session is managed via cookies or persistent connection (Layer 5)

Data is broken into TCP segments (Layer 4)

Routed via IP (Layer 3)

Sent as Ethernet frames (Layer 2)

Over Wi-Fi or cable (Layer 1)

---Essential Network Protocols and Ports for DevOps:
| Protocol | Port | Purpose | DevOps Relevance |
|----------|------|---------|------------------|
| **HTTP** | 80 | Web traffic | Basic web servers, API calls |
| **HTTPS** | 443 | Secure web traffic | Secure API calls, dashboards (e.g., Grafana, Jenkins) |
| **FTP** | 21 | File transfer | Transferring deployment artifacts |
| **SSH** | 22 | Secure remote login | Managing servers, Ansible, Git (SSH keys) |
| **DNS** | 53 | Domain resolution | Resolving service URLs, internal DNS |
| **SMTP** | 25 / 587 | Sending email | Sending alerts from CI/CD tools |
| **SNMP** | 161 | Monitoring network devices | Infrastructure health checks |
| **NTP** | 123 | Time sync | Ensuring time consistency in logs |
| **MySQL** | 3306 | DB communication | Database connections from apps |
| **PostgreSQL** | 5432 | DB communication | Similar to MySQL for Postgres setups |
| **Docker API** | 2375 / 2376 | Docker engine communication | Remote container management |
| **Kubernetes API** | 6443 | K8s control plane | kubectl and cluster management |

🔒 Secure server management via SSH

📦 Artifact deployment using FTP or HTTPS

📈 Monitoring via SNMP/NTP

☁️ Service resolution using DNS

📬 Notifications through SMTP

🧪 Running CI/CD pipelines using services on known ports
