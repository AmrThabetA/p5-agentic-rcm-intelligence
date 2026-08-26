# Evaluation Summary

P5 separates backend verification, dry-run validation, live model evaluation, and business UAT. They are different evidence types and should not be presented as interchangeable.

## Recorded evidence

| Evidence | Result | What it establishes |
|---|---:|---|
| Automated test suite | 245 passing | Backend tools, semantic views, permissions, grounding, and Gen2 onboarding controls passed an isolated run on 20 Aug 2026 |
| Golden-set dry run | 55/55 | Harness schema, dispatch, and stored-truth validation passed with zero live model calls |
| Full live evaluation | 49/55 automated passes | Three items were human-adjudicated and three automated checks failed |
| Targeted live follow-up | 2 items passed | Two selected items passed; the full 55-item set and one open item were not rerun |

## Behaviours covered

- Typed tools return governed results for valid inputs and reject invalid parameters.
- Semantic-view aggregates reconcile to source data.
- Viewer, analyst, and admin capabilities are enforced in code.
- Unsupported numeric statements fail closed.
- Charts must reference an existing query result.
- Configured replacement extracts pass validation, version stamping, truth generation, and rollback controls.
- Unsafe or out-of-scope requests are evaluated through the golden set and attack cases.

## Evidence boundary

The automated suite and dry run support the implemented backend. They do not demonstrate the unimplemented UI/API workflows, production authentication, persistent audit service, complete appeal workflow, operational readiness, or business acceptance.

UAT is planned but has not been executed or approved. The repository should therefore avoid “release-ready,” “production-ready,” or “100% accurate” claims unless later evidence supports them.
