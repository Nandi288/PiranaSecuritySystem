# Pirana Guarding — Enterprise Security & Shift Tracking System 🛡️

An end-to-end security workforce management and operations web portal engineered to manage daily shift rotations, eliminate attendance fraud, and provide executive oversight across client sites.

---

## 📌 Problem & Impact

Physical security operations are prone to timesheet fraud, static credential sharing, and unauthorized site presence. **Pirana Guarding** modernizes guard deployment through dynamic check-in verification, real-time business rule validation, and centralized operational monitoring.

* **Rotation Scale:** Manages shift rotations for up to **12 active guards per site**.
* **Zero-Trust Attendance:** Engineered a dynamically generated, **daily-expiring QR code check-in engine** that eliminated **100% of static credential and code-reuse attendance tampering**.
* **Automated Guardrails:** Programmed real-time business rule evaluation to **block off-duty personnel** from unauthorized portal and site check-ins.
* **Executive Oversight:** Centralized command via a **Director Dashboard** tracking live attendance, shift timestamps, and site incident metrics.

---

## ✨ Key Engineering Features

* **Anti-Fraud QR Check-In Engine:** Implemented dynamically refreshing QR tokens with daily expiration logic to verify physical guard presence and prevent proxy attendance.
* **Automated Shift & Rota Validation:** Server-side evaluation of guard rosters to restrict system access strictly to assigned, active shift windows.
* **Director Command Dashboard:** Centralized view summarizing active site headcounts, real-time check-in timestamps, shift completion rates, and open incident logs.
* **Incident Management:** Standardized reporting pipeline allowing field guards to document on-site irregularities, site hazards, and security breaches.
* **Role-Based Access Control (RBAC):** Strict operational segregation between Site Directors/Supervisors (roster management, approvals, analytics) and On-Site Guards (authentication, clock-in, incident submission).

---

## 🛠️ Architecture & Tech Stack

* **Backend:** C# · ASP.NET MVC / ASP.NET Core
* **Data Access & ORM:** Entity Framework / ADO.NET
* **Database:** Microsoft SQL Server (Relational architecture with normalized shift, site, and audit logs)
* **Frontend & UI:** Razor Views, HTML5, CSS3, JavaScript
* **Security & Auth:** ASP.NET Identity (Hashed credentials, session lifecycle management, and role-based authorization)

---

## 🗄️ Relational Schema Highlights

The SQL Server database enforces strict relational constraints and audit trails across key business entities:

* `Guards`: Stores guard credentials, deployment statuses, contact details, and site assignments.
* `Sites`: Facility locations, client profiles, and active post capacities (up to 12 guards/site).
* `ShiftRotations`: Daily rosters defining start/end windows, meal breaks, and duty schedules.
* `AttendanceTokens`: Dynamic, expiring QR verification records mapped to specific dates and locations.
* `AttendanceLogs`: Tamper-evident clock-in/out records with accurate timestamps and compliance flags.
* `Incidents`: Structured event reports categorized by severity and linked to active shifts.

---

## 🚀 Getting Started

### Prerequisites
* [.NET SDK](https://dotnet.microsoft.com/download)
* [Visual Studio 2022](https://visualstudio.microsoft.com/) (ASP.NET and web development workload)
* [Microsoft SQL Server](https://www.microsoft.com/sql-server/) & SQL Server Management Studio (SSMS)

### Local Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Nandi288/pirana-guarding.git](https://github.com/Nandi288/pirana-guarding.git)
   cd pirana-guarding
