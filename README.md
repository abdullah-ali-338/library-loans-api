# 📚 Library Loans API

![Python Version](https://img.shields.io/badge/Language-Python_3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-Personal_Use-blue?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-FastAPI_%7C_SQLite_%7C_SQLAlchemy-orange?style=for-the-badge)

A relational database service built with FastAPI and SQLite that manages 10,000+ loan records with sub-millisecond query performance and database-enforced lending integrity.

🌐 **GitHub Repo:** [github.com/abdullah-ali-338/library-loans-api](https://github.com/abdullah-ali-338/library-loans-api)

---

## ✨ Features

- **Sub-Millisecond Queries:** Optimized query execution times (< 2ms) across 10,000+ loan records via tailored composite indexes.
- **Race Condition Prevention:** Partial unique indexes enforced directly at the database layer to eliminate double lending under concurrent requests.
- **Normalized Schema Design:** Strict relational design separating books, physical copies, library members, and active loan transactions.
- **Pre-Sorted Index Seeking:** Composite covering index eliminates temporary B-Tree sorts on `ORDER BY borrowed_at DESC` queries.

---

## 🛠️ Tech Stack

- **Framework:** FastAPI
- **Database:** SQLite
- **ORM / Query Engine:** SQLAlchemy (Raw SQL execution)
- **Validation:** Pydantic
- **Server:** Uvicorn

---

## 📁 Repository Structure

```text
LibraryLoansAPI/
├── main.py             # FastAPI app, endpoints, and seeding routes
├── database.py         # Connection pooling, table schemas, and custom indexes
├── models.py           # Pydantic validation schemas
├── requirements.txt    # Python dependencies
└── README.md           # Documentation
