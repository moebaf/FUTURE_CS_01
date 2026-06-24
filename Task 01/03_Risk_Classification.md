# FUTURE_CS_01 - Task 01

# Risk Classification

## Introduction

After identifying the vulnerabilities discovered through OWASP ZAP and Nmap scanning, I classified each finding according to its potential impact and likelihood of exploitation. Risk classification helps security teams prioritize remediation efforts by focusing on the issues that pose the greatest threat to the organization.

---

## Risk Classification Table

| Vulnerability                                       | Source    | Risk Level | Justification                                                                                                                                               |
| --------------------------------------------------- | --------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Content Security Policy (CSP) Header Not Set        | OWASP ZAP | Medium     | Missing CSP protections may increase the likelihood of successful Cross-Site Scripting (XSS) attacks if other vulnerabilities exist within the application. |
| CSP Failure to Define Directive with No Fallback    | OWASP ZAP | Low        | Missing fallback directives weaken browser security controls but do not directly expose the application to compromise.                                      |
| Cross-Domain Misconfiguration                       | OWASP ZAP | Medium     | Overly permissive cross-domain policies could allow unauthorized access to resources and increase exposure to cross-origin attacks.                         |
| CSP script-src unsafe-eval                          | OWASP ZAP | High       | The use of unsafe-eval weakens Content Security Policy protections and may facilitate exploitation of XSS vulnerabilities.                                  |
| FTP Service Exposed (Port 21)                       | Nmap      | Medium     | FTP does not provide encryption by default and may expose credentials or sensitive data if used insecurely.                                                 |
| Information Disclosure Through Service Enumeration  | Nmap      | Low        | Version disclosure assists attackers during reconnaissance but does not directly compromise the system.                                                     |
| Multiple Exposed Services Increasing Attack Surface | Nmap      | Medium     | Additional exposed services increase the number of potential entry points available to attackers.                                                           |

---

## Summary

Most findings identified during this assessment fall within the Low to Medium risk categories. However, the use of the CSP unsafe-eval directive represents a High-Risk finding due to its potential impact on browser-side security controls. Addressing higher-risk issues first will help reduce the overall attack surface and improve the security posture of the application.
