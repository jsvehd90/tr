# Contributing Guide

This document defines the engineering review process for this repository. All contributors must follow this process before implementing changes.

---

## Engineering Principles

- **DRY** — aggressively flag and eliminate duplication
- **Well-tested code is mandatory** — better too many tests than too few
- **Engineered enough** — not fragile or hacky, but not over-engineered
- **Correctness over speed** — optimize for correctness and edge cases before optimizing for implementation speed
- **Explicit over clever** — prefer readable, explicit solutions

---

## Review Process

### Step 0 — Classify the Change

Before opening a PR or starting implementation, answer:

**Is this a BIG change or a SMALL change?**

| | BIG | SMALL |
|---|---|---|
| **Definition** | Affects system design, multiple components, or carries significant risk | Scoped to a single component or small, well-understood fix |
| **Review depth** | All four sections; highlight top 3–4 issues per section | One focused question per section; keep it concise |

---

### Step 1 — Architecture Review

Evaluate **before writing code**:

- Overall system design and component boundaries
- Dependency graph and coupling risks
- Data flow and potential bottlenecks
- Scaling characteristics and single points of failure
- Security boundaries (auth, data access, API limits)

> ⏸ **Pause here.** Discuss findings with the team. Do not proceed until this section is approved.

---

### Step 2 — Code Quality Review

Evaluate:

- Project structure and module organisation
- DRY violations
- Error handling patterns and missing edge cases
- Technical debt risks
- Areas that are over-engineered or under-engineered

> ⏸ **Pause here.** Discuss findings with the team. Do not proceed until this section is approved.

---

### Step 3 — Test Review

Evaluate:

- Test coverage (unit, integration, e2e)
- Quality of assertions
- Missing edge cases
- Failure scenarios that are not tested

> ⏸ **Pause here.** Discuss findings with the team. Do not proceed until this section is approved.

---

### Step 4 — Performance Review

Evaluate:

- N+1 queries or inefficient I/O
- Memory usage risks
- CPU hotspots or heavy code paths
- Caching opportunities
- Latency and scalability concerns

> ⏸ **Pause here.** Discuss findings with the team. Do not proceed until this section is approved.

---

## For Each Issue Found

Provide:

1. **Clear description** of the problem
2. **Why it matters** — impact on correctness, maintainability, performance, or security
3. **2–3 options** (always include "do nothing" if reasonable)

For each option, state:

| Field | Description |
|---|---|
| Effort | Estimated time/complexity |
| Risk | Probability and severity of introducing new problems |
| Impact | Benefit if the option is taken |
| Maintenance cost | Long-term cost of living with the change |

4. **Recommended option** — be opinionated. State why.

Then **ask for approval before implementing**.

---

## Workflow Rules

- Do **not** assume priorities or timelines
- After each review section (Architecture → Code → Tests → Performance), pause and ask for feedback
- Do **not** implement anything until the reviewer confirms direction

---

## Pull Request Process

1. Use the [PR template](.github/PULL_REQUEST_TEMPLATE.md) — fill in every section
2. Self-review against all four sections before requesting a review
3. Address all reviewer comments before merging
4. Squash commits to a clean history before merging

---

## Issue Reporting

Use the [Architecture / Code Review issue template](.github/ISSUE_TEMPLATE/architecture-review.md) to raise review findings or propose changes.
