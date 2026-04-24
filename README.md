End-to-End DevSecOps Pipeline Project

Overview

This project demonstrates a full DevSecOps implementation securing an application across the software development lifecycle.

It integrates automated security controls into CI/CD pipelines, containerization, terraform, and runtime environments.


Architecture

CI/CD: Jenkins pipeline
Containerization: Docker
Orchestration: Kubernetes
Security Scanning:
  * SAST
  * SCA
  * Container scanning
  * DAST
* Supply Chain Security:
  * SBOM generation
  * Image signing & verification

Security Controls Implemented
1. Static Application Security Testing (SAST)
* Integrated SonarQube into Jenkins pipeline
* Enforced quality gates to block insecure code

2. Software Composition Analysis (SCA)
* Scanned dependencies for vulnerabilities
* Blocked builds on high/critical issues

3. Container Security
* Hardened Docker images (non-root user, minimal base image)
* Scanned images for vulnerabilities

4. SBOM Generation
* Generated CycloneDX SBOM using Trivy
* Stored artifacts for traceability

5. Dynamic Application Security Testing (DAST)
* Performed runtime scanning using OWASP ZAP

6. Image Signing & Verification
* Signed container images using Cosign
* Verified integrity before deployment

7. Kubernetes Security
* Implemented RBAC and network policies
* Enforced least privilege access

8. Terraform Security
* Secure terraform code using Checkov before deployment.
* Ensure misconfiguration of terraform code is corrected before deployment.

CI/CD Pipeline Flow
1. Code Commit Trigger
2. SAST Scan
3. Dependency Scan (SCA)
4. Build Application
5. Build Container Image
6. SBOM Generation
7. Container Vulnerability Scan
8. Deploy to Staging
9. DAST Scan
10. Image Signing
11. Approval Gate
12. Production Deployment

Key Features
* Security enforced at every stage of CI/CD
* Automated failure on high-risk vulnerabilities
* Supply chain protection via signed artifacts
* Continuous integration on every commit

Results
* Reduced vulnerable dependencies
* Eliminated hardcoded secrets
* Improved container security posture
* Ensured artifact integrity before deployment

Lessons Learned
* Security must be integrated early (shift-left)
* Automation is critical for consistency
* Supply chain security is essential in modern DevOps

Future Improvements

* Add Infrastructure as Code scanning
* Implement runtime policy enforcement
* Integrate SIEM for monitoring

Author

Femi Omogbehin (DevSecOps Engineer) Portfolio Project
