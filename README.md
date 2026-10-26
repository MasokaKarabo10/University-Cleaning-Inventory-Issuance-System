# University-Cleaning-Inventory-Issuance-System

Java Swing desktop application for managing a university's cleaning-supply inventory: materials, suppliers, cleaners, and stock issuance. Built as a 4-person group project for PRG381 (Belgium Campus iTversity, 2026).

Tech: Java · Swing (NetBeans GUI Builder) · JDBC · PostgreSQL · Git/GitHub

Dashboard Materials Management

✨ Features
Staff authentication with role-based access (Storekeeper / Supervisor)
Dashboard with summary statistics and low-stock alerts
Full CRUD for Materials, Suppliers, Cleaners and Stock Issuance
Stock deducted automatically on issuance; over-issuing is blocked
Search/filter, plus inventory, low-stock, issuance-history and usage reports
Input validation and centralized exception handling

🏗️ Architecture
com.university.cleaninginventory
├── model   → entity classes (Material, Supplier, Cleaner, User, StockIssuance)
├── dao     → JDBC data-access classes (PreparedStatement-based)
├── ui      → Swing forms
└── util    → DB connection, validation, exception handling

Database: PostgreSQL. materials.supplier_id is a foreign key to suppliers, so every material is traceable to its supplier.

👤 My Contribution (Karabo Masoka)
Materials Management: full CRUD, reorder levels, search/filter, supplier linkage
Suppliers Management: full CRUD with contact validation
Centralized exception handling & transactions: shared handler, commit/rollback on stock issuance. 

👥 Team
Member	Focus
Karabo Masoka	Materials, Suppliers, Exception Handling & Transactions
Blessing Maaka	Authentication, Dashboard, Cleaners & Stock Issuance
Katlego Lethole	Authentication, Dashboard, Cleaners & Stock Issuance
Phenyo Pooko	Authentication, Dashboard, Cleaners & Stock Issuance
Willem Carl Els	Reports & Validation/Exception

🚀 Run Locally
Install JDK 21+, NetBeans, and PostgreSQL.
Clone the repo and open the project in NetBeans.
Create a database (e.g. cleaninginventorydb) and run sql/schema.sql.
Copy db.properties.example to db.properties and enter your own DB credentials.
Add the PostgreSQL JDBC driver to the project libraries, then Run.
