# IntelliHire: AI-Powered Job Application & Career Simulation Platform

An intelligent, full-stack recruitment and career navigation platform designed to bridge the gap between job seekers and recruitment workflows. By leveraging modern Natural Language Processing (NLP), custom Named Entity Recognition (NER), TF-IDF vectorization, and semantic embeddings, the system automates resume parsing, calculates real-time candidate-to-job matching scores, and generates actionable career trajectory simulations.

---

## Key Features

- **Automated Resume Parsing:** Extracts structured data (skills, experience, contact details, education) from PDF and DOCX files using custom spaCy NER pipelines and rule-based extractors.
- **Semantic Job Matching:** Computes relevance and alignment between candidate profiles and job listings using cosine similarity over dense semantic embeddings and TF-IDF representations.
- **Career Trajectory & Gap Analysis:** Identifies missing skillsets for target job roles and simulates potential career pathways with recommended learning curves.
- **Interactive Recruiter & Applicant Dashboard:** Real-time application tracking, profile management, and ranking metrics.
- **RESTful Architecture:** Modular backend powered by FastAPI/Flask with structured schema validation and CORS integration.

---

## Architecture Overview

```text
├── frontend/             # Single Page Application (React / Vite / Tailwind CSS)
│   ├── src/
│   │   ├── components/   # UI components (Uploaders, Job Cards, Analytics)
│   │   ├── services/     # Axios / API clients
│   │   └── pages/        # Dashboard, Resume Analysis, Job Search
│   └── package.json
│
├── backend/              # Core API & NLP Services (Python / FastAPI)
│   ├── app/
│   │   ├── api/          # Route handlers & endpoints
│   │   ├── core/         # Config, security, and environment settings
│   │   ├── models/       # Pydantic schemas and DB entities
│   │   └── services/     # NLP pipelines, embedding engines, matcher logic
│   ├── models/           # Pre-trained models, spaCy pipelines, or vectorizers
│   ├── requirements.txt
│   └── main.py
└── README.md

---
```
## Tech Stack
**Machine Learning & NLP**
- spaCy (en_core_web_sm / Custom NER): Entity extraction for resumes and job descriptions.

- Scikit-Learn: TF-IDF vectorization, cosine similarity, and feature extraction.

- Sentence-Transformers: Dense embeddings for deep semantic matching.

- PyPDF2 / pdfminer.six / python-docx: Document parsing and text sanitation.

**Backend**
- FastAPI / Uvicorn: High-throughput asynchronous REST API.

- Pydantic: Request/response validation and settings management.

- Python-dotenv: Configuration and secret management.

**Frontend**
- React.js (Vite / Next.js): Dynamic client interface.

- Tailwind CSS: Responsive, modern UI styling.

- Lucide Icons & Chart.js: Visualizations for score matching and skill gap distribution.
