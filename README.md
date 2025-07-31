# 🌐 SupplySphere  
**Blockchain-Powered Supply Chain Traceability with AI Assistance**  
*"Because what you eat & take should always be trusted."*

---

## 📌 Executive Summary  
SupplySphere is a **decentralized, AI-enhanced supply chain traceability platform** designed to restore **trust and transparency** in global trade.  
From **farm to shelf** and **lab to pharmacy**, every step of a product’s journey is **securely logged** on the blockchain and instantly accessible via **QR code scanning**.

We combine:
- **Blockchain** → Tamper-proof product history
- **AI** → Predictive analytics & intelligent queries
- **Modern Web** → Accessible, intuitive dashboards

---

## 🚨 Problem Statement  
Every year:  
- **10% of food** sold globally is **mislabeled**  
- **Millions die** from counterfeit medicine  
- Supply chain fraud & inefficiencies cost **billions**  

The **core issue**: A **broken trust chain** between producers, distributors, and consumers.  
Current systems are **centralized, siloed, and easily manipulated**.

---

## 💡 Solution Overview  
SupplySphere delivers:
- **End-to-end traceability** using **blockchain**  
- **AI-powered insights** into supplier reliability & delivery efficiency  
- **Role-specific dashboards** for Suppliers, Vendors, Analysts, and Admins  
- **QR-coded product verification** for instant consumer trust

---

## 🚀 Features

### 🔑 Role-Based Dashboards (RBAC)
- **Supplier** → Upload inventory, update delivery status  
- **Vendor/Retailer** → Search products, request orders, verify deliveries  
- **Analyst** → View supplier reliability & demand trends  
- **Admin** → Manage users, logs, analytics

### 📦 Smart Inventory System
- Add/update products with metadata  
- Stock level alerts (🟡 Low, 🔴 Out)  
- QR code generation  
- AI demand prediction

### 🚚 End-to-End Shipment Tracking
- Status: **Pending → In Transit → Delivered**  
- Blockchain logs for tamper-proof records  
- ETA predictions via AI

### 🔗 Blockchain-Powered Verification
- Immutable product history  
- Timestamped certification proof  
- Public verifiable logs

### 🤖 AI Assistant
- Query supply chain data in plain English  
- Examples: *“What’s my pending order value?”*  
- Powered by OpenAI / Llama

### 📊 Analytics & Reporting
- KPI dashboards (delivery time, stockouts, costs)  
- CSV/PDF export  
- Filter by supplier, region, product

### 🔒 Authentication & Security
- JWT-based authentication  
- Multi-role RBAC  
- Optional 2FA  
- API rate limiting

---

## 🛠 Tech Stack

| Layer | Technology | Reason |
|-------|------------|--------|
| **Frontend** | Next.js, TailwindCSS, ShadCN | Modern, responsive UI |
| **Backend** | Flask (Python) | Lightweight API |
| **Blockchain** | ICP + dfx.json | Tamper-proof records |
| **Database** | PostgreSQL / MongoDB | Scalable, flexible storage |
| **AI Layer** | OpenAI / Llama | Natural language queries |
| **Charts** | Recharts / D3.js | Data visualization |
| **Auth** | JWT + RBAC | Secure multi-role access |

---

## 🏗 System Architecture

```mermaid
graph TD
  A[Frontend - Next.js] -->|REST API| B[Backend - Flask]
  B --> C[(PostgreSQL / MongoDB)]
  B --> D[Blockchain - ICP]
  B --> E[AI Layer - OpenAI/Llama]
  A --> F[QR Scanner - Consumer App]


---

🗄 Database Schema

ER Diagram

erDiagram
    USERS {
        int id
        string name
        string email
        string password_hash
        string role
    }
    PRODUCTS {
        int id
        string name
        string description
        string batch_id
        date production_date
        date expiry_date
    }
    SHIPMENTS {
        int id
        int product_id
        string status
        datetime estimated_arrival
        datetime actual_arrival
    }
    INVENTORY_LOGS {
        int id
        int product_id
        int quantity
        datetime timestamp
    }
    BLOCKCHAIN_LOGS {
        int id
        string transaction_hash
        int product_id
        datetime timestamp
    }
    AI_QUERY_LOGS {
        int id
        int user_id
        string query
        string response
        datetime timestamp
    }

    USERS ||--o{ PRODUCTS : owns
    PRODUCTS ||--o{ SHIPMENTS : shipped_in
    PRODUCTS ||--o{ INVENTORY_LOGS : tracked_in
    PRODUCTS ||--o{ BLOCKCHAIN_LOGS : verified_in


---

🔌 API Design

Method	Endpoint	Description

POST	/auth/login	User login
POST	/auth/register	Create new user
GET	/products	List products
POST	/products	Add product
GET	/shipments	List shipments
POST	/shipments	Create shipment
GET	/analytics	Get analytics
GET	/blockchain/:id	Verify product



---

👥 User Journey

Supplier

1. Log in


2. Add product batch


3. Generate QR code


4. Update shipment status



Vendor

1. Search products


2. Request order


3. Verify delivery



Analyst

1. View KPI dashboard


2. Filter results


3. Export reports



Admin

1. Manage users


2. Audit logs


3. Oversee analytics




---

📅 MVP Roadmap

[x] Role-based authentication

[x] Product & batch creation

[x] QR code generation

[x] Blockchain transaction logging

[ ] AI assistant integration

[ ] Full analytics panel

[ ] Mobile optimization



---

🎯 Hackathon Fit

SupplySphere is:

Web3-native → Blockchain for product trust

AI-driven → Human-friendly querying & predictive analytics

Globally impactful → Addresses food & medicine fraud at scale

Scalable → Designed for both enterprise & local supply chains



---

📜 License

MIT License


---

🌍 Region

ICP HUB Kenya

