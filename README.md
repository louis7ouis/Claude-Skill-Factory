# Claude-Skill-Factory

> System prompts that turn Claude into a specialist — not a better chatbot.

By default, Claude tries to please. These skills make it perform.

Each skill gives Claude a strict role, enforced rules, and professional-grade output logic. The difference isn't subtle.

---

## The problem with default Claude

Ask Claude to review your code. It'll say *"Great approach! Here are a few suggestions..."* and bury the SQL injection vulnerability three paragraphs down.

Ask it for an architecture recommendation. It'll suggest Kubernetes — even if you're a solo dev with $50/month.

Ask it anything. It'll start with *"Certainly! I'd be happy to help..."*

Skills fix this.

---

## How it works

You paste a skill into Claude's system prompt. Claude stops acting like an assistant that tries to please — and starts acting like a specialist that knows exactly what to ask, what to never skip, and how to structure its output.

**No coding required. Takes about 60 seconds.**

### Claude.ai (browser / app)

1. Open **Claude.ai → Projects → Create Project**
2. Download the `.skill` file from this repo and open it with any text editor
3. Inside the zip, find `SKILL.md` — copy its entire contents
4. Paste into the **Project Instructions** field
5. Done. Every conversation in that project now runs the skill.

### Claude API

1. Download and extract the `.skill` file
2. Copy the contents of `SKILL.md`
3. Paste as your `system` prompt
4. Done.

---

## Before / After

**Default Claude — Code Review**

> "This looks great overall! A few things worth considering: you might want to add some error handling here, and the variable names could be a bit clearer. Great use of async/await by the way!"

**Security-PRO — Code Review**

> 🛑 **SECURITY** — Unsanitized user input passed directly to SQL query on line 34. SQL injection vector. Fix immediately.
>
> ⚠️ **LOGIC** — Race condition in the session handler. Two concurrent requests can both pass the auth check before either writes to the DB.
>
> 💡 **PERFORMANCE** — N+1 query in the user loop. Batch with a single JOIN.
>
> 🧹 **CLEAN CODE** — `data2` on line 12 is undescriptive. No other issues.

Same code. Completely different output.

---

## Available Skills

