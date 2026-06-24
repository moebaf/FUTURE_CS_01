# FUTURE_CS_01 - Task 01
# Scanning Our Target

## Introduction

under this file i will be explaing some of the vulnarbilities found when scanning our target we scanned our target in the file before 'scanning_our_target'.
the format remains the same ohase one is vulnarabilities found in owasp,phase 02 vuln found using nmap and phase 03 


# phase01 owasp zap vulnarabilities 

## Vulnerability 1 – Content Security Policy (CSP) Header Not Set

### Description
During the OWASP ZAP scan, I identified that the target website did not have a Content Security Policy (CSP) header configured. A CSP header is an important security mechanism that helps prevent attacks such as Cross-Site Scripting (XSS) by controlling which resources can be loaded and executed by a user's browser. Without a properly configured CSP, malicious scripts may be executed if an attacker is able to inject content into the application.

### Evidence
<img width="680" height="384" alt="image" src="https://github.com/user-attachments/assets/5888e56b-9310-4853-bae0-f91d8841b4c2" />










