# Data Architecture

## What it is

Data architecture is the design of how an organization's data is modeled, stored, moved, governed, and used. It answers questions like: what data do we have, where does it live, who owns it, how does it flow between systems, how do we keep it correct and safe, and how do we make it useful for operations and analytics.

One fact shapes everything in this domain: data outlives applications. Systems get replaced every five to ten years. The data they manage often lives for decades. That makes data decisions some of the most expensive-to-reverse decisions in the whole architecture, and it makes data the strongest lock-in surface a vendor can own.

## What it covers

- **Data models.** Conceptual, logical, and physical models, plus agreed definitions of core entities like customer, product, and order.
- **Storage and platforms.** Operational databases, warehouses and lakehouses, caches, object storage, and whether each engine fits its workload.
- **Data movement.** Pipelines, ETL and ELT, streaming, replication. Batch versus real time.
- **Ownership and governance.** Which system is the source of truth for each entity. Stewardship, quality rules, master data.
- **Lifecycle.** Retention, archiving, deletion, and the legal obligations around them, like privacy law and data residency.
- **Consumption.** Analytics, reporting, APIs, machine learning, and who gets access to what.

## Key artifacts

- Entity and domain models, and data dictionaries
- Data flow diagrams and lineage documentation
- A source-of-truth register mapping each entity to its owning system
- Retention and classification policies
- Platform selection records with the workload reasoning behind them

## Typical decisions

- Which database engines (relational, document, key-value, graph, columnar) for which workloads
- One warehouse or lakehouse platform or several, and which one
- A centralized data platform or federated domain ownership (data mesh style)
- Where transformation logic lives, and in what tooling
- Residency and sovereignty: which countries the data is allowed to sit in

## What a reviewer looks for

- **Is the source of truth clear?** Does every core entity have exactly one authoritative system? Duplicated ownership is the root of most data quality misery.
- **Do the engines fit the workloads?** Was the database chosen for the job, or was the job bent to fit a license the company already owned? Both happen.
- **How fragile are the pipelines?** How many hops between source and consumption? What breaks silently? Who notices?
- **Is compliance real?** Are retention and deletion actually implemented, or do they only exist in a policy document? Could the organization honor a deletion request end to end?
- **What would leaving cost?** This is the sharpest vendor question in the data domain. What would it cost, in fees, time, and re-engineering, to move the data and its transformation logic somewhere else? Proprietary storage formats, proprietary transformation dialects, and per-gigabyte egress pricing are the three classic lock-in mechanisms. A data architecture with no written answer to "how would we leave?" has quietly answered "we can't."

## A note on vendor neutrality

Data platform vendors compete hardest for the center of the architecture, the warehouse or lakehouse everything flows through, because whoever owns the center taxes every flow. Sales-agent architecture in this domain looks like this: the platform gets chosen before the workloads are understood; "free" migration help rewrites your pipelines into the vendor's proprietary dialect; and consumption pricing gets modeled at pilot scale instead of production scale. An independent reviewer prices year three, not month three.

---

**Related topics**

- [Integration Architecture](integration-architecture.md)
- [Infrastructure & Cloud Architecture](infrastructure-cloud-architecture.md)
- [Vendor-Bias Red Flags](../05-templates-and-checklists/vendor-bias-red-flags.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
