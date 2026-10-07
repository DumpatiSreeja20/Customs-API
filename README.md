# Customs Customer & Branch API 🚀

A fully working Dockerized REST API for managing customers and their branches.  
Built with FastAPI, PostgreSQL, Docker Compose, and SQLAlchemy.

## 🧠 Project Purpose

This backend service manages customer and branch records for a customs-related business.  
It showcases clean API design, modular structure, database relationships, and Docker-based deployment.

## 🌐 Live Swagger Docs
Once running, go to: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## ⚙️ Tech Stack

- 🐍 FastAPI – Lightweight web framework for APIs  
- 🐘 PostgreSQL – Relational database  
- 🐳 Docker Compose – One-command full environment  
- 🔁 SQLAlchemy – ORM for table relationships  
- ✅ Pydantic – Request/response validation  

---

## 🧪 API Endpoints

### Customers
- `GET /customers` – List all
- `POST /customers` – Create
- `GET /customers/{cust_id}` – View
- `DELETE /customers/{cust_id}` – Delete

### Branches
- `POST /branches` – Create
- `GET /branches` – List
- `GET /branches/{branch_id}` – View

---

## 🐳 Setup Instructions (Docker)

```bash
git clone https://github.com/YOUR_USERNAME/customs-api.git
cd customs-api
docker compose up --build

## 📬 Sample Postman Collection

Download: [postman_collection.json](postman_collection.json)

> This was auto-generated from the OpenAPI spec (`openapi.json`) using Postman.

## 📊 ER Diagram

Visualize the database schema here:  
👉 [View on dbdiagram.io](https://dbdiagram.io/d/68558899f039ec6d362d9081)

- `customers` → holds customer info (name, email, gstin)
- `branches` → belongs to a customer via `customer_id`
- One-to-many: A customer can have many branches

## 📁 Folder Structure

customs-api/
├── app/
│   ├── main.py             # FastAPI entry-point
│   ├── database.py         # SQLAlchemy engine/session
│   ├── models.py           # ORM tables (Customer, Branch)
│   ├── schemas.py          # Pydantic models
│   └── routers/
│       ├── customers.py    # /customers endpoints
│       └── branches.py     # /branches endpoints
├── Dockerfile              # Build the API image
├── docker-compose.yml      # Run API + Postgres together
├── postman_collection.json # Collection for manual testing
├── erd.png                 # Schema diagram image
├── requirements.txt
└── README.md               # ← you are here


## 🚀 Demo Steps (via Swagger UI)

1. `POST /customers` – Create a customer (e.g., Ocean Exports)
2. `POST /branches` – Add a branch using `customer_id = 1`
3. `GET /customers/1` – Fetch customer along with its branches
4. `GET /branches` – List all branches (optional `customer_id` filter)
5. `DELETE /customers/1` – Remove customer (auto deletes branches)

## 👤 Author

**Sreeja_Dumpati**   
GitHub: [@sreejadumpati20](https://github.com/DumpatiSreeja20)  
Project: Customs API – Intern Evaluation Task




