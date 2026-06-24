# FUTURE_CS_01 - Task 01

# Scanning Our Target

## Introduction

For this assessment, I selected OWASP Juice Shop as my target application. OWASP Juice Shop is an intentionally vulnerable web application developed by OWASP for security training and penetration testing practice. I chose this application because it provides a safe and realistic environment for identifying common web application vulnerabilities and improving my vulnerability assessment skills.

---

# Phase 01 – Scanning the Target Using OWASP ZAP

## Step 1 – Installing OWASP ZAP

To perform web application security testing, I installed OWASP ZAP on my Kali Linux machine. OWASP ZAP (Zed Attack Proxy) is an open-source web application security scanner used to identify vulnerabilities in web applications and APIs. It helps security professionals discover and assess common security weaknesses before they can be exploited by attackers.

<img width="722" height="310" alt="image" src="https://github.com/user-attachments/assets/5f98cfb0-e72c-4fe8-8f13-7c2835cba7e1" />

---

## Step 2 – Scanning the Website and Generating a Report

After launching OWASP ZAP, I configured the application to Attack Mode and entered the target URL:

`https://owasp.org/www-project-juice-shop/`

I then initiated an automated scan to identify potential security vulnerabilities and misconfigurations within the target application.

<img width="1919" height="924" alt="image" src="https://github.com/user-attachments/assets/8da77cc5-fca1-4bea-941f-2f70cd05561a" />

Once the scan was completed, I generated a report and exported it in HTML format for further analysis. The report has been included in this repository as:

**report.html**

---

## Full Scan Report

The complete OWASP ZAP scan report can be found in:

📄 **report.html**

---

# Phase 02 – Scanning the Target Using Nmap

## Running an Nmap Scan

To gather information about the target's exposed services, I performed a service version scan using the following command:

```bash
nmap -sV demo.owasp-juice.shop
```

The `-sV` option enables service version detection, allowing Nmap to identify the technologies and versions running on open ports.

<img width="509" height="204" alt="image" src="https://github.com/user-attachments/assets/c135549b-0a67-4ed8-85e8-ea016cd6b27e" />

The scan identified four open ports:

* FTP (21)
* HTTP (80)
* HTTPS (443)
* HTTP Proxy (8080)

Additionally, Nmap revealed technologies including an F5 BIG-IP load balancer and Apache HTTP Server 2.4.68.

Although the presence of open ports does not automatically indicate a vulnerability, exposed services increase the attack surface of a system. Misconfigured, outdated, or poorly secured services can provide opportunities for attackers to gain unauthorized access. The information gathered during this phase helped guide the vulnerability assessment activities performed in the next stage of the project.
