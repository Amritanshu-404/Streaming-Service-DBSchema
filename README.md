# 🎬 Streaming Service Database Management System

<div align="center">

![SQL Server](https://img.shields.io/badge/SQL%20Server-MSSQL-CC2927?logo=microsoft-sql-server)
![T-SQL](https://img.shields.io/badge/T--SQL-Optimized-blue)
![Database](https://img.shields.io/badge/Database-Relational-green)
![Normalization](https://img.shields.io/badge/Normalization-3NF-orange)

**A fully structured and normalized relational database system for subscription-based streaming platforms**

[Features](#-key-features) • [Architecture](#-architecture-diagrams) • [Entities](#-entities--relationships) • [SQL Components](#-sql-components-implemented) • [Tech Stack](#-technologies-used)

</div>

---

## 📖 Overview

This project presents a comprehensive **relational database management system (RDBMS)** designed for subscription-based online streaming platforms. It models real-world OTT platforms like **Netflix**, **Amazon Prime Video**, **Hotstar**, and **Hulu**.

The system handles complete platform functionality including:

- 👤 User account management
- 💳 Subscription plans & billing
- 💰 Payment processing
- 🎥 Content metadata & cataloging
- 📱 Multi-device tracking
- 🕒 Watch history & analytics
- 🌍 Region-based content licensing

The database is implemented using **Microsoft SQL Server (MSSQL)** with real-world relational modeling and optimized SQL operations.

---

## 📸 Architecture Diagrams

### **Entity-Relationship (ER) Diagram**

<div align="center">

![ER Diagram](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/blob/main/ER.png)

</div>

### **Relational Schema**

<div align="center">

![Relational Schema](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/blob/main/Schema.png)

</div>

---

## 🚀 Key Features

### 🔐 User Management
- Complete user information and account details storage
- Registration timestamps tracking
- Account status monitoring (active/inactive)
- User authentication support

### 💳 Subscription Handling
- Multiple subscription tiers (Basic, Standard, Premium)
- Subscription lifecycle tracking (start/end dates)
- Renewal status monitoring
- Plan upgrade/downgrade support

### 🎥 Content Catalog
- Comprehensive metadata for movies & series
- Attributes: title, genre, duration, release date
- Rating system integration
- Age rating & content description
- Multi-language support

### 📱 Device Registration
- Track all devices registered per user
- Multi-device streaming rules enforcement
- Device limit management
- Device type identification (TV, Mobile, Tablet, etc.)

### 🕒 Watch History Tracking
- Complete viewing history logs
- Progress tracking for resume functionality
- Completion status for recommendations
- Timestamp-based analytics

### 💰 Payment System
- Detailed payment transaction records
- Multiple payment method support
- Amount, timestamp, and status tracking
- Payment history for billing inquiries

### 🌍 Content Licensing
- Region-based access control
- License validity tracking (start/end dates)
- Geographic content restrictions
- Legal compliance management

---

## 🧩 Entities & Relationships

### **Core Entities**

| Entity | Description |
|--------|-------------|
| **Users** | Stores user account information |
| **Subscription Plans** | Defines available subscription tiers |
| **Subscriptions** | Links users to their active plans |
| **Contents** | Catalog of movies and series |
| **Watch History** | Tracks user viewing activity |
| **Payments** | Records financial transactions |
| **Devices** | Manages registered streaming devices |
| **Content Licensing** | Handles region-based content access |

### **Relationship Summary**

```
Users (1) ──────── (M) Subscriptions
Users (1) ──────── (M) Watch History
Users (1) ──────── (M) Payments
Contents (1) ────── (M) Watch History
Contents (1) ────── (M) Content Licensing
Subscription Plans (1) ── (M) Subscriptions
Subscriptions (1) ─────── (M) Devices
```

**Key Relationships:**
- One user → many subscriptions
- One user → many watch history records
- One content item → many watch history entries
- One subscription → many devices
- One subscription plan → many users
- One content item → many content licenses
- One user → many payment records

These relationships ensure **referential integrity** and **efficient data retrieval**.

---

## 📦 Project Contents

This comprehensive project includes:

- ✅ **ER Diagram** & Relational Schema with visual representations
- ✅ **Entity Descriptions** with complete attribute lists
- ✅ **Normalized Schema** (1NF → 2NF → 3NF)
- ✅ **SQL DDL Scripts** (CREATE TABLE statements)
- ✅ **SQL DML Scripts** (INSERT sample data)
- ✅ **User-Defined Functions** (parameterized & non-parameterized)
- ✅ **Stored Procedures** with TRY–CATCH error handling
- ✅ **Cursor Implementation** for iterative processing
- ✅ **Analytical SQL Queries** (reports, statistics, revenue analysis)

---

## 🔧 Technologies Used

| Technology | Purpose |
|-----------|---------|
| **Microsoft SQL Server (MSSQL)** | Primary database engine |
| **T-SQL (DDL & DML)** | Table creation, data manipulation, queries |
| **Stored Procedures** | Encapsulated server-side business logic |
| **User-Defined Functions** | Reusable data-retrieval utilities |
| **Cursors** | Iterative SQL record processing |
| **Normalization (1NF–3NF)** | Data redundancy reduction & consistency |
| **ER Modeling** | Structured database design methodology |

---

## 📊 SQL Components Implemented

### 🗂️ Table Creation (DDL)

Complete DDL scripts for all core modules:

- ✅ Users table with authentication fields
- ✅ Subscription Plans with pricing tiers
- ✅ Subscriptions linking users and plans
- ✅ Contents with comprehensive metadata
- ✅ Watch History with progress tracking
- ✅ Devices with registration details
- ✅ Payments with transaction records
- ✅ Content Licensing with region mapping

### 📝 Sample Data Insertion (DML)

Realistic sample records for:

- 👥 Multiple user profiles
- 💳 Various subscription plans
- 💰 Payment transactions
- 🎬 Diverse content metadata
- 🕒 Watch history logs
- 🌍 Regional licensing data
- 📱 Multiple device registrations

### ⚙️ User-Defined Functions

**Implemented Functions:**
1. **Get All User First Names** – Retrieves list of all registered users
2. **Filter Plans by Cost Range** – Returns subscription plans within price bounds

### 🔄 Stored Procedures

**Key Procedures:**
1. **Retrieve User Details** – Fetches complete user information
2. **Filter Content by Language** – Returns content matching language preference
3. **User Watch History with Error Handling** – Joins user and watch history with TRY–CATCH blocks

### 🔁 Cursor Implementation

- Iterates over subscription plans
- Prints detailed plan information
- Demonstrates cursor-based processing

### 📈 Analytical Queries

**Business Intelligence Queries:**
- 📊 Active users by subscription plan
- 💵 Total revenue generation analysis
- 🎥 Watch history insights and trends
- 🔄 Subscription renewal tracking
- 🕐 Recently watched content (last 3 years)
- 📉 User engagement metrics
- 🌍 Regional content performance

---

## 🎯 Purpose & Applications

This system serves as a **realistic simulation** of how major streaming platforms manage:

✨ **Scalability:**
- Handles millions of users
- Manages thousands of content items
- Processes high-volume transactions

💼 **Business Operations:**
- Subscription billing automation
- Playback analytics for recommendations
- Regional licensing compliance
- Revenue tracking and forecasting

🔧 **Technical Excellence:**
- Performance-optimized data handling
- Referential integrity enforcement
- Normalized data structure
- Industry-standard practices

**Bridges academic database principles with real industry implementations.**

---

## 🛠️ Installation & Setup

### Prerequisites
- Microsoft SQL Server 2016 or higher
- SQL Server Management Studio (SSMS)

### Quick Start

1. **Clone the Repository**
```bash
git clone https://github.com/Amritanshu-404/Streaming-Service-DBSchema.git
cd Streaming-Service-DBSchema
```

2. **Open SSMS**
- Connect to your SQL Server instance

3. **Execute DDL Scripts**
- Run table creation scripts in order

4. **Insert Sample Data**
- Execute DML scripts to populate tables

5. **Test Functions & Procedures**
- Run provided test queries

---

## 🔮 Future Enhancements

Potential extensions for this project:

- [ ] 🔌 **REST API Integration** – Connect database to web services
- [ ] 📊 **Advanced Analytics Dashboard** – Real-time reporting
- [ ] 🤖 **Machine Learning Integration** – Content recommendations
- [ ] 🔔 **Notification System** – Payment reminders, new content alerts
- [ ] 📱 **Mobile App Backend** – Native app support
- [ ] 🌐 **Multi-region Deployment** – Distributed database architecture
- [ ] 🔐 **Enhanced Security** – Encryption, role-based access control

---

## 🧾 Conclusion

This project successfully demonstrates the creation of a **scalable**, **normalized**, and **functional** database system for modern streaming platforms.

**Key Achievements:**
- ✅ Comprehensive data modeling
- ✅ Optimized SQL operations
- ✅ Real-world business logic implementation
- ✅ Industry-standard best practices
- ✅ Extensible architecture

The system integrates user management, subscription plans, payment processing, device tracking, content licensing, and analytics into a cohesive RDBMS—all implemented using MSSQL best practices.

**Ready for extension into:**
- API integration layers
- Backend application systems
- Advanced analytics engines
- Production-grade deployments

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Authors

<div align="center">

**Developed by:**

**Siddharth Kumar**  
GitHub: [@siddharthkumar](https://github.com/your-username)

**Ritesh Singh Kushwaha**  
GitHub: [@riteshkushwaha](https://github.com/your-username)

**Amritanshu Kumar**  
GitHub: [@Amritanshu-404](https://github.com/Amritanshu-404)

</div>

---

## 📞 Contact & Support

Have questions or suggestions?

- 🐛 [Report Issues](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/issues)
- 💡 [Request Features](https://github.com/Amritanshu-404/Streaming-Service-DBSchema/issues/new)
- ⭐ [Star this Repository](https://github.com/Amritanshu-404/Streaming-Service-DBSchema)

---

<div align="center">

**If you find this project helpful, please consider giving it a ⭐!**

Made with ❤️ for database enthusiasts.

</div>
