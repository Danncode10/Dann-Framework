# **Dann Framework**

### *A Question-First Software Development Framework for Solo Developers*

> **Principle:**
> *If you can’t answer the question clearly, don’t code it yet.*

---

# **PHASE 1 — Project Planning & Problem Definition**

## 1.1 Problem Statement

**Questions**

* What problem am I solving?
* Who experiences this problem?
* How often does the problem occur?
* Why is this problem worth solving?
* What happens if this problem remains unsolved?

**Suggested Answer Guide**

> “Users struggle with ___ because ___. This causes ___ and results in ___.”

---

## 1.2 Target Users

**Questions**

* Who are the primary users?
* Are there secondary users or admins?
* What is their technical skill level (This refers to how comfortable users are with technology and digital platforms.) ?
* What devices do they commonly use?

**Suggested Answer Guide**

> “Primary users are ___ with ___ level of technical skill, mostly using ___ devices.”

---

## 1.3 Project Goals (Version 1 Focus)

**Questions**

* What is the single most important outcome?
* What must the system do *perfectly*?
* What can be ignored for now?

**Suggested Answer Guide**

> “Version 1 succeeds if users can ___ without ___.”

---

## 1.4 Competition & Market Scan

**Questions**

* What existing solutions exist?
* What features do they offer?
* What do users complain about?
* What feature is missing or poorly done?

**Suggested Answer Guide**

> “Competitors solve ___ but fail at ___. My project focuses on ___.”

---

## 1.5 Feature Definition & Scope Control

**Questions**

* What are MUST-HAVE features?
* What are NICE-TO-HAVE features?
* What features are explicitly excluded?

**Suggested Answer Guide**

> MUST: Authentication, core workflow
> NICE: Analytics, themes
> OUT: AI, mobile app (Version 1)

---

## 1.6 Platform & Project Type

**Questions**

* Is this a website by default?
* Will it expand to mobile, AI, or robotics?
* Does it require real-time processing?
* Does it integrate with hardware?

**Suggested Answer Guide**

> “Version 1 is a web application; mobile is planned for Version 4.”

---

## 1.7 User Requirements

**Questions**

* What actions can users perform?
* What actions are restricted?
* What errors must be user-friendly?
* Accessibility needs?

---

## 1.8 System Requirements

**Questions**

* Expected number of users?
* Response time expectations?
* Availability requirements?
* Storage needs?

**Suggested Answer Guide**

> “System should support 1k users with <500ms response time.”

---

## 1.9 Software Evolution Roadmap

**Questions**

* What is Version 1?
* What improves in Version 2?
* When does AI appear?
* When does mobile appear?

**Suggested Answer Guide**

* V1: Core functionality
* V2: UI/UX
* V3: AI / automation
* V4: Mobile app

## 1.10 Monetization Strategy

**Questions**

* Does this web/app have premium features?
* Is it free?
* Does it run ads?

**Suggested Answer Guide**

> “The app is ___ (free/paid/ads-supported). Premium features include ___.”

---

# **PHASE 2 — Software Requirements Specification (SRS)**

## 2.1 Functional Requirements

**Questions**

* What functions must exist?
* What triggers each function?
* What output is produced?

**Example**

> “The system shall allow users to register using email and password.”

---

## 2.2 Non-Functional Requirements

**Questions**

* Performance limits?
* Security level?
* Scalability needs?
* Usability expectations?

---

## 2.3 Technical Requirements

**Questions**

* Preferred programming languages?
* Frameworks?
* Database type?
* APIs required?

---

## 2.4 Constraints

**Questions**

* Time limit?
* Budget?
* Skill limitations?
* Legal/compliance?

---

## 2.5 Acceptance Criteria

**Questions**

* How do we know this feature works?
* What test confirms success?

**Example**

> “Login is successful when user reaches dashboard within 1 second.”

---

## 2.6 Tech Stack Selection (AWS-First)

**Questions**

