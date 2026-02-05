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

## 2.6 Tech Stack Selection

**Questions**

*   **Frontend:** Next.js (Primary), React, Vue.js, Svelte?
*   **Backend as a Service (BaaS):** Supabase (Primary), Firebase?
*   **Custom Backend (Optional):** FastAPI, Node.js (Express), Serverless Functions?
*   **Database:** PostgreSQL (via Supabase), other SQL/NoSQL?
*   **Hosting:** Vercel (for Next.js), Render, Fly.io, AWS (EC2/ECS/Lambda)?
*   **Domain & DNS (If Web):** 

**Suggested Guide**

>   **Recommended Baseline for Solo/Startup:** Next.js (Frontend) + Supabase (BaaS for Database, Auth, Storage).
>   **Consider FastAPI:** If complex, custom Python backend logic is required beyond what a BaaS provides.
>   Start simple, leverage managed services for speed. Focus on core features first.

---

## 2.7 Security Design (Service-Oriented)

**Questions**

* Auth method (e.g., Supabase Auth, OAuth)?
* Role-based access control?
* Encryption strategy (data in transit, data at rest)?
* Secrets management (e.g., environment variables, external secret stores)?
* What to include in .env files?
* Backup and recovery plan?

**Suggested Guide**

> Leverage established BaaS security features (like Supabase Auth and RLS). For custom backend, implement robust authentication and authorization. Use environment variables for non-sensitive config and dedicated secret management tools for sensitive credentials.

## 2.8 Environment Variables (.env) Questionnaire

**Questions**

* What environment variables are required for the application (e.g., API keys, database URLs, ports)?
* Which variables contain sensitive information (secrets) that should not be committed to version control?
* How will .env files be managed for different environments (development, staging, production)?
* What is the process for sharing .env templates or examples without exposing secrets?

**Suggested Answer Guide**

> “Required variables include ___ (e.g., SUPABASE_URL, SUPABASE_ANON_KEY, API_KEY). Sensitive variables are ___ and will be securely managed (e.g., through your hosting provider's secret management for production like Vercel's Environment Variables, or a dedicated secret management tool). Use .env.example for templates, and document setup in README.”

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

> GitHub Actions → Vercel (for Next.js) / Other hosting platforms

---

## 6.3 Monitoring & Logging

**Questions**

* What metrics matter?
* Error tracking?
* Alerting rules?

**Suggested Guide**

> CloudWatch + logs + alarms

---

## 6.4 Cost Estimation (Cloud/SaaS)

**Questions**

* Monthly cost (for hosting, BaaS, etc.)?
* Cost per user?
* Budget alerts?

**Suggested Guide**

> Monitor costs through your chosen cloud/SaaS providers (e.g., Vercel, Supabase, Render) and set up their native budget alerts.

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

## **Recommended Project Structure for Solo Developers (Next.js, Supabase, Optional FastAPI)**

To maintain consistency across projects and provide clarity for solo developers, this structure is tailored for a Next.js frontend leveraging Supabase for backend services, with an optional dedicated FastAPI backend. It aligns with the Dann Framework's phases.

```
.
├── .env.example
├── .gitignore
├── README.md
├── docs
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
├── nextjs-app
│   ├── .env.local.example
│   ├── .eslintrc.json
│   ├── .gitignore
│   ├── next.config.mjs
│   ├── package.json
│   ├── postcss.config.js
│   ├── public
│   ├── src
│   │   ├── app                # Next.js App Router (pages, API routes)
│   │   │   ├── api
│   │   │   └── (auth)         # Example for auth routes/middleware
│   │   ├── components
│   │   ├── lib                # Utility functions, Supabase client setup
│   │   ├── styles
│   │   └── types
│   ├── tailwind.config.ts
│   ├── tsconfig.json
│   └── yarn.lock # or package-lock.json
├── (optional-fastapi-backend)
│   ├── app
│   │   ├── api
│   │   ├── core
│   │   ├── crud
│   │   ├── main.py
│   │   └── models
│   ├── requirements.txt # or pyproject.toml
│   └── tests
└── Dockerfile # For optional-fastapi-backend
```

**Folder Descriptions**

-   **`.env.example` / `.env.local.example`**: Templates for environment variables to ensure consistent setup across environments.
-   **`docs/`**: Comprehensive documentation, including API documentation and specific phase documents from the Dann Framework.
-   **`nextjs-app/`**: The main Next.js application, serving as the frontend and potentially containing API routes for basic backend functionalities.
    -   **`src/app/`**: Next.js App Router specific files.
        -   **`api/`**: Next.js API routes (e.g., for server-side logic, interacting with external APIs, or proxying requests).
        -   **`(auth)/`**: Example grouping for authentication-related routes or middleware.
    -   **`src/components/`**: Reusable UI components.
    -   **`src/lib/`**: Client-side logic, Supabase client initialization, and utility functions.
    -   **`src/styles/`**: Global styles and styling configurations.
    -   **`src/types/`**: TypeScript type definitions.
-   **`(optional-fastapi-backend)/`**: This directory is included if a dedicated FastAPI backend is necessary for complex, custom logic not efficiently handled by Supabase or Next.js API routes.
    -   **`app/`**: The core FastAPI application.
        -   **`api/`**: FastAPI endpoint definitions.
        -   **`core/`**: Core configurations and utilities for FastAPI.
        -   **`crud/`**: Database CRUD operations (if FastAPI manages a separate database or complex interactions).
        -   **`main.py`**: The main FastAPI application entry point.
        -   **`models/`**: FastAPI data models (e.g., Pydantic).
    -   **`requirements.txt` / `pyproject.toml`**: Python dependency management.
    -   **`tests/`**: Backend unit and integration tests.
-   **`Dockerfile`**: For containerizing the optional FastAPI backend for deployment, if used. This would be located in the optional-fastapi-backend directory, or at the root if a Docker Compose setup is preferred.

This structure allows for a clear separation of concerns, flexibility to scale, and easy integration of additional services while keeping the core development experience focused on Next.js and Supabase for most common use cases.

This structure ensures familiarity and organization across all projects, aligning with the Dann Framework's emphasis on clarity and planning.

---

## **Dann Framework Law**

> **Code is cheap. Clarity is expensive. Pay for clarity first.**
