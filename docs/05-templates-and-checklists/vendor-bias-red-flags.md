# Vendor-Bias Red Flags

These are the concrete signals that an "architecture" is really a sales proposal wearing architecture's clothes. You do not need an architecture background to use this list. A sponsor, a procurement lead, or a project manager can run it in twenty minutes against any proposal, evaluation, or solution design. Ideally before anything is signed, while the findings are still cheap.

No single flag proves anything. Several together form a pattern. Each flag links back to the chapter that explains the mechanism behind it.

## In the documents

- [ ] **Only one serious option.** Alternatives are missing, or get "considered" in a single dismissive line while the winner gets forty pages. An evaluation with one real candidate is a purchase order. See [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md).
- [ ] **Criteria that showed up after the winner.** The evaluation criteria are dated after the vendor's presentations, or they read like the winner's feature list. See [Conflicts of Interest](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md).
- [ ] **Requirements traceable to the datasheet.** Requirement wording matches the vendor's collateral, or "must support <the winner's proprietary feature>" appears as a requirement.
- [ ] **No stated downsides.** The proposal has no trade-offs section, or every weakness is "addressed in the roadmap." Real architecture names what it sacrifices.
- [ ] **Exit appears nowhere.** No exit cost, no migration-away scenario, no data egress analysis anywhere in the document set. See [Solution Architecture](../02-types-of-architecture/solution-architecture.md).
- [ ] **Vendor prose inside the architecture.** Paragraphs, diagrams, or "best practice" sections lifted word for word from vendor material and presented as the project's own analysis.

## In the numbers

- [ ] **Pilot-scale pricing for a production decision.** Costs modeled at month-one volumes, with year-three growth, renewal terms, and the return to list price after the initial discount all missing. See [Data Architecture](../02-types-of-architecture/data-architecture.md) and [Infrastructure & Cloud](../02-types-of-architecture/infrastructure-cloud-architecture.md).
- [ ] **The bundle discount is the whole argument.** The case for the single-vendor stack rests on the bundle price, not on whether each component fits. The discount is one number in the model, not the model.
- [ ] **Exit-only costs are missing from the comparison.** Egress fees, converting out of proprietary formats, contractual minimums. Leaving them out flatters the most locked-in option.
- [ ] **An endless professional services tail.** The vendor's own consultants stretch indefinitely into the future, unpriced beyond phase one.

## In the process

- [ ] **The vendor ran the requirements workshop.** The "free" discovery session, architecture workshop, or well-architected assessment that shaped the requirements was run by a party selling into them. See [Review Methods](../03-architecture-review/review-methods-and-frameworks.md).
- [ ] **The evaluation effort was lopsided.** The favored option got a funded proof of concept and executive briefings. The alternatives got a spreadsheet row.
- [ ] **Nobody has mapped the advisors' interests.** No one can say, in writing, what each external advisor earns under each outcome. Or the question was never asked at all. See [Conflicts of Interest](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md).
- [ ] **The seller validates the sale.** The party that designed or sells the solution is also the party "reviewing" it. Vendor assessment programs, the integrator reviewing its own build, the reseller's advisory arm. See [Why Independence Matters](../04-independent-third-party-review/why-independence-matters.md).
- [ ] **The urgency belongs to the seller's calendar.** The deadline is driven by the vendor's quarter-end or an expiring discount, not by the project's needs. Discounts that expire at quarter-end have a way of coming back.
- [ ] **Resistance to independent eyes.** Suggestions of an external review get answered with "no time," "no budget," or "we already had the vendor's assessment", and the answers come from the people who shaped the proposal. See [The Role of the Architect](../01-foundations/role-of-the-architect.md).

## What to do when the flags cluster

1. **Pause the signature.** Nothing on this list says the proposal is wrong. It says the proposal is unverified. Pausing is the cheap step. Signing is the expensive one.
2. **Commission a focused independent decision review.** One to two weeks, aimed at exactly this decision, following the [engagement guide](../04-independent-third-party-review/engaging-independent-reviewers.md).
3. **Re-run the evaluation fairly** if the review confirms the capture: frozen criteria, equal effort per option, interests disclosed. See the [management techniques](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md).
4. **Keep the vendor's expertise.** As testimony. The point was never to throw the vendor out. It is to return them to their proper role, and the verdict to yours.

---

**Related topics**

- [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md)
- [Architecture Review Checklist](architecture-review-checklist.md)
- [Engaging Independent Reviewers](../04-independent-third-party-review/engaging-independent-reviewers.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
