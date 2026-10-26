# Code Review Agent Test Notes

These notes specify expected behavior for `.github/agents/code-review-agent.agent.md`. They are review guidance, not executable tests.

## Checks

- Review changes against requirements, the currently approved architecture and plan, design-review findings, and applicable tests.
- Keep the review read-only; do not modify implementation while reviewing.
- Report actionable findings first, ordered by severity, with file, location, problem, impact, and recommended fix.
- Treat proposed or pending architecture decisions as unresolved; identify documentation claims that exceed implemented behavior.
- Distinguish test-double evidence from production integration and call out missing edge-case coverage.
- End the review with exactly `APPROVED` or `CHANGES REQUIRED`; neither result is human approval to publish.