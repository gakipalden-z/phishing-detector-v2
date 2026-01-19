# DevSecOps Implementation

This project implements DevSecOps principles by integrating security checks directly into the CI/CD pipeline.

## CI/CD Pipeline
- GitHub Actions is used to automate testing and security scanning
- The pipeline runs automatically on every push to the main branch

## Security Tools Used
- Bandit: Static Application Security Testing (SAST) for Python code
- pip-audit: Dependency vulnerability scanning
- pytest: Automated unit testing

## Benefits
- Early detection of vulnerabilities
- Secure-by-design development
- Continuous security validation
