# Rehearsal Worlds roadmap

This is a public planning repository. There is no product implementation or playable build yet. The image is an AI-generated vision reference, not a screenshot. All waves and tasks are proposed; no completed work, community approval or funding is implied.

The order reflects dependencies, not calendar commitments. Each wave advances only when its stated outcome is demonstrated and a maintainer accepts the next scope. Capacity targets are hypotheses to test.

## W1 — One company you can reset

Specify a complete business scenario and its ground truth.

- **W1-T1: Model the customer-return world.** Define support, inventory, order records, roles and allowed outcomes using synthetic data.
- **W1-T2: Define repeatable world reset.** Specify seeds, clocks, identities and initialization boundaries.

## W2 — A working rehearsal environment

Build the reference world and observation surface.

- **W2-T1: Implement the three application modules.** Create usable synthetic support, stock and order interfaces and APIs.
- **W2-T2: Implement reset and event replay.** Capture enough state transitions to reconstruct what occurred.

## W3 — Score the work, not the performance

Make success and failure independently checkable.

- **W3-T1: Build outcome evaluators.** Check final state, authorization, duplicate effects and incomplete work.
- **W3-T2: Add controlled fault injection.** Introduce stale records, interruptions, conflicting instructions and service failures.

## W4 — Teams can author their own worlds

Turn the fixture into an extensible product.

- **W4-T1: Publish a scenario and app module kit.** Document state models, interfaces, seed data and evaluator extensions.
- **W4-T2: Build private world authoring.** Allow teams to model policies with synthetic or explicitly approved data.

## W5 — Comparable across agents and versions

Make evaluations reproducible without encouraging benchmark gaming.

- **W5-T1: Connect two agent runners.** Record budgets, tool access, environment versions and run conditions.
- **W5-T2: Test unseen scenario variations.** Create held-out variations and evaluate transfer across policy changes.

## W6 — A maintained laboratory of work

Prove practical value and keep worlds current.

- **W6-T1: Pilot continuous workflow regression.** Run a consented team's agent against versioned scenarios after changes.
- **W6-T2: Publish world maintenance and cost guidance.** Measure runtime cost, reset reliability and module maintenance effort.

See [TASKS.md](TASKS.md) for observable acceptance criteria.
