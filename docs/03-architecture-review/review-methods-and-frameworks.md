# Review Methods and Frameworks

There is more than one way to run an architecture review. This chapter surveys the established methods, explains when each fits, and, in keeping with the theme of this guide, takes an honest look at the review frameworks that vendors themselves hand out.

## Scenario-based evaluation: ATAM and its family

The Architecture Tradeoff Analysis Method (ATAM), developed at the Software Engineering Institute, is the best-known formal method. Its core idea is that quality attributes only become testable through concrete scenarios. For example: "when the payment provider times out during checkout peak, the order must still complete within N seconds without double-charging." The review gathers scenarios like this from stakeholders, prioritizes them, and walks the architecture through each one, surfacing:

- **Sensitivity points**: decisions that a quality attribute critically depends on
- **Trade-off points**: decisions that push several attributes in opposite directions
- **Risks**: scenarios the architecture handles badly, and why

Full ATAM is heavyweight: days of workshops and a lot of stakeholders. Its lasting contribution is the scenario discipline, which every lighter method borrows. Related methods from the same family include SAAM (its predecessor) and various lightweight derivatives.

## Lightweight decision-based reviews

Most practical reviews today center on decisions. Take the architecture decision records and, for each significant decision, ask a fixed set of questions:

1. What problem does this decision solve, and who can confirm that problem is real?
2. What alternatives were considered, and were they evaluated honestly?
3. What are the consequences, including cost, operability, and exit? Who accepted them?
4. What evidence exists beyond assertion? A prototype, a benchmark, a reference?
5. What future fact would make us revisit this decision, and would we even notice it?

This scales from an afternoon (one decision, before a signature) to weeks (a whole estate). And it naturally surfaces the vendor-bias signals: decisions with no real alternatives, consequence sections with no exit analysis, evidence that consists entirely of the vendor's own benchmark. The [review checklist](../05-templates-and-checklists/architecture-review-checklist.md) turns this battery into a working tool, domain by domain.

## Checklist and pillar frameworks

The vendor well-architected frameworks (AWS Well-Architected, Azure Well-Architected, Google Cloud Architecture Framework) organize review around pillars such as reliability, security, cost, performance, and operations, each with detailed question sets. They are genuinely useful, widely known, and free.

Just be clear about what they are and what they are not:

- **They review how well you use that vendor.** They never ask whether that vendor, or a cloud service at all, was the right choice. The selection question, which is the most expensive one, sits outside the framework by design.
- **Their cost pillar optimizes spend within the platform.** Rightsizing, reservations, storage tiers. It never compares spend against alternatives, and it never mentions exit cost.
- **The free assessment is a sales instrument as well as an engineering one.** Its findings reliably resolve to adopting more of the vendor's managed services. That can be sound advice and still be advice from an interested party.

The practical stance: use these frameworks for what they are good at, which is operational hygiene on a platform you already chose for good reasons. Pair them with independent review for the questions they cannot ask. A well-architected badge on a wrongly-chosen platform is a well-organized mistake.

## Peer review and architecture review boards

Internal mechanisms, whether a standing architecture review board (ARB) or ad-hoc peer review across teams, catch a large share of honest mistakes cheaply, and they build shared standards along the way. But they have structural limits. Board members share the organization's assumptions and politics. They may have sponsored the very decisions under review. And they rarely have time to verify anything beyond the documents. Boards work best as the routine layer, with [independent external review](../04-independent-third-party-review/README.md) saved for the decisions where the stakes, or the conflicts of interest, are bigger than an internal process can credibly handle.

## Choosing a method

| Situation | A fitting method |
|---|---|
| Major system, many stakeholders, contested quality attributes | Scenario-based workshop, ATAM style |
| One big decision, before a signature | Lightweight decision review with an independent reviewer |
| Ongoing delivery governance | An ARB plus checkpoint reviews |
| Health check of a workload on an established cloud platform | Well-architected framework, plus an independent look at cost and lock-in |
| Vendor-influenced architecture, procurement, due diligence | Independent third-party review ([Section 4](../04-independent-third-party-review/README.md)) |

Methods combine well. The constants are the scenario and decision discipline, and the follow-through described in [the review process](review-process-and-lifecycle.md).

---

**Related topics**

- [The Review Process and Lifecycle](review-process-and-lifecycle.md)
- [Why Independence Matters](../04-independent-third-party-review/why-independence-matters.md)
- [Architecture Review Checklist](../05-templates-and-checklists/architecture-review-checklist.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
