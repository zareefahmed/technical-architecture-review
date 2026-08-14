# Security Architecture

## What it is

Security architecture is the design of how a system resists, detects, and recovers from attack and misuse. Unlike the other domains, it is not a layer of the stack. It is a property of the whole. It cuts across application, data, infrastructure, and integration decisions, and it is only as strong as the weakest of them.

## What it covers

- **Identity and access.** Authentication, authorization, identity providers, trust between services, privileged access.
- **Trust boundaries.** Where untrusted meets trusted, and what gets validated, filtered, or isolated at each crossing.
- **Data protection.** Encryption in transit and at rest, key management, secrets handling, controls driven by data classification.
- **Threat modeling.** Systematically asking what can go wrong (STRIDE and similar methods) and designing defenses for it.
- **Detection and response.** Logging, alerting, audit trails, and the path from alert to action.
- **Compliance.** Legal and contractual security obligations, mapped to actual controls.

## Key artifacts

- Threat models for the critical flows
- The identity and access design: tenant model, role model, trust relationships
- A data classification scheme and the controls mapped to it
- Security diagrams that show the trust boundaries
- A control catalog mapped to compliance requirements

## Typical decisions

- The central identity provider and how federation works
- Zero-trust or perimeter-based network posture, or an honest hybrid
- Key management: cloud-managed, hardware security modules, bring your own key
- What gets logged, kept, and watched, and by whom
- Which security capabilities are products and which are practices

## What a reviewer looks for

- **Does a threat model exist, and is it fresh?** Was one done at all? Does it cover the flows that matter? Has anyone revisited it since the design changed?
- **Are the trust boundaries enforced?** Are the boundaries on the diagram actually enforced in code and configuration, or just drawn?
- **How scattered is identity?** How many places do identities and permissions live? Can access be revoked everywhere with one action?
- **How are secrets handled?** Where do credentials live, how do they rotate, who can read them?
- **Would anyone notice a breach?** Take the scenarios in the organization's own threat model. Would they be detected? How fast, and by which alert?
- **Can you recover?** Backups that have actually been restored, and incident runbooks that name real people.

## A note on vendor neutrality

Security is a fear-driven market, which makes it unusually easy to sell products into. The result is a belief that safety is something you buy rather than something you design. The sales-agent pattern in this domain is the tool-stack answer to a design question. Ask a vendor-aligned advisor "how should we secure this system?" and the answer is a list of products, theirs. The architectural answer starts with trust boundaries, identity, and least privilege, and only then asks which controls need tooling. Reviewers also watch for security-vendor pile-up: overlapping tools bought in successive fear cycles, each half-deployed, together costing more than the risk they retire. An independent reviewer has no reason to add another box. That is exactly why their advice, which is often "you don't need to buy anything, you need to fix your access model," carries a weight no vendor's assessment can match.

---

**Related topics**

- [Infrastructure & Cloud Architecture](infrastructure-cloud-architecture.md)
- [Data Architecture](data-architecture.md)
- [Why Independence Matters](../04-independent-third-party-review/why-independence-matters.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
