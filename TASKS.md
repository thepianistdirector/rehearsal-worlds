# Rehearsal Worlds: proposed work packages

These are planning briefs. No task is complete or approved for automatic execution. Before implementation, maintainers must publish a scoped task revision with the actual repository, paths, tools and validation commands.

## W1-T1 — Model the customer-return world

**Wave:** W1 · **Status:** Planned · **Prerequisites:** None; begin with maintainer scope review

Define support, inventory, order records, roles and allowed outcomes using synthetic data.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- The scenario includes an ordinary return, an ineligible return and an ambiguous policy case.
- Expected outcomes describe application state and permissions, not exact agent wording.

## W1-T2 — Define repeatable world reset

**Wave:** W1 · **Status:** Planned · **Prerequisites:** W1-T1

Specify seeds, clocks, identities and initialization boundaries.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Two resets with the same version and seed produce equivalent starting conditions.
- No real customer data or live external delivery is required.

## W2-T1 — Implement the three application modules

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Create usable synthetic support, stock and order interfaces and APIs.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A person can complete the full return workflow through the same surfaces available to the agent.
- Unauthorized actions fail in both interface and API paths.

## W2-T2 — Implement reset and event replay

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Capture enough state transitions to reconstruct what occurred.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A run can be reset and its consequential events replayed in order.
- A failed run does not contaminate the next scenario.

## W3-T1 — Build outcome evaluators

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Check final state, authorization, duplicate effects and incomplete work.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A persuasive but incorrect agent answer fails the outcome check.
- Intentionally duplicated returns and unauthorized changes are detected.

## W3-T2 — Add controlled fault injection

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Introduce stale records, interruptions, conflicting instructions and service failures.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Each failure is reproducible and has an explicit expected safe outcome.
- Reports distinguish agent errors, environment errors and unsupported cases.

## W4-T1 — Publish a scenario and app module kit

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Document state models, interfaces, seed data and evaluator extensions.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A contributor builds a second scenario without editing the runner core.
- Malformed modules fail validation before execution.

## W4-T2 — Build private world authoring

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Allow teams to model policies with synthetic or explicitly approved data.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Exports identify data provenance and do not include private data by default.
- Access controls separate world authors, evaluators and agent runs.

## W5-T1 — Connect two agent runners

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Record budgets, tool access, environment versions and run conditions.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Both runners operate against the same scenario and evaluator contract.
- Reports disclose retries and incomplete runs rather than hiding them.

## W5-T2 — Test unseen scenario variations

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Create held-out variations and evaluate transfer across policy changes.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Public examples and held-out evaluation cases remain distinct.
- A benchmark-specific shortcut fails a deliberately varied scenario.

## W6-T1 — Pilot continuous workflow regression

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Run a consented team's agent against versioned scenarios after changes.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A known regression is caught before a real workflow is enabled.
- The team can trace a failure to a scenario, environment version and resulting state.

## W6-T2 — Publish world maintenance and cost guidance

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Measure runtime cost, reset reliability and module maintenance effort.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- An independent operator reproduces a published evaluation.
- Supported scope and simulation-to-reality limitations are visible beside results.
