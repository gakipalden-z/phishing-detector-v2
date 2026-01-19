# System Architecture

## Overview
This project is a Flask-based web application designed to detect phishing emails. 
It follows a simple three-layer architecture consisting of a backend application, frontend templates, and static assets.

## Backend Architecture
The backend is implemented using Python and Flask.

Main components:
- `server.py`: Main Flask application handling routes, authentication, and phishing analysis
- Business logic for analyzing email content and detecting phishing patterns
- Session-based authentication with role-based access control (RBAC)

## Frontend Architecture
The frontend uses Flask templates (Jinja2):

- HTML templates are stored in `src/backend/templates/`
- Templates include login, dashboard, email analysis, results, and admin views
- Templates dynamically render results returned by the backend

## Static Files
Static assets are stored in `src/backend/static/`:
- `styles.css` provides styling for all HTML pages
- Static separation improves maintainability and performance

## User Interaction Flow
1. User accesses the login page
2. User authenticates using credentials (and MFA if enabled)
3. User submits email content for analysis
4. Backend processes the email
5. Result is displayed using visual indicators (safe / suspicious / phishing)

## Deployment Architecture
- Source code is hosted on GitHub
- CI/CD pipeline is implemented using GitHub Actions
- Security and test checks run automatically on each push

