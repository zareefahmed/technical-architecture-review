# What Is Technical Architecture?

Technical architecture is the set of important decisions about a system. Specifically, the decisions that are expensive to change once they are made. It defines the shape of a solution: its parts, how they talk to each other, the technologies they run on, and the qualities the whole thing must have, like performance, security, availability, cost, and maintainability.

Here is a simple test for whether something is an architectural decision. Ask yourself: if we got this wrong, how much would it cost to reverse in a year? Choosing a variable name costs nothing to reverse. Choosing a database engine, an integration pattern, a cloud provider, or an identity model can cost months of work and a lot of money. Those are architecture.

## Architecture is decisions, not diagrams

Diagrams and documents are pictures of the architecture. They are useful, but the architecture itself is the body of decisions and the reasoning behind them. This matters for review. A reviewer who only looks at diagrams is reviewing the drawing. A reviewer who digs into the decisions and their justifications is reviewing the architecture.

Every significant decision has three parts worth writing down:

1. **The decision itself.** What was chosen.
2. **The context.** The requirements and constraints that made a choice necessary.
3. **The trade-off.** What was given up, and which alternatives were rejected and why.

When that third part is missing, when there is a chosen product but no record of rejected alternatives, that is often the first sign the "architecture" was built backwards. It started from a product instead of a problem. We come back to this idea again and again, and it gets its full treatment in [Not a Sales Agent](../04-independent-third-party-review/not-a-sales-agent.md).

## Architecture vs. design vs. implementation

| Level | What it deals with | Cost to change | Example |
|---|---|---|---|
| **Architecture** | System structure, technology choices, quality attributes | High. Weeks to months. | "Events flow through a message broker, and each service owns its own data." |
| **Design** | Structure inside a component | Moderate. Days to weeks. | "The order service uses a state machine for order status." |
| **Implementation** | Code-level choices | Low. Hours to days. | "This function uses a hash map instead of a list." |

The line between these levels is blurry, and it moves depending on context. In a small project the database schema might be architectural. In a large one it might be local design. What matters is that a team knows which of its decisions are the expensive ones, because those deserve careful analysis and independent review.

## Quality attributes: the real subject of architecture

Functional requirements like "the system lets a customer place an order" rarely drive architecture. Almost any structure can eventually deliver a feature. What actually drives architecture is the non-functional requirements, usually called quality attributes:

- **Performance and scalability.** How fast, for how many users, growing how quickly.
- **Availability and resilience.** What happens when parts fail.
- **Security and privacy.** Who can do what, and how data is protected.
- **Cost.** The cost to build, the cost to run, and the total cost of ownership over years.
- **Maintainability.** How hard the system is to change tomorrow.
- **Portability and exit cost.** How hard it is to leave a technology or a vendor.

That last one gets far less attention than it deserves, and it is exactly the attribute a vendor-aligned architect has every reason to ignore. An architecture that meets every launch-day requirement but cannot be exited is not a good architecture. It is a well-decorated dependency.

## Why this definition matters for review

Since architecture is the set of expensive-to-reverse decisions, an architecture review is really a review of decisions before they become expensive. It asks: were the right questions posed? Were real alternatives considered? Do the trade-offs serve the organization that has to live with them? These questions are hardest to answer honestly when the person who made the decisions, or the vendor who profits from them, is the one answering. That is the case we build in [Section 4](../04-independent-third-party-review/README.md).

---

**Related topics**

- [The Scope of Architecture in Technical Projects](scope-of-architecture-in-projects.md)
- [The Role of the Architect](role-of-the-architect.md)
- [Why Architecture Review Matters](../03-architecture-review/why-architecture-review-matters.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
