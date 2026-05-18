# TECHNICAL_SPEC.md

## Project Overview
TestCo - SaaS Analytics is a platform designed to provide businesses with comprehensive analytics and reporting capabilities. It will allow users to connect various data sources, visualize key performance indicators through interactive dashboards, and generate custom reports to gain actionable insights into their operations. The platform aims to be scalable, secure, and user-friendly.

## Tech Stack
- Backend: FastAPI==0.110.0 (Python)
- Web Server: Uvicorn==0.27.1
- Database: PostgreSQL (via SQLAlchemy==2.0.25)
- Frontend: Basic HTML/CSS/JavaScript (for initial MVP, future React/Vue.js)

## File Tree
.
|-- backend/
|   |-- app/
|   |   |-- __init__.py
|   |   |-- main.py
|   |   |-- api/
|   |   |   |-- __init__.py
|   |   |   |-- v1/
|   |   |   |   |-- __init__.py
|   |   |   |   |-- endpoints/
|   |   |   |   |   |-- __init__.py
|   |   |   |   |   |-- analytics.py
|   |   |-- core/
|   |   |   |-- __init__.py
|   |   |   |-- config.py
|   |   |-- db/
|   |   |   |-- __init__.py
|   |   |   |-- base.py
|   |   |   |-- session.py
|   |   |-- models/
|   |   |   |-- __init__.py
|   |   |   |-- analytics_data.py
|   |   |-- schemas/
|   |   |   |-- __init__.py
|   |   |   |-- analytics.py
|   |-- tests/
|   |   |-- __init__.py
|   |   |-- test_analytics.py
|   |-- Dockerfile
|   |-- requirements.txt
|   |-- .env.example
|-- frontend/
|   |-- public/
|   |   |-- index.html
|   |   |-- css/
|   |   |   |-- style.css
|   |   |-- js/
|   |   |   |-- main.js
|   |-- README.md
|-- README.md

## API Endpoints
- Method: GET
  - Path: /api/v1/analytics/data
  - Request body: None (expects query parameters for filtering, e.g., ?start_date=YYYY-MM-DD&end_date=YYYY-MM-DD&metric=sales)
  - Response: { "data": [ { "timestamp": "YYYY-MM-DDTHH:MM:SSZ", "metric_name": "value" } ], "message": "Analytics data retrieved successfully" }
  - Auth: Bearer token required

- Method: POST
  - Path: /api/v1/analytics/data
  - Request body: { "timestamp": "YYYY-MM-DDTHH:MM:SSZ", "metric_name": "value" }
  - Response: { "message": "Data point added successfully", "id": "uuid" }
  - Auth: Bearer token required

## Environment Variables
- DATABASE_URL="postgresql+psycopg2://user:password@host:port/dbname"
- SECRET_KEY="your_super_secret_key"
- CORS_ORIGINS="http://localhost:3000,https://yourdomain.com"

## Dependencies (backend/requirements.txt)
fastapi==0.110.0
uvicorn==0.27.1
SQLAlchemy==2.0.25
psycopg2-binary==2.9.9
pydantic==2.6.1
python-dotenv==1.0.1
python-jose[cryptography]==3.3.0
passlib[bcrypt]==1.7.4
requests==2.31.0
