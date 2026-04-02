# Claude-Skill-Factory

**High-precision system prompts that transform Claude from a general chatbot into a domain expert.**

Each skill is a drop-in `.skill` file — load it into your Claude setup and get specialized, professional-grade behavior instantly. No vague responses. No unnecessary padding. Just expert execution.

---

## What is a Skill?

A `.skill` file is a structured prompt package that gives Claude a specialized persona, strict operating rules, and domain-specific logic. Unlike generic system prompts, these skills enforce behavior — they define what Claude asks, what it never skips, and how it structures output.

### How to use

1. Download the `.skill` file
2. Extract it — each skill contains a `SKILL.md` and optional `references/` folder
3. Copy the contents of `SKILL.md` into your Claude system prompt (API, Claude.ai Projects, or any compatible interface)
4. That's it — Claude now operates as the specified expert

---

## Available Skills

| Skill | Domain | What it does |
|-------|--------|--------------|
| [Architecture-PRO](#architecture-pro) | Cloud & System Design | Forces budget/load/team collection before any tech recommendation |
| [Design-PRO](#design-pro) | UI/UX Design | Enforces Apple/Microsoft-level design quality across any framework |
| [Documentation-PRO](#documentation-pro) | Technical Writing | Generates enterprise-grade docs with mandatory ambiguity resolution |
| [Meeting-PRO](#meeting-pro) | Meeting Intelligence | Extracts tasks, owners, and deadlines — never lets gaps slip through |
| [Performance-PRO](#performance-pro) | Efficiency & Focus | Eliminates filler, maximizes signal, enforces direct execution |
| [Security-PRO (Code Review)](#security-pro) | Cybersecurity & Code Quality | Brutal, structured review: security → bugs → performance → clean code |

---

## Skill Details

### Architecture-PRO
> *"Never suggest a tech stack without knowing budget, load, and team size."*

Claude acts as a **Lead Cloud Architect** across AWS, GCP, Azure, on-prem, and hybrid setups.

**Enforced behavior:**
- Refuses to recommend any stack until it collects: monthly budget, expected user load, and team size
- Internally scores every option on scalability, cost, complexity, resilience, and time-to-production
- Stack logic adapts automatically: `< $500/mo + ≤3 devs` → managed/serverless; `> $5k/mo` → full cloud-native
- Output includes trade-off analysis, migration risk, and cost projections

**Files:** `SKILL.md` + `references/patterns.md`, `cloud-providers.md`, `databases.md`

---

### Design-PRO
> *"Maximum 2–3 colors, 4px spacing grid, never eckig, never gradient-overload."*

Enforces **Apple/Microsoft quality philosophy** across any tech: HTML/CSS, React, ImGui, Flutter, Tkinter, WPF, Qt, or pure SVG.

**Enforced behavior:**
- Default palette: white/blue with `#2563EB` as brand primary — consistent across all outputs
- Spacing system: strict 4px grid (4, 8, 12, 16, 24, 32, 48px)
- Border radius: 8–12px containers, 4–6px buttons — enforced, not suggested
- Single shadow layer max: `box-shadow: 0 2px 8px rgba(0,0,0,0.08)`
- Font stack: Inter, SF Pro, or Segoe UI — no generic fallbacks

**Files:** `SKILL.md` + `references/color-tokens.md`, `component-patterns.md`

---

### Documentation-PRO
> *"If there's a magic value without a comment, stop and ask before writing a word."*

Claude acts as a **Senior Technical Writer + Software Architect** with enterprise-level output quality (React/Django/FastAPI bar).

**Enforced behavior:**
- Mandatory pre-doc analysis: traces data flow, identifies all exported symbols, flags ambiguities
- Clarification gate: stops and asks before documenting if any parameter is ambiguous (`data`, `tmp`, `val`, etc.) or side effects are unclear
- Output language follows user input — German in, German out; code identifiers stay as-is
- Covers: README, API reference, JSDoc/docstrings, inline comments, module docs

**Files:** `SKILL.md` + `references/doc-examples.md`

---

### Meeting-PRO
> *"Every task needs an owner and a deadline. No exceptions."*

Claude acts as an **Executive Assistant for C-Level leadership**, processing raw transcripts into structured intelligence.

**Enforced behavior:**
- Extracts: decisions, action items, open questions, risks/blockers, metadata
- Validates every task for owner + deadline — flags incomplete items before finalizing output
- Mandatory gap-filling: generates targeted questions for any missing owner or deadline
- Language-agnostic: German transcript → German output; French → French

**Files:** `SKILL.md`

---

### Performance-PRO
> *"No warmup sentences. No problem summaries. No 'I hope this helps'."*

A meta-skill that controls **how Claude works**, not what it knows. Enforces direct, high-signal execution on any task.

**Enforced behavior:**
- Instant task classification: Clear/Complete → execute now; Missing critical info → ask one question; Ambiguous core → one-line clarification; Complex → sketch structure first
- Eliminates: intro sentences, problem restatements, filler closings, double-explanations, hedge phrases
- For coding tasks specifically: always asks language + framework if missing, never guesses
- Works as a standalone skill or combined with any domain skill

**Files:** `SKILL.md` + `references/decision-patterns.md`

---

### Security-PRO (Code Review)
> *"No 'good approach, but...' — show the vulnerabilities directly."*

Claude acts as a **Senior Staff Software Engineer + Cybersecurity Expert**. Works across all languages, optimized for C#/.NET, JavaScript/TypeScript, and Python.

**Review priority order (always enforced):**
1. 🛑 **Security** — SQLi, XSS, CSRF, hardcoded secrets, auth bypasses, path traversal, SSRF
2. ⚠️ **Logic bugs** — race conditions, off-by-one, unhandled edge cases, exception swallowing
3. 💡 **Performance** — N+1 queries, O(n²) loops, blocking I/O in async, unnecessary allocations
4. 🧹 **Clean Code** — DRY violations, SOLID breaches, magic numbers, deep nesting

**Files:** `SKILL.md`

---

## Combining Skills

Skills are composable. Load multiple `SKILL.md` files into the same system prompt for compound behavior:

```
Architecture-PRO + Performance-PRO  →  fast, structured architecture decisions
Documentation-PRO + Security-PRO    →  secure, well-documented code reviews
Design-PRO + Performance-PRO        →  no-fluff UI implementation
```

---

## Roadmap

- [ ] `Analytics-PRO` — data analysis and visualization expert
- [ ] `API-PRO` — REST/GraphQL API design with OpenAPI output
- [ ] `Refactor-PRO` — aggressive, opinionated code refactoring
- [ ] `Startup-PRO` — product strategy and GTM advisor

---

## License

MIT — use freely, modify as needed, attribution appreciated.
