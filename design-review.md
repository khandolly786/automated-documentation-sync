# Design Review

## Review Status

Review completed against the repository-root `requirements.md`, `architecture.md`, and `impl-plan.md`. The user selected the overtime-operations product scope on 2026-10-26. The architecture and plan now contain proposals for that scope; these proposals have not received formal human architecture or implementation-plan approval.

## Findings

### DR-001 — High: Overtime-operations scope requires approved architecture and implementation tasks

- **Evidence:** The requirements business context and FR-001 through FR-038 define runtime overtime eligibility, calculation, tracking, and submission. The user selected that operations scope. The architecture now proposes separate documentation-sync and overtime-operations workflows, and the implementation plan proposes new operations tasks. Neither proposal has formal architecture/plan approval, and no overtime calculation or request model exists in the implementation.
- **Impact:** Implementation against the expanded scope before approval could encode an unreviewed system boundary; treating existing policy parsing tests as operational coverage would leave required behavior unimplemented.
- **Recommendation:** Review and approve or revise the proposed architecture and operations tasks before implementation. Keep payroll execution, payment confirmation, and policy-exception authority out of scope unless separately approved; do not invent their `Not Found` values.
- **Disposition:** Scope selected by user; proposed architecture and plan pending human approval.

### DR-002 — Medium: Architecture and plan approval evidence must stay aligned

- **Evidence:** The previous plan said architecture/design approval was complete despite the design review marking approval pending. AD-001 and the plan now identify the revised operations boundary as proposed and pending approval.
- **Impact:** If future edits revert either artifact to an approved state without an approval record, implementation could proceed under an unapproved architecture.
- **Recommendation:** Record explicit human approval in both authoritative artifacts before unblocking downstream implementation tasks.
- **Disposition:** Status corrected in this proposal; human approval evidence remains pending.

### DR-003 — High: Sensitive-data access controls are not testable yet

- **Evidence:** NFR-004 requires protection of wage data, associate identifiers, approval evidence, and contact information, while marking the specific access-control requirements `Not Found`. The architecture recommends authentication, least privilege, encryption, and auditing, but the identity provider, reviewer roles, authorization model, and retention policy remain unresolved in the architecture and release-readiness document.
- **Impact:** The project cannot demonstrate who may view or change sensitive records, how reviewer authorization is enforced, or which tests prove those controls. This is a production security risk, even though the release-readiness document correctly lists related decisions as human-gated.
- **Recommendation:** Before production integration, obtain human approval for the identity provider, reviewer and administrator roles, sensitive-data access matrix, audit access, encryption/key boundary, and retention requirements. Convert the approved controls into testable requirements and verification cases; keep unresolved values as `Not Found`.
- **Disposition:** Open production blocker; human approval required.

## Review Coverage

| Area | Result |
|---|---|
| Requirements and architecture scope | User selected operations scope; proposed architecture and tasks require approval (DR-001) |
| Approval governance and traceability | Approval state is marked pending consistently; approval evidence remains required (DR-002) |
| Security and sensitive-data handling | Finding DR-003; production remains blocked |
| Reliability, failure handling, and publication gating | Architecture defines checkpoints, fail-closed behavior, idempotency, and human approval; provider-specific retry and publication choices remain human-gated |
| Requirement traceability | Proposed T37-T42 add runtime operations tasks; implementation coverage remains unverified until those tasks are approved and completed |
| Scalability and performance | Provider-neutral recommendations are documented; policy-change frequency and document volume remain `Not Found` |

## Approval

This review records analysis, the user's scope selection, and recommendations only. Approval or rejection of the proposed architecture and plan, and disposition of DR-003, remain `Pending`.