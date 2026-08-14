# Enterprise Architecture

## What it is

Enterprise architecture (EA) is the practice of describing and steering an organization's entire technology landscape. All of its systems, data, platforms, and how they relate to what the business does. The goal is to make sure individual projects add up to a coherent whole instead of an accidental collection.

Where a project asks "how do we build this system?", EA asks "how do all our systems, together, serve the business, today and over the next five years?"

## What it covers

- **Business and IT alignment.** Mapping business capabilities to the systems that support them, and finding the gaps and the duplicates.
- **The application portfolio.** What exists, what it costs, and what should get investment, be tolerated, or be retired.
- **Standards and reference architectures.** The approved technologies, patterns, and platforms that projects are expected to use, plus a sane exception process for when they should not.
- **Roadmaps and transitions.** The sequence of change from the landscape you have to the one you want.
- **Governance.** The forums and decision rights (including architecture review boards) through which architectural decisions get made and enforced.

Well-known frameworks include TOGAF and the Zachman Framework. Most real organizations use a pragmatic subset rather than a full framework, and that is fine.

## Key artifacts

- Capability maps and application portfolio inventories
- Descriptions of the target state and the transition states on the way there
- A technology standards catalog and reference architectures
- Architecture principles: short, memorable rules of the road
- Roadmaps

## Typical decisions

- Buy, build, or reuse for a needed capability
- Consolidating duplicate systems after growth or an acquisition
- Approving (or forbidding) a new platform for organization-wide use
- Strategic vendor relationships, and how concentrated they are allowed to get

## What a reviewer looks for

An independent reviewer looking at enterprise architecture asks:

- **Is the portfolio honest?** Does the inventory reflect reality or an aspiration? Are running costs and technical debt visible for each system?
- **Where did the standards come from?** Were the standard technologies chosen through fair comparison, or did they crystallize around whichever vendor had the strongest account team? The standards catalog is the most leveraged place for vendor capture in the whole organization, because it pre-decides every future project's shortlist.
- **How concentrated is the vendor risk?** What fraction of critical capabilities depends on a single vendor? Is that concentration a decision or an accident? Is there an exit position for each strategic vendor?
- **Does governance have teeth, and limits?** Does the review board actually change outcomes? And can projects get timely exceptions when the standards genuinely do not fit?
- **Is the roadmap real?** Are the transition states funded and sequenced, or is the target state just a poster on the wall?

## How it relates to solution architecture

EA sets the context that [solution architecture](solution-architecture.md) works within: the standards a solution must follow, the systems it must connect to, and the direction it must not contradict. When EA is healthy, it protects solution architects from vendor pressure. "Our standards require a fair comparison" is a powerful shield. When EA has itself been captured by a vendor, it does the opposite. It hard-codes the sales agent's conclusion into policy.

---

**Related topics**

- [Solution Architecture](solution-architecture.md)
- [The Scope of Architecture in Technical Projects](../01-foundations/scope-of-architecture-in-projects.md)
- [Conflicts of Interest and Vendor Bias](../04-independent-third-party-review/conflicts-of-interest-and-vendor-bias.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
