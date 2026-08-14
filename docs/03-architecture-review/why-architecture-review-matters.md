# Why Architecture Review Matters

Architecture is made of the decisions that are expensive to reverse (see the [definition](../01-foundations/what-is-technical-architecture.md)). It follows that the cheapest moment to catch a wrong architectural decision is before it gets built. An architecture review is simply the deliberate act of creating that moment.

## The economics: problems get more expensive with distance

A flaw in a requirement or an architectural decision costs little to fix on paper, more during the build, and enormously more in production. Decades of software engineering research, going back to Boehm's early studies, puts the multiplier anywhere from 10 times to over 100 times, depending on how late the discovery comes. Architectural flaws sit at the extreme end of that curve because they are, by definition, the structural ones: the wrong database engine, the integration pattern that cannot scale, the vendor commitment with no way out. Nobody refactors their way out of those in a sprint.

A review that costs a few person-weeks routinely catches decisions whose reversal would cost person-years. That asymmetry is the entire business case, and it is not a subtle one.

## What review protects you against

**1. Honest mistakes.** Competent architects get things wrong: an untested assumption about load, a consistency requirement nobody wrote down, a technology limit that only shows up at scale. Review puts a second qualified mind on the problem while fixing it is still cheap.

**2. The author's blind spots.** The person who designed a system is the worst-placed person to find its flaws, because they see what they intended, not what they built. This is why code review is standard practice in every serious engineering organization. It is strange that many of those same organizations ship architectures, which cost a thousand times more to change than code, with no equivalent scrutiny at all.

**3. Decisions nobody made.** Some of the worst outcomes come not from wrong decisions but from decisions that were never consciously made. Exit strategy, data ownership, failure behavior: these default their way into existence. A structured review checks for the absence of decisions, which a delivery team, heads-down on what exists, rarely does.

**4. Interested advice.** When parts of the architecture were shaped by people with a revenue stake, whether vendors, resellers, or consultancies selling the build, review is what separates advice from advocacy. This is the subject of [Section 4](../04-independent-third-party-review/README.md), and it changes who is allowed to do the reviewing. Checking vendor-influenced decisions requires a reviewer who is not the vendor.

## What review is not

- **Not a gate for its own sake.** A review board that rubber-stamps everything, or nitpicks formatting, adds delay instead of assurance. The output of a real review is a ranked list of risks with concrete recommendations, not a pass or fail stamp.
- **Not an insult to the team.** Surgeons operate with checklists and pilots fly with cross-checks, not because anyone suspects them of incompetence, but because the stakes justify systematic error-catching. The same logic applies to million-dollar technical decisions.
- **Not just for new builds.** Existing systems often benefit the most. Reviewing a running system means testing its architecture against observed reality: incidents, costs, and how fast change actually happens, instead of predictions.

## When review matters most

Review earns its cost almost anywhere, but the leverage peaks when:

- A **major purchase or vendor commitment** is about to be signed, and the decision is about to become very expensive to reverse.
- A **system is about to scale** past the assumptions it was designed under.
- **Delivery is struggling** and nobody can agree on why.
- An **inherited estate** needs to be understood before money goes into it, for example in due diligence or after an acquisition.
- The architecture was **produced or heavily influenced by someone who profits from it.** In that case, review is not just useful. It is the only honest basis for the decision.

---

**Related topics**

- [The Review Process and Lifecycle](review-process-and-lifecycle.md)
- [Benefits and Outcomes](benefits-and-outcomes.md)
- [Why Independence Matters](../04-independent-third-party-review/why-independence-matters.md)

**Navigate:** [← Section index](README.md) · [↑ Home](../../README.md)
