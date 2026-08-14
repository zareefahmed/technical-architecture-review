# Architecture Review Checklist

The reviewer's question set. It starts with decision-quality checks that apply to everything, then goes domain by domain following the [architecture types](../02-types-of-architecture/README.md), and ends with the vendor-neutrality screen. Not every item applies to every review, so scope it using the [review process](../03-architecture-review/review-process-and-lifecycle.md). And remember: an item nobody can answer is itself a finding.

## A. Decision quality (apply to every significant decision)

- [ ] The problem this decision solves is written down, and a named business stakeholder confirms it is real
- [ ] At least two credible alternatives were evaluated, at comparable depth, against criteria fixed **before** the scoring
- [ ] The trade-offs of the chosen option are stated: what was sacrificed, and who accepted that
- [ ] The consequences include cost at production scale, operability, and **exit cost**
- [ ] There is evidence beyond assertion: a prototype, a benchmark (ask whose), a reference visit, a structured analysis
- [ ] The decision is recorded (an ADR or similar) with a date, an author, and a status
- [ ] Revisit triggers are named: what future fact would reopen this decision, and would anyone actually notice it

## B. Requirements and scope

- [ ] Quality attributes (performance, availability, security, cost, ease of change) are quantified, not adjectives
- [ ] Every requirement traces to a business stakeholder, and none trace only to a vendor document
- [ ] An [architecture scope statement](../01-foundations/scope-of-architecture-in-projects.md) exists, listing which decisions the architecture owns
- [ ] The expensive decision areas where **no** conscious decision was made are identified (exit, data ownership, and disaster recovery are the usual missing ones)

## C. Software / application

- [ ] The architectural style is justified by a quality attribute, not fashion, and it fits the team's size and skills
- [ ] Component boundaries line up with change: things that change together live together
- [ ] Failure behavior is designed for each dependency: timeouts, retries, idempotency, backpressure
- [ ] Sampled code matches the documented architecture (write down what was sampled)
- [ ] The entanglement of business logic with proprietary SDKs and frameworks is known and deliberate

## D. Data

- [ ] Every core entity has exactly one documented source of truth
- [ ] Storage engines match their workloads (chosen for the job, not for a license the company already had)
- [ ] Retention, deletion, and residency obligations are actually implemented, not just written in a policy
- [ ] Getting the data out (formats, volumes, fees, proprietary transformation logic) is priced as an exit scenario
- [ ] Pipeline failure is detectable: someone gets alerted when data stops flowing or goes wrong

## E. Infrastructure and cloud

- [ ] The disaster recovery plan has an execution date and a result, not just a target on paper
- [ ] The cost model covers year-three production scale, including egress, cross-zone traffic, logs, and renewal terms
- [ ] The platform's complexity matches the team's capacity (ask: who runs this at 3 a.m.?)
- [ ] Committed-spend agreements are understood: the growth they assume, the renewal exposure, and what happens if usage falls short
- [ ] The environment and account layout limits blast radius and enforces guardrails

## F. Security

- [ ] A threat model exists for the critical flows, and it is newer than the current design
- [ ] The trust boundaries on the diagram are enforced in code and configuration (verify by sampling)
- [ ] Access can be revoked everywhere with one action, and privileged access is inventoried
- [ ] Secrets: where they are stored, how they rotate, and who can read them
- [ ] Detection: would the organization notice the scenarios in its own threat model? Through which alert, and how fast?
- [ ] Security purchases map to modeled threats, not to the fear cycle of the year they were bought

## G. Integration

- [ ] An integration catalog exists: every interface, its owner, its contract, and how critical it is
- [ ] No undocumented coupling (shared databases, file drops) goes around the official interfaces
- [ ] Contracts are versioned, with a compatibility and deprecation policy
- [ ] Critical flows have designed failure paths: queues, dead letters, reconciliation, paging
- [ ] Every middleware product still passes the "would we choose this today?" test

## H. Vendor neutrality and commercial coherence

- [ ] The interests map exists: every advisor to this architecture, their employer, and what they gain from each outcome (see the [field guide](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md))
- [ ] The evaluation criteria predate the vendor presentations (check the document dates)
- [ ] No requirement text traces word for word to vendor collateral
- [ ] Every major vendor dependency has a priced answer to "how would we leave?", even if the answer is "expensively, and we accept that knowingly"
- [ ] The contracts and pricing were in the review's scope and were actually read
- [ ] The full [Vendor-Bias Red Flags](vendor-bias-red-flags.md) screen has been run
- [ ] Nobody validated a decision they authored or profit from (see [why](../04-independent-third-party-review/why-independence-matters.md))

---

**Related topics**

- [Review Report Template](review-report-template.md)
- [Vendor-Bias Red Flags](vendor-bias-red-flags.md)
- [Review Methods and Frameworks](../03-architecture-review/review-methods-and-frameworks.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
