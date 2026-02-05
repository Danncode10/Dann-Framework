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
