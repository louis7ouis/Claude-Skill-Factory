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
3. Inside the zip you'll find a file called `SKILL.md` — copy its entire contents
4. Paste it into the **"Project Instructions"** field in Claude
5. Done. Every conversation in that project now runs the skill.

**If you use the Claude API:**
1. Download and extract the `.skill` file
2. Copy the contents of `SKILL.md`
3. Paste it as your `system` prompt parameter
4. Done.

---

## Available Skills

| Skill | What it's for | Core behavior |
|-------|--------------|---------------|
| [Architecture-PRO](#architecture-pro) | System & cloud design | Won't recommend a single technology until it knows your budget, team size, and expected traffic |
| [Design-PRO](#design-pro) | UI/UX across any framework | Enforces Apple/Microsoft-level visual standards — colors, spacing, fonts, shadows, all defined |
| [Documentation-PRO](#documentation-pro) | Code & API documentation | Stops and asks before writing docs if anything in your code is ambiguous — no assumptions |
| [Meeting-PRO](#meeting-pro) | Meeting transcripts | Pulls out every decision, task, owner, and deadline — asks you to fill in anything missing |
| [Performance-PRO](#performance-pro) | Claude's output quality | Cuts all filler from responses — no intros, no "I hope this helps", just the answer |
| [Security-PRO](#security-pro) | Code review | Reviews code in strict order: security holes first, then bugs, then performance, then style |

---

## Skill Details

### Architecture-PRO
> *"Never suggest a tech stack without knowing budget, load, and team size."*

**What it does:** Claude becomes a Lead Cloud Architect. It won't touch a technology recommendation until it has three things from you: your monthly infrastructure budget, your expected traffic/user load, and how many engineers are on the team. Once it has those, it gives you a full analysis — trade-offs, costs, risks, and the reasoning behind every choice.

**Why that matters:** Generic Claude will happily suggest Kubernetes to a solo developer with $50/month. This skill won't. The output adapts to your actual situation.

**Includes:** Reference files for architecture patterns, cloud providers, and database selection.

---

### Design-PRO
> *"Clean, modern, consistent — every time, any framework."*

**What it does:** Claude enforces a strict design system whenever it builds a UI — doesn't matter if it's React, plain HTML, Flutter, ImGui, WPF, or anything else. The rules are fixed: max 2–3 colors, 4px spacing grid, specific border radii, one shadow layer max, defined font stack.

**Why that matters:** Without this skill, Claude produces visually inconsistent UIs that look different every time. With it, you get the same quality standard across every component it touches.

**Includes:** Color token reference and component pattern library.

---

### Documentation-PRO
> *"If the code is ambiguous, stop and ask — don't guess and document."*

**What it does:** Claude acts as a Senior Technical Writer. Before writing a single line of documentation, it analyzes your code for ambiguous variable names, unexplained magic values, unclear side effects, and undocumented dependencies. If it finds any, it asks you to clarify before proceeding. Output matches the quality bar of projects like React or FastAPI.

**Why that matters:** Bad docs come from assumptions. This skill eliminates assumptions by making them explicit before writing starts.

**Output language follows your input** — write in German, get German docs. Code identifiers stay as-is.

**Includes:** Documentation examples reference file.

---

### Meeting-PRO
> *"Every task needs an owner and a deadline. No exceptions."*

**What it does:** Paste in a meeting transcript (any language, any format) and Claude extracts everything that matters: decisions made, action items with owners and deadlines, open questions, and blockers. If any task is missing an owner or a deadline, it generates targeted follow-up questions before giving you the final output — it never silently skips incomplete items.

**Why that matters:** Most meeting summaries lose the accountability. This skill treats a nameless task as an unfinished deliverable and forces resolution.

---

### Performance-PRO
> *"No warmup. No 'great question'. No 'I hope this helps'. Just the answer."*

**What it does:** This is a meta-skill — it changes *how* Claude responds, not what it knows. It eliminates intro sentences, problem restatements, closing pleasantries, and hedge phrases. It also enforces a simple decision rule: if the task is clear, execute immediately; if one critical thing is missing, ask exactly that one thing; if the core is ambiguous, clarify in one sentence.

**Why that matters:** Default Claude wastes a lot of tokens on warmup. Every response starts with "Certainly! I'd be happy to help..." — this skill removes all of that.

**Works with any other skill** — stack it on top of Architecture-PRO, Design-PRO, or any combination.

---

### Security-PRO
> *"No 'good approach, but...' — show the vulnerabilities first."*

**What it does:** Claude reviews your code as a Senior Staff Engineer and Cybersecurity Expert. The review always follows the same priority order, no exceptions:

1. 🛑 **Security** — SQL injection, XSS, CSRF, hardcoded secrets, missing auth checks, path traversal
2. ⚠️ **Logic bugs** — race conditions, off-by-one errors, unhandled edge cases, swallowed exceptions
3. 💡 **Performance** — N+1 queries, O(n²) loops, blocking I/O in async code, unnecessary memory use
4. 🧹 **Clean code** — duplicate code, SOLID violations, magic numbers, excessive nesting

All four sections always appear in the output — even if a section is empty, it's listed as clean.

**Works with:** C#/.NET, JavaScript/TypeScript, Python, and any other language.

---

## Combining Skills

Skills are composable — copy multiple `SKILL.md` files into the same system prompt and Claude runs all of them simultaneously:

```
Architecture-PRO + Performance-PRO   →  fast, no-fluff architecture decisions
Documentation-PRO + Security-PRO     →  secure code with complete docs
Design-PRO + Performance-PRO         →  clean UI output, zero padding
```

---

## Roadmap

- [ ] `Analytics-PRO` — data analysis and chart generation
- [ ] `API-PRO` — REST/GraphQL design with OpenAPI spec output
- [ ] `Refactor-PRO` — opinionated, aggressive code refactoring
- [ ] `Startup-PRO` — product strategy and GTM planning

---

## License

MIT — free to use, modify, and distribute. Attribution appreciated.
