# Solution Architecture

## What it is

Solution architecture (SA) takes a single business problem and designs the complete answer to it: the applications, data, infrastructure, integrations, and commercial arrangements that together deliver the outcome. It sits between [enterprise architecture](enterprise-architecture.md), which gives it context, and the specialist domains ([software](software-application-architecture.md), [data](data-architecture.md), [infrastructure](infrastructure-cloud-architecture.md), [integration](integration-architecture.md)) that it draws on.

This is where the central idea of this guide lives:

> **"Solutions Architecture must be solutions architecture, not a sales agent of a specific vendor."**

Why does the quote name SA specifically? Because solution architecture is the discipline that picks technologies and vendors for a concrete, funded project. It is the point where money meets design. And so it is the point where every vendor's commercial machinery focuses its attention. The full story is in [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md).

## What it covers

- **Requirements and quality attributes.** Turning a business need into measurable technical requirements.
- **Option analysis.** Producing credible alternative shapes of a solution (build, buy, compose, extend) and comparing them fairly.
- **End-to-end design.** Components, data flows, integrations, deployment, and operations for the chosen option.
- **Technology and vendor selection.** Matching products and platforms to requirements, with eyes open about cost, lock-in, and exit.
- **Commercial and technical coherence.** Licensing, support, and contract terms that match the technical design, and the other way around.
- **Delivery feasibility.** A solution the available team can actually build and run.

## Key artifacts

- The solution architecture document (SAD): context, requirements, options considered, chosen design, trade-offs
- Architecture decision records (ADRs) for each significant choice
- Option comparison matrices with weighted criteria, written before anyone knows the preferred option
- A cost model covering the cost to build, the cost to run, and the cost to exit
- A risk register with architectural risks and their mitigations

## Typical decisions

- Build, buy, or SaaS for each major capability
- Which products make the shortlist, which one wins, and on what criteria
- Where the solution's data lives and who owns it
- How much of a single vendor's ecosystem to adopt (the bundling decision)
- What the exit strategy is for each major dependency

## The two directions of solution architecture

The same activities can run in two opposite directions, and the direction decides everything:

| | **Solution-first (genuine SA)** | **Product-first (sales-agent SA)** |
|---|---|---|
| Starting point | The problem and its constraints | A product to be sold |
| Requirements | Drive the evaluation | Get edited to match the product |
| Alternatives | Genuinely compared | Straw men, or missing entirely |
| Trade-offs | Stated and owned | Played down or deferred |
| Lock-in and exit cost | A first-class criterion | Never mentioned |
| Deliverable | A decision the client owns | A proposal the vendor owns |

Here is the uncomfortable part: both directions produce a professional-looking architecture document. Telling them apart from the artifacts alone is genuinely hard. That is exactly why [independent review](../04-independent-third-party-review/README.md) exists.

## What a reviewer looks for

- **The direction of the reasoning.** Do the documents show requirements leading to a choice, or a choice retrofitted with requirements? Check the dates and versions. Were the evaluation criteria written before or after the preferred product showed up?
- **Whether the alternatives were real.** Were the rejected options ever viable, and did they get the same rigor as the winner? A comparison where one column was filled in by that product's vendor is not a comparison.
- **Exit cost.** Is it quantified anywhere? If a solution has a major vendor dependency and no exit analysis, that absence is a finding all by itself.
- **The cost model.** Does it cover running costs at realistic scale, license growth terms, egress and renewal traps, and the professional services tail?
- **Fit to the team.** Can the client's own staff run this, or does the design quietly require the vendor's services forever?
- **Who wrote what.** Which sections of the document originated from vendor material? Verbatim vendor prose is common, and it is detectable.

---

**Related topics**

- [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md)
- [The Role of the Architect](../01-foundations/role-of-the-architect.md)
- [Vendor-Bias Red Flags](../05-templates-and-checklists/vendor-bias-red-flags.md)
- [Enterprise Architecture](enterprise-architecture.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
