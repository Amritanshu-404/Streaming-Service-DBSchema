# 🎬 Streaming Service DB  
This project presents a fully structured and normalized **relational database management system (RDBMS)** designed for a subscription-based online streaming platform.  
It models  relational database systems, real OTT platforms like Netflix, Amazon Prime Video, Hotstar & Hulu. platform functionality such as:

- User accounts  
- Subscription plans  
- Payments  
- Content metadata  
- Device tracking  
- Watch history  
- Region-based content licensing  

The database is implemented using **Microsoft SQL Server (MSSQL)** with real-world relational modeling and optimized SQL operations.

---

## 📸 Architecture Diagrams  
> **Replace the URL placeholders with actual image URLs after uploading your diagrams.**

### **ER Diagram**
![ER Diagram](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/blob/main/ER.png)  
*Figure 1 — Entity Relationship Diagram (replace with your actual image link).*

### **Relational Schema**
![Relational Schema](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/blob/main/Schema.png)  
*Figure 2 — Relational Schema showing tables, PKs and FKs (replace with your actual image link).*

---

## 🚀 Key Features  

### 🔐 **User Management**
- Stores user information and account details  
- Tracks registration timestamps & account status  

### 💳 **Subscription Handling**
- Multiple subscription plans (Basic, Standard, Premium, etc.)  
- Start/end dates, renewal status, and subscription lifecycle tracking  

### 🎥 **Content Catalog**
- Stores detailed metadata for movies & series  
- Title, genre, duration, release date, rating, age rating & description  

### 📱 **Device Registration**
- Tracks all devices registered by a user  
- Supports multi-device streaming rules  

### 🕒 **Watch History Tracking**
- Logs content watched by users  
- Tracks progress & completion for recommendations  

### 💰 **Payment System**
- Records user payment details  
- Amount, payment method, timestamp & payment status  

### 🌍 **Content Licensing**
- Region-based access control for content  
- License start & end dates stored for legal compliance  

---

## 📦 Project Contents  
This project includes:

- ✔ ER Diagram & Relational Schema (URL placeholders included)  
- ✔ Entity descriptions & full attribute lists  
- ✔ Normalized schema (1NF → 2NF → 3NF)  
- ✔ SQL DDL scripts (CREATE TABLE statements)  
- ✔ SQL DML scripts (INSERT sample data)  
- ✔ User-defined functions (parameterized & non-parameterized)  
- ✔ Stored procedures with TRY–CATCH blocks  
- ✔ Cursor implementation  
- ✔ Analytical SQL queries (reports, statistics, revenue, trends)  

---

## 🧩 Entities & Relationships  

### **Core Entities**
- Users  
- Subscription Plans  
- Subscriptions  
- Contents  
- Watch History  
- Payments  
- Devices  
- Content Licensing  

### **Relationship Summary**
- One user → many subscriptions  
- One user → many watch history records  
- One content item → many watch history entries  
- One subscription → many devices  
- One subscription plan → many users  
- One content item → many content licenses  
- One user → many payment records  

These relationships ensure referential integrity and efficient data retrieval.

---

## 🔧 Technologies Used  
| Technology | Purpose |
|-----------|---------|
| **MSSQL (Microsoft SQL Server)** | Database engine |
| **T-SQL (DDL & DML)** | Table creation, inserts, updates, relational queries |
| **Stored Procedures** | Encapsulated server-side logic |
| **Functions** | Reusable data-retrieval utilities |
| **Cursors** | Iterative SQL processing |
| **Normalization (1NF–3NF)** | Reduces redundancy, improves consistency |
| **ER Modeling** | Database structure design |

---

## 📊 SQL Components Implemented  

### ✔ **Table Creation**
Complete scripts for all main modules:
- Users  
- Subscription Plans  
- Subscriptions  
- Contents  
- Watch History  
- Devices  
- Payments  
- Content Licensing  

### ✔ **Sample Data Insertion**
Includes realistic sample records for:
- Users  
- Plans  
- Payments  
- Content metadata  
- Watch history  
- Licensing  
- Devices  

### ✔ **Functions**
- Retrieve first names of all users  
- Retrieve subscription plans within a cost range  

### ✔ **Stored Procedures**
- Retrieve user details  
- Filter content by language  
- TRY–CATCH error-handled SP for joining user/watch history  

### ✔ **Cursor**
- Iterates over subscription plans and prints details  

### ✔ **Analytical Queries**
- Active users by plan  
- Total revenue generation  
- Watch history insights  
- Subscription renewal tracking  
- Recently watched content (last 3 years)  

---

## 🎯 Purpose  
This system serves as a **realistic simulation** of how major streaming platforms manage:

- Millions of users  
- Thousands of content items  
- Subscription billing  
- Playback analytics  
- Regional licensing  
- Performance-optimized data handling  

It bridges academic database principles with actual industry implementations.

---

## 🧾 Conclusion  
The project successfully demonstrates the creation of a **scalable**, **normalized**, and **functional** database for a modern streaming platform.  
It integrates user management, plans, payments, device tracking, licensing and analytics into a cohesive RDBMS—all implemented in MSSQL using best practices.

This can be extended into API integration, backend systems, or advanced analytics engines.

---

## 👥 Authors  
- **Siddharth Kumar**  
- **Ritesh Singh Kushwaha**  
- **Amritanshu Kumar**

---

## 📌 Notes  
- Replace the ER & Schema image URLs with your actual hosted images.  
- Recommended hosting options: GitHub `/assets/`, GitHub raw links, or any public image CDN.

---

