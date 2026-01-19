# Threat Model

## Overview
This document identifies potential threats to the phishing detection system and explains how risks are mitigated.

## Identified Threats

### 1. Phishing Attacks
Threat:
- Attackers may attempt to bypass detection logic using obfuscated or shortened URLs

Mitigation:
- Keyword analysis and suspicious domain detection
- Continuous improvement through rule-based detection

### 2. Authentication Risks
Threat:
- Unauthorized access to admin or analysis features
- Credential stuffing or brute-force attempts

Mitigation:
- Secure login mechanism
- Role-based access control (RBAC)
- Optional multi-factor authentication (MFA)

### 3. Input Validation Risks
Threat:
- Malicious input such as scripts or malformed data (XSS, injection)

Mitigation:
- Server-side input validation
- Escaping output in templates
- Controlled rendering using Jinja2

### 4. Dependency Vulnerabilities
Threat:
- Vulnerable third-party Python packages

Mitigation:
- Dependency scanning using `pip-audit`
- Regular updates via `requirements.txt`
- Automated checks in CI pipeline

## Risk Summary
By combining secure coding practices, dependency scanning, and CI automation, the system reduces its overall attack surface.
