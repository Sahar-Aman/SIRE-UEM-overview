<div align="center">

# SIRE — University Lab Management System

**Full-stack web platform for the centralized management of university laboratories.**

*Solo-developed end-to-end · Final Degree Project · Universidad Europea de Madrid · Graded 10/10 with Distinction (Matrícula de Honor)*

![Status](https://img.shields.io/badge/status-handoff%20to%20production-blue)
![Grade](https://img.shields.io/badge/grade-10%2F10%20Matr%C3%ADcula%20de%20Honor-brightgreen)
![Stack](https://img.shields.io/badge/stack-Angular%20%7C%20Django%20%7C%20MySQL-informational)
![License](https://img.shields.io/badge/source-restricted-lightgrey)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Screenshots](#-screenshots)
- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Key Features](#-key-features)
- [User Roles & Permissions](#-user-roles--permissions)
- [Security](#-security)
- [Development Journey](#-development-journey)
- [My Role](#-my-role)
- [Outcome & Recognition](#-outcome--recognition)
- [Why the Code Isn't Public](#-why-the-code-isnt-public)
- [Contact](#-contact)

---

## 🎯 Overview

**SIRE** (*Sistema de Inventario y Reservas*) is a full-stack web application designed, developed and prepared for production deployment for the laboratories of **Universidad Europea de Madrid**. It replaces the fragmented, manual workflow previously based on spreadsheets, emails and paper forms with a single integrated platform that centralizes inventory, equipment, reservations, purchasing, and technical staff coordination.

The project was built end-to-end by a single developer over 5 months as a Final Degree Project (TFG), from initial stakeholder interviews with university lab staff to production-ready deployment configuration. It was graded **10 out of 10 with Distinction (Matrícula de Honor)** and, following the defense, the university requested a commercial proposal for its long-term deployment and maintenance.

<div align="center">

| Metric | Value |
|:------:|:-----:|
| REST API endpoints | **~50** |
| Angular components | **60+** |
| Database entities | **26** |
| User roles | **8** |
| Fine-grained permissions | **18** |
| Development timeline | **5 months** |
| Final grade | **10 / 10 · Distinction** |

</div>

---

## 📸 Screenshots

> *Screenshots of the working application. All personal data shown is fictitious (seed data).*

<div align="center">

### 🔐 Authentication
<img src="./screenshots/01-login.png" alt="Login screen" width="720"/>

*Login screen with JWT authentication and password recovery via SMTP.*

---

### 🏠 Dashboard (role-adapted)
<img src="./screenshots/02-dashboard.png" alt="Main dashboard" width="720"/>

*Dashboard adapted to the authenticated user's role, showing pending tasks, low-stock alerts and upcoming reservations.*

---

### 📦 Inventory management
<img src="./screenshots/03-inventory.png" alt="Inventory list" width="720"/>

*Consumables inventory with search, filtering, mass upload (CSV/XLSX) and automatic low-stock alerts.*

---

### 🔬 Equipment & QR identification
<img src="./screenshots/04-equipment-qr.png" alt="Equipment with QR" width="720"/>

*Detailed equipment records with QR-based identification for quick access from mobile devices in the lab.*

---

### 🧪 Biological materials
<img src="./screenshots/05-biologicals.png" alt="Biological materials" width="720"/>

*Specific control for biological materials with lot, expiry and location traceability.*

---

### 📅 Reservations calendar
<img src="./screenshots/06-reservations-calendar.png" alt="Reservations calendar" width="720"/>

*Visual calendar with real-time capacity control and conflict prevention.*

---

### 🛒 Purchase requests
<img src="./screenshots/07-purchases.png" alt="Purchase requests" width="720"/>

*Full purchase-request flow: submission, approval, tracking and reception.*

---

### 👥 User management (admin)
<img src="./screenshots/08-users.png" alt="User administration" width="720"/>

*Role-based user administration with a fine-grained 18-permission matrix.*

---

### 🔔 Alerts & audit log
<img src="./screenshots/09-audit.png" alt="Audit log" width="720"/>

*Full audit trail of every relevant operation performed in the system.*

</div>

> 📁 To add or replace screenshots, drop PNG/JPG files into `./screenshots/` and reference them by filename above. Recommended width: 1440–1920 px at 72 dpi.

---

## ❓ The Problem

Before SIRE, Universidad Europea de Madrid managed its engineering laboratories through a mix of:

- 📊 Multiple **spreadsheets** across different departments, often out of sync.
- 📧 **Email chains** for lab reservations, with no central visibility.
- 📄 **Paper forms** for purchase requests and incident reporting.
- 📞 **Verbal communication** between lab technicians and coordinators.

This created concrete daily problems:

- ❌ **Stock inconsistencies** — materials marked as available were actually missing.
- ❌ **Double-booked labs** — two groups arriving to the same room at the same time.
- ❌ **No traceability** — impossible to know who used what, when, or why.
- ❌ **Manual, error-prone reporting** — end-of-term reports required hours of spreadsheet reconciliation.
- ❌ **No accountability** — incidents (spilled reagents, broken equipment) had no owner.

The Laboratory Coordination team needed a single tool that different profiles (students, teachers, technicians, coordinators, purchasing staff, administration) could use with different levels of access, in real time.

---

## 💡 The Solution

**SIRE** centralizes the full lifecycle of laboratory operations in one integrated web platform:

- 📦 Inventory of consumables, materials and reagents.
- 🔬 Equipment records with QR-based identification.
- 🧪 Biological materials with lot, expiry and location traceability.
- 📅 Room and equipment reservations with real-time capacity control.
- 🛒 Purchase requests with approval and tracking workflows.
- 👥 Technical staff coordination and shift assignment.
- 📤 Mass CSV/XLSX data upload with pre-validation.
- 🔔 Automated low-stock alerts and notifications.
- 📊 Full operational audit trail.

The platform is designed as a **decoupled client-server architecture**, deployable in production with commodity Linux infrastructure, and adaptable to any faculty or lab-based organization with minor domain adjustments.

---

## 🛠 Tech Stack

<div align="center">

### Backend
![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-6.0-092E20?logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-3.17-A30000?logo=django&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-Auth-000000?logo=jsonwebtokens&logoColor=white)

### Frontend
![Angular](https://img.shields.io/badge/Angular-19-DD0031?logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)

### Database
![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?logo=mysql&logoColor=white)

### Infrastructure & DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white)
![Gunicorn](https://img.shields.io/badge/Gunicorn-499848?logo=gunicorn&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Server-E95420?logo=ubuntu&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)

</div>

**Detailed breakdown:**

| Layer | Technologies |
|-------|--------------|
| **Backend** | Python 3, Django 6.0, Django REST Framework 3.17, `djangorestframework-simplejwt`, Gunicorn |
| **Frontend** | Angular 19, TypeScript, RxJS, reactive forms, guards, HTTP interceptors |
| **Database** | MySQL 8 (containerized with Docker), Django ORM |
| **Infrastructure** | Ubuntu Server, Nginx (reverse proxy + static files), Docker Compose |
| **Security** | JWT tokens, dual-layer permission validation, HTTPS with HSTS, secure cookies, XSS protection, anti-clickjacking |
| **Tooling** | Git, VS Code, Postman (API testing), Figma (UI wireframes) |

---

## 🏗 Architecture

SIRE follows a **decoupled three-tier client-server architecture** communicating over HTTP/HTTPS with JSON payloads.

```
                       ┌────────────────────────┐
                       │   User (web browser)   │
                       └────────────┬───────────┘
                                    │ HTTPS
                                    ▼
                       ┌────────────────────────┐
                       │  Nginx (reverse proxy  │
                       │  + static file server) │
                       └────┬───────────────┬───┘
                            │               │
                    /api/*  │               │  /*
                            ▼               ▼
                    ┌──────────────┐  ┌──────────────────┐
                    │   Gunicorn   │  │  Angular 19 SPA  │
                    │    (WSGI)    │  │    (compiled)    │
                    └──────┬───────┘  └──────────────────┘
                           │
                           ▼
              ┌──────────────────────────────┐
              │  Django 6 + DRF              │
              │  • ~50 REST endpoints        │
              │  • JWT authentication        │
              │  • 18-permission role matrix │
              │  • Business validation layer │
              └──────────────┬───────────────┘
                             │ ORM (parameterized SQL)
                             ▼
              ┌──────────────────────────────┐
              │  MySQL 8 (Docker container)  │
              │  • 26 relational entities    │
              │  • Full audit trail          │
              └──────────────────────────────┘
```

**Request flow:**

1. The user accesses SIRE from any modern web browser.
2. Nginx serves the compiled Angular SPA and acts as a reverse proxy for API calls.
3. Angular sends JWT-authenticated REST requests to the backend.
4. Django validates the token, checks the role's permissions against the 18-permission matrix, and executes the business logic.
5. The response returns as JSON to the frontend.
6. Every relevant operation is persisted for traceability and auditing.

---

## ⚡ Key Features

### 📦 Inventory management
- Full CRUD for consumables with categorization.
- **Automated low-stock alerts** with configurable thresholds per item.
- Movement history (who took what, when, how much).
- Mass upload via **CSV / XLSX** with pre-validation and error reporting.

### 🔬 Equipment management
- Detailed equipment records with photos, technical specs and maintenance history.
- **QR-based identification** for instant access from mobile devices in the lab.
- Availability tracking and reservation integration.

### 🧪 Biological materials
- Specific control with **lot, expiry date and physical location** traceability.
- Compliance-oriented workflow for regulated materials.

### 📅 Reservations & capacity control
- Visual weekly and monthly calendars.
- **Real-time conflict detection** — no double bookings.
- Configurable **room capacity** (people, equipment count) with hard limits.
- Approval workflow where needed.

### 🛒 Purchase requests
- Full request lifecycle: submission → approval → tracking → reception.
- Integration with inventory (automatic stock update on reception).
- Cost centre and budget tracking.

### 👥 User & permission management
- **8 distinct user roles**, each with a tailored interface.
- **18 fine-grained permissions** distributed across roles.
- Dual-layer permission validation (frontend guards + backend enforcement).

### 🔔 Notifications & auditing
- Real-time alerts (stock, reservations, approvals) shown in the UI.
- Email notifications via SMTP (password recovery, key events).
- **Complete operational audit log** — every action is traceable to a user, timestamp and payload.

---

## 👥 User Roles & Permissions

The system supports **8 differentiated user profiles**, each with its own interface and permission set. All permission checks are enforced twice: once in the frontend (Angular guards) and once in the backend (Django REST Framework permission classes).

| Role | Description |
|------|-------------|
| 🎓 **Student** | Views their own reservations and requests materials for practical sessions. |
| 👨‍🏫 **Teacher** | Reserves labs and equipment for their classes, requests materials for group activities. |
| 🔧 **Lab Technician** | Manages inventory, prepares labs, handles day-to-day operations. |
| 📋 **Lab Coordinator** | Approves reservations and purchases, oversees lab activity. |
| 🛒 **Purchasing Manager** | Manages the full purchase-request workflow and supplier relationships. |
| 🧑‍🔬 **Researcher** | Uses labs and equipment for research projects, requests biological materials. |
| 🖥 **Administration** | Manages users, generates reports, oversees the platform. |
| ⚙️ **System Administrator** | Full system access, platform configuration, security auditing. |

---

## 🔒 Security

Security is enforced at multiple layers:

- ✅ **JWT authentication** with short-lived access tokens and refresh rotation.
- ✅ **Dual-layer permission validation** — never trust the frontend alone.
- ✅ **SQL injection prevention** via strict ORM parameterization (no raw SQL).
- ✅ **HTTPS-ready** with HSTS, secure cookies and anti-clickjacking headers.
- ✅ **XSS protection** through Angular's automatic sanitization and CSP-ready configuration.
- ✅ **Password recovery** through signed one-time SMTP links (no password sent in plaintext).
- ✅ **Full audit log** of every state-changing operation.
- ✅ **CORS whitelist** restricted to the institutional origin in production.

---

## 🗺 Development Journey

The project was developed over **5 months** following an **iterative, user-centred methodology**:

1. **Requirements gathering** — Interviews with the Lab Coordination team, lab technicians and administration staff at Universidad Europea de Madrid. Identification of pain points and workflow modelling.
2. **Architecture design** — Data model (26 entities), permission matrix, endpoint contracts, UI wireframes in Figma.
3. **Backend development** — Django models, REST API, JWT authentication, permission classes, business validation.
4. **Frontend development** — Angular SPA, role-adapted interfaces, reactive forms, real-time validation.
5. **Integration & testing** — Manual and functional testing across all user roles, edge case validation.
6. **Deployment preparation** — Dockerization, Nginx and Gunicorn configuration, HTTPS setup, environment-based configuration for production.
7. **Handoff & documentation** — Complete technical documentation, user manuals per role, deployment manual.

Throughout the project, regular check-ins with the Lab Coordination team ensured the tool matched real operational needs rather than a purely academic vision.

---

## 👤 My Role

**I designed, developed and prepared this project for production entirely on my own** as my Final Degree Project. Specifically:

- 🎤 **Requirements gathering** with real university stakeholders (coordination, lab technicians, administration).
- 🏗 **Architecture and stack decisions** (three-tier design, JWT strategy, ORM choice, deployment approach).
- 💾 **Data modelling** — designed the 26-entity relational schema from scratch.
- ⚙️ **Backend development** — full Django + DRF implementation, ~50 REST endpoints, authentication, permissions, business logic.
- 🎨 **Frontend development** — Angular 19 SPA with 60+ components, UI/UX design for 8 differentiated user profiles.
- 🔒 **Security implementation** — JWT, permission matrix, HTTPS configuration, input validation.
- 🐳 **DevOps and deployment** — Dockerization, Nginx and Gunicorn configuration, Ubuntu Server preparation.
- 📚 **Documentation** — technical memoir (~190 pages), user manuals per role, and deployment guide.

The only external contribution was academic supervision from **Ing. Jairo García Fernández** (thesis director).

---

## 🏆 Outcome & Recognition

- 🎓 **Graded 10 / 10 with Distinction (Matrícula de Honor)** — the highest academic recognition in the Spanish university system.
- ✅ **Approved by Universidad Europea de Madrid** for institutional deployment.
- 💼 **Commercial handoff in progress** — following the successful defense, the university requested a formal proposal for the deployment and long-term maintenance of the platform.
- 📚 **Full technical memoir** of ~190 pages submitted alongside the platform.
- 🔐 **Intellectual property registered** with the Regional Intellectual Property Registry of Madrid.

---

## 🔒 Why the Code Isn't Public

This system is being prepared for deployment to a real institutional production environment. Publishing the source code publicly would:

- 🚨 Expose authentication logic, JWT handling and permission enforcement for an active system.
- 🚨 Reveal the full REST endpoint structure and data model to potential attackers.
- 🚨 Compromise the security posture of the university's institutional deployment.
- ⚖️ Conflict with the intellectual property and licensing terms being negotiated.

This repository therefore serves as a **project showcase and technical case study**, not a code distribution.

**Interested in a technical demo or code review?** Serious enquiries (recruiters, potential clients, collaborators) can request a **private walkthrough** — reach out via the contact section below.

---

## 📬 Contact

**Sahar Amanmohammadi**
*Full-Stack Developer · Cybersecurity Analyst*

- 📧 [saharamanmohamadi@gmail.com](mailto:saharamanmohamadi@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/sahar-amanmohammadi)
- 🌍 Madrid, Spain

---

<div align="center">

*Built with ❤️ and a lot of coffee ☕ during 5 months of TFG development.*

**© 2026 Sahar Amanmohammadi — All rights reserved.**

</div>
