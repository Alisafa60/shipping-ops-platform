# Shipping Ops Platform

A self-hosted shipping company operations platform for shipment tracking, stock workflows, invoicing, payments, role-based access control, and configurable Excel imports.

Built for shipping teams that still rely heavily on spreadsheets but need a centralized system for daily operations: shipments, inventory, invoices, payments, employee tasks, client visibility, and internal governance.

---

## Demo

<p align="center">
  <img src="./assets/preview.gif" width="100%" />
</p>

<p align="center">
  <a href="./assets/demo.mp4">Watch Full 2-Minute Demo</a>
</p>

---

## Highlights

- Shipment lifecycle tracking
- Loaded, transit, and in-stock inventory workflows
- Configurable Excel import pipeline with validation and embedded image extraction
- Client and supplier invoice management
- Multi-currency financial calculations
- Payments and refunds
- Role-aware dashboards
- Persistent access-control matrix
- Audit logging and activity tracking
- Client portal support

---

## Screenshots

### Stock, Transit & Import Workflow

Shipment items are tracked across original, loaded, transit, and in-stock operational states, with Excel imports, validation history, and stock movement workflows.

![Stock Workflow](./assets/stock-workflow.png)

---

### Invoice Management

Client and supplier invoice workflows with multi-currency totals, payment states, refunds, balances, and linked shipment data.

![Invoices](./assets/invoices.png)

---

### Activity Log

Audit trail for operational and administrative actions across shipments, invoices, users, access control, and authentication events.

![Activity Log](./assets/activity-log.png)

---

### Admin Dashboard

Operational overview with shipment metrics, financial summaries, task visibility, charts, and recent activity.

![Dashboard](./assets/dashboard1.png)

---

### Dashboard Analytics

Role-aware dashboard widgets for monitoring shipment states, invoice status, revenue, and operational activity.

![Dashboard Analytics](./assets/dashboard2.png)

---

### Shipment Management

Shipment list with lifecycle statuses, invoice linkage, filtering, and operational actions.

![Shipments](./assets/shipments.png)

---

### Client Portal

Client-facing dashboard for shipment visibility, invoice tracking, outstanding balances, and recent activity.

![Client Dashboard](./assets/client-dashboard.png)

---

### Access Control

Database-backed permission matrix that allows the super admin to configure what admins and employees can access.

![Access Control](./assets/access-control.png)

---

## Product Scope

The platform combines shipping operations, stock handling, invoicing, payments, refunds, tasks, audit logs, exchange rates, user management, and access control into a single internal system.

It is designed for companies that still depend on spreadsheets, manual coordination, and fragmented operational tooling, but need a centralized platform for day-to-day logistics and financial workflows.

---

## Operational Workflows

The platform is designed around operational shipping-company workflows, where imported inventory, loaded quantities, transit valuation, stock carry-forward, invoicing, and access governance are treated as connected operational states.

Examples include:

- Original shipment items remain separate from loaded inventory
- Transit valuation is tracked independently from original shipment data
- Stock can be derived from leftover shipment quantities or entered manually
- Stock can be allocated into existing shipments or moved directly into loaded items
- Shipment items can be imported from Excel files or created manually through operational workflows
- Embedded product/item images can be extracted from imported Excel files and linked to shipment items
- Excel imports are previewed, validated, and reviewed before being applied
- Invoice totals are calculated from payments, refunds, exchange rates, discounts, and commissions
- User capabilities are controlled through a configurable permission matrix

---

## Roles & Access Control

The system supports four operational roles:

- `SUPER_ADMIN`
- `ADMIN`
- `EMPLOYEE`
- `CLIENT`

The super admin can configure role capabilities through a persistent database-backed permission matrix. This allows different companies to adapt operational permissions to their own workflows, whether for shipment handling, stock operations, imports, invoicing, or administrative management.

Client access is intentionally constrained and focused on shipment and invoice visibility.

---

## Tech Stack

### Backend

- Kotlin
- Ktor
- PostgreSQL
- Exposed ORM
- Flyway migrations
- Apache POI for Excel parsing
- Koin dependency injection
- JWT authentication with refresh token rotation

### Frontend

- React 19
- TypeScript
- Vite
- Chakra UI
- TanStack Query
- React Router
- i18next
- dnd-kit
- Recharts
- Axios

---

## Architecture Notes

The backend is built with Ktor, a lightweight and non-opinionated framework in the JVM ecosystem that gives explicit control over routing, middleware, authentication, serialization, and application structure.

The project favors explicit configuration and composable infrastructure over heavy framework abstraction, shaping much of the authentication, session, import, and operational workflow architecture.

The backend is organized around controllers, services, repositories, models, and configuration modules.

The frontend is organized around route pages, domain components, API services, query hooks, shared layout, theming, and localization utilities.

The project is built as a production-oriented internal operations system focused on real-world logistics and financial workflows.

---

## About This Repository

This repository is a showcase repository for a private shipping operations application.

The application is available for licensing, customization, or private deployment.

For inquiries, contact: `alisafa6100 [at] gmail [dot] com`
