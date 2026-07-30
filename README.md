# 🚀 SpecGuard AI
### Intelligent Requirements-to-Code Drift Detection and Software Change Impact Analysis Platform

> **SpecGuard AI** is an AI-powered Software Engineering platform that automatically maintains traceability between software requirements and source code, detects requirement-to-code drift, performs software change impact analysis, and predicts the risk of software modifications using Large Language Models (LLMs), Semantic Code Analysis, Knowledge Graphs, and Machine Learning.
---

## 📖 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Solution](#-solution)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Project Workflow](#-project-workflow)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Core Modules](#-core-modules)
- [Artificial Intelligence Components](#-artificial-intelligence-components)
- [Knowledge Graph](#-knowledge-graph)
- [Machine Learning](#-machine-learning)
- [Example Use Case](#-example-use-case)
- [Installation](#-installation)
- [Running the Project](#-running-the-project)
- [Screenshots](#-screenshots)
- [Future Enhancements](#-future-enhancements)
- [Contributors](#-contributors)
- [License](#-license)

---

# 📌 Overview

Modern software systems evolve continuously through bug fixes, feature additions, API updates, database changes, and code refactoring.

During this evolution, software implementations often begin to deviate from their original Software Requirement Specification (SRS). These inconsistencies are difficult to detect manually and may introduce security issues, business logic violations, or broken functionality.

**SpecGuard AI** automates this process by continuously analysing software requirements, source code, APIs, database schemas, test cases, and version changes to ensure that implementation remains aligned with approved requirements.

The platform combines modern Artificial Intelligence techniques with Software Engineering principles to provide explainable traceability and intelligent software maintenance.

---

# ❗ Problem Statement

Maintaining traceability between software requirements and implementation is one of the biggest challenges in software maintenance.

Traditional Requirement Traceability Matrices (RTMs) are usually created manually and quickly become outdated.

As software evolves:

- Developers modify source code
- APIs change
- Database schemas evolve
- Business logic gets updated
- Security checks may accidentally disappear

Although the software may still compile successfully, it may no longer satisfy its original requirements.

Identifying these mismatches manually is difficult, expensive, and time-consuming.

SpecGuard AI solves this problem through intelligent requirement analysis, semantic code understanding, graph-based traceability, and AI-driven impact analysis.

---

# 💡 Solution

SpecGuard AI automatically:

- Reads Software Requirement Specification (SRS) documents
- Extracts structured software requirements
- Analyses source code
- Maps requirements to implementation
- Builds an intelligent knowledge graph
- Detects software changes
- Performs impact analysis
- Detects requirement drift
- Predicts change risk
- Generates AI-powered recommendations

---

# ✨ Key Features

## 📄 Requirement Analysis

- Upload SRS documents
- AI-based requirement extraction
- Functional & Non-functional requirement classification
- Actor, action, resource and constraint extraction

---

## 💻 Source Code Analysis

- Parse source code
- Identify:
  - Files
  - Classes
  - Methods
  - Functions
  - APIs
  - Routes
  - Dependencies

---

## 🔗 Requirement-to-Code Mapping

Uses semantic similarity instead of keyword matching.

Example:

Requirement:

```
Only administrators can delete student accounts.
```

Possible matching functions:

```
deleteStudent()
removeStudent()
eraseUser()
deleteAccount()
```

---

## 🧠 Knowledge Graph

Maintains relationships among:

- Requirements
- Functions
- APIs
- Database Tables
- Test Cases
- Commits
- Risks

---

## 🔍 Requirement Drift Detection

Automatically detects whether code changes violate original requirements.

Example:

Requirement:

```
Only Admin can delete student accounts.
```

Original code

```python
if user.role == "admin":
    deleteStudent()
```

Modified code

```python
deleteStudent()
```

SpecGuard AI raises a **Critical Drift Alert** because authorization validation has been removed.

---

## 📊 Software Change Impact Analysis

Determines:

- Which requirements are affected
- Which APIs are affected
- Which database tables are affected
- Which test cases need re-execution

---

## ⚠️ Risk Prediction

Predicts whether a software modification is:

- 🟢 Low
- 🟡 Medium
- 🟠 High
- 🔴 Critical

using Machine Learning models.

---

## 📈 Analytics Dashboard

Displays

- Traceability Graph
- Drift Alerts
- Risk Scores
- Project Statistics
- Impact Reports
- AI Recommendations

---

# 🏗 System Architecture

```
                    +-------------------+
                    |   User / Admin    |
                    +---------+---------+
                              |
                              |
                     Upload SRS & Source Code
                              |
                              ▼
                 +---------------------------+
                 |      FastAPI Backend      |
                 +-------------+-------------+
                               |
      ------------------------------------------------------
      |            |             |            |             |
      ▼            ▼             ▼            ▼             ▼
 Requirement   Code Parser   API Parser   DB Parser   Git Analyzer
 Extraction
      |                                          |
      +----------------------+-------------------+
                             |
                             ▼
                  Semantic Requirement Mapping
                             |
                             ▼
                 Requirement Traceability Graph
                             |
      ------------------------------------------------
      |                    |                         |
      ▼                    ▼                         ▼
 Drift Detection     Impact Analysis        Risk Prediction
      |                    |                         |
      +--------------------+-------------------------+
                           |
                           ▼
                    React Dashboard
```

---

# 🔄 Project Workflow

```
User

↓

Create Project

↓

Upload SRS

↓

LLM extracts requirements

↓

Upload Source Code

↓

Code Analysis

↓

Requirement Mapping

↓

Knowledge Graph

↓

Software Change Detection

↓

Impact Analysis

↓

Requirement Drift Detection

↓

Risk Prediction

↓

Dashboard & Reports
```

---

# 🛠 Technology Stack

| Component | Technology |
|------------|------------|
| Frontend | React.js |
| Styling | Tailwind CSS |
| Backend | FastAPI |
| Language | Python |
| Database | PostgreSQL |
| Knowledge Graph | Neo4j |
| LLM | Ollama / Hosted LLM |
| Code Embedding | CodeBERT |
| ML Models | Scikit-learn, XGBoost |
| Authentication | JWT |
| Code Parsing | Python AST / Tree-sitter |
| Version Control | Git |
| Deployment | Docker |

---

# 📂 Project Structure

```
SpecGuard-AI/

│
├── frontend/
│   ├── components/
│   ├── pages/
│   ├── assets/
│   ├── services/
│   └── App.jsx
│
├── backend/
│   ├── api/
│   ├── auth/
│   ├── models/
│   ├── services/
│   ├── graph/
│   ├── ml/
│   ├── parsers/
│   ├── utils/
│   └── main.py
│
├── database/
│
├── uploads/
│
├── reports/
│
├── docs/
│
├── tests/
│
├── docker/
│
├── requirements.txt
│
└── README.md
```

---

# 🧩 Core Modules

- User Authentication
- Project Management
- SRS Document Management
- AI Requirement Extraction
- Requirement Classification
- Source Code Analysis
- API Analysis
- Database Analysis
- Semantic Requirement Mapping
- Knowledge Graph
- Change Detection
- Drift Detection
- Change Impact Analysis
- Risk Prediction
- Analytics Dashboard
- Report Generation

---

# 🤖 Artificial Intelligence Components

### Large Language Model (LLM)

Responsible for:

- Requirement extraction
- Requirement classification
- Constraint understanding
- Recommendation generation

---

### Semantic Code Analysis

Uses CodeBERT embeddings to understand code semantically instead of relying on keyword matching.

---

### Machine Learning

Predicts software change risk using features such as:

- Lines Added
- Lines Deleted
- Number of Changed Files
- Cyclomatic Complexity
- Dependencies
- Requirement Criticality
- Historical Defects
- Test Coverage

Models:

- Logistic Regression
- Random Forest
- XGBoost

---

# 🌐 Knowledge Graph

The knowledge graph maintains relationships among software artifacts.

Example:

```
Requirement

↓

Implemented By

↓

Function

↓

Called By

↓

API

↓

Uses

↓

Database

↓

Validated By

↓

Test Case
```

This enables explainable impact analysis and traceability.

---

# 📊 Machine Learning Pipeline

```
Git Changes

↓

Feature Extraction

↓

Data Preprocessing

↓

Feature Engineering

↓

ML Model

↓

Risk Prediction

↓

Dashboard
```

---

# 📝 Example Use Case

Requirement:

```
FR-01

Only administrators shall be allowed to delete student accounts.
```

The platform extracts:

```
Actor:
Administrator

Action:
Delete

Resource:
Student Account

Constraint:
Administrator Only
```

If a developer later removes the authorization check,

SpecGuard AI

- Detects the modified function
- Identifies affected requirement
- Finds impacted APIs
- Finds affected test cases
- Generates a Critical Drift Alert
- Suggests corrective actions

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/your-username/SpecGuard-AI.git
```

Navigate into the project

```bash
cd SpecGuard-AI
```

Install dependencies

```bash
pip install -r requirements.txt
```

Start Backend

```bash
uvicorn main:app --reload
```

Start Frontend

```bash
npm install
npm run dev
```

---

# 🚀 Running the Project

Backend

```
http://localhost:8000
```

Frontend

```
http://localhost:5173
```

API Documentation

```
http://localhost:8000/docs
```

---

# 📷 Screenshots

> Add screenshots here after completing the project.

Example

- Dashboard
- Requirement Extraction
- Knowledge Graph
- Drift Detection
- Impact Analysis
- Reports

---

# 🔮 Future Enhancements

- Java support
- C++ support
- JavaScript support
- GitHub Pull Request integration
- CI/CD integration
- GraphRAG
- IDE Plugin
- Architecture Drift Detection
- Automatic Test Case Generation
- Multi-Agent AI Review
- Enterprise Local LLM Deployment

---

# 👨‍💻 Contributors

**P. Mokshith Reddy**

Software Engineering Project

---

# 📜 License

This project is developed for educational and research purposes as part of a Software Engineering course.

---

# ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub.

---

## 📧 Contact

For questions, suggestions, or collaborations:

📩 Email: vighneshrcb18@gmail.com

---

> **SpecGuard AI** aims to bridge the gap between software requirements and implementation by leveraging Artificial Intelligence, Knowledge Graphs, and Machine Learning to make software maintenance smarter, safer, and more efficient.
