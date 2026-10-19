# Graduation-project-
Graduation Project Reposatory 
# Delta Smart Hospital Platform

An integrated, AI-enabled web platform that connects patient, doctor, nurse, laboratory, pharmacy, and emergency workflows in a university hospital.

> Graduation Project, Level 4. Status: **in development**.

## Overview

University hospitals often run appointments, vital signs, lab requests, and prescriptions in separate systems or on paper. This platform puts them in one secure system with a dedicated portal for each role, and adds three AI services to support doctors and hospital management.

## Features

| Portal | What it does |
|---|---|
| Patient | Register, book appointments, view medical record, lab results, prescriptions, notifications |
| Doctor | Daily schedule, patient records, diagnosis, test requests, prescriptions, AI insights |
| Nurse | Record vital signs, nursing notes, alert doctors about abnormal readings |
| Laboratory | Receive test requests, update status, enter results |
| Pharmacy | Drugs and inventory, dispensing, drug-interaction and low-stock alerts |
| Emergency | Fast registration, triage, waiting list, bed board, real-time critical alerts |
| Admin | Dashboard with KPIs, charts, statistics, user management |

**Main workflow:** book appointment, vital signs, examination, lab request and result, prescription, dispensing, patient views everything in their account.

## AI Services

| Service | Purpose |
|---|---|
| No-show prediction | Estimates the probability that a patient will miss an appointment |
| Risk prediction | Estimates patient deterioration risk, with explanations of the main factors (SHAP) |
| Record summarization | Produces a short summary of a patient's record for the doctor |

AI outputs are **decision support only**. The doctor remains responsible for all clinical decisions.

## Architecture

```
React frontend  ->  REST API (backend)  ->  PostgreSQL
                        |
                        +--> AI services (no-show, risk, summarization)
```

- Role-based access control (RBAC) with JWT authentication
- Audit log for access to sensitive records
- WebSocket for real-time alerts
- AI services run separately and are called by the backend

## Tech Stack

| Area | Tools |
|---|---|
| Frontend | React, Vite, Tailwind CSS, React Router, TanStack Query, Axios, Recharts |
| Backend | Python, FastAPI, SQLAlchemy, Alembic, JWT, WebSocket |
| Database | PostgreSQL |
| AI / ML | Python, Pandas, scikit-learn, XGBoost, SHAP |
| NLP | Hugging Face Transformers or an LLM API |
| DevOps | Docker, Docker Compose, GitHub Actions |
| Testing | pytest, Playwright, Locust |
| Design and docs | Figma, OpenAPI/Swagger, dbdiagram.io |

> Update this table if the team changes any technology.

## Repository Structure

```
.
├── backend/        # API, authentication, business logic
├── frontend/       # React portals
├── ai/             # Models, training notebooks, AI service APIs
├── database/       # Schema, migrations, seed scripts
├── docs/           # SRS, ERD, API docs, user guides
├── docker-compose.yml
├── .env.example
└── README.md
```

> Adjust the folders to match the actual repository.


