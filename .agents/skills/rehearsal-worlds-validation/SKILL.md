---
name: rehearsal-worlds-validation
description: Validate a scoped Rehearsal Worlds contribution using its domain invariants and reproducible evidence; apply the checks relevant to the saved task.
---

# Validate reproducible agent evaluation worlds

Read the exact task revision and select the checks that address its acceptance criteria. This skill does not expand a task to the entire roadmap or authorize future implementation. These are validation instructions, not claims of an existing product.

1. Define the customer-return scenario through source records in the support, order and inventory modules. Expected outcomes must come from world state, not the agent's self-reported success.

2. Record seed, world version, initial state and event order. Reset and replay twice; compare the task-relevant state and disclose nondeterministic boundaries.

3. Include a successful trace, a plausible but incorrect trace and an incomplete trace. The evaluator must distinguish them without reading a hidden answer exposed to the agent.

4. Inject only the declared faults and retain their timing: missing records, timeouts, duplicate actions and unavailable modules. Recovery must not silently reset an inconvenient failure.

5. Keep training examples and held-out variations separate. Describe what the synthetic world approximates; a score in it is not proof of reliability in a real organization.

For every selected check, record fixture/setup, actions, expected outcome, observed outcome and reproducible evidence. State which checks were not applicable and why; do not count unrun checks as passing.
