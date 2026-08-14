# Integration Architecture

## What it is

Integration architecture is the design of how systems connect: the interfaces, protocols, message flows, and middleware through which independent systems exchange data and trigger each other's behavior. Almost no system stands alone. In most organizations the integration layer is the nervous system, and its quality decides how fast the whole estate can change.

## What it covers

- **Interface design.** APIs, events, files, shared data. Contracts and how they are versioned.
- **Interaction styles.** Request and response, publish and subscribe, batch. Synchronous chains versus asynchronous flows.
- **Middleware.** API gateways, message brokers, event streaming platforms, integration platforms. And whether each one is actually needed.
- **Consistency across systems.** Eventual consistency, idempotency, ordering, deduplication, reconciliation.
- **Failure behavior.** What happens when one side is down: queues, retries, dead letters, circuit breakers, compensations.
- **Third-party connections.** Partners, SaaS products, legacy systems. The messy edges.

## Key artifacts

- An integration catalog: every interface, its owner, its contract, its style, and how critical it is
- Interface contracts (OpenAPI, AsyncAPI, schema registries)
- Flow diagrams for the critical cross-system transactions
- A versioning and deprecation policy

## Typical decisions

- Point-to-point connections or a mediated setup with brokers and gateways, and where each is acceptable
- Whether to adopt an event streaming platform, and which one
- A shared canonical data model at the boundaries, or contracts per interface
- Building integrations in-house versus buying an integration platform
- How legacy systems get wrapped and, eventually, replaced

## What a reviewer looks for

- **Does the catalog exist?** An organization that cannot list its interfaces cannot know its own blast radius. This is a common finding, and a serious one.
- **Where is the hidden coupling?** Integrations that go around the official layer through shared databases or file drops. Synchronous chains where one slow system stalls five others.
- **Is there contract discipline?** Versioning, backward compatibility, consumer-driven tests. Or the alternative: deploy and pray.
- **Are the failure paths designed?** For each critical flow: what queues, what retries, what reconciles, and who gets paged.
- **Does the middleware earn its keep?** Does each middleware product justify its complexity and its license cost, or is it a leftover from an old sales cycle that everything must now route through?

## A note on vendor neutrality

Integration middleware has a special lock-in shape: the product embeds itself in every connection, so the cost of removing it grows with each integration built on top. The sales-agent pattern here is the platform tax. An enterprise service bus or integration platform gets sold as "strategic," and afterwards every project must budget for its licenses, its specialists, and its release calendar. Sometimes that trade is worth it. The review question is whether anyone ever actually evaluated it, and whether new integrations still pass the "would we choose this today?" test. Open protocols and standard contract formats (plain HTTP APIs, AsyncAPI, standard event schemas) are the counterweight that keeps your exit open. The more logic lives in portable contracts instead of proprietary flow definitions, the cheaper every future change, including the change called leaving.

---

**Related topics**

- [Software / Application Architecture](software-application-architecture.md)
- [Data Architecture](data-architecture.md)
- [Enterprise Architecture](enterprise-architecture.md)
- [Conflicts of Interest and Vendor Bias](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
