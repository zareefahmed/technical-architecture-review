# Conflicts of Interest and Vendor Bias

The architecture table seats many people, and most of them care about more than the quality of the solution. This chapter is a field guide: the standing conflicts of interest by role, the subtler biases that need no paycheck at all, and the techniques that keep both from steering your decisions.

## Who wants what: a map of the table

| Party | Their legitimate role | Their standing interest | The sharpest risk |
|---|---|---|---|
| **Vendor solutions architect** | Expert on their own product's use and limits | Consumption and deal growth for their employer | Shapes the solution around their catalog; alternatives never appear |
| **Reseller / channel partner** | Sourcing, licensing logistics, first-line expertise | Margins and rebates that differ by vendor and product tier | "Neutral" advice that reliably lands on the highest-margin line |
| **Consulting / SI partner** | Delivery capacity and experience | Billable volume; partner status with vendors; follow-on work | Recommends whatever maximizes the build; co-sells partnered vendors |
| **Internal architect** | Owns the design for the organization | Career capital in familiar technologies; pride of authorship | Defends past decisions; picks the familiar over the fitting |
| **Internal sponsor / IT leadership** | Owns the budget and the outcome | Publicly announced positions; vendor relationships; org politics | The decision was made before the analysis; review becomes a rubber stamp |
| **Independent reviewer** | Validates the reasoning | The review fee; a reputation for rigor | Softens findings to get rehired; inflates severity to look valuable |

Two things are worth noticing in this table. First, every row has an interest, including the internal ones and the independent reviewer. The difference is what kind. The vendor architect's interest points at a specific technical outcome, which is what disqualifies them from validation work. The independent reviewer's interest (reputation, being rehired) points at the quality of the review itself, and it is managed through disclosure and engagement terms (see [how](engaging-independent-reviewers.md)). Second, the partner rows are the ones organizations misread most often. The vendor's interest is at least printed on their business card. The partner's interest arrives under a neutral-looking brand. So ask any "independent" advisor the direct question: what do you earn, and from whom, if we choose each of these options? The answer is informative. So is the discomfort.

## Bias without a paycheck

Removing the commercial stakes does not remove bias. The honest kinds matter just as much, because they wear no logo:

- **Familiarity bias.** Architects recommend what they know. Deep expertise in one stack makes every problem look like that stack's use case. An architect who knows only one ecosystem gives vendor-aligned advice for free.
- **Certification gravity.** A career built on one vendor's certification ladder creates loyalty with no invoice attached.
- **Authorship bias.** The person who designed the current system gets asked to evaluate its replacement, or its critique.
- **Anchoring.** Whoever presents first, usually the vendor with the polished deck, sets the frame that every alternative gets measured against.
- **Sunk-cost reasoning.** "We've already invested so much in this platform." The money already spent is gone either way. Only the future costs differ between the options.
- **Social proof.** "Everyone uses X" substitutes the market's combined marketing budget for an analysis of your problem.

A serious review process treats these as seriously as the commercial conflicts. Bring in reviewers with diverse backgrounds, freeze the criteria before the candidates present, and put the question "what would change your mind?" to every advocate.

## How to manage it

Conflicts of interest get managed, not eliminated, because vendors and partners bring real expertise the project needs. The discipline looks like this:

1. **Write the interests down.** One page, kept with the project: every advisor, their employer, and what they gain from each possible outcome. Just writing this down changes how meetings go.
2. **Separate testimony from verdict.** Interested parties inform. Disinterested parties decide and validate. A vendor architect presenting to your evaluation is healthy. A vendor architect scoring your evaluation is self-audit.
3. **Freeze criteria before contact.** Evaluation criteria and weights get written and signed off before the candidate products present. Criteria that shift after the demos are the fingerprint of capture.
4. **Demand equal effort per option.** Every shortlisted option gets the same depth of analysis, the same access, the same proof-of-concept budget. An evaluation where one option got a funded pilot and the others got a paragraph is not an evaluation.
5. **Disclose or disqualify.** Advisors state their interests as the price of entry. An interest discovered undisclosed disqualifies the advice, retroactively.
6. **Put independence at the signature points.** Full-time independence everywhere is unaffordable. Independence at the [moments of signature](../03-architecture-review/review-process-and-lifecycle.md), meaning selection reviews and pre-contract reviews, is not.

The working-tool version of this chapter is the [Vendor-Bias Red Flags checklist](../05-templates-and-checklists/vendor-bias-red-flags.md).

---

**Related topics**

- [Not a Sales Agent](not-a-sales-agent.md)
- [Why Independence Matters](why-independence-matters.md)
- [Vendor-Bias Red Flags](../05-templates-and-checklists/vendor-bias-red-flags.md)
- [The Role of the Architect](../01-foundations/role-of-the-architect.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