* Frontend: React / Next.js?
* Backend: FastAPI / Node?
* Database: RDS / DynamoDB?
* Hosting: EC2 / ECS / Lambda?
* Domain & DNS (If Web): 

**Suggested Guide**

> Start simple: Monolith + EC2 + RDS
> Scale later: Microservices + ECS

---

## 2.7 Security Design (Service-Oriented)

**Questions**

* Auth method?
* IAM roles?
* Encryption strategy?
* Secrets storage?
* What to include in .env files?
* Backup plan?

**Suggested Guide**

> Use AWS Cognito, IAM roles, Secrets Manager, CloudWatch

## 2.8 Environment Variables (.env) Questionnaire

**Questions**

* What environment variables are required for the application (e.g., API keys, database URLs, ports)?
* Which variables contain sensitive information (secrets) that should not be committed to version control?
* How will .env files be managed for different environments (development, staging, production)?
* What is the process for sharing .env templates or examples without exposing secrets?

**Suggested Answer Guide**

> “Required variables include ___ (e.g., DATABASE_URL, API_KEY). Sensitive variables are ___ and will be stored in ___ (e.g., AWS Secrets Manager for production). Use .env.example for templates, and document setup in README.”

---

# **PHASE 3 — Software Design**

## 3.1 High-Level Design (HLD)

**Questions**

* What architecture style?
* What are major modules?
* How does data flow?

---

## 3.2 Low-Level Design (LLD)

**Questions**

* Class structures?
* Database schema?
* API endpoints?
* Core algorithms?
* Pseudocode for logic?

---

# **PHASE 4 — System Modeling (UML)**

## 4.1 Context Model

System Context Diagram (Input, Process, Output arrows and System at the center)
**Question:** Who interacts with what?

## 4.2 Interaction Model

Sequence Diagram
**Question:** What happens step-by-step?

## 4.3 Structural Model

Class Diagram / ER Diagram
**Question:** How is data structured?

## 4.4 Behavioral Model

State Machine Diagram
**Question:** How does state change over time?

---

# **PHASE 5 — SDLC Strategy**

## 5.1 SDLC Selection

**Questions**

* Is the scope stable?
* Is feedback frequent?
* Is risk high?

**Suggested Guide**

> Solo Dev Default:
> Waterfall planning + Agile development + Incremental releases

---

# **PHASE 6 — Deployment, Operations & Cost**

## 6.1 Deployment Strategy

**Questions**

* Manual or automated?
* Environments?
* Rollback strategy?

---

## 6.2 CI/CD Pipeline

**Questions**

* When do builds trigger?
* Automated tests?
* Deployment automation?

**Suggested Guide**

> GitHub Actions → AWS ECS / EC2

---

## 6.3 Monitoring & Logging

**Questions**

* What metrics matter?
* Error tracking?
* Alerting rules?

**Suggested Guide**

> CloudWatch + logs + alarms

---

## 6.4 Cost Estimation (AWS)

**Questions**

* Monthly cost?
* Cost per user?
* Budget alerts?

**Suggested Guide**

> Set AWS Budget alerts early

---

# **PHASE 7 — Maintenance & Sustainability**

## 7.1 Technical Debt Plan

**Questions**

* What shortcuts exist?
* When will they be fixed?

---

## 7.2 Documentation Strategy

**Questions**

* README completeness?
* API docs?
* Architecture docs?
* Setup instructions?

---

## 7.3 Exit or Handover Plan

**Questions**

* Can another dev run this?
* Are credentials transferable?
* Is infra reproducible?
* Can project be paused or sold?

---

# **PHASE 8 — Final Review Checklist**

* Problem is clear
* Scope is controlled
* Version 1 is minimal
* Costs are known
* Security is planned
* Future is mapped

---

## **Recommended Folder Structure for Website Projects**

To maintain consistency across projects and make it easy to switch between them, follow this folder structure for website-based applications. This structure is based on the Dann Framework phases and supports a backend-frontend architecture.

