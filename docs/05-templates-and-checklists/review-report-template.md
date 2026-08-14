# Review Report Template

A ready-to-copy skeleton for an architecture review report. Delete the guidance comments (`<!-- ... -->`) as you fill it in. The structure follows the [review process](../03-architecture-review/review-process-and-lifecycle.md), and the severity definitions are at the end.

---

```markdown
# Architecture Review: <system / decision under review>

| | |
|---|---|
| **Sponsor** | <who commissioned the review and receives the findings> |
| **Reviewer(s)** | <names, firm> |
| **Independence statement** | <the reviewer's disclosed interests, and confirmation of no contingent work, per the engagement terms> |
| **Review period** | <dates> |
| **Report date & version** | <date, v1.0> |

## 1. Executive summary

<!-- Half a page at most. The three to five findings that matter, the overall
     risk picture, and the single most important recommendation. Write it for
     a reader who will read nothing else. -->

## 2. Scope and method

- **In scope:** <systems, decisions, documents, environments>
- **Out of scope:** <and why>
- **Criteria:** <the quality attributes and business constraints judged against>
- **Method:** <document study, interviews (list the roles), verification done,
  such as code, config, and cost sampling, or tests observed>
- **Access limitations:** <anything requested and not provided. This is
  important context for the findings>

## 3. Context

<!-- One page: the business problem, the history of this architecture, the
     commercial situation (vendors, contracts, upcoming signatures), and why
     the review was commissioned now. -->

## 4. Findings

<!-- One block per finding, most severe first. Every finding carries evidence
     and a concrete recommendation. No observations without either. -->

### F-1. <finding title> (Severity: Critical / High / Medium / Low)

- **Evidence:** <what was seen and where: a document, a code path, a cost report, an interview>
- **Impact:** <what happens if this goes unaddressed, to whom, and roughly when>
- **Recommendation:** <the specific action, not "consider improving">
- **Effort estimate:** <rough order: days / weeks / months>

### F-2. ...

## 5. What is sound

<!-- Deliberately list the significant decisions that were examined and found
     solid. This makes the report a fair map instead of a defect list, and it
     stops sound decisions from being argued over again and again. -->

## 6. Decision log impact

| Decision | Review outcome | Note |
|---|---|---|
| <ADR-nn or decision name> | Confirmed / Modified / Reversed / **Missing, must be made** | |

## 7. Follow-through log

<!-- Filled in with the sponsor at playback. The review is not closed until
     this table has owners and dates. -->

| Finding | Accepted? | Owner | Target date | Status |
|---|---|---|---|---|
| F-1 | | | | Open |

## Appendix A. Interview list
## Appendix B. Documents reviewed
## Appendix C. Verification detail
```

---

## Severity definitions

- **Critical**: material harm is likely on the current path (an outage, a breach, runaway cost, lock-in you cannot use). Act before the next irreversible step, whether that is a signature or a go-live.
- **High**: significant probable harm or cost. Address within the current quarter or phase.
- **Medium**: real risk or waste, but the timing is manageable. Schedule it deliberately.
- **Low**: an improvement opportunity. Fix when convenient.

Two conventions are worth keeping. First, findings are about decisions and artifacts, never about people. A report that reads like a performance review gets its findings suppressed, and honestly, that is fair. Second, "missing decision" is a first-class finding type (see the last row of section 6). The exit strategy that does not exist, or the disaster recovery plan that was never tested, belongs in the log with the same weight as a wrong decision. Usually more.

---

**Related topics**

- [The Review Process and Lifecycle](../03-architecture-review/review-process-and-lifecycle.md)
- [Benefits and Outcomes](../03-architecture-review/benefits-and-outcomes.md) (what to demand from findings)
- [Engaging Independent Reviewers](../04-independent-third-party-review/engaging-independent-reviewers.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
