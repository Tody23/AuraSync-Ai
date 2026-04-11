# Aura-Sync
# Try the Website Demo Here:
# https://tody23.github.io/AuraSync-demo
<p align="center"><strong>The AI operating system for Messenger-first commerce in the Philippines.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/Fastify-5-black?style=for-the-badge&logo=fastify" alt="Fastify">
  <img src="https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=111827" alt="React">
  <img src="https://img.shields.io/badge/Supabase-PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase">
  <img src="https://img.shields.io/badge/OpenAI-GPT--4o--mini-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI">
  <img src="https://img.shields.io/badge/Messenger-Meta-0084FF?style=for-the-badge&logo=messenger&logoColor=white" alt="Messenger">
  <img src="https://img.shields.io/badge/AfterShip-Logistics-FF6A00?style=for-the-badge&logo=aftership&logoColor=white" alt="AfterShip">
</p>

<p align="center">Aura-Sync is a vertical SaaS platform for businesses that sell and support customers through <strong>Facebook Messenger</strong>. It brings AI replies, order capture, fulfillment workflows, CRM intelligence, approvals, logistics, campaigns, and billing into one real-time system designed around how Filipino social commerce actually operates.</p>

<p align="center"><strong>📖 Product Docs:</strong> <code>Available on request</code></p>

---

## What is Aura-Sync?

Aura-Sync turns Messenger conversations into structured business operations. A customer sends a message, Aura-Sync verifies the webhook, routes the event through a guarded AI pipeline, updates customer and order context, and pushes the result into a live dashboard where teams can review, approve, escalate, fulfill, and analyze.

This is not a generic chatbot wrapper. It is a full operating layer for Messenger-based selling: inquiry handling, order collection, pending-order review, shipment tracking, customer intelligence, team assignment, reporting, and SaaS billing all sit in the same product. For operators, that means fewer handoffs and less spreadsheet work. For investors and partners, it means a software surface with multiple monetizable layers inside one workflow.

| | | |
|---|---|---|
| **🤖 AI Auto-Replies** | **🛒 Order Capture** | **📦 Shipment Alerts** |
| **🧠 CRM Intelligence** | **🔐 Approval Queue** | **📣 Campaign Manager** |
| **👥 Team Assignment** | **💳 Wallet + Credits** | **🇵🇭 Taglish-First UX** |

---

## Why It Matters

- **Large workflow, narrow channel**  
  Many Philippine sellers already run demand, support, and fulfillment through Facebook pages and Messenger threads. Aura-Sync is built around that existing behavior instead of trying to force teams into an email-helpdesk model.

- **One product, multiple revenue surfaces**  
  The codebase already supports subscriptions, AI credits, wallet mechanics, and super-admin tenant controls. This is product infrastructure for a SaaS business, not just a chatbot prototype.

- **Operational depth, not just AI veneer**  
  The platform spans messaging, order-state logic, approval routing, shipment alerts, analytics, and CRM scoring. That creates a much stronger moat than a simple “ask an LLM and send the reply back” stack.

- **Local market fit by design**  
  Taglish behavior, Messenger-first UX, PHP billing concepts, and PH-relevant fulfillment flows are not add-ons. They are embedded in the product logic.

---

## Verified Product Highlights

These are based on the current codebase and shipped dashboard/API surface.

<details>
<summary><strong>AI & Conversation Automation</strong></summary>

- **Messenger webhook to AI pipeline**  
  Incoming Meta events are signature-verified, deduplicated, rate-limited, queued with `pg-boss`, and processed asynchronously so Messenger delivery constraints are respected.

- **Guarded AI orchestration**  
  The runtime includes input sanitization, prompt-injection checks, FAQ bypass logic, structured prompt building, function-firewall validation, output filtering, and fallbacks before a reply is sent.

- **Order-state-aware replies**  
  Aura-Sync tracks the conversation through product selection, quantity confirmation, cart completion, form collection, and order confirmation so the bot follows the actual sales flow instead of improvising.

- **Custom replies, greeting logic, and knowledge-driven answers**  
  The platform supports greeting detection, trigger-based replies, business-specific FAQs, products, policies, and chatbot behavior rules configurable from the dashboard.

- **FAQ retrieval pipeline with hybrid matching**  
  The current system includes lexical matching, semantic embeddings, FAQ confidence handling, and FAQ health/training workflows rather than only blind LLM prompting.

</details>

<details>
<summary><strong>Sales, Orders & Fulfillment</strong></summary>

- **Pending order workflow**  
  Orders captured from chat can be reviewed, approved, rejected, and communicated back to the customer through Messenger.

