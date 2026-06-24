# FUTURE_CS_01 - Task 01

# Identifying Vulnerabilities

## Introduction

In this section, I analyze the vulnerabilities discovered during the assessment of the target application. The findings are organized according to the scanning methods used during the previous phase. Phase 01 contains vulnerabilities identified using OWASP ZAP, while Phase 02 contains issues discovered through Nmap reconnaissance and service enumeration.

---

# Phase 01 – Vulnerabilities Identified Using OWASP ZAP

## Vulnerability 1 – Content Security Policy (CSP) Header Not Set

### Description

During the OWASP ZAP scan, I identified that the target website did not have a properly configured Content Security Policy (CSP) header. CSP is an important security mechanism that helps protect web applications against attacks such as Cross-Site Scripting (XSS) by controlling which resources are allowed to execute within a user's browser. Without a CSP header, malicious scripts may be executed if an attacker successfully injects content into the application.

### Evidence

<img width="680" height="384" alt="image" src="https://github.com/user-attachments/assets/5888e56b-9310-4853-bae0-f91d8841b4c2" />

---

## Vulnerability 2 – CSP Failure to Define Directive with No Fallback

### Description

The OWASP ZAP scan identified a Content Security Policy configuration issue where one or more directives were not defined and no fallback policy was provided. When fallback directives are missing, browsers may apply less restrictive behavior than intended, potentially increasing the risk of unauthorized or malicious content being loaded and executed.

### Evidence

<img width="692" height="382" alt="image" src="https://github.com/user-attachments/assets/2b85d0e8-c1b6-4534-9644-b1628e081f93" />

---

## Vulnerability 3 – Cross-Domain Misconfiguration

### Description

OWASP ZAP generated an alert indicating a potential Cross-Domain Misconfiguration. This finding suggests that Cross-Origin Resource Sharing (CORS) or related cross-domain settings may be overly permissive. If improperly configured, attackers may be able to access resources from unauthorized origins, increasing the risk of data exposure and cross-origin attacks.

### Evidence

<img width="1326" height="769" alt="image" src="https://github.com/user-attachments/assets/73309932-005c-47a4-88f1-872e203fa60a" />

---

## Vulnerability 4 – CSP script-src unsafe-eval

### Description

The scan identified the use of the `unsafe-eval` directive within the Content Security Policy. This directive allows the execution of dynamically generated code through functions such as `eval()`, `setTimeout()`, and `setInterval()` when supplied with string arguments. Allowing `unsafe-eval` weakens CSP protections and may increase the risk of successful Cross-Site Scripting (XSS) attacks if malicious code is injected into the application.

### Evidence

<img width="1446" height="771" alt="image" src="https://github.com/user-attachments/assets/645e8909-a554-4d17-9224-8763bdfe34f5" />

---

# Phase 02 – Vulnerabilities Identified Using Nmap

## Vulnerability 1 – FTP Service Exposed (Port 21)

### Description

During the Nmap scan, I identified that an FTP service was accessible on port 21. FTP is a legacy protocol that does not encrypt data by default, making transmitted credentials and files vulnerable to interception. If the service is not properly secured, it may also be susceptible to brute-force attacks and unauthorized access attempts.

---

## Vulnerability 2 – Information Disclosure Through Service Enumeration

### Description

Nmap successfully identified technologies and service versions running on the target, including Apache HTTP Server 2.4.68 and F5 BIG-IP. While version disclosure is not a vulnerability by itself, publicly exposing detailed software information can assist attackers in researching known vulnerabilities and planning targeted attacks against the identified technologies.

---

## Vulnerability 3 – Multiple Exposed Services Increasing Attack Surface

### Description

The scan revealed several externally accessible services, including FTP, HTTP, HTTPS, and HTTP Proxy services. Each exposed service expands the organization's attack surface. If any of these services are misconfigured, unpatched, or improperly secured, they may provide attackers with potential entry points into the environment.

---

## Conclusion

The vulnerabilities identified during both OWASP ZAP and Nmap scanning demonstrate the importance of secure configuration, service hardening, and continuous security monitoring. While some findings represent misconfigurations rather than direct vulnerabilities, each issue contributes to the overall risk profile of the application and should be reviewed as part of a comprehensive security improvement strategy.
