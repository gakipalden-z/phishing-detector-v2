# OWASP Security Testing

## Overview
This document maps the OWASP Top 10 risks to the phishing detection application and explains mitigation strategies.

## Relevant OWASP Top 10 Risks

### A1: Broken Access Control
Mitigation:
- Role-based access control implemented in backend
- Restricted admin functionality

### A2: Cryptographic Failures
Mitigation:
- Sensitive credentials are not stored in plain text
- Environment variables used for secrets (not committed to GitHub)

### A3: Injection
Mitigation:
- No direct database queries
- Input validation and controlled processing of user input

### A7: Identification and Authentication Failures
Mitigation:
- Secure login system
- Optional MFA for enhanced authentication security

### A8: Software and Data Integrity Failures
Mitigation:
- Dependency integrity checked using `pip-audit`
- Automated CI pipeline prevents insecure code from merging

## Security Testing Tools
- Bandit: Static analysis for Python security issues
- pip-audit: Dependency vulnerability scanning
- pytest: Automated test execution

## Conclusion
The application aligns with OWASP recommendations by integrating security checks throughout the development lifecycle.
