# Expense Reporting System Showcase

Enterprise expense management and financial governance platform designed to integrate employees, managers, finance teams, projects, tasks, approvals, auditing, and strategic reporting into a single operational ecosystem.

This repository showcases the architecture, workflows, interfaces, REST APIs, mobile application, reporting engine, and business structure of a complete enterprise reimbursement management system.

---

# Project Origin

This system originated as part of the **Residência em TIC** initiative promoted by **Brisa** in partnership with **ULBRA**.

The project was developed as an enterprise software solution proposal focused on improving organizational expense management, approval workflows, financial traceability, and operational governance.

## Development Team

The software development responsibilities were primarily handled by:

- Felipe Macedo
- Hector Peres

Main development responsibilities included:

- Backend architecture
- REST APIs
- Business rules
- Database structure
- Authentication
- Approval workflows
- Mobile application
- Reporting engine
- Financial governance logic
- Frontend integrations

Other project participants contributed mainly to:

- Visual presentation
- Documentation support
- Project explanation
- Presentation structure

---

# System Demonstration

A complete demonstration video showcasing all operational flows of the platform is available below.

The demonstration includes:

- Employee expense submission
- Expense item registration
- Approval workflows
- Financial validation
- Partial approvals and adjustments
- PDF and CSV reporting
- Administrative management
- Mobile application flows
- Embedded manuals
- End-to-end reimbursement lifecycle

## Full Demonstration Video

The video below demonstrates the complete operational flow of the platform, including employee expense submission, manager approvals, financial validation, reporting, and mobile workflows.

