# 📖 Story: Salon POS Commission Tracking

---

## 🏷️ Title
Tracking Employee Commissions and Live Inventory Consumption Simultaneously inside a Salon POS

---

## 📝 Background
While building a POS system for beauty salons, we needed to model checkouts. Salon visits usually combine service bookings (e.g., haircuts) and product purchases (e.g., shampoos), with service employees earning varying commissions.

---

## ❓ Problem
Calculations of employee commissions change based on the service category, while service delivery consumes salon back-bar inventory. Storing raw data in a decoupled way without strict relational checks can lead to commission mismatches and incorrect inventory logs.

---

## ⚖️ Decision
We chose to design a schema using strict foreign key relationships, intermediate pivot tables (linking sales, services, and employees), and wrapping updates in database transactions.

---

## 🛠️ Implementation
* Structured intermediate tables (`sale_service_employee`) to track exactly who performed which service for every invoice.
* Used database transaction blocks to ensure that when a checkout completes, inventory drops and commission calculations persist simultaneously or fail together.

---

## 📈 Result
* **Precise Commission Reports**: Prevented payment calculation conflicts.
* **Live Inventory Sync**: Back-bar inventory levels update instantly upon service completion.

---

## 🎓 Lessons

### General Lesson
* Always map complex business logic dependencies directly into database constraints to prevent data desynchronization.

### Technical Lesson
* Eager load critical pivot relationships in Eloquent to prevent N+1 queries when loading transaction logs.

### Business Lesson
* Transparency in employee payouts is critical; systems must keep clear audits for all commission calculations.

---

## 🎨 Social Media Distribution Playbook

### 🔗 Potential LinkedIn Angles
* How to model database schemas that link transactions, inventory, and employee commissions.

### 🎥 Potential Video Angles
* Whiteboarding the database relationship diagram for service POS software.

### 📨 Potential Newsletter Angles
* A detailed look at intermediate tables and compound relationships in Laravel Eloquent.
