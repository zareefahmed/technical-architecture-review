# Software / Application Architecture

## What it is

Software (or application) architecture is the internal structure of a single application or system: its components and modules, the boundaries between them, how they communicate, and the patterns that keep the code organized as it grows. Where [solution architecture](solution-architecture.md) decides which systems make up the answer, software architecture decides how each system is built inside.

## What it covers

- **Decomposition.** Modules, services, layers. Where the boundaries fall and why.
- **Architectural style.** Monolith, modular monolith, microservices, event-driven, serverless, or (most often) a deliberate mix.
- **Communication.** Synchronous versus asynchronous, APIs, events, shared data. And what happens between parts when something fails.
- **State and data ownership.** Which component owns which data, and how consistency is kept.
- **Cross-cutting concerns.** Logging, configuration, error handling, observability, and where authorization gets enforced.
- **Ease of change.** How well the structure supports the changes the business is likely to ask for.

## Key artifacts

- Component and container diagrams (the C4 model is a widely used convention)
- Interface and API contracts
- Decision records for the style and boundary choices
- Coding standards and dependency rules that keep the structure real over time

## Typical decisions

- Monolith or services, and if services, how many and along which boundaries
- Framework and language choices
- Synchronous chains or event-driven flows for the key transactions
- Where validation and authorization are enforced
- What gets bought as a library or SaaS versus written in-house

## What a reviewer looks for

- **Does the style fit the problem and the team?** Microservices for a five-person team, or an event mesh for a simple CRUD application, is complexity bought for no reason. A reviewer asks what quality attribute each piece of structural complexity actually buys.
- **Are the boundaries good?** Do components that change together live together? Are there hidden couplings, like shared databases or chatty interfaces, that contradict the diagram?
- **What happens on failure?** For each dependency: what happens when it is slow or down? Timeouts, retries, idempotency, backpressure.
- **How deep do vendor dependencies go?** How entangled is the business logic with a specific framework or a vendor's proprietary SDK? An application whose core logic imports a cloud vendor's libraries on every page has made an exit-cost decision without ever writing it down.
- **Does the code match the document?** Reviewers sample the actual codebase. A beautiful architecture the code ignores is a governance problem, not a documentation problem.

## A note on vendor neutrality

Software architecture seems far away from procurement, but vendor influence reaches it through proprietary SDKs, patterns built around specific managed services, and the "reference architectures" vendors publish. Reference architectures are useful teaching material, and they are also marketing. They show the vendor's services composed with each other, never with a competitor's. Adopting one wholesale means adopting a bundling decision nobody consciously made. The antidote is an explicit portability stance for each component: decide which parts are allowed to bind tightly to a vendor service (with the exit cost written down), and which parts must stay portable.

---

**Related topics**

- [Solution Architecture](solution-architecture.md)
- [Integration Architecture](integration-architecture.md)
- [Review Methods and Frameworks](../03-architecture-review/review-methods-and-frameworks.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
