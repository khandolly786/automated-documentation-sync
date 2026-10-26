# Requirements Coverage Report

This report records provider-neutral end-to-end evidence for T36. Existing evidence covers documentation synchronization and test-double workflows; it does not demonstrate runtime overtime eligibility, compensation, request tracking, or submission. Approved tasks T37-T42 cover that outstanding work. Production provider, identity, repository, retention, and recovery decisions remain human-gated as defined in `impl-plan.md`.

| Requirement set | Documentation-sync evidence | Overtime runtime status |
|---|---|---|
| FR-001 to FR-002 | Catalog, required-input validation, synchronization, and end-to-end tests | Request/result records and runtime capture not implemented; planned T37 |
| FR-003 to FR-016 | Clarification records, input validation, review evidence, and approval-gate tests | Runtime eligibility and overtime approval workflow not implemented; planned T38 and T40 |
| FR-017 to FR-024 | Canonical policy, versioning, change detection, conflict, and unit tests | Compensation calculation not implemented; planned T39 |
| FR-025 to FR-030 | Change detection, clarification precedence, catalog linkage, and end-to-end tests | Scenario calculations and compensatory-off rules not implemented; planned T38-T39 |
| FR-031 to FR-035 | Policy parsing, catalog linkage, and documentation workflow tests | Overtime reporting and submission routing not implemented; planned T40-T41 |
| FR-036 to FR-038 | SYNC workflow, review, checkpoint, and namespace integration tests | Overtime statuses/history not implemented; planned T40 |
| FR-039 | Review/change-set rendering and unresolved-item approval-gate tests | Payment confirmation evidence remains `Not Found`; no payment evidence invented |
| NFR-001 to NFR-003 | Documentation artifacts, checkpoints, and regression tests | Runtime overtime records/calculation precision remain unverified; planned T37 and T39 |
| NFR-004 | Provider-neutral review authorization boundary tests | Overtime-data access controls are not implemented; detailed access model remains `Not Found` and human-gated |
| NFR-005 | Classification, provenance, clarification separation, and rendering tests | Runtime classification/status separation remains unverified; planned T37, T40 |

The end-to-end suite covers happy path, empty input, missing required inputs, conflicts, approval gating, publication failure using a fake, partial-run failure, and status separation.