# Claude-Skill-Factory

> **Plug-in system prompts that turn Claude into a domain expert — not a better chatbot.**

By default, Claude is helpful but generic. These skills change that. Each one gives Claude a strict role, enforced rules, and professional-grade output logic. The difference isn't subtle.

---

## The idea in one sentence

You paste a skill into Claude's system prompt, and Claude stops acting like an assistant that tries to please — and starts acting like a specialist that knows exactly what to ask, what to never skip, and how to structure its output.

---

## How to use a skill

> No coding required. Takes about 60 seconds.

**If you use Claude.ai (browser/app):**

1. Open **Claude.ai → Projects → Create Project**
2. Download the `.skill` file from this repo and open it with any text editor (Notepad, TextEdit, etc.)
3. Copy the entire file contents
4. Paste it into the **"Project Instructions"** field in Claude
5. Done. Every conversation in that project now runs the skill.

**If you use the Claude API:**

1. Download the `.skill` file
2. Copy its contents
3. Paste it as your `system` prompt parameter
4. Done.

---

## Available Skills (30)

### 🛠️ Engineering & Architecture

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Architecture-PRO](#architecture-pro) | System & cloud design | Won't recommend a single technology until it knows your budget, team size, and expected traffic |
| [API-Security-PRO](#api-security-pro) | API security auditing | Scans every endpoint for auth flaws, injection risks, and broken access control — before anything else |
| [Automation-Architect-PRO](#automation-architect-pro) | Workflow & process automation | Maps your current process before designing automation — never automates a broken workflow |
| [DevOps-Strategist-PRO](#devops-strategist-pro) | CI/CD and infrastructure strategy | Enforces a deploy-safety-first mindset — rollback plans required before any pipeline recommendation |
| [Tech-Debt-Manager-PRO](#tech-debt-manager-pro) | Technical debt analysis | Quantifies debt by business impact, not just code smell — prioritizes what costs you money |
| [Vulnerability-Scanner-PRO](#vulnerability-scanner-pro) | Code vulnerability detection | Fixed scan order: injection → broken auth → sensitive data → misconfig → known CVEs |
| [Threat-Intelligence-PRO](#threat-intelligence-pro) | Cybersecurity threat analysis | Maps threats to your specific stack and threat model — no generic advisories |
| [Incident-Responder-PRO](#incident-responder-pro) | Security incident response | Follows a strict triage sequence — contain first, investigate second, report third |
| [Performance-PRO](#performance-pro) | Claude's output quality | Cuts all filler from responses — no intros, no "I hope this helps", just the answer |

### 🎨 Design & UX

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Design-PRO](#design-pro) | UI/UX across any framework | Enforces Apple/Microsoft-level visual standards — colors, spacing, fonts, shadows, all defined |
| [UX-Researcher-PRO](#ux-researcher-pro) | User research & testing | Designs research around your actual user questions — won't generate personas without real data |

### 📝 Documentation & Communication

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Documentation-PRO](#documentation-pro) | Code & API documentation | Stops and asks before writing docs if anything in your code is ambiguous — no assumptions |
| [Content-Strategist-PRO](#content-strategist-pro) | Content planning & strategy | Ties every content piece to a measurable business goal — no content for content's sake |
| [Knowledge-Graph-PRO](#knowledge-graph-pro) | Knowledge structuring & mapping | Builds explicit entity-relationship maps before any knowledge base work starts |

### 💼 Business & Operations

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Meeting-PRO](#meeting-pro) | Meeting transcripts | Pulls out every decision, task, owner, and deadline — asks you to fill in anything missing |
| [Budget-Optimizer-PRO](#budget-optimizer-pro) | Budget planning & optimization | Never suggests cuts without modeling the downstream impact on revenue or operations |
| [CRM-Optimizer-PRO](#crm-optimizer-pro) | CRM strategy & process | Audits your pipeline hygiene before recommending any CRM changes |
| [Decision-Support-PRO](#decision-support-pro) | Structured decision-making | Forces explicit criteria and trade-off weighting before any recommendation is made |
| [Financial-Forecaster-PRO](#financial-forecaster-pro) | Financial modeling & forecasting | Surfaces assumptions explicitly — every forecast shows what it's sensitive to |
| [Lead-Qualifier-PRO](#lead-qualifier-pro) | Sales lead qualification | Applies a consistent scoring framework — removes gut-feel from pipeline prioritization |
| [Process-Miner-PRO](#process-miner-pro) | Business process analysis | Maps the actual process first, then identifies the real bottlenecks — not the assumed ones |
| [Supply-Chain-Risk-PRO](#supply-chain-risk-pro) | Supply chain risk management | Categorizes risks by probability and impact before any mitigation plan is proposed |

### 👥 People & HR

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Employee-Engagement-PRO](#employee-engagement-pro) | Employee engagement strategy | Diagnoses disengagement root causes before recommending any initiative |
| [Performance-Review-PRO](#performance-review-pro) | Performance review writing | Structures feedback around observable behaviors, not personality traits |
| [Talent-Scout-PRO](#talent-scout-pro) | Recruiting & talent acquisition | Builds role-specific evaluation criteria before sourcing — no generic job descriptions |

### ⚖️ Legal & Compliance

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Contract-Reviewer-PRO](#contract-reviewer-pro) | Contract analysis & review | Flags missing clauses and unfavorable terms — always in plain language, never legal jargon |
| [GDPR-Audit-PRO](#gdpr-audit-pro) | GDPR & data privacy auditing | Checks every data flow against GDPR requirements — no compliance assumptions |
| [Regulatory-Watch-PRO](#regulatory-watch-pro) | Regulatory change monitoring | Maps regulatory changes directly to your business processes — no generic compliance alerts |
| [Risk-Manager-PRO](#risk-manager-pro) | Enterprise risk management | Scores risks on a consistent 5×5 matrix — likelihood × impact, every time |

### 🔧 Prompt Engineering

| Skill | What it's for | Core behavior |
| --- | --- | --- |
| [Prompt-Optimizer-PRO](#prompt-optimizer-pro) | System prompt optimization | Rewrites prompts to be explicit, testable, and free of ambiguity — shows the before/after diff |
| [Security-PRO](#security-pro) | Code security review | Reviews code in strict order: security holes first, then bugs, then performance, then style |

---

## Skill Details

### Architecture-PRO

> *"Never suggest a tech stack without knowing budget, load, and team size."*

Claude becomes a Lead Cloud Architect. It won't touch a technology recommendation until it has three things from you: your monthly infrastructure budget, your expected traffic/user load, and how many engineers are on the team. Once it has those, it gives you a full analysis — trade-offs, costs, risks, and the reasoning behind every choice.

---

### API-Security-PRO

> *"An API is only as secure as its most exposed endpoint."*

Claude acts as an API Security Specialist. It audits every endpoint systematically: authentication mechanisms, authorization checks, input validation, rate limiting, and data exposure. It won't give you a general "looks fine" — it gives you a prioritized list of findings with severity levels and fix recommendations.

---

### Automation-Architect-PRO

> *"Never automate a broken process. Fix it first."*

Claude becomes an Automation Architect. Before designing any workflow automation, it maps your current process step-by-step and identifies manual bottlenecks, error-prone handoffs, and unnecessary steps. Only after the process is understood does it propose an automation design — with tool recommendations, failure handling, and maintenance considerations.

---

### Budget-Optimizer-PRO

> *"Every cut has a downstream cost. Show it."*

Claude acts as a Financial Operations Analyst. It never suggests a budget reduction without modeling its downstream effect on revenue, headcount, or service quality. Every recommendation comes with a sensitivity analysis — what happens if assumptions are wrong.

---

### CRM-Optimizer-PRO

> *"A CRM is only as useful as the data inside it."*

Claude becomes a CRM Strategy Consultant. Before recommending any process change or tool feature, it audits your pipeline data quality, stage conversion rates, and field usage. It fixes the foundation before building on top of it.

---

### Content-Strategist-PRO

> *"Content without a measurable goal is just noise."*

Claude acts as a Senior Content Strategist. Every content piece is tied to a specific business objective, target audience segment, and success metric. It won't plan a content calendar without knowing what you're trying to move — traffic, leads, retention, or brand.

---

### Contract-Reviewer-PRO

> *"Spot what's missing, not just what's wrong."*

Claude becomes a Contract Review Specialist. It reads contracts looking for missing standard clauses, unbalanced terms, ambiguous language, and hidden liability. Every finding is explained in plain English — no legal jargon. It tells you what to negotiate, not just what's risky.

---

### Decision-Support-PRO

> *"A decision without explicit criteria isn't a decision — it's a guess."*

Claude acts as a Decision Intelligence Analyst. Before any recommendation, it forces explicit definition of decision criteria, constraints, and stakeholder priorities. It then scores each option against those criteria transparently — so you can see exactly why one option scores higher than another.

---

### Design-PRO

> *"Clean, modern, consistent — every time, any framework."*

Claude enforces a strict design system whenever it builds a UI — React, plain HTML, Flutter, ImGui, WPF, or anything else. The rules are fixed: max 2–3 colors, 4px spacing grid, specific border radii, one shadow layer max, defined font stack. Without this skill, Claude produces visually inconsistent UIs every time. With it, you get the same quality standard across every component it touches.

---

### DevOps-Strategist-PRO

> *"No deployment without a rollback plan."*

Claude becomes a Senior DevOps Engineer. It designs CI/CD pipelines with rollback plans, blast-radius minimization, and observability built in from the start. It won't recommend a deployment strategy that doesn't answer: "What happens when this fails?"

---

### Documentation-PRO

> *"If the code is ambiguous, stop and ask — don't guess and document."*

Claude acts as a Senior Technical Writer. Before writing a single line of documentation, it analyzes your code for ambiguous variable names, unexplained magic values, unclear side effects, and undocumented dependencies. If it finds any, it asks you to clarify before proceeding. Output language follows your input — write in German, get German docs.

---

### Employee-Engagement-PRO

> *"You can't fix disengagement without knowing what's causing it."*

Claude becomes an HR Strategy Consultant. It diagnoses engagement issues by category — manager relationships, role clarity, growth paths, compensation fairness, or workload — before recommending any initiative. No generic "wellness programs" without a root cause first.

---

### Financial-Forecaster-PRO

> *"Every forecast is only as good as its assumptions. Show them."*

Claude acts as a Financial Analyst. Every model it builds makes its assumptions explicit and visible. It shows what the forecast is most sensitive to — and what would have to be true for the numbers to be wrong.

---

### GDPR-Audit-PRO

> *"Data compliance isn't a checkbox — it's a data flow."*

Claude becomes a GDPR Compliance Auditor. It traces every data flow through your system against GDPR requirements: lawful basis, consent mechanisms, data minimization, retention policies, third-party processors, and breach notification readiness. No assumptions — every gap is documented.

---

### Incident-Responder-PRO

> *"Contain first. Investigate second. Report third."*

Claude acts as a Security Incident Response Lead. It follows a strict sequence: immediate containment actions, blast radius assessment, root cause investigation, and post-incident report. It won't jump to root cause before containment is confirmed.

---

### Knowledge-Graph-PRO

> *"Before building a knowledge base, map what you actually know."*

Claude becomes a Knowledge Engineer. It builds explicit entity-relationship maps before structuring any knowledge base or documentation system. It surfaces gaps, duplicates, and undocumented dependencies in your existing knowledge before adding more.

---

### Lead-Qualifier-PRO

> *"Gut feel isn't a qualification framework."*

Claude acts as a Sales Intelligence Analyst. It applies a consistent scoring framework (fit, intent, timing, authority, budget) to every lead — removing subjective prioritization from your pipeline. Every score is explained with evidence, not instinct.

---

### Meeting-PRO

> *"Every task needs an owner and a deadline. No exceptions."*

Paste in a meeting transcript and Claude extracts everything that matters: decisions made, action items with owners and deadlines, open questions, and blockers. If any task is missing an owner or a deadline, it generates targeted follow-up questions before giving you the final output — it never silently skips incomplete items.

---

### Performance-PRO

> *"No warmup. No 'great question'. No 'I hope this helps'. Just the answer."*

This is a meta-skill — it changes *how* Claude responds, not what it knows. It eliminates intro sentences, problem restatements, closing pleasantries, and hedge phrases. Works with any other skill — stack it on top of Architecture-PRO, Design-PRO, or any combination.

---

### Performance-Review-PRO

> *"Feedback on behaviors, not personality."*

Claude becomes an HR Writing Specialist. It structures every performance review around specific, observable behaviors tied to role expectations — not vague traits like "attitude" or "team player." Output is fair, defensible, and actionable.

---

### Process-Miner-PRO

> *"Map the real process — not the documented one."*

Claude acts as a Business Process Analyst. It maps your actual workflow (including the undocumented workarounds and exception paths) before identifying bottlenecks. The documented process and the real process are often different — this skill finds the difference.

---

### Prompt-Optimizer-PRO

> *"A vague prompt produces a vague answer. Make the contract explicit."*

Claude becomes a Prompt Engineering Specialist. It rewrites your system prompts to be unambiguous, testable, and free of contradictions. Every rewrite comes with a before/after comparison and an explanation of what each change fixes.

---

### Regulatory-Watch-PRO

> *"A regulation only matters if it changes something you actually do."*

Claude acts as a Regulatory Intelligence Analyst. It maps regulatory changes directly to your specific business processes, data practices, and risk exposures — no generic compliance summaries. Every alert is tied to a concrete operational impact.

---

### Risk-Manager-PRO

> *"Every risk gets the same matrix. No exceptions."*

Claude becomes an Enterprise Risk Manager. It scores every risk on a consistent 5×5 likelihood × impact matrix, categorizes risks by type (operational, financial, legal, reputational, technical), and produces a prioritized risk register with mitigation owners.

---

### Security-PRO

> *"No 'good approach, but...' — show the vulnerabilities first."*

Claude reviews your code as a Senior Staff Engineer and Cybersecurity Expert. The review always follows the same priority order: 🛑 Security → ⚠️ Logic bugs → 💡 Performance → 🧹 Clean code. All four sections always appear — even if a section is clean, it's listed as such. Works with any language.

---

### Supply-Chain-Risk-PRO

> *"Risk you haven't mapped is risk you can't manage."*

Claude acts as a Supply Chain Risk Analyst. It categorizes every risk by probability and impact before proposing any mitigation. It covers supplier concentration, geographic exposure, lead time variance, and single points of failure — systematically, not anecdotally.

---

### Talent-Scout-PRO

> *"A job description without evaluation criteria isn't a job description — it's a wish list."*

Claude becomes a Talent Acquisition Strategist. It builds role-specific, measurable evaluation criteria before sourcing begins. Every job description it writes includes what "good" looks like at 30, 60, and 90 days — not just requirements.

---

### Tech-Debt-Manager-PRO

> *"Technical debt is a business problem, not just a code problem."*

Claude acts as a Senior Engineering Lead. It quantifies technical debt in terms of business impact: deployment speed, incident frequency, onboarding time, and feature velocity. It prioritizes what to fix based on what costs you money — not just what's messy.

---

### Threat-Intelligence-PRO

> *"Generic threat advisories are noise. Map threats to your actual stack."*

Claude becomes a Threat Intelligence Analyst. It maps every identified threat to your specific technology stack, architecture, and threat model. No generic CVE summaries — every finding is contextualized to what matters for your environment.

---

### UX-Researcher-PRO

> *"No personas without real user data."*

Claude acts as a Senior UX Researcher. It designs research plans around your actual user questions and business decisions — not template personas. It specifies methodology (interviews, usability testing, surveys, analytics review) based on what kind of evidence you actually need.

---

### Vulnerability-Scanner-PRO

> *"Scan in order. Every time."*

Claude becomes a Security Engineer. It follows a fixed scanning sequence: injection vulnerabilities → broken authentication → sensitive data exposure → security misconfiguration → known CVEs. Nothing is skipped, and findings are ranked by exploitability and business impact.

---

## Combining Skills

Skills are composable — paste multiple skill files into the same system prompt and Claude runs all of them simultaneously:

```
Architecture-PRO + Performance-PRO        →  fast, no-fluff architecture decisions
Documentation-PRO + Security-PRO          →  secure code with complete docs
Design-PRO + Performance-PRO              →  clean UI output, zero padding
Risk-Manager-PRO + Supply-Chain-Risk-PRO  →  full enterprise risk coverage
GDPR-Audit-PRO + Contract-Reviewer-PRO   →  end-to-end compliance review
Threat-Intelligence-PRO + Incident-Responder-PRO  →  detect and respond, in order
```

---

## Roadmap

- `Analytics-PRO` — data analysis and chart generation
- `Refactor-PRO` — opinionated, aggressive code refactoring
- `Startup-PRO` — product strategy and GTM planning
- `Data-Pipeline-PRO` — ETL design and data quality enforcement

---

## License

MIT — free to use, modify, and distribute. Attribution appreciated.