```
.
├── backend
│   ├── app
│   │   ├── __init__.py
│   │   ├── __pycache__
│   │   ├── api
│   │   ├── auth
│   │   ├── core
│   │   ├── crud
│   │   ├── main.py
│   │   └── models
│   ├── dev.sh
│   ├── poetry.lock
│   ├── pyproject.toml
│   ├── seed.py
│   └── tests
├── Dockerfile
├── Docs
│   ├── api_docs
│   │   └── README.md
│   ├── Calendar.md
│   ├── DannFramework_docs
│   │   ├── Phase 1: Project Planning & Problem Definition.md
│   │   ├── Phase 2: Software Requirements Specification (SRS).md
│   │   ├── Phase 3: Software Design.md
│   │   ├── Phase 4: System Modeling (UML).md
│   │   ├── Phase 5: SDLC Strategy.md
│   │   ├── Phase 6: Deployment, Operations & Cost.md
│   │   ├── Phase 7: Maintenance & Sustainability.md
│   │   └── Phase 8: Final Review Checklist.md
│   ├── git_commit_format.md
│   └── Versions
│       ├── Changelog
│       ├── README.md
│       ├── Version 1.md
│       └── Version 2.md
├── README.md
├── tunnel.sh
├── ui
│   ├── CONTRIBUTING.md
│   ├── dist
│   │   ├── assets
│   │   └── index.html
│   ├── index.html
│   ├── package-lock.json
│   ├── package.json
│   ├── playwright.config.js
│   ├── postcss.config.js
│   ├── README.md
│   ├── requirements.txt
│   ├── src
│   │   ├── App.jsx
│   │   ├── components
│   │   ├── layouts
│   │   ├── main.jsx
│   │   ├── pages
│   │   ├── services
│   │   ├── store
│   │   ├── styles
│   │   ├── test
│   │   └── utils
│   ├── tailwind.config.js
│   ├── tests
│   │   └── basic-flows.spec.js
│   └── vite.config.js
└── venv
    ├── include
    │   ├── python3.12
    │   └── site
    ├── lib
    │   └── python3.12
    └── pyvenv.cfg
```

### Folder Descriptions

- **backend/**: Contains the server-side application code. Uses FastAPI/Python structure.
  - **app/**: Main application module.
    - **api/**: API endpoint definitions.
    - **auth/**: Authentication logic.
    - **core/**: Core configurations and utilities.
    - **crud/**: Database CRUD operations.
    - **models/**: Data models (e.g., SQLAlchemy).
  - **tests/**: Backend unit and integration tests.
  - **dev.sh**: Development script.
  - **poetry.lock/pyproject.toml**: Dependency management.
  - **seed.py**: Database seeding script.

- **ui/**: Frontend application. Clone a starting UI repository here (e.g., React/Vite setup).
  - **src/**: Source code.
    - **components/**: Reusable UI components.
    - **layouts/**: Page layouts.
    - **pages/**: Application pages.
    - **services/**: API service functions.
    - **store/**: State management (e.g., Redux, Zustand).
    - **styles/**: Styling files.
    - **utils/**: Utility functions.
  - **tests/**: Frontend tests (e.g., Playwright).
  - **dist/**: Build output.

- **Docs/**: Documentation following the Dann Framework phases.
  - **api_docs/**: API documentation.
  - **DannFramework_docs/**: Documentation for each phase as per the framework.
  - **Versions/**: Version-specific changelogs and notes.
  - **git_commit_format.md**: Guidelines for commit messages.

- **venv/**: Python virtual environment (created with `python -m venv venv`).

- **Dockerfile**: Containerization for deployment.

- **tunnel.sh**: Script for tunneling (e.g., ngrok).

This structure ensures familiarity and organization across all projects, aligning with the Dann Framework's emphasis on clarity and planning.

---

## **Dann Framework Law**

> **Code is cheap. Clarity is expensive. Pay for clarity first.**
