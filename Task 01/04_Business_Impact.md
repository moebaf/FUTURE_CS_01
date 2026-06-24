# FUTURE_CS_01 - Task 01

# Business Impact

## Introduction

Security vulnerabilities can affect organizations in different ways depending on the nature of the weakness and the assets being protected. This section explains the potential business impact associated with each vulnerability identified during the assessment.

---

## Business Impact Analysis

### Content Security Policy (CSP) Header Not Set

A missing CSP header may increase the risk of successful Cross-Site Scripting (XSS) attacks. If exploited, attackers could execute malicious scripts within users' browsers, potentially leading to account compromise, session hijacking, or theft of sensitive information. Such incidents may damage customer trust and the organization's reputation.

---

### CSP Failure to Define Directive with No Fallback

Weak CSP configurations reduce the effectiveness of browser security controls. While the immediate impact is limited, the issue may contribute to the success of other attacks and weaken the organization's overall security posture.

---

### Cross-Domain Misconfiguration

Improper cross-domain policies may allow unauthorized websites to interact with application resources. This could result in data leakage, unauthorized access to information, and increased exposure to cross-origin attacks that affect user privacy and data confidentiality.

---

### CSP script-src unsafe-eval

Allowing unsafe-eval increases the likelihood of malicious code execution within the browser. If combined with another vulnerability such as XSS, attackers may gain access to user sessions, manipulate application behavior, or steal sensitive information. This could lead to financial losses, regulatory concerns, and reputational damage.

---

### FTP Service Exposed (Port 21)

An exposed FTP service may allow attackers to intercept credentials or transferred files if encryption is not enforced. Unauthorized access to business systems could result in data breaches, operational disruption, and potential loss of sensitive information.

---

### Information Disclosure Through Service Enumeration

Publicly exposed software versions provide attackers with valuable reconnaissance information. This may enable them to identify known vulnerabilities and launch targeted attacks against the organization's infrastructure.

---

### Multiple Exposed Services Increasing Attack Surface

Each publicly accessible service presents a potential entry point for attackers. A larger attack surface increases the likelihood of successful compromise if any exposed service contains vulnerabilities or misconfigurations.

---

## Conclusion

Although not all findings directly expose the application to compromise, each contributes to the organization's overall risk profile. Addressing these issues proactively helps reduce security risks, protect sensitive information, and maintain customer trust.
