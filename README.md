# OWASP Top 10 Web Application Security Assessment for GRC Professionals

**Author:** Ebere Emilia Ikechukwu

---

## Introduction

Web applications remain one of the most frequently targeted assets in modern cyberattacks. As organizations increasingly rely on web-based services, identifying and mitigating application vulnerabilities has become critical for both cybersecurity and compliance teams.

This project focused on assessing vulnerable web applications using the OWASP Top 10 framework, which highlights the most critical web application security risks. The objective was not only to identify technical vulnerabilities but also to evaluate their business, governance, risk and compliance (GRC) implications.

---

## Scenario & Business Context

A security assessment was conducted on the OWASP Broken Web Applications (BWA) platform.

Due to an upcoming organizational merger, the environment was required to meet updated security and compliance standards. The assessment focused on identifying security weaknesses, mapping findings to the OWASP Top 10 framework, and evaluating their potential impact on business operations, regulatory obligations, and organizational risk exposure.

---

## Assessment Objectives

- Identify vulnerable web applications and exposed services on the target system  
- Configure and utilize Burp Suite Professional for traffic interception and analysis  
- Detect vulnerabilities aligned with the OWASP Top 10 framework  
- Assess compliance and business risk impact  
- Present findings in a structured and auditable format  

---

## Scope of Assessment

### Target Environment
- OWASP Broken Web Applications (BWA) VM  

### Applications Tested
- BodgeIt Store  
- WebGoat  

### Testing Type
- Internal web application security assessment  
- Controlled laboratory environment  

---

## Lab Environment Setup

| Component | Description |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | OWASP Broken Web Applications VM |
| Interception Tool | Burp Suite Professional |

---

# Technical Methodology

## Phase 1: Discovery & Reconnaissance

### Step 1: Target Discovery
The target system was verified as active and reachable using network connectivity testing.

---

### Step 2: Service Enumeration
A network scan was performed using Nmap to identify exposed services and open ports.

**Nmap Service Enumeration** (Go to images folder to view all pictures)

---

### Step 3: Application Discovery
Multiple vulnerable applications were discovered, including:
- BodgeIt Store  
- WebGoat  

---

## Phase 2: Tool Configuration & Scanning

### Step 4: Burp Suite Configuration
Burp Suite was configured as an interception proxy to capture and analyze HTTP traffic.

**Burp Suite Configuration** (Go to images folder to view all pictures)

---

### Step 5: Automated Scanning
Automated scanning was performed to identify:
- Common vulnerabilities  
- Misconfigurations  
- Security weaknesses  

**Burp Suite Automated Scan** (Go to images folder to view all pictures)

---

# Manual Testing & OWASP Top 10 Validation

## A01: Broken Access Control
An unprotected administrative endpoint (`/admin.jsp`) was accessible without authentication.

**Evidence:** (Go to images folder to view all pictures)

---

## A02: Cryptographic Failures
Sensitive credentials were transmitted in plaintext over the network.

**Evidence:** (Go to images folder to view all pictures)

---

## A03: Injection
SQL Injection was identified through manipulation of input fields.

**Evidence:** (Go to images folder to view all pictures)

---

## A07: Authentication Failures
Weak password policies and lack of account lockout controls were observed.

---

# Risk Assessment & Mapping

| OWASP Category | Vulnerability | Application | Risk Level | Compliance | Business Impact |
|---|---|---|---|---|---|
| A01 | Broken Access Control | BodgeIt Store | High | PCI DSS 7.2.1 | Unauthorized admin access |
| A02 | Cryptographic Failures | WebGoat | High | PCI DSS 4.1 | Credential exposure |
| A03 | Injection | BodgeIt Store | High | PCI DSS 6.5.1 | Database compromise |
| A07 | Auth Failures | BodgeIt Store | Medium–High | NIST PR.AC-1 | Unauthorized access |

---

# Key Findings

- Critical SQL Injection vulnerability identified  
- Administrative access control bypass detected  
- Sensitive data transmitted without encryption  
- Weak authentication controls observed  

---

# Executive Summary

A full security assessment was performed on a legacy web application environment using the OWASP Top 10 framework.

The assessment revealed multiple high-risk vulnerabilities requiring immediate remediation to prevent:
- Data breaches  
- Regulatory violations  
- Financial losses  
- Reputational damage  

---

# Recommendations

- Implement secure coding practices (parameterized queries, input validation)  
- Enforce strong authentication and access control  
- Implement HTTPS/TLS encryption  
- Integrate security testing into SDLC  
- Conduct developer security training  

---

# Conclusion

The system presents a **high security risk** and requires urgent remediation to align with modern security and compliance standards.

---

# Disclaimer

All testing was conducted in a controlled educational environment using intentionally vulnerable systems.

---

# Project Deliverables

## Report Document

📄 **Official Lab Report Download Link:** [OWASP_Top_10 Web_Application_Testing for_GRC Professionals_Ebere_Emilia_IKechukwu.pdf](OWASP_Top_10%20Web_Application_Testing%20for_GRC%20Professionals_Ebere_Emilia_IKechukwu.pdf)

---

## GitHub Repository Structure

```text
OWASP-Top10-GRC-Assessment/
│
├── README.md
├── OWASP_Top_10 Web_Application_Testing for_GRC Professionals_Ebere_Emilia_IKechukwu.pdf
├── reports/
│   └── (Go to images folder to view all pictures)
├── screenshots/
│   └── (Go to images folder to view all pictures)
├── methodology/
│   └── testing-methodology.md
└── remediation/
    └── recommendations.md

#grc #riskmanagement #cybersecurity