| Skill | What it does | Key rule |
|---|---|---|
| [Architecture-PRO](#architecture-pro) | System & cloud design | Won't recommend a single technology until it knows your budget, team size, and expected traffic |
| [Design-PRO](#design-pro) | UI/UX across any framework | Enforces Apple/Microsoft-level visual standards — colors, spacing, fonts, shadows, all defined |
| [Documentation-PRO](#documentation-pro) | Code & API documentation | Stops and asks before writing docs if anything is ambiguous — no assumptions |
| [Meeting-PRO](#meeting-pro) | Meeting transcripts | Pulls every decision, task, owner, and deadline — asks you to fill in anything missing |
| [Performance-PRO](#performance-pro) | Claude's output quality | Cuts all filler from responses — no intros, no "I hope this helps", just the answer |
| [Security-PRO](#security-pro) | Code review | Reviews in strict order: security first, then bugs, then performance, then style |
| [API-Security-PRO](#api-security-pro) | API security auditing | Checks auth, input validation, rate limiting, and exposure before anything else |
| [Automation-Architect-PRO](#automation-architect-pro) | Workflow automation | Maps dependencies and failure points before suggesting any tooling |
| [Budget-Optimizer-PRO](#budget-optimizer-pro) | Cost analysis | Won't optimize what it hasn't measured first |
| [Content-Strategist-PRO](#content-strategist-pro) | Content & growth strategy | Enforces niche + avatar definition before any content is planned |
| [Contract-Reviewer-PRO](#contract-reviewer-pro) | Contract analysis | Flags missing clauses and one-sided terms before summarizing |
| [CRM-Optimizer-PRO](#crm-optimizer-pro) | CRM workflow design | Audits data quality before recommending any process changes |
| [Decision-Support-PRO](#decision-support-pro) | Structured decisions | Forces explicit trade-off mapping before any recommendation |
| [DevOps-Strategist-PRO](#devops-strategist-pro) | CI/CD and infra | Won't design pipelines without knowing your current bottleneck |
| [Employee-Engagement-PRO](#employee-engagement-pro) | Team & HR strategy | Diagnoses root causes before suggesting any engagement program |
| [Financial-Forecaster-PRO](#financial-forecaster-pro) | Financial modeling | Requires actual data — refuses to model on assumptions |
| [GDPR-Audit-PRO](#gdpr-audit-pro) | GDPR compliance | Full data flow mapping before any compliance recommendation |
| [Incident-Responder-PRO](#incident-responder-pro) | Incident handling | Follows strict triage order — containment before root cause analysis |
| [Knowledge-Graph-PRO](#knowledge-graph-pro) | Knowledge structuring | Maps entity relationships before building any graph structure |
| [Lead-Qualifier-PRO](#lead-qualifier-pro) | Sales qualification | Applies a defined scoring framework — no gut-feel recommendations |
| [Performance-Review-PRO](#performance-review-pro) | Employee reviews | Separates observation from interpretation throughout |
| [Process-Miner-PRO](#process-miner-pro) | Process analysis | Documents the actual process before suggesting the ideal one |
| [Prompt-Optimizer-PRO](#prompt-optimizer-pro) | Prompt engineering | Analyzes failure modes before rewriting anything |
| [Regulatory-Watch-PRO](#regulatory-watch-pro) | Regulatory tracking | Scopes jurisdiction before any compliance analysis |
| [Risk-Manager-PRO](#risk-manager-pro) | Risk assessment | Quantifies likelihood and impact before prioritizing anything |
| [Supply-Chain-Risk-PRO](#supply-chain-risk-pro) | Supply chain analysis | Maps dependencies before assessing exposure |
| [Talent-Scout-PRO](#talent-scout-pro) | Recruiting strategy | Defines the role scorecard before sourcing begins |
| [Tech-Debt-Manager-PRO](#tech-debt-manager-pro) | Technical debt | Classifies debt by impact before recommending remediation |
| [Threat-Intelligence-PRO](#threat-intelligence-pro) | Threat analysis | Establishes threat actor profile before any mitigation plan |
| [UX-Researcher-PRO](#ux-researcher-pro) | UX research | Validates research questions before designing any study |
| [Vulnerability-Scanner-PRO](#vulnerability-scanner-pro) | Security scanning | Scans in severity order — critical and high before medium or low |

---

## Skill Details

### Architecture-PRO

> *"Never suggest a tech stack without knowing budget, load, and team size."*

Claude becomes a Lead Cloud Architect. It won't touch a technology recommendation until it has three things: your monthly infrastructure budget, your expected traffic, and your team size. Once it has those, it gives a full analysis — trade-offs, costs, risks, and the reasoning behind every choice.

Generic Claude suggests Kubernetes to a solo developer with $50/month. This skill won't.

---

### Design-PRO

> *"Clean, modern, consistent — every time, any framework."*

Claude enforces a strict design system whenever it builds a UI — React, plain HTML, Flutter, ImGui, WPF, or anything else. Fixed rules: max 2–3 colors, 4px spacing grid, specific border radii, one shadow layer max, defined font stack.

Without this skill, Claude produces visually inconsistent UIs that look different every time. With it, same quality standard across every component.

---

### Documentation-PRO

> *"If the code is ambiguous, stop and ask — don't guess and document."*

Before writing a single line of documentation, Claude analyzes your code for ambiguous variable names, unexplained magic values, unclear side effects, and undocumented dependencies. If it finds any, it asks you to clarify before proceeding.

Bad docs come from assumptions. This skill eliminates assumptions before writing starts.

---

### Meeting-PRO

> *"Every task needs an owner and a deadline. No exceptions."*

Paste in a meeting transcript — any language, any format — and Claude extracts every decision, action item with owner and deadline, open question, and blocker. If any task is missing an owner or deadline, it generates follow-up questions before giving you the final output.

---

### Performance-PRO

> *"No warmup. No 'great question'. No 'I hope this helps'. Just the answer."*

A meta-skill — changes how Claude responds, not what it knows. Eliminates intro sentences, problem restatements, closing pleasantries, and hedge phrases.

Works with any other skill. Stack it on top of Architecture-PRO, Security-PRO, or any combination.

---

### Security-PRO

> *"No 'good approach, but...' — show the vulnerabilities first."*

Claude reviews code as a Senior Staff Engineer and Cybersecurity Expert. Review order is fixed:

1. **Security** — SQL injection, XSS, CSRF, hardcoded secrets, missing auth checks, path traversal
2. **Logic bugs** — race conditions, off-by-one errors, unhandled edge cases
3. **Performance** — N+1 queries, O(n²) loops, blocking I/O
4. **Clean code** — duplicates, SOLID violations, magic numbers

All four sections always appear — even if a section is empty, it's listed as clean.

---

## Combining Skills

Skills are composable. Copy multiple `SKILL.md` files into the same system prompt and Claude runs all of them:

```
Architecture-PRO + Performance-PRO   →  fast, no-fluff architecture decisions
Documentation-PRO + Security-PRO     →  secure code with complete docs
Design-PRO + Performance-PRO         →  clean UI output, zero padding
```

---

## Roadmap

- `Analytics-PRO` — data analysis and chart generation
- `API-PRO` — REST/GraphQL design with OpenAPI spec output
- `Refactor-PRO` — opinionated, aggressive code refactoring
- `Startup-PRO` — product strategy and GTM planning

---

## License

MIT — free to use, modify, and distribute. Attribution appreciated.
