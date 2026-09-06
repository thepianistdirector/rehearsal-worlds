# Rehearsal Worlds: task contracts

Twelve proposed work packages, with named waves and dependency order. None is completed by publishing this document. The linked Tanduna revision is the contribution authority; this repository records the maintainer's intended contract while Tanduna's structured requirement support is being updated.

Every task below names its repository, branch, verified planning commit, preferred model, allowed fallback, immutable public skills, task-specific testing procedure and maintainer acceptance flow. A later implementation task still needs its prerequisite code, a rebased execution revision, narrow file scope and real functional commands. Do not treat the current planning commit as if that future code exists.

The allowed model pair is GPT-6 Astra and Claude Fable 5.1, with the effort stated per task. A model declaration is not independent runtime evidence; unresolved proof remains visible to the maintainer. See [CONTRIBUTING.md](CONTRIBUTING.md) and [the machine-readable authored contracts](task-contracts.json).

## W1-T1 — Model the customer-return world

**Wave:** W1 · **Prerequisites:** None; maintainer scope review first

Define support, inventory, order records, roles and allowed outcomes using synthetic data.

**Saved Tanduna task:** [W1-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_40a5200c086330612ee6214c257c0b3e)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Maintainer accepts the scoped design protocol; this is not product implementation.

**Preferred:** `gpt-6-astra` / medium. **Accepted fallback:** `claude-fable-5-1` / medium. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- The scenario includes an ordinary return, an ineligible return and an ambiguous policy case.
- Expected outcomes describe application state and permissions, not exact agent wording.

### Testing procedure

Trace one customer return across support, order and inventory records. Define the successful terminal state, a plausible incorrect state and an incomplete state using source records instead of agent narration.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W1-T2 — Define repeatable world reset

**Wave:** W1 · **Prerequisites:** W1-T1

Specify seeds, clocks, identities and initialization boundaries.

**Saved Tanduna task:** [W1-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_a49b8fa64275c81d80e2b1e47d07e3e2)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Two resets with the same version and seed produce equivalent starting conditions.
- No real customer data or live external delivery is required.

### Testing procedure

Specify a seed, initial records and event order, reset twice and compare expected world state. Include pending events and a failed prior attempt in the reset contract; identify nondeterministic boundaries.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T1 — Implement the three application modules

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2

Create usable synthetic support, stock and order interfaces and APIs.

**Saved Tanduna task:** [W2-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_0e255aa07580a378923efec11334b021)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A person can complete the full return workflow through the same surfaces available to the agent.
- Unauthorized actions fail in both interface and API paths.

### Testing procedure

Run a return through the three application modules and inspect each source record. Submit a missing-order reference and conflicting inventory action; verify consistent errors and unchanged unrelated records.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T2 — Implement reset and event replay

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2

Capture enough state transitions to reconstruct what occurred.

**Saved Tanduna task:** [W2-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_39c00ac768889da8c4512a886460e76d)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A run can be reset and its consequential events replayed in order.
- A failed run does not contaminate the next scenario.

### Testing procedure

Replay one recorded event stream twice from a reset world and compare task-relevant state. Interrupt replay, recover and repeat; record world version, seed and any intentionally variable fields.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T1 — Build outcome evaluators

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2

Check final state, authorization, duplicate effects and incomplete work.

**Saved Tanduna task:** [W3-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_c497eb7eb21257adfd700b1e3040c091)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A persuasive but incorrect agent answer fails the outcome check.
- Intentionally duplicated returns and unauthorized changes are detected.

### Testing procedure

Evaluate successful, plausible-wrong and incomplete traces against actual world state. Modify a wrong trace to claim success and confirm the evaluator still rejects it without exposing hidden answers to the agent.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T2 — Add controlled fault injection

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2

Introduce stale records, interruptions, conflicting instructions and service failures.

**Saved Tanduna task:** [W3-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_e3c99c050ae88241894accc9740f0e2f)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Each failure is reproducible and has an explicit expected safe outcome.
- Reports distinguish agent errors, environment errors and unsupported cases.

