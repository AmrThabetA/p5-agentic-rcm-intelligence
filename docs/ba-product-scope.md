# BA and Product Scope

P5 was shaped around three user groups with different decisions, permissions, and evidence needs.

## Users and needs

| User | Primary need | Product response |
|---|---|---|
| Executive/viewer | Fast financial visibility without record-level exposure | Aggregate KPIs, governed question answering, charts, and source details |
| RCM/AR analyst | Find recoverable denials before filing windows expire | Ranked queue, governed evidence, and human-reviewed appeal preparation |
| Admin/auditor | Reconstruct and challenge system activity | Version, evidence, role, and decision records |

## Requirements themes

- Governed, typed RCM queries rather than free-text SQL
- Recoverability ranking by eligible value and urgency
- Deterministic, versioned compliance verdicts
- Fail-closed blocking of unsupported numeric statements
- Role boundaries enforced outside the prompt
- Charts bound to stored query results
- Named-human approval before any external action
- Traceability from business requirement through specification, story, evidence, and UAT scenario
- Repeatable onboarding and rollback for configured data extracts

## Delivery artifacts

The controlled workspace contains:

- Vision, BRD, glossary/data dictionary, stakeholder register, and RACI
- Five as-is/to-be process narratives with conceptual maps; formal BPMN 2.0 remains planned
- Compliance, privacy, and security requirements
- RTM, RAID/decision log, and change-control record
- SRS with 50 system functional and 20 system non-functional requirements
- Nine fully dressed use cases and nine draft UML model specifications
- Nine Figma UI designs with an acceptance map
- Jira backlog with 10 epics and 52 stories, including acceptance criteria
- UAT plan with 12 scenarios and pending sign-off roles

## Delivery status

The documentation and backlog are draft/pre-baseline. Publication does not imply stakeholder approval, UAT acceptance, or release authorisation. The strongest implementation evidence currently covers the governed backend and configuration-driven data onboarding; the full application layer and product surfaces remain designed/not implemented.

Public exports should remove workspace identifiers, private comments, credentials, and personal information.
