# 🛡️ Zero-Trust Cloud Infrastructure (AWS + Cloudflare + GoDaddy)

A capstone project implementing a **Zero-Trust security architecture** that integrates **AWS EC2**, **Cloudflare WAF/Tunnel/Access**, and **GoDaddy DNS**.  
Designed to protect high-risk business environments (finance, e-commerce) by enforcing **TLS 1.3 encryption**, **DNSSEC**, and **identity-based access via GitHub SSO**.

---

## 🏗️ Architecture Overview

### Components
- **AWS EC2 Instance:** Secure hosting for the web service with limited HTTPS access.  
- **Cloudflare WAF & Tunnel:** Masks public IPs, routes encrypted traffic, enforces Zero Trust rules.  
- **GitHub SSO Integration:** Centralized user identity management via OAuth2.  
- **GoDaddy DNS:** Managed domain with DNSSEC for tamper-proof resolution.  
- **AWS GuardDuty + CloudTrail:** Continuous threat detection and event logging.

---

## ⚙️ Implementation Highlights
| Phase | Summary |
|-------|----------|
| **Infrastructure Setup** | Deployed AWS EC2, restricted Security Groups, configured Elastic IP. |
| **Cloudflare Integration** | Enabled WAF, TLS 1.3 Full-Strict, DNSSEC, and caching for performance. |
| **SSO & Access Control** | Integrated GitHub SSO via Cloudflare Access; enforced role-based access. |
| **Monitoring & IR Plan** | Configured CloudTrail, GuardDuty, CloudWatch; authored 12-step IR Plan. |

---

## 📊 Results
- Reduced public attack surface by **~90%**.  
- Achieved full **end-to-end encryption** with TLS 1.3 and DNSSEC.  
- Implemented **Zero-Trust user verification** and **centralized monitoring**.  
- Designed for **GDPR / PCI DSS compliance**.

---

## 📁 Deliverables
| File | Description |
|------|-------------|
| [Project Charter](./Project-Charter.pdf) | Defines objectives, stakeholders, and risk strategy. |
| [Project Scope](./Project-Scope.pdf) | Outlines technical and business requirements. |
| [Final Report](./Final-Report.pdf) | Full documentation of implementation and outcomes. |
| [Cloudflare Steps](./Cloudflare-Steps.pdf) | Step-by-step configuration guide. |
| [Incident Response Plan](./Incident-Response-Plan.pdf) | Detailed playbook for detection and containment. |
| [Presentation Slides](./Presentation-Slides.pptx) | Final capstone presentation. |

---

## 🧠 Skills Demonstrated
✅ Cloud Security Architecture (AWS, Cloudflare, GoDaddy)  
✅ Identity & Access Management (SSO, OAuth2)  
✅ DNSSEC & TLS 1.3 Implementation  
✅ Zero-Trust Design & Policy Enforcement  
✅ Incident Response & Threat Detection (GuardDuty, CloudTrail)  
✅ Technical Documentation & Compliance Writing  

---

## 📈 Future Enhancements
- Deploy HAProxy or Load Balancer for redundancy  
- Integrate Splunk or ELK for SIEM correlation  
- Add MFA support to GitHub SSO  
- Automate DNS validation using Terraform  

---

**Author:** *Devarshi Mahadevwala*  
**Certification:** ISC² CC | CySA+ (In Progress)  
