# Product Architect Implementation Planning Prompt

This file contains the product-architecture planning prompt for converting
Alfred into a persistent web-based forensic agent platform. It can be pasted
directly into the corresponding chat.

```text
You are a senior Product Architect.

Your task is to create a clear implementation plan to convert this repo into a
persistent web-based forensic agent platform.

Current state:
- The repo already contains agents, workflows, scripts, governance or operating
  principles, wiki content, queue management, state layers, and guardrails.
- The repo remains the source of truth.
- I do not want runtime use to depend on ChatGPT or Codex Desktop.
- I want a persistent backend service with a web UI that uses the OpenAI API
  from the backend only.

Goal:
Produce a practical implementation plan only. Do not code yet.

The plan should cover:
1. Target architecture
2. Components to add
3. Components to reuse from the repo
4. Backend API design
5. Web UI design
6. Persistent runtime design
7. Queue or worker design
8. OpenAI API integration approach
9. Tool or script execution model
10. Approval workflow
11. Audit logging
12. Evidence integrity and scope controls
13. Database or state model
14. Local development setup
15. Security considerations
16. Testing strategy
17. Phased implementation roadmap
18. Risks, assumptions, and open questions

Important constraints:
- Frontend must never call OpenAI directly.
- The model must not directly execute shell commands.
- Existing governance and guardrails must not be bypassed.
- Evidence should be referenced by path, hash, metadata, or extracted
  summaries, not stored directly in LLM context.
- Every tool run and agent action must be auditable.
- Prefer boring, maintainable architecture over clever agent complexity.

Instructions:
- Start by inspecting the repo structure.
- Treat the existing repo as the source of truth for current capabilities and
  constraints.
- Before writing recommendation output, check the current issue map and backlog files.
  Update or reference existing findings when they cover the same issue; create a
  new recommendation file only for a materially new review angle.
- Reuse existing scripts, workflows, catalogs, governance, and control-plane
  concepts where practical instead of redesigning them from scratch.
- Identify what should remain repo-owned and what should move into persistent
  runtime services.
- Distinguish clearly between:
  - what already exists,
  - what can be wrapped or exposed,
  - what must be added,
  - what should be deferred.
- Do not produce generic SaaS architecture. This is a forensic operations
  platform with analyst control, approvals, evidence boundaries, and durable
  auditability.
- Do not redesign the investigative methodology. Focus on platform
  implementation structure.

Output format:
1. Executive summary
2. Recommended target architecture
3. Current repo assets to reuse
4. New components to add
5. Detailed implementation plan by area
6. Phased roadmap
7. Risks, assumptions, and open questions

Be concrete.
Prefer explicit component boundaries, service responsibilities, and data flows.
Where useful, name likely modules, services, API groups, and runtime
responsibilities.
```

## Related Navigation

- [Expert audit prompts](README.md)
- [Expert recommendation issue map](../../../memory/sensory/Recommendations/2026-05-29-expert-recommendation-issue-map.md)
