# The Role of the Architect

Architecture is done by people, and the value of an architecture depends on whose interests the architect serves. This chapter describes the role: its responsibilities, the skills it needs, and above all its loyalty. Everything else in this guide rests on one claim: an architect's duty runs to the problem and the organization, never to a product.

## Responsibilities

An architect on a technical project is accountable for:

1. **Understanding the problem before proposing solutions.** That means the requirements, the constraints, the quality attributes, and the business context that gives them weight.
2. **Producing real alternatives.** A single option is not a decision. It is a foregone conclusion. Genuine architecture work produces at least two credible candidates and a reasoned comparison between them.
3. **Making trade-offs out loud.** Every choice sacrifices something. The architect's job is to say what, clearly, in writing.
4. **Recording decisions.** Decision records that capture the context, the options, the choice, and the consequences are the most important artifact of the role. More important than any diagram.
5. **Keeping the build honest.** Making sure the system being built matches the architecture that was decided, and updating the architecture when the build teaches everyone something new.
6. **Owning the long tail.** Running costs, operability, ease of change, and exit cost. These appear on nobody's launch checklist and everybody's five-year budget.

## The loyalty question

Architects show up in projects under many different employers:

- **In-house architects**, employed by the organization that owns the system.
- **Consultancy architects**, employed by a services firm delivering the project.
- **Vendor solutions architects**, employed by a software, hardware, or cloud vendor. They are usually attached to a sales account, and their incentives are often tied to consumption or deal size.
- **Partner and reseller architects**, employed by firms whose margins and partner status depend on selling particular vendors' products.

All four can be skilled, honest people. But the incentives built into these roles differ enormously. A vendor solutions architect can be a brilliant engineer and still be unable, as a matter of job description, to recommend a competitor's product. That is not a character flaw. It is a conflict of interest, and it has to be managed like one. The full story is in [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md) and [Conflicts of Interest and Vendor Bias](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md).

The practical rule for anyone sponsoring a project:

> **Know who pays each architect at your table, and never let a party with a revenue stake in the answer be the only one evaluating the question.**

Vendor architects are genuinely valuable as experts on their own product. They know how to use it well, where its limits are, and where it is heading. Consult them for exactly that. What they must not be allowed to do, unchecked, is define your requirements, write your shortlist, or judge their own proposal.

## The skills the role needs

- **Breadth beyond any single stack.** An architect who knows one ecosystem deeply and nothing else can only ever recommend that ecosystem. Bias born of ignorance produces the same result as bias born of incentive.
- **Trade-off thinking.** Being comfortable with "it depends", and having the discipline to say on what.
- **Communication.** Architecture only works if decision-makers understand it. Translating between engineering and business is half the job.
- **Commercial literacy.** Licensing, pricing models, contract terms, and exit costs are part of the technical decision, not someone else's problem.
- **Intellectual honesty.** The willingness to recommend against your own earlier decision, your favorite technology, or your own employer's product when the evidence points that way. This is the rarest skill on the list, and it is the one that independence exists to protect.

## The architect and the review

A good architect wants to be reviewed. Review is how a decision earns confidence, and independent review is the only way a sponsor can tell a well-reasoned architecture from a well-presented one. An architect who resists outside scrutiny of their big decisions is signaling something. Sometimes it is insecurity. Sometimes it is the awareness that the decisions will not survive the scrutiny. Either signal deserves attention.

---

**Related topics**

- [What Is Technical Architecture?](what-is-technical-architecture.md)
- [Solution Architecture](../02-types-of-architecture/solution-architecture.md)
- [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md)
- [Engaging Independent Reviewers](../04-independent-third-party-review/engaging-independent-reviewers.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
