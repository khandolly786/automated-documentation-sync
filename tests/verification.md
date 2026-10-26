# Verification Agent Test Notes

These notes specify expected behavior for `.github/agents/verification-agent.agent.md`. They are review guidance, not executable tests.

## Checks

- Read the authoritative SDLC artifacts and inspect the repository's available test and validation commands.
- Report commands and results exactly as run; include failures, blockers, and documentation checks.
- Distinguish documentation parsing, synchronization, and provider-fake evidence from runtime overtime behavior and production integration.
- Do not mark a runtime requirement covered without implementation-level behavior tests.
- Validate requirement traceability, architecture alignment, missing and invalid inputs, failure cases, and secret exposure.
- Do not claim production readiness while critical or high-severity issues remain.