# 🏠 BarirFee — Case Study

> **Modern Multi-Tenant Building & Flat Management ERP Platform**

BarirFee is an ERP platform designed to manage multiple residential buildings, flats, residents, billing cycles, payments, receipts, notices, complaints/tickets, notifications, and platform administration from a single system.

This repository is a **case-study/documentation repository only**. It does not contain the running BarirFee application source code.

---

## 🎯 Product Overview

BarirFee addresses the operational needs of multi-unit residential buildings by bringing building administration and resident-facing services into one platform.

The system is designed around a **multi-tenant architecture**, where buildings can operate as isolated accounts with their own flats, residents, ledgers, billing information, and administrative workflows.

---

## ✨ Current Feature Areas

### 🏢 Multi-Tenant Building Management
- Separate building accounts
- Building and flat registry
- Floor and flat management
- Resident ledgers
- Building-specific data isolation

### 💳 Billing & Service Charges
- Monthly service-charge cycles
- Periodic maintenance charges
- Automated bill generation
- Multiple billing/split methods
  - Equal distribution
  - By square feet
  - By ownership share

### 💰 Payments & Receipts
Supported payment workflows include:
- bKash
- Nagad
- Rocket
- Bank Transfer
- Cash

The application also supports automated payment receipt generation and PDF export.

### 👥 Role-Based Portals

#### Super Admin
- Platform-level statistics
- Building management
- Subscription controls
- Audit logs
- Platform configuration

#### Building Admin
- Flat registry
- Billing-cycle generation
- Payment approval
- Notice-board management
- Ticket/complaint handling

#### Owners & Tenants
- View/pay bills
- Payment history
- Download PDF receipts
- Submit complaint/ticket requests

### 🔔 Notifications
- Real-time notification workflows
- Firestore-based notification support
- WhatsApp OTP integration

### 🎨 Platform Branding
The application includes configurable platform branding capabilities such as:
- Platform name
- Logo
- Primary color
- Contact information
- Footer/watermark text

### 🛠️ System Administration
- Maintenance mode
- User profile management
- Session management
- Role-aware application access
- Audit-oriented administration

---

## 🧩 User & Access Model

The application currently defines these main roles:

| Role | Primary responsibility |
|---|---|
| Super Admin | Platform-wide administration |
| Building Admin | Individual building operations |
| Owner | Flat ownership and resident services |
| Tenant | Resident services and billing |

---

## 🏗️ Technical Architecture

BarirFee uses a full-stack TypeScript architecture.

### Frontend
- React 19
- TypeScript 5.8+
- Vite 6
- Material UI
- Tailwind CSS
- React Router
- TanStack React Query
- React Hook Form
- Zod
- Lucide / React Icons
- Recharts

### Backend
- Node.js
- Express
- TypeScript
- JWT authentication
- bcrypt
- Helmet
- Express Rate Limit
- esbuild

### Data & Cloud Services
- Neon PostgreSQL
- Firebase / Firestore
- Local/offline JSON fallback
- Cloud/serverless deployment support

### Mobile
- Capacitor
- Android

### Deployment
The project is structured to support:
- Vercel/serverless deployment
- VPS deployment
- Docker
- PM2
- Nginx

---

## 🔄 Application Flow

```text
                    ┌─────────────────────┐
                    │     Super Admin     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      BarirFee       │
                    │   Multi-Tenant ERP  │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
       ┌────────────┐   ┌────────────┐   ┌────────────┐
       │ Building A │   │ Building B │   │ Building N │
       └─────┬──────┘   └─────┬──────┘   └─────┬──────┘
             │                │                │
       ┌─────┴─────┐    ┌─────┴─────┐    ┌─────┴─────┐
       │ Admin     │    │ Admin     │    │ Admin     │
       │ Owners    │    │ Owners    │    │ Owners    │
       │ Tenants   │    │ Tenants   │    │ Tenants   │
       └───────────┘    └───────────┘    └───────────┘
```

---

## 🔐 Security & Isolation

The application is designed with:
- Role-based access
- JWT-based sessions
- Password hashing
- Security headers through Helmet
- Rate limiting
- Building-level data isolation
- Separate resident/admin experiences

Sensitive production credentials and environment variables are **not part of this case-study repository**.

---

## 📱 Web + Android

The same application codebase supports a web application and Android packaging through Capacitor.

This allows BarirFee to provide a consistent product experience across:
- Desktop browsers
- Mobile browsers
- Android application

---

## 📄 Payment & Receipt Workflow

A typical payment workflow can be represented as:

```text
Resident
   │
   ▼
View Bill
   │
   ▼
Select Payment Method
   │
   ├── bKash
   ├── Nagad
   ├── Rocket
   ├── Bank Transfer
   └── Cash
   │
   ▼
Payment Processing / Approval
   │
   ▼
Payment Record
   │
   ▼
Receipt Generation
   │
   ▼
PDF Receipt
```

---

## 🧠 Engineering Highlights

The BarirFee implementation demonstrates several practical engineering patterns:

- Multi-tenant application design
- Role-based UI routing
- Full-stack TypeScript
- React + Express integration
- PostgreSQL cloud persistence
- Serverless-compatible backend structure
- Offline/local data fallback
- Payment workflow handling
- PDF receipt generation
- Firebase notification integration
- Responsive web application
- Capacitor Android packaging
- Production build separation between client and server

---

## 📦 Repository Safety

This repository is intentionally maintained separately from the production application.

**Important:**
- No BarirFee production source code is copied here.
- No production environment variables are stored here.
- No database credentials are stored here.
- No running deployment is modified by this repository.
- Changes to this repository do not change the running BarirFee application.

The actual application remains in the private BarirFee repository.

---

## 📌 Technology Snapshot

| Layer | Technology |
|---|---|
| UI | React + TypeScript |
| Build | Vite |
| Styling | Material UI + Tailwind CSS |
| Backend | Node.js + Express |
| Database | Neon PostgreSQL |
| Notifications | Firebase / Firestore |
| Authentication | JWT + bcrypt |
| Validation | Zod |
| PDF | jsPDF |
| Mobile | Capacitor Android |
| Deployment | Vercel / VPS / Docker |
| Security | Helmet + Rate Limiting |

---

## 🚀 Product Direction

Potential future expansion areas can include deeper accounting, advanced property-management automation, analytics, integrations, and additional resident services.

These are **future possibilities**, not claims about currently implemented features.

---

## 👨‍💻 Project

**BarirFee**  
Modern Building & Flat Management ERP

**Case Study Repository:** `iaaasif/BarirFee-case-study`

**Source Application:** Private production repository

---

> **Case-study documentation is based on the current BarirFee repository structure and implementation documentation.**
