# Infrastructure & Cloud Architecture

## What it is

Infrastructure architecture is the design of the platforms your systems run on: compute, network, storage, and the operational machinery around them. In most modern projects that means cloud architecture: choosing and combining cloud services, designing the account and network layout, and balancing convenient managed services against portable building blocks. On-premises and hybrid setups are still common and perfectly legitimate.

## What it covers

- **Compute and runtime.** Virtual machines, containers, orchestration (Kubernetes), serverless, and which fits which workload.
- **Network layout.** Segmentation, traffic in and out, private connectivity, DNS, load balancing.
- **Environments and landing zones.** Account and subscription structure, environment separation, guardrails.
- **Resilience.** Availability zones and regions, failover design, backup and disaster recovery, recovery time and recovery point targets.
- **Operations.** Observability, capacity, patching, infrastructure as code, deployment pipelines.
- **Cost.** The monthly bill, what drives it, and how it is governed through budgets, tagging, and rightsizing.

## Key artifacts

- Deployment and network diagrams
- The landing zone and environment design
- Infrastructure-as-code repositories (this is the real architecture, and it is versioned)
- A disaster recovery plan with tested recovery figures
- A cost model and regular reporting of the actual spend

## Typical decisions

- One cloud provider, several, or a hybrid with on-premises. And what "multi-cloud" actually means in practice, if anything
- Managed services versus running your own (a managed database versus self-hosted, serverless versus containers)
- Region strategy: latency, residency, failover
- Kubernetes or not. This is a cost and complexity decision as much as a technical one
- Committed spend: how much future usage to promise a vendor in exchange for a discount

## What a reviewer looks for

- **Are the resilience claims tested?** A disaster recovery plan that has never been executed is a hypothesis. Reviewers ask for the date and the result of the last failover test.
- **What does it cost at real scale?** The run rate modeled at production load and growth, including the pricing lines that surprise people: egress, cross-zone traffic, per-request charges, log ingestion.
- **Is the complexity honest?** Does the platform match the team? A full Kubernetes estate run by two people is an availability risk dressed up as sophistication.
- **How does the security topology hold up?** Segmentation, the blast radius of one compromised workload, how secrets are handled. This overlaps with [Security Architecture](security-architecture.md).
- **What do the commitments assume?** Committed-spend deals and enterprise agreements: what growth do they assume, and what happens to your unit prices at renewal, once your workloads are too embedded to move?

## A note on vendor neutrality

Cloud is where the "sales agent" dynamic is most industrialized. Every major provider employs account teams whose job title is literally "Solutions Architect" and whose performance is measured on consumption growth. Their free architecture reviews, credit programs, and well-architected assessments are genuinely useful. They are also stages in a sales funnel. Every recommendation lands on the provider's own services, and alternatives outside the catalog simply do not appear. The sensible response is not to refuse the free expertise. It is to weigh it as what it is: expert testimony from an interested party, checked by someone who has no consumption target. See [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md) and [Why Independence Matters](../04-independent-third-party-review/why-independence-matters.md).

---

**Related topics**

- [Security Architecture](security-architecture.md)
- [Data Architecture](data-architecture.md)
- [Review Methods and Frameworks](../03-architecture-review/review-methods-and-frameworks.md) (covers vendor well-architected frameworks and their limits)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
