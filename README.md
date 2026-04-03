# Claude Skill Factory 🏭

> **Plug-in system prompts that turn Claude into a domain expert — not a better chatbot.**

By default, Claude is helpful but generic. These skills change that. Each one gives Claude a strict role, enforced output rules, and professional-grade logic. The difference isn’t subtle.

-----

## What is a Skill?

A `.skill` file is a structured system prompt. Paste it into Claude’s system prompt field and Claude instantly behaves like a specialist — it knows what to ask before acting, what to never skip, and how to format its output. No coding required.

-----

## How to Use a Skill

**Claude.ai (browser or app):**

1. Go to **Claude.ai → Projects → Create Project**
1. Open the `.skill` file with any text editor (Notepad, TextEdit, VS Code)
1. Copy the full contents and paste them into the **“Project Instructions”** field
1. Done — every conversation in that project now runs the skill

**Claude API:**

1. Open the `.skill` file and copy its contents
1. Paste as your `system` parameter in the API request
1. Done

> **Combining skills:** Copy multiple `.skill` files into the same system prompt and Claude runs all of them at once — see [Combining Skills](#combining-skills) below.

-----

## All Skills — 31 Total

Skills are grouped by domain. Click any skill name to view the file.

-----

### 🧑‍💻 Software Engineering

|Skill                                               |One-liner                                                                                 |
|----------------------------------------------------|------------------------------------------------------------------------------------------|
|[Architecture-PRO](Architecture-pro.skill)          |System & cloud design — won’t suggest a stack without knowing budget, load, and team size |
|[Design-PRO](Design-pro.skill)                      |UI/UX for any framework — enforces a strict design system: colors, spacing, fonts, shadows|
|[Documentation-PRO](Documentation-pro.skill)        |Stops and asks before writing docs if anything in your code is ambiguous — no guessing    |
|[Performance-PRO](Performance-pro.skill)            |Meta-skill — cuts all filler from Claude’s responses, no warmup, no “great question”      |
|[Security-PRO](Security-pro.skill)                  |Code review in strict order: security holes first, then bugs, then performance, then style|
|[Tech-Debt-Manager-PRO](Tech-Debt-Manager-PRO.skill)|Identifies, prioritizes, and creates actionable plans for reducing technical debt         |
|[Prompt-Optimizer-PRO](Prompt-Optimizer-PRO.skill)  |Analyzes and rewrites prompts for maximum clarity, precision, and output quality          |
|[Knowledge-Graph-PRO](Knowledge-Graph-PRO.skill)    |Structures complex information into connected knowledge graphs and relationship maps      |

-----

### 🔐 Security & Compliance

|Skill                                                       |One-liner                                                                                     |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------|
|[API-Security-PRO](API-Security-PRO.skill)                  |Audits API designs and implementations for authentication flaws, injection risks, and exposure|
|[Vulnerability-Scanner-PRO](Vulnerability-Scanner-PRO.skill)|Scans code for known vulnerability patterns — reports severity, impact, and remediation       |
|[Threat-Intelligence-PRO](Threat-Intelligence-PRO.skill)    |Analyzes threat landscapes, attack vectors, and produces structured intelligence reports      |
|[Incident-Responder-PRO](Incident-Responder-PRO.skill)      |Structured incident response — containment, root cause analysis, and post-mortem output       |
|[GDPR-Audit-PRO](GDPR-Audit-PRO.skill)                      |Reviews systems, processes, and data flows against GDPR requirements — gaps and fixes         |
|[Regulatory-Watch-PRO](Regulatory-Watch-PRO.skill)          |Tracks regulatory requirements and flags compliance obligations relevant to your context      |
|[Risk-Manager-PRO](Risk-Manager-PRO.skill)                  |Identifies, scores, and prioritizes operational and business risks with mitigation plans      |

-----

### ⚙️ DevOps & Architecture

|Skill                                                     |One-liner                                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------|
|[DevOps-Strategist-PRO](DevOps-Strategist-PRO.skill)      |CI/CD pipeline design, infrastructure planning, and DevOps workflow optimization             |
|[Automation-Architect-PRO](Automation-Architect-PRO.skill)|Designs automation strategies across tools and workflows — identifies what to automate first |
|[Process-Miner-PRO](Process-Miner-PRO.skill)              |Maps and analyzes business processes to find bottlenecks, redundancies, and improvement areas|

-----

### 💼 Business & Operations

|Skill                                                 |One-liner                                                                                   |
|------------------------------------------------------|--------------------------------------------------------------------------------------------|
|[Decision-Support-PRO](Decision-Support-PRO.skill)    |Frames complex decisions with criteria, trade-offs, and a structured recommendation         |
|[Meeting-PRO](Meeting-pro.skill)                      |Extracts every decision, owner, and deadline from a transcript — asks you to fill any gaps  |
|[Content-Strategist-PRO](Content-Strategist-PRO.skill)|Builds content strategies with audience analysis, channel mix, and measurable goals         |
|[CRM-Optimizer-PRO](CRM-Optimizer-PRO.skill)          |Analyzes CRM data and workflows to improve pipeline management and customer retention       |
|[Lead-Qualifier-PRO](Lead-Qualifier-PRO.skill)        |Scores and qualifies leads using defined criteria — outputs ranked lists with reasoning     |
|[Supply-Chain-Risk-PRO](Supply-Chain-Risk-PRO.skill)  |Maps supply chain dependencies and identifies single points of failure and risk exposure    |
|[Contract-Reviewer-PRO](Contract-Reviewer-PRO.skill)  |Reviews contracts for risk clauses, missing terms, and negotiation points — not legal advice|

-----

### 💰 Finance

|Skill                                                     |One-liner                                                                                 |
|----------------------------------------------------------|------------------------------------------------------------------------------------------|
|[Financial-Forecaster-PRO](Financial-Forecaster-PRO.skill)|Builds financial forecasts with scenario analysis — always states assumptions explicitly  |
|[Budget-Optimizer-PRO](Budget-Optimizer-PRO.skill)        |Analyzes budgets, finds inefficiencies, and proposes prioritized cost optimization actions|

-----

### 👥 HR & People

|Skill                                                   |One-liner                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
|[Talent-Scout-PRO](Talent-Scout-PRO.skill)              |Writes job specs, evaluates candidate profiles, and structures interview frameworks    |
|[Performance-Review-PRO](Performance-Review-PRO.skill)  |Structures and writes performance reviews — balanced, specific, and development-focused|
|[Employee-Engagement-PRO](Employee-Engagement-PRO.skill)|Designs engagement surveys, analyzes results, and produces actionable improvement plans|

-----

### 🎨 Design & UX

|Skill                                       |One-liner                                                                                  |
|--------------------------------------------|-------------------------------------------------------------------------------------------|
|[Design-PRO](Design-pro.skill)              |UI/UX for any framework — enforces Apple/Microsoft-level visual standards every time       |
|[UX-Researcher-PRO](UX-Researcher-PRO.skill)|Plans user research, designs interview guides, and synthesizes findings into clear insights|

-----

## Skill Details

### Architecture-PRO

> *“Never suggest a tech stack without knowing budget, load, and team size.”*

Claude becomes a Lead Cloud Architect. It won’t touch a technology recommendation until it has three things from you: monthly infrastructure budget, expected traffic/user load, and team size. Once it has those, it gives a full analysis — trade-offs, costs, risks, and the reasoning behind every choice.

-----

### Design-PRO

> *“Clean, modern, consistent — every time, any framework.”*

Claude enforces a strict design system whenever it builds a UI — doesn’t matter if it’s React, plain HTML, Flutter, or anything else. The rules are fixed: max 2–3 colors, 4px spacing grid, specific border radii, one shadow layer max, defined font stack.

-----

### Documentation-PRO

> *“If the code is ambiguous, stop and ask — don’t guess and document.”*

Before writing a single line of documentation, Claude analyzes your code for ambiguous variable names, unexplained magic values, unclear side effects, and undocumented dependencies. If it finds any, it asks you to clarify first. Output language follows your input — write in German, get German docs.

-----

### Meeting-PRO

> *“Every task needs an owner and a deadline. No exceptions.”*

Paste in a meeting transcript (any language, any format) and Claude extracts all decisions, action items with owners and deadlines, open questions, and blockers. If any task is missing an owner or deadline, it generates targeted follow-up questions — it never silently skips incomplete items.

-----

### Performance-PRO

> *“No warmup. No ‘great question’. No ‘I hope this helps’. Just the answer.”*

This meta-skill changes *how* Claude responds, not what it knows. It eliminates intro sentences, problem restatements, closing pleasantries, and hedge phrases. Decision rule: if the task is clear, execute immediately; if one critical thing is missing, ask exactly that one thing.

> Works with any other skill — stack it on top of any combination.

-----

### Security-PRO

> *“No ‘good approach, but…’ — show the vulnerabilities first.”*

Claude reviews code as a Senior Staff Engineer and Cybersecurity Expert. The review always follows the same priority order:

1. 🛑 **Security** — SQL injection, XSS, CSRF, hardcoded secrets, missing auth checks
1. ⚠️ **Logic bugs** — race conditions, off-by-one errors, unhandled edge cases
1. 💡 **Performance** — N+1 queries, O(n²) loops, blocking I/O in async code
1. 🧹 **Clean code** — duplicate code, SOLID violations, magic numbers, excessive nesting

All four sections always appear — even if a section is empty, it’s listed as clean.

-----

### API-Security-PRO

> *“Authentication, authorization, and exposure — audited in that order.”*

Claude audits REST and GraphQL API designs and implementations for security vulnerabilities. Checks authentication mechanisms, authorization logic, rate limiting, input validation, data exposure, and OWASP API Top 10 issues. Outputs a prioritized findings report with fix guidance.

-----

### GDPR-Audit-PRO

> *“Data flows first, compliance gaps second, remediation third.”*

Claude maps data flows and processing activities against GDPR requirements. Identifies gaps in consent management, data subject rights, retention policies, third-party data sharing, and DPA agreements. Output is a structured audit report with risk ratings.

-----

### Financial-Forecaster-PRO

> *“Every forecast states its assumptions. Every scenario has a name.”*

Claude builds financial forecasts with explicit assumption documentation — no silent inputs. Always produces three scenarios (conservative, base, optimistic) with labeled drivers for each. Never presents a single-point forecast as fact.

-----

### Decision-Support-PRO

> *“Define the decision, list the criteria, score the options, recommend one.”*

Claude frames complex decisions using a structured framework: decision statement, success criteria, options, scoring matrix, and a single clear recommendation with reasoning. Never outputs a pros/cons list without a final recommendation.

-----

### Process-Miner-PRO

> *“Map the current process before designing the future one.”*

Claude analyzes business processes by mapping current-state workflows, identifying bottlenecks, redundant steps, and handoff failures before making any recommendations. Output includes a process map, waste analysis, and prioritized improvement backlog.

-----

## Combining Skills

Copy multiple `.skill` files into the same system prompt — Claude runs all of them simultaneously:

```
Architecture-PRO + Performance-PRO       →  fast, no-filler architecture decisions
Security-PRO + Documentation-PRO         →  secure code with complete audit trail
Design-PRO + Performance-PRO             →  clean UI output, zero padding
Meeting-PRO + Performance-PRO            →  tight meeting summaries, no fluff
GDPR-Audit-PRO + Risk-Manager-PRO        →  compliance risk with business impact scoring
Vulnerability-Scanner-PRO + API-Security →  full-stack security review in one pass
```

-----

## Repository Structure

```
Claude-Skill-Factory/
├── API-Security-PRO.skill
├── Architecture-pro.skill
├── Automation-Architect-PRO.skill
├── Budget-Optimizer-PRO.skill
├── CRM-Optimizer-PRO.skill
├── Content-Strategist-PRO.skill
├── Contract-Reviewer-PRO.skill
├── Decision-Support-PRO.skill
├── Design-pro.skill
├── DevOps-Strategist-PRO.skill
├── Documentation-pro.skill
├── Employee-Engagement-PRO.skill
├── Financial-Forecaster-PRO.skill
├── GDPR-Audit-PRO.skill
├── Incident-Responder-PRO.skill
├── Knowledge-Graph-PRO.skill
├── Lead-Qualifier-PRO.skill
├── Meeting-pro.skill
├── Performance-Review-PRO.skill
├── Performance-pro.skill
├── Process-Miner-PRO.skill
├── Prompt-Optimizer-PRO.skill
├── Regulatory-Watch-PRO.skill
├── Risk-Manager-PRO.skill
├── Security-pro.skill
├── Supply-Chain-Risk-PRO.skill
├── Talent-Scout-PRO.skill
├── Tech-Debt-Manager-PRO.skill
├── Threat-Intelligence-PRO.skill
├── UX-Researcher-PRO.skill
└── Vulnerability-Scanner-PRO.skill
```

-----

## Roadmap

- `Analytics-PRO` — data analysis and chart generation with explicit methodology
- `API-Designer-PRO` — REST/GraphQL design with OpenAPI spec output
- `Refactor-PRO` — opinionated, aggressive code refactoring with justification
- `Startup-PRO` — product strategy and GTM planning
- `Legal-Brief-PRO` — legal document summarization and clause extraction

-----

## License

MIT — free to use, modify, and distribute. Attribution appreciated.