### Testing procedure

Inject each declared fault at a fixed event boundary and retain its schedule. Repeat with the same seed, then change only the fault; compare resulting state and ensure recovery does not erase the failure.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T1 — Publish a scenario and app module kit

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2

Document state models, interfaces, seed data and evaluator extensions.

**Saved Tanduna task:** [W4-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_18245e258e899590516f7b5b5fa4456f)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A contributor builds a second scenario without editing the runner core.
- Malformed modules fail validation before execution.

### Testing procedure

Have a second author add a scenario and module using the kit. Run valid and malformed packages in a fresh world; verify version errors and expected outcomes remain inspectable.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T2 — Build private world authoring

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2

Allow teams to model policies with synthetic or explicitly approved data.

**Saved Tanduna task:** [W4-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_7285183aaf92cc2743578089cbe2fb93)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Exports identify data provenance and do not include private data by default.
- Access controls separate world authors, evaluators and agent runs.

### Testing procedure

Author a synthetic private-world package from approved inputs, export and reopen locally. Inspect the data boundary and verify no private records are required in the public example or accidentally included in export.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T1 — Connect two agent runners

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Record budgets, tool access, environment versions and run conditions.

**Saved Tanduna task:** [W5-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_e34f26f0c581576d30cfacffe709d1d7)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Both runners operate against the same scenario and evaluator contract.
- Reports disclose retries and incomplete runs rather than hiding them.

### Testing procedure

Connect two distinct agent runners to the same world interface and compare action visibility and outcomes. Test cancellation and a runner that reports success without achieving the objective.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W5-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T2 — Test unseen scenario variations

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Create held-out variations and evaluate transfer across policy changes.

**Saved Tanduna task:** [W5-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_497369dafc83371f1c6cc3fd441f86cd)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Public examples and held-out evaluation cases remain distinct.
- A benchmark-specific shortcut fails a deliberately varied scenario.

### Testing procedure

Keep an unseen variation set separate from authoring examples. Run the evaluator on held-out cases and record per-case outcomes, including wrong but persuasive traces; document leakage checks and limitations.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W5-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T1 — Pilot continuous workflow regression

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Run a consented team's agent against versioned scenarios after changes.

**Saved Tanduna task:** [W6-T1](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_9bf5d8475fc6654fba8bb0cf39faba2a)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A known regression is caught before a real workflow is enabled.
- The team can trace a failure to a scenario, environment version and resulting state.

### Testing procedure

Run a workflow regression before and after an intentional behavior change. Show the failure, retained trace and reproducible reset; ask a pilot maintainer to diagnose it using only the published report.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W6-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T2 — Publish world maintenance and cost guidance

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Measure runtime cost, reset reliability and module maintenance effort.

**Saved Tanduna task:** [W6-T2](https://tanduna.com/p/rehearsal-worlds/tasks/tsk_60fae9c3b49727b53f1e2ab1e3630084)

**Repository:** [https://github.com/thepianistdirector/rehearsal-worlds](https://github.com/thepianistdirector/rehearsal-worlds) · **Branch:** `main`

**Planning base commit:** [`dc006b12a69d45ed600597f739b57540447de5f8`](https://github.com/thepianistdirector/rehearsal-worlds/commit/dc006b12a69d45ed600597f739b57540447de5f8)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Rehearsal Worlds validation](https://raw.githubusercontent.com/thepianistdirector/rehearsal-worlds/dc006b12a69d45ed600597f739b57540447de5f8/.agents/skills/rehearsal-worlds-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- An independent operator reproduces a published evaluation.
- Supported scope and simulation-to-reality limitations are visible beside results.

### Testing procedure

Have a second operator install, version, reset and retire a world package. Measure execution/storage cost for a fixed workload and document update compatibility, failed runs and unsupported real-world claims.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check dc006b12a69d45ed600597f739b57540447de5f8
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W6-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.
