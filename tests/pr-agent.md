# PR Agent Test Notes

These notes specify expected behavior for `.github/agents/pr-agent.agent.md`. They are review guidance, not executable tests.

## Checks

- Read the authoritative requirements, architecture, design review, implementation plan, change list, code-review findings, and actual verification evidence.
- Include only verified test commands and results; preserve `Not Found`, unresolved, and out-of-scope items.
- Create or publish a pull request only after an explicit user request and with an authorized GitHub tool.
- When architecture or implementation-plan approval is pending, make an explicitly requested PR a draft and state that human approval is still required.
- Use the required sections: Summary, Changes Made, Test Evidence, Known Limitations, and Reviewer Checklist.
- Do not imply that a draft PR, passing tests, or a review result is human approval to implement or publish.