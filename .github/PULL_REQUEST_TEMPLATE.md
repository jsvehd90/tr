## Change Classification

> **Is this a BIG change or a SMALL change?**
>
> - **BIG**: Review all sections step-by-step. Highlight the top 3–4 issues per section.
> - **SMALL**: Ask one focused question per section. Keep the review concise.

- [ ] BIG change
- [ ] SMALL change

---

## Description

<!-- What does this PR do? Why is it needed? -->

---

## 1. Architecture Review

<!-- Evaluate the following before requesting review: -->

- [ ] Overall system design and component boundaries make sense
- [ ] No new tight coupling introduced; dependency graph is clean
- [ ] Data flow is straightforward with no obvious bottlenecks
- [ ] No new single points of failure introduced
- [ ] Security boundaries respected (auth, data access, API limits)

**Notes / concerns:**

<!-- Leave blank if none -->

---

## 2. Code Quality Review

- [ ] Project structure and module organization is consistent
- [ ] No DRY violations (no duplicated logic)
- [ ] Error handling covers edge cases
- [ ] No significant new technical debt introduced
- [ ] Code is "engineered enough" — not fragile/hacky, not over-engineered

**Notes / concerns:**

<!-- Leave blank if none -->

---

## 3. Test Review

- [ ] Unit tests added or updated for new/changed logic
- [ ] Integration tests cover cross-component paths where relevant
- [ ] Edge cases and failure scenarios are tested
- [ ] Assertions are meaningful (not just "no exception thrown")

**Notes / concerns:**

<!-- Leave blank if none -->

---

## 4. Performance Review

- [ ] No N+1 queries or inefficient I/O patterns introduced
- [ ] No obvious memory usage regressions
- [ ] No new CPU-heavy hot paths without justification
- [ ] Caching opportunities considered
- [ ] Latency / scalability impact assessed

**Notes / concerns:**

<!-- Leave blank if none -->

---

## Checklist

- [ ] I have reviewed the [Contributing Guide](../CONTRIBUTING.md) and followed the review process
- [ ] All CI checks pass
- [ ] Reviewer approval obtained before merging
