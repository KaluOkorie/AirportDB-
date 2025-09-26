# ✈️ AirportDB: A Modern Airport Management System

Welcome to **AirportDB**, a comprehensive and secure database system designed to power the heart of modern airport operations. This project was developed as part of my Advanced Databases module, showcasing a full-stack approach to relational database design, from conceptual ERD to a production-ready SQL Server implementation.

Moving beyond a simple academic exercise, AirportDB tackles real-world challenges like high-concurrency ticketing, real-time revenue tracking, and robust security, ensuring a seamless experience for both passengers and staff. It's a testament to how thoughtful database architecture can drive efficiency, security, and insight in a critical industry.

---

## 🚀 Key Features

*   **End-to-End Ticketing & Reservation:** Manages the entire passenger journey, from booking a flight with a unique PNR to issuing e-boarding passes and assigning seats.
*   **Smart Automation:** Automates complex calculations for baggage fees, meal upgrades, and preferred seating, reducing human error.
*   **Real-Time Revenue Analytics:** Provides a dynamic breakdown of revenue streams (fares, baggage, services) per employee and flight via dedicated views.
*   **Robust Security Model:** Implements Role-Based Access Control (RBAC) with password hashing and salting, ensuring that staff, supervisors, and passengers only access what they need.
*   **Comprehensive Audit Trail:** Tracks every critical change to passenger or employee data for full transparency and compliance.
*   **High-Concurrency Ready:** Uses transactions and row-level locking to prevent issues like double-booking during peak travel times.

---

## 🗃️ Database Design

### Entity-Relationship Diagram (ERD)
The database schema is built around core entities like `Passengers`, `Flights`, `Reservations`, and `Tickets`, with clear relationships ensuring data integrity. The design emphasizes clarity and scalability.

![AirportDB ERD](path/to/your/ERD-image.png) 
*<!-- Pro-Tip: Actually upload an image of your ERD and link it here! -->*

### Normalization
The database is rigorously normalized to the **Third Normal Form (3NF)**, effectively eliminating data redundancy and update anomalies. This ensures that each piece of information is stored in one place, making the system more efficient and reliable.

---

## 💻 Installation & Setup

To explore AirportDB on your own SQL Server instance:

1.  **Restore the Database:**
    *   Download the `AirportDB-Full_Database_Backup.bak` file from this repository.
    *   Use SQL Server Management Studio (SSMS) to restore the backup to your local SQL Server instance.

2.  **Explore the Schema:**
    *   Open the database to examine the tables, views, stored procedures, and functions.
    *   Key objects to check out:
        *   `EmployeeRevenueBreakdown` View: For financial insights.
        *   `IssueTicket` Stored Procedure: For the core booking logic.
        *   `AuditLog` Table: To see the security tracking in action.

3.  **Run Example Queries:**
    *   The project includes hypothetical data. Try running `SELECT * FROM EmployeeRevenueBreakdown;` to see the revenue analysis view.

---

## 🛡️ Security & Performance

**Security wasn't an afterthought—it was a priority.** The system employs:
*   **Role-Based Access Control (RBAC):** Distinct permissions for `Ticketing Staff`, `Supervisors`, and `Passengers`.
*   **Data Protection:** Passwords are hashed with a unique salt for each user.
*   **SQL Injection Prevention:** All dynamic inputs are handled through parameterized queries in stored procedures.

**Performance is optimized for speed:**
*   **Strategic Indexing:** Non-clustered indexes on frequently searched columns (e.g., `LastName`, `DoB`) ensure quick query responses.
*   **Efficient Joins:** The schema design minimizes complex joins, and views are used to simplify common data aggregations.

---

## 💾 Backup & Recovery Strategy

A reliable system needs a reliable safety net. AirportDB implements a multi-layered backup plan:
*   **Full Backups:** Weekly complete snapshots of the database.
*   **Differential Backups:** Daily backups of changes since the last full backup.
*   **Transaction Log Backups:** Hourly backups for point-in-time recovery, minimizing data loss.

This strategy ensures business continuity, allowing for a quick recovery in case of any unforeseen events.

---

## 🎯 Conclusion & Future Vision

AirportDB is more than just a database; it's a foundation for building intelligent, efficient, and secure airport management software. It demonstrates a deep understanding of database principles, from ACID compliance to real-world application security.

**Ideas for the future?** This system could be extended with:
*   API integration for mobile check-in and flight status updates.
*   Advanced analytics with Power BI for predictive staffing and revenue forecasting.
*   Cloud migration to Azure SQL Database for enhanced scalability and managed services.

---

## 👋 Let's Connect!

I'm passionate about using technology to solve complex problems. If you're interested in databases, software architecture, or just want to talk tech, feel free to reach out!

*   **GitHub:** [KaluOkorie](https://github.com/KaluOkorie)
*   **LinkedIn:** [<!-- Your LinkedIn Profile Link -->](https://linkedin.com/in/yourprofile)

> *“The key to efficient travel lies not just in the aircraft, but in the data that guides every passenger smoothly to their destination.”*
