# The Scope of Architecture in Technical Projects

Architecture is not a phase that ends when the diagrams get approved. In a real project it is a thread that runs from the first feasibility conversation all the way to decommissioning, and it covers every decision that would be expensive to reverse. This chapter maps out that territory, so a review knows what it is responsible for.

## Architecture across the project lifecycle

| Project stage | The architectural work | What goes wrong when it is skipped |
|---|---|---|
| **Inception / feasibility** | Frame the problem. Identify constraints, quality attributes, and rough options. Estimate cost ranges. | The project commits to a solution before anyone understands the problem. |
| **Selection / procurement** | Evaluate candidate technologies and vendors against the requirements. Run a fair comparison. | Requirements get written after the product is chosen, shaped to fit it. |
| **Design** | Define components, interfaces, data flows, and deployment. Record decisions and trade-offs. | Structure emerges by accident from whoever writes code first. |
| **Build** | Guard the decisions. Keep the implementation consistent with the architecture, and update the architecture when reality proves it wrong. | The architecture and the system quietly drift apart. The documents describe a system that does not exist. |
| **Operation** | Check whether the promised qualities are actually being delivered. Manage capacity, cost, and technical debt. | Costs drift, incidents repeat, and nobody owns the "why". |
| **Evolution / exit** | Plan major changes, migrations, and eventual replacement. Keep exit costs known and manageable. | The organization discovers it is locked in only when it tries to leave. |

Two of these stages deserve special attention, because they are where vendor influence concentrates:

- **Selection and procurement** is where the "sales agent" problem strikes first. If the architecture function is absent or weak here, products get chosen based on relationships, demos, and bundled discounts. Everything downstream inherits that choice.
- **Evolution and exit** is where the bill arrives. Exit cost is an architectural property, and it gets decided (usually by nobody deciding anything) years before it has to be paid.

## What sits inside the scope

In a typical technical project, the architecture covers:

- **Structural decisions.** Components, boundaries, interfaces, and how responsibilities are divided.
- **Technology choices.** Languages, frameworks, databases, platforms, cloud services, and third-party products.
- **Integration decisions.** How this system connects to everything else. See [Integration Architecture](../02-types-of-architecture/integration-architecture.md).
- **Data decisions.** Who owns which data, how it is modeled, kept, moved, and protected. See [Data Architecture](../02-types-of-architecture/data-architecture.md).
- **Deployment and operations decisions.** Where and how the system runs. See [Infrastructure & Cloud Architecture](../02-types-of-architecture/infrastructure-cloud-architecture.md).
- **Security decisions.** Identity, access, trust boundaries, and defenses. See [Security Architecture](../02-types-of-architecture/security-architecture.md).
- **Commercial and technical decisions together.** Licensing models, vendor commitments, support arrangements, and exit strategy. These count as architecture because they constrain your future technical choices just as hard as any interface does.

## What sits outside the scope

Architecture should not swallow everything. Project management (schedule, staffing), product management (which features to build), and detailed design inside components belong to their own disciplines. An architecture that tries to control every decision becomes a bottleneck. One that controls nothing is decoration. The discipline is simple: own the expensive-to-reverse decisions, delegate the rest, and be clear about which is which.

## A practical artifact: the scope statement

Every project benefits from a one-page architecture scope statement. It lists the decision areas the architecture owns, the quality attributes it commits to, and the constraints it works under. Reviews get much more effective when this exists, because the reviewer can then check for completeness. They can ask: which expensive decisions were never consciously made? That question matters more than auditing the decisions that were made. The [Architecture Review Checklist](../05-templates-and-checklists/architecture-review-checklist.md) is built to surface exactly these gaps.

---

**Related topics**

- [What Is Technical Architecture?](what-is-technical-architecture.md)
- [The Review Process and Lifecycle](../03-architecture-review/review-process-and-lifecycle.md)
- [Conflicts of Interest and Vendor Bias](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
