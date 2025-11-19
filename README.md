Objective:
The objective of this assignment is to apply DevSecOps principles to container security. Specifically, the goals are:
1.To build a baseline Docker image and run a vulnerability scan using Trivy.
2.To identify and document vulnerabilities in a professional security report.
3.To harden the Dockerfile by using a minimal base image (Alpine), creating a non‑root user, and adding a HEALTHCHECK instruction.
4.To rescan the hardened image and compare results with the baseline, showing improvements in security posture.



How i approached the task:
I approached this task in a structured way, step by step, to make sure I covered both the technical and security aspects:
Step 1: Baseline Setup
I started by writing a baseline Dockerfile using the official Node.js 18 image.Built the image (myapp:baseline) and added a simple Node.js app (server.js) to run inside the container.This gave me a working container to scan.
Step 2: Vulnerability Scan
I used Trivy to scan the baseline image.Documented the vulnerabilities found (2 High, 1 Low).This established the initial security posture.
Step 3: Harden the Dockerfile
I improved the Dockerfile by applying DevSecOps best practices:
Switched to Alpine base image (smaller, reduced attack surface).Created a non‑root user to enforce least privilege.Added a HEALTHCHECK instruction for runtime monitoring.Built the hardened image (myapp:secure).
Step 4: Rescan & Compare
Ran Trivy again on the hardened image.Found OS‑level vulnerabilities (OpenSSL) plus the same app‑level issues.
Step 5: Documentation & Reporting
Wrote a Security Scan Report with baseline vs hardened results.Explained why hardened image shows more vulnerabilities but is still more secure in practice.Concluded with DevSecOps principle: scan → fix → rescan → document.