- **Order management workspace**  
  Teams can create, update, filter, inspect, and print order labels from the dashboard instead of relying on spreadsheets.

- **Cancellation and confirmation safeguards**  
  The platform contains explicit order confirmation and cancel-intent handling to reduce accidental or hallucinated actions.

- **Shipment lifecycle integration**  
  AfterShip webhooks update shipment state, prevent duplicate processing, and queue delivery alerts for customers.

- **Proactive logistics messaging**  
  Delivery alerts and stuck-shipment checks are scheduled jobs in the server, not just planned ideas.

</details>

<details>
<summary><strong>CRM Intelligence</strong></summary>

- **Conversation analysis on resolution**  
  Resolved conversations are analyzed into summary, tags, sentiment, lead score, and follow-up signals, then written back into customer and conversation intelligence fields.

- **Live sentiment monitoring**  
  The system can run lightweight sentiment analysis during active conversations, not only after they end.

- **Escalation context for agents**  
  When a case needs a human, Aura-Sync can assemble customer, order, shipment, summary, sentiment, and suggested actions into a context card.

- **Follow-up detection and lead scoring**  
  Scheduled jobs flag conversations that have gone stale and rescore active pipelines over time.

- **Training Hub + FAQ Health**  
  The dashboard includes dedicated surfaces for identifying knowledge gaps and FAQ performance quality.

</details>

<details>
<summary><strong>Team Operations</strong></summary>

- **Conversation assignment**  
  Aura-Sync includes agent workload views and assignment configuration, including smart-routing support.

- **Approvals for sensitive actions**  
  Higher-risk AI actions can be routed into a human approval queue with expiry handling and notifications.

- **Notes, tags, notifications, and reusable responses**  
  Teams can work from shared operational context instead of fragmented chat history.

- **RBAC and multi-user collaboration**  
  Owners, admins, agents, and super admins operate with scoped permissions across tenant workspaces.

</details>

<details>
<summary><strong>Growth & SaaS Operations</strong></summary>

- **Campaign manager**  
  The current product includes campaign creation, scheduling, audience preview, and send execution workers.

- **Billing, subscriptions, and AI credits**  
  Tenants have subscription state, AI credit balance, usage visibility, daily limits, and alert thresholds.

- **PHP wallet system**  
  The platform supports wallet balances and wallet-to-credit purchases with atomic transaction logic and idempotency protection.

- **Super-admin controls**  
  Admin pages cover tenant management, subscription activation, wallet top-ups, audit logs, and AI call visibility.

</details>

---

## How It Works

```text
Customer message on Messenger
        |
        v
Meta webhook verification + replay protection
        |
        v
Queued processing via pg-boss workers
        |
        v
Aura-Sync loads tenant rules, customer history, order state, FAQs, and logistics context
        |
        v
AI decides whether to reply, update state, queue approval, escalate, or trigger operations
        |
        +--> Messenger response to customer
        |
        +--> Realtime dashboard update for the team
        |
        +--> Follow-up jobs, analytics, CRM scoring, logistics alerts, billing usage
```

---

## Architecture Overview

```text
 [ Facebook Messenger ]
           |
           v
 [ Meta Webhook + HMAC Verification ]
           |
           v
 [ Fastify API ]
           |
           v
 [ pg-boss Queue + Scheduled Workers ]
           |
   +-------+-------------+------------------+------------------+
   |                     |                  |                  |
   v                     v                  v                  v
 [ AI Pipeline ]   [ Supabase Postgres ] [ AfterShip ]   [ Meta Send API ]
   |                     |                  |                  |
   +---------------------+------------------+------------------+
                         |
                         v
              [ React Dashboard + Supabase Realtime ]
```

---

## Dashboard Surface

Aura-Sync already exposes a broad operating surface in the dashboard, including:

- **Analytics**
- **Conversations**
- **Customers**
- **Orders**
- **Pending Orders**
- **Approvals**
- **Tags**
- **Campaigns**
- **Chatbot**
- **Billing**
- **Settings**
- **Team**
- **Assignment**
- **Logistics**
- **Training Hub**
- **FAQ Health**
- **Super Admin: Overview, Tenants, Audit Logs, AI Calls**

---

## Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| Backend | Fastify + TypeScript | APIs, webhook processing, middleware, orchestration |
| Frontend | React 19 + Vite + Tailwind CSS 4 | Real-time dashboard UI |
| Database | Supabase PostgreSQL | Tenant data, auth, RLS, realtime |
| Queueing | pg-boss | Async jobs, retries, scheduled workers |
| AI | OpenAI + vLLM-compatible provider support | Replies, CRM analysis, assistant flows, safety checks |
| Validation | Zod | Structured response and payload validation |
| Auth | Supabase Auth + JOSE | Authentication and token verification |
| Messaging | Meta Messenger APIs | Inbound and outbound customer messaging |
| Logistics | AfterShip | Tracking registration, status updates, alert triggers |
| Charts | Recharts + Nivo | Analytics visualization |
| Deployment | Docker + Google Cloud tooling | App and model deployment paths |