[![Watch the full demonstration](/assets/video/image/sgs.png)](https://drive.google.com/file/d/1VeybErGhXSpcmeAaQZuUTQl5by_Uq6rJ/view?usp=sharing)

---

# Overview

The platform was designed to go beyond traditional reimbursement systems.

Instead of functioning as a simple expense registration application, the system integrates:

- Employees
- Managers
- Finance teams
- Projects
- Tasks
- Expense items
- Multi-level approvals
- Financial validations
- Audit logs
- Strategic reporting
- Operational manuals
- Mobile workflows

The result is a complete enterprise governance environment focused on operational visibility, financial control, and approval intelligence.

---

# Core Concept

The platform centralizes the entire reimbursement lifecycle inside a structured enterprise workflow.

```text
Employee
   ↓
Expense Registration
   ↓
Manager Approval
   ↓
Financial Validation
   ↓
Payment Processing
   ↓
Strategic Reporting
   ↓
Audit & Governance
```

---

# Main Features

# Employee Workflow

Employees can:

- Create expense reports
- Register expenses linked to projects and tasks
- Attach receipts and invoices
- Scan QR Codes
- Edit reports before submission
- Respond to requested corrections
- Monitor approval status
- View historical submissions
- Access operational manuals

---

# Manager Workflow

Managers can:

- Approve or reject reports
- Perform partial approvals
- Apply item-level adjustments (glosas)
- Request corrections
- Analyze employee submissions
- Monitor project expenses
- Validate reimbursement consistency
- Track approval history

---

# Finance Workflow

Finance teams can:

- Validate approved reports
- Process reimbursements
- Generate PDF reports
- Export CSV spreadsheets
- Track payment status
- Monitor financial summaries
- Analyze approval history
- Access audit logs

---

# Administrative Workflow

Administrators can:

- Manage users
- Configure permissions
- Register projects
- Manage tasks
- Configure expense types
- Configure task types
- Manage notifications
- Access governance information

---

# System Differentiators

Unlike traditional reimbursement platforms, this system:

- Integrates projects, tasks, and expenses
- Supports granular approval by item
- Provides partial approvals and corrections
- Maintains full audit traceability
- Generates strategic financial reports
- Separates organizational responsibilities clearly
- Supports enterprise governance
- Includes embedded operational manuals
- Offers mobile and web integration
- Centralizes operational and financial visibility

---

# Enterprise Features

- Multi-role architecture
- Financial governance
- Approval workflows
- Audit logging
- Strategic reporting
- JWT authentication
- REST API architecture
- Mobile integration
- Embedded operational manuals
- PDF export
- CSV export
- Project-task integration
- Item-level approval system

---

# Technology Stack

# Backend

- Java
- Spring Boot
- Spring Security
- JPA / Hibernate
- JWT Authentication

---

# Frontend Web

- Vue.js
- Vue Router
- Axios
- Vite

---

# Mobile Application

- Flutter
- Dart

---

# Database

- PostgreSQL

---

# Infrastructure

- Docker
- PM2
- Cloud Deployment

---

# APIs

- REST APIs

---

# Repository Structure

```text
expense-reporting-system-showcase/
│
├── backend/
│
├── frontend/
│
├── mobile/
│
├── screenshots/
│
├── docs/
│   ├── architecture/
│   ├── workflows/
│   ├── manuals/
│   └── api/
│
└── README.md
```

---

# Backend Structure

```text
backend/
├── config/
├── controller/
├── dto/
├── exception/
├── model/
├── repository/
├── security/
├── service/
└── templates/
```

---

# Frontend Structure

```text
frontend/
├── pages/
│   ├── administrador/
│   ├── funcionario/
│   ├── gerente/
│   ├── financeiro/
│   └── manual/
│
├── components/
├── layouts/
├── router/
├── plugins/
├── styles/
└── utils/
```

---

# Mobile Structure

```text
mobile/
├── lib/
│   ├── screens/
│   ├── shared/
│   ├── core/
│   ├── data/
│   └── services/
│
├── assets/
└── android/
```

---

# REST API Architecture

The platform uses a REST-based architecture integrating:

```text
Frontend Web
        ↓
REST API
        ↓
Spring Boot Backend
        ↓
PostgreSQL Database
        ↓
Mobile Application
```

---

# Main API Endpoints

# Authentication

```http
POST /api/login
```

---

# Users

```http
GET    /api/usuarios
POST   /api/usuarios
PUT    /api/usuarios/{id}
DELETE /api/usuarios/{id}
```

---

# Projects

```http
GET    /api/projetos
POST   /api/projetos
PUT    /api/projetos/{id}
DELETE /api/projetos/{id}
```

---

# Tasks

```http
GET    /api/tarefas
POST   /api/tarefas
PUT    /api/tarefas/{id}
DELETE /api/tarefas/{id}
```

---

# Expense Reports

```http
GET    /api/prestacoes-contas
GET    /api/prestacoes-contas/minhas
GET    /api/prestacoes-contas/{id}

POST   /api/prestacoes-contas
POST   /api/prestacoes-contas/{id}/submeter

PUT    /api/prestacoes-contas/{id}

DELETE /api/prestacoes-contas/{id}
```

---

# Expenses

```http
GET    /api/despesas/{id}
POST   /api/despesas
PUT    /api/despesas/{id}
DELETE /api/despesas/{id}
```

---

# Reports

```http
GET /api/relatorios/prestacoes
GET /api/relatorios/prestacoes/pdf
```

---

# Security

The system implements:

- JWT Authentication
- Spring Security
- Role-based access control
- Authorization filters
- Protected routes
- Audit logging

---

# User Roles

| Role | Responsibilities |
|---|---|
| Employee | Register and submit expenses |
| Manager | Approve, reject, and adjust expenses |
| Finance | Validate reimbursements and reports |
| Admin | Manage users and permissions |

---

# Reporting Engine

The reporting system supports:

## Filters

- Date range
- Project
- Task
- Employee
- Approval status

## Export Options

- PDF reports
- CSV spreadsheets

## Financial Metrics

- Registered amount
- Approved amount
- Glosado amount
- Payment history

---

# Audit & Governance

The platform maintains complete traceability through:

- Audit logs
- Approval history
- Financial records
- User activity monitoring
- Expense tracking
- Approval decisions
- Manager observations

---

# Embedded Manuals

The platform includes integrated manuals designed to support onboarding, operational standardization, and internal training.

## Available Manuals

| Manual | Purpose |
|---|---|
| ManualAdmin.vue | Administrative operations |
| ManualFinanceiro.vue | Finance workflow |
| ManualFuncionario.vue | Employee workflow |
| ManualGerente.vue | Manager approvals |
| ManualMobile.vue | Mobile application |
| CentralAjuda.vue | Help center |

---

# Current Status

## Backend

- Operational
- JWT authentication implemented
- Approval workflow implemented
- Reporting system implemented
- Audit logging implemented

---

## Frontend

- Administrative module implemented
- Employee workflow implemented
- Manager workflow implemented
- Finance workflow implemented
- Embedded manuals implemented

---

## Mobile

- Authentication implemented
- Expense reporting implemented
- Report management implemented
- Financial workflow implemented

---

# Future Improvements

- ERP integrations
- OCR for receipts and invoices
- Push notifications
- Advanced BI dashboards
- Multi-company environments
- Real-time workflow tracking
- AI-assisted expense validation

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Java | Backend |
| Spring Boot | REST API |
| PostgreSQL | Database |
| Vue.js | Web Frontend |
| Flutter | Mobile App |
| Docker | Infrastructure |
| JWT | Authentication |
| JPA/Hibernate | ORM |
| Vite | Frontend Build Tool |

---

# Author

Felipe Macedo and Hector Peres

Developer focused on enterprise systems, APIs, integrations, financial governance, workflow automation, and strategic software architecture.

---

# Strategic Vision

This platform was designed not merely as a reimbursement application, but as a complete enterprise financial governance solution capable of integrating operational workflows, approval intelligence, auditing, strategic reporting, and organizational financial visibility into a unified ecosystem.
