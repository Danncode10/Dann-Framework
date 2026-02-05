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