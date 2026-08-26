# Public Glossary Sample

This is a concise, sanitized sample of the draft P5 glossary. Definitions are based on synthetic portfolio data and require business/data-owner validation before production use.

| Term | Working definition | Status note |
|---|---|---|
| Revenue Cycle Management (RCM) | Operational and financial activities covering claim preparation, submission, payment, denial management, accounts receivable, and recovery | Business interpretation requires stakeholder validation |
| Recoverable denial | An eligible denied claim still within the configured filing window and ranked using governed inputs | Backend definition implemented; business eligibility and filing window need validation |
| Expected recoverable value | Claim amount multiplied by the governed overturn probability for the denial reason | Calculated in tested code, not by the LLM |
| Revenue leakage | In the synthetic RCM dataset, claim amount less amount paid | Demonstration definition only |
| Semantic view | A predefined, parameterized calculation over an approved source; no free-text SQL | Implemented |
| Deterministic rules engine | Versioned code that produces compliance verdicts from approved rules | Implemented backend; production rules need approval |
| Grounding validator | A fail-closed control that checks numeric statements against trusted tool results or approved constants | Implemented |
| Result envelope | Standard tool output containing the result plus source, parameters, query ID, time, and version metadata | Implemented pattern |
| Evidence lineage | Metadata connecting an output to its source, query, parameters, execution time, and applicable versions | Partly implemented end to end |
| Human in the loop | A named, authorized human must approve an external action | Safety principle established; complete workflow not implemented |
| Dry-run evaluation | Validation of the harness, tools, and stored truths without a live model call | Implemented |
| UAT | Business acceptance testing against approved scenarios and expected results | Planned; not executed |
