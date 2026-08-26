# Sanitized Jira Story Samples

These examples were selected from the live P5RCM Jira backlog to show the story format, traceability, and acceptance discipline. Private links, account details, and comments are excluded. All three items are currently in **Idea**, carry the **draft-pre-baseline** label, and have **High** priority.

## P5RCM-11 / DS-001 — Server-side role capability enforcement

**Epic:** Governance, Security and Access Foundation  
**MoSCoW:** Must

**Story**

As an Information Security and Privacy Owner, I want every tool, route, and data request checked against the server-resolved session role before it executes, so that no user can reach data or functions outside their authority regardless of what they type.

**Acceptance criteria**

1. Capability is resolved before execution and ignores any role or authority claimed in prompt text.
2. A denied request identifies the required role class without revealing withheld data, record counts, or schema details.
3. The denial records the session, role, capability, and time.
4. Negative tests exercise viewer, analyst, and admin roles against every capability, with zero unauthorized grants.

**Trace sample:** BRD FR-05, NFR-03, SEC-04 → SRS SFR-012 → UC-02/04/05/08/09 → processes P-01/03/04 → Jira DS-001.

**Delivery boundary:** Backend role controls are implemented; production IAM and end-to-end application enforcement remain pending.

---

## P5RCM-40 / DS-030 — Recoverable-denial eligibility filtering

**Epic:** Denial Prioritisation and Evidence  
**MoSCoW:** Must

**Story**

As an RCM Analyst, I want only genuinely recoverable denials to enter my queue, so that I do not spend effort on claims that cannot be recovered.

**Acceptance criteria**

1. Claims failing an eligibility condition are excluded, and an exclusion reason is available for each claim.
2. Identical inputs produce the same eligible set on repeat execution.
3. Eligibility comes from the typed tool result; the agent cannot add or remove claims.
4. The result envelope records the ruleset version applied.

**Trace sample:** BRD FR-03 → SRS SFR-007 → UC-04 → Jira DS-030.

**Delivery boundary:** Filtering is implemented and covered by backend tests; the analyst-facing queue is not implemented.

---

## P5RCM-54 / DS-044 — End-to-end evidence lineage resolution

**Epic:** Audit, Lineage and Evidence  
**MoSCoW:** Must

**Story**

As an Auditor, I want to resolve any displayed figure or decision back to the source rows that produced it, so that the organisation can defend an output to a regulator or payer.

**Acceptance criteria**

1. A displayed figure, insight, or appeal claim resolves through the tool result and parameters to the semantic view and accepted data generation.
2. Every link records the version that was in force at the time.
3. A broken link is identified explicitly and is not presented as a complete lineage chain.
4. Historical outputs resolve against their original data generation rather than the current generation.

**Trace sample:** BRD FR-12 → SRS SFR-031/SFR-003 → UC-08 → Jira DS-044.

**Delivery boundary:** Result-envelope stamping exists; durable retrieval across superseded generations remains designed/not implemented.

## Why these samples

Together they demonstrate three central product controls: authorization is enforced outside the LLM, operational ranking is deterministic, and every material output is intended to remain traceable. They also show how P5 distinguishes backend evidence from complete end-to-end delivery.
