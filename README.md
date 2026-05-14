# Comprehensive Web Assessment & Security Governance (Graduation Project)

## 📌 Project Overview
This repository contains the full documentation for my Cybersecurity Graduation Project. The project is divided into three comprehensive phases, moving from active technical exploitation of a vulnerable web environment (`testphp.vulnweb.com`) to high-level security governance and quantitative risk analysis. 

Instead of merely listing technical vulnerabilities, this project bridges the gap between offensive security and enterprise risk management by calculating financial impacts and drafting organizational security policies.

## 🎯 Scope & Target Environment
* **Target Application:** `http://testphp.vulnweb.com`
* **Assessment Types:** Vulnerability Assessment, Network Traffic Analysis, Quantitative Risk Analysis, and Policy Governance.

## 🛠️ Tools & Methodologies
* **Offensive Tools:** Nmap (Network Mapping), Nessus (Vulnerability Scanning), Burp Suite (Web Proxy).
* **Traffic Analysis:** Wireshark (Deep-packet inspection).
* **Governance Frameworks:** Quantitative Risk Analysis formulas (SLE, ARO, ALE), standard IT policy structuring.

## 📂 Phase Breakdown & Key Findings

### Phase 1: Reconnaissance & Vulnerability Assessment
* **Objective:** Map the external attack surface and identify critical system flaws.
* **Findings:** Leveraged Nmap and Nessus to uncover multiple high-severity vulnerabilities, including a **CVSS 10.0** vulnerability tied to an End-of-Life PHP backend. 
* **Impact:** The outdated infrastructure allowed for severe exploitation, leaving the underlying database and server open to remote code execution and data exfiltration.

### Phase 2: Network Traffic Analysis & Web Hardening
* **Objective:** Analyze in-transit data and evaluate transport-layer defenses.
* **Findings:** Intercepted network traffic using Wireshark and identified severe transport-layer weaknesses. The application lacked basic HTTPS enforcement, transmitted session cookies insecurely over plaintext, and was missing critical security headers (CSP, HSTS).
* **Impact:** Any attacker positioned on the network could easily perform Man-in-the-Middle (MITM) attacks, sniffing plaintext credentials and hijacking active user sessions.

### Phase 3: Quantitative Risk Analysis & Security Policy Design
* **Objective:** Translate technical vulnerabilities into business risk metrics and establish a governance framework.
* **Quantitative Risk Analysis (GRC):** Conducted a financial impact assessment on the exposed customer database. Calculated the Single Loss Expectancy (SLE), Annualized Rate of Occurrence (ARO), and Annualized Loss Expectancy (ALE) to justify security budgets to executive management.
* **Security Governance:** Authored comprehensive organizational security policies from scratch, including:
  * Acceptable Use Policy (AUP)
  * Corporate Password Policy
  * Incident Reporting & Response Guidelines

## 🛡️ Strategic Remediation Strategy
I developed a structured, three-phase system hardening strategy to address the identified risks:
1. **Platform Modernization:** Decommission End-of-Life PHP and migrate to a supported, secure backend framework.
2. **Transport-Layer Security:** Enforce TLSv1.3 across all endpoints, implement HSTS, and secure all session cookies with `HttpOnly` and `Secure` flags.
3. **Defense-in-Depth:** Deploy a Web Application Firewall (WAF) to filter malicious traffic and monitor for future injection attempts.

## 📄 Repository Structure
* [Phase 1: Vulnerability Assessment Report](./QUESTION_1_Vulnerability_Assessment.pdf) - Full Nmap/Nessus scanning report and findings.
* [Phase 2: Network Traffic Analysis Report](./QUESTION_2_Traffic_Analysis.pdf) - Wireshark deep-packet inspection and HTTP/TLS analysis.
* [Phase 3: Quantitative Risk Analysis Report](./Question_3_Risk_and_Governance.pdf) - Financial risk calculations (ALE) and corporate security policies.