---

## Philippine Market Focus

Aura-Sync is designed for how many Philippine SMEs actually operate online.

- **Messenger-first commerce** instead of email-ticket assumptions
- **Taglish-friendly AI behavior** with Filipino defaults in the prompt layer
- **Courier-aware fulfillment support** through AfterShip for PH-relevant logistics flows
- **PHP-based billing mechanics** with wallet and AI credit handling
- **Privacy-conscious product design** aligned with Philippine data handling expectations

For local sellers running support and fulfillment through Facebook pages, this matters more than adding another generic chatbot to the stack. The product is opinionated around the channel that already has the customer relationship.

---

## Strategic Positioning

Aura-Sync sits at the intersection of three categories:

- **AI customer service**
- **Social commerce operations**
- **SMB vertical SaaS for the Philippines**

That combination matters. Global chatbot tools usually stop at conversation automation. Traditional CRMs rarely feel native to Messenger selling. Local service businesses often deliver custom setups rather than scalable software. Aura-Sync is positioned to bridge that gap with a productized, multi-tenant platform.

---

## Security & Governance

Aura-Sync is designed to automate business operations without treating security as an afterthought. The current platform already includes multiple layers of operational control across messaging, AI execution, tenant isolation, and billing flows.

- **Tenant isolation by design**  
  Tenant-scoped data is protected with restrictive row-level security so the platform boundary is enforced at the database layer, not only in application code.

- **Guarded AI execution**  
  AI actions sit behind input sanitization, injection screening, function-call validation, output filtering, and approval workflows for higher-risk operations.

- **Verified event ingestion**  
  Meta and AfterShip callbacks are protected with signature verification, replay resistance, deduplication, and rate-limited public endpoints.

- **Operational auditability**  
  Sensitive business actions are written to audit logs, giving owners and platform operators a review trail across administrative and financial flows.

- **Payments and ledger safety**  
  Wallet and AI credit flows use append-only ledgers, idempotent transaction patterns, and atomic balance updates to reduce inconsistency and double-processing risk.

- **Production hardening at the edge**  
  The platform includes route-level rate limits, CORS controls, security headers, and encrypted tenant secrets for stored credentials.

This repository is intentionally a showcase. Internal security implementation details are summarized rather than fully disclosed.

---

## Screenshots / Demo

![Dashboard - Analytics Overview](screenshots/dashboard-overview.png)
![Dashboard - Conversations Workspace](screenshots/conversations-view.png)
![Dashboard - Orders and Fulfillment](screenshots/order-management.png)
![Dashboard - Chatbot Configuration](screenshots/chatbot-settings.png)
![Dashboard - Billing and Credits](screenshots/billing.png)

> Replace these placeholders with real product screenshots or short GIF demos before publishing the public repository.

---

## Pricing

Aura-Sync already includes subscription, credits, and wallet infrastructure in the product. Public pricing can stay intentionally lightweight while early pilots and go-to-market packaging are being finalized.

| Plan | Status | Notes |
|---|---|---|
| Starter | Available for controlled rollout | Current billing layer supports subscription activation and AI credit usage |
| Growth | Coming Soon | Best for larger support and sales teams |
| Business | Coming Soon | Best for high-volume operations and advanced workflows |
| Enterprise | By inquiry | For custom deployment, partnerships, and multi-brand setups |

**Interested in pilot access?** Contact us for a demo.

---

## Roadmap

- [ ] MFA for tenant admins and stronger account-security defaults
- [ ] Customer-facing consent flow during first interaction
- [ ] More polished logistics visualization inside the conversation workspace
- [ ] Expanded online payment options for wallet top-ups
- [ ] AI ghostwriter suggestions for human agents
- [ ] More onboarding guidance and readiness scoring for new tenants

---

## Request a Demo

If you run customer support, order intake, and fulfillment through Facebook Messenger, Aura-Sync is built for that exact workflow.

- **Demo requests:** `your-email@example.com`
- **Partnerships / investor conversations:** `your-email@example.com`
- **Website:** `https://your-domain.com`

---

## Notice

**Proprietary software.** This repository is a public showcase only. Production source code remains private.

Built in the Philippines for Messenger-first commerce teams.
