# Not a Sales Agent

> ## "Solutions Architecture must be solutions architecture, not a sales agent of a specific vendor."

This essay unpacks the principle at the center of this guide. It is not an attack on vendors, their products, or the people who work for them. It is a precise claim about a role: what solutions architecture is for, what happens when that role quietly gets performed by a vendor's sales function, and how an organization keeps the two apart.

## What the words mean

**Solutions architecture** is the discipline of designing the complete answer to a business problem: understanding the requirements and constraints, producing real alternatives, weighing trade-offs openly, and choosing technologies because they serve the problem (see the [full chapter](../02-types-of-architecture/solution-architecture.md)).

A **sales agent** is someone whose job is to make a purchase of a specific product happen. There is nothing dishonorable about sales. But it is a different job with a different loyalty. The salesperson's duty runs to their employer's revenue. The architect's duty runs to the client's problem.

The quote names a failure mode: the sales function wearing the architect's title. When the person designing your solution is paid by the party selling its components, designing and selling have merged into one activity. And the merger is invisible, because the output looks exactly like architecture. Same diagrams, same document templates, same vocabulary of requirements and best practices.

## Why this happens so often

It is worth being clear-eyed about why this pattern shows up everywhere, without anyone acting in bad faith:

**1. The title itself has been adopted by sales organizations.** At most major technology vendors, "Solutions Architect" is a pre-sales role. It is attached to named sales accounts, and performance is measured, directly or through the account team, on revenue, consumption growth, or deal progression. These people are often excellent engineers. But an engineer whose quarterly review depends on your consumption of their employer's services is in no position to tell you to consume less of them, or none at all.

**2. The expertise is real, which makes the bias credible.** The vendor's architect genuinely knows their platform better than anyone else in the room. Their advice on how to use the product well is excellent, and you should take it. The capture happens one level up: whether to use the product, how much of the ecosystem to adopt, what the alternatives are. On those questions their expertise is real but their answer was decided before they walked in.

**3. It arrives free, early, and helpful.** Vendor architects appear at exactly the moment a project is under-resourced and grateful: free workshops, free architecture reviews, free reference designs, proof-of-concept credits. Every one of those artifacts is genuinely useful. And every one quietly installs the vendor's products as the default that everything else must argue against. By the time a formal evaluation happens, it is scored against requirements that were drafted, sometimes word for word, from the vendor's datasheet.

**4. The ecosystem recruits third parties.** Resellers and consulting partners earn margins, rebates, and partner-tier status from specific vendors. Their architects' certifications and career capital live inside one ecosystem. So a partner's "independent" recommendation of the vendor whose partnership funds their business is the sales-agent pattern at one remove. Harder to see, identical in effect. See [Conflicts of Interest and Vendor Bias](conflicts-of-interest-and-vendor-bias.md) for the full field guide.

## The two directions of reasoning

Everything comes down to which direction the reasoning runs:

- **Solution-first** (architecture): problem, then requirements, then constraints, then alternatives, then trade-offs, then technology. The technology appears at the end, as a conclusion.
- **Product-first** (sales): product, then capabilities, then requirements that showcase them, then justification. The technology was there at the beginning, as a premise.

Both directions produce a complete, professional architecture document. But the direction leaves fingerprints, and they show up in the artifacts and their history:

| Signal | Solution-first | Product-first |
|---|---|---|
| Evaluation criteria | Written before the candidates were scored; traceable to business needs | Appear after the winner; read like the winner's feature list |
| Alternatives | Real, costed, seriously argued | Straw men, or "considered and rejected" in one line |
| Trade-offs | Stated and owned ("we accept X to get Y") | Only strengths; every weakness is "on the roadmap" |
| Exit cost | Quantified, or at least named | Absent from the entire document set |
| Cost model | Year three at production scale, renewal terms included | Month one at pilot scale, discounts in the headline |
| Where requirements came from | Business stakeholders, dated early | Phrases traceable to vendor collateral |

The [Vendor-Bias Red Flags checklist](../05-templates-and-checklists/vendor-bias-red-flags.md) turns this table into a working tool.

## What it costs

Product-first architecture is not just impure. It is expensive, in specific and repeatable ways:

- **Mismatched capability.** The product's strengths define the shape of the solution, and the problem's actual needs get whatever is left over. Organizations end up running their business the way the product prefers, permanently.
- **Over-scoping.** Sales-driven designs consistently include more modules, tiers, and capacity than the problem needs. Quotas do not reward minimalism.
- **Lock-in nobody decided on.** Exit cost is the one trade-off a sales agent never brings up, so it gets accepted by default instead of by choice. The bill arrives at renewal time, when unit prices go up and the organization can no longer credibly leave.
- **Inflated total cost of ownership.** Pilot-scale pricing, growth assumptions that favor the vendor, and a professional services tail (the vendor's own consultants, forever) all compound quietly.
- **Weakened internal capability.** When design is outsourced to the seller, the organization's own architectural muscle wastes away. That makes the next decision even more dependent on vendor guidance than this one.

## What genuine solutions architecture looks like

Here is the positive version of the principle:

1. **The problem belongs to the client.** It is stated in the client's terms and validated with the people who own it, before any product gets named.
2. **The alternatives are real.** At least two credible options, evaluated at equal depth, against criteria frozen before the scoring starts. "We only seriously considered one" is a finding, not a method.
3. **The trade-offs are said out loud.** Every recommendation names what it sacrifices. An architecture with no stated downsides is an advertisement.
4. **Exit is designed, not discovered.** Every major dependency comes with a priced answer to "how would we leave?" Even if the answer is "expensively, and we accept that with open eyes."
5. **Best-of-need beats best-of-brand.** A single-vendor bundle is a legitimate outcome when the evaluation actually concludes so. It is never a legitimate starting assumption. The bundle discount is one number in the model, not the model.
6. **Vendor expertise is used as testimony, not as verdict.** Vendor architects get called in as expert witnesses on their own products. Weighing that testimony belongs to someone with no stake: the client's own architect, or an [independent reviewer](why-independence-matters.md).
7. **The reasoning can be audited.** Decisions, alternatives, and trade-offs are recorded well enough that a third party could reconstruct the why. Because sooner or later, someone should (see [the review process](../03-architecture-review/review-process-and-lifecycle.md)).

## Where independent review comes in

An organization cannot always staff pure solution-first architecture on its own. The expertise gap is real, and vendor help will keep being useful and free. That is fine, on one condition: the resulting decisions get checked by someone who is actually free to disagree with them. This is the load-bearing link to [the rest of this section](README.md). Independent third-party review is the mechanism that lets you accept interested help safely. The vendor's architect may draft. The sales agent may pitch. But before anything is signed, someone who profits from neither outcome walks the reasoning from end to end.

That is what keeps solutions architecture solutions architecture.

---

**Related topics**

- [Solution Architecture](../02-types-of-architecture/solution-architecture.md)
- [Why Independence Matters](why-independence-matters.md)
- [Conflicts of Interest and Vendor Bias](conflicts-of-interest-and-vendor-bias.md)
- [Vendor-Bias Red Flags](../05-templates-and-checklists/vendor-bias-red-flags.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
