# 🛡️ Zero-Trust Cloud Infrastructure (AWS + Cloudflare + GoDaddy)

This repository showcases a **Zero-Trust Cloud Infrastructure** designed and implemented as part of a postgraduate **Cybersecurity and Threat Management** capstone at **Seneca Polytechnic**.  
The project demonstrates a **real-world deployment of Zero-Trust principles** — integrating **AWS**, **Cloudflare Zero Trust**, and **GoDaddy DNS** — to eliminate public exposure, ensure encrypted communications, and enforce identity-based access control.

---

## 📘 Project Context
Organizations adopting cloud computing often face challenges balancing accessibility and security.  
Traditional perimeter security models fail against modern threats where insider risks, stolen credentials, and lateral movement dominate.

This project applies the **Zero-Trust security model** — *“never trust, always verify”* — by designing a multi-layered cloud environment with:
- Identity-based authentication  
- Continuous monitoring  
- Encrypted traffic paths  
- Minimal public attack surface  

The goal: secure a simulated corporate infrastructure hosting a web application while maintaining accessibility for verified users.

---

## ⚙️ Implementation Overview

### 🔹 1. AWS Cloud Infrastructure
- Provisioned **Amazon EC2 instance** as the secure backend host.  
- Applied **least-privilege Security Groups** allowing inbound traffic only over HTTPS (443) and SSH (22) from trusted IPs.  
- Configured **IAM roles** separating administrative and operational privileges.  
- Activated **CloudWatch**, **CloudTrail**, and **GuardDuty** for continuous logging, anomaly detection, and compliance visibility.  
- Allocated an **Elastic IP** and connected it to Cloudflare via encrypted tunnel for secure external access.

### 🔹 2. Cloudflare Zero Trust Configuration
- Onboarded the **GoDaddy domain** into Cloudflare DNS and enabled **DNSSEC** to protect DNS integrity.  
- Enforced **TLS 1.3 (Full-Strict)** for full encryption between users, Cloudflare, and origin.  
- Deployed **Cloudflare Tunnel** to hide the origin IP — removing any direct public access.  
- Configured **WAF rules** to block reconnaissance, injection, and DDoS attempts.

### 🔹 3. Access Control and SSO
- Implemented **Cloudflare Access** using **GitHub as an SSO provider** (OAuth2).  
- Created **Zero-Trust policies** based on user identity, device, and session context.  
- Validated SSO integration by restricting portal access to authorized GitHub organization members.

### 🔹 4. Incident Response and Monitoring
- Developed a **12-step Incident Response Plan (IRP)** outlining detection, containment, eradication, and recovery phases.  
- Tested detection workflows via **GuardDuty alerts** and **CloudWatch alarms** simulating brute-force and DDoS behaviors.  
- Centralized logs through **CloudTrail** for traceability and forensic readiness.

---

## 📄 Project Deliverables
| File | Description |
|------|--------------|
| [Project-Scope.pdf](./Project-Scope.pdf) | Defines objectives, success criteria, and technical scope |
| [Project-Proposal.pdf](./Project-Proposal.pdf) | Initial business and technical justification for the Zero-Trust model |
| [Product-Overview.pdf](./Product-Overview.pdf) | Executive summary of architecture and design choices |
| [Cloudflare-Configuration-Steps.pdf](./CloudFlare-Configuration-Steps.pdf) | Hands-on guide for Cloudflare DNSSEC, WAF, and Tunnel configuration |
| [Final-Report.pdf](./Final-Report.pdf) | Complete documentation covering design, results, and risk mitigation |
| [Final-Presentation-Slides.pptx](./Final-Presentation-Slides.pptx) | Final presentation used during project defense |

---

## 📈 Key Results
- Reduced attack surface by **approximately 90%** through Cloudflare Tunnel and private network routing.  
- Achieved **end-to-end encryption** using **TLS 1.3 (Full-Strict)** and **DNSSEC validation**.  
- Enforced **identity-based access control** with GitHub SSO and Cloudflare Access.  
- Enabled **proactive monitoring** and alerting through GuardDuty and CloudTrail.  
- Developed a complete **Incident Response Plan** tested against simulated attacks.

---

## 🧠 Skills Demonstrated
- **Zero-Trust Architecture Design**  
- **Cloud Security (AWS EC2, IAM, CloudTrail, GuardDuty)**  
- **Network Security (WAF, DNSSEC, TLS 1.3)**  
- **Identity & Access Management (SSO, OAuth2, RBAC)**  
- **Incident Response Planning & Detection Engineering**  
- **Technical Documentation & Compliance Writing**

---

## 🚀 Future Enhancements
- Implement **Terraform automation** for infrastructure provisioning.  
- Integrate **Splunk or ELK** for SIEM-based correlation and analytics.  
- Deploy a **multi-region AWS architecture** for disaster recovery.  
- Add **MFA enforcement** to the GitHub SSO workflow.  

---

## 📚 References
- [AWS Cloud Security Documentation](https://aws.amazon.com/security/)  
- [Cloudflare Zero Trust Platform](https://www.cloudflare.com/zero-trust/)  
- [MITRE ATT&CK Framework](https://attack.mitre.org/)  
- [OWASP Secure Configuration Guidelines](https://owasp.org/)  

---

**Author:** *Devarshi Mahadevwala*  
**Certifications:** ISC² CC | CySA+ (In Progress)  
*Cloud & Cybersecurity Professional*
