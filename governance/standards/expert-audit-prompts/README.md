# Expert Audit Prompts

Purpose:
- formalize the recurring expert-review prompts used to assess Alfred
- keep the canonical prompt pack under governance instead of recommendation staging
- keep the recommendation-output path explicit: `memory\sensory\Recommendations`

Files:
- [base-audit-prompt.md](base-audit-prompt.md)
- [code-reviewer-audit-prompt.md](code-reviewer-audit-prompt.md)
- [prompt-engineer-audit-prompt.md](prompt-engineer-audit-prompt.md)
- [security-engineer-audit-prompt.md](security-engineer-audit-prompt.md)
- [devops-engineer-audit-prompt.md](devops-engineer-audit-prompt.md)
- [ai-engineer-audit-prompt.md](ai-engineer-audit-prompt.md)
- [dfir-expert-audit-prompt.md](dfir-expert-audit-prompt.md)
- [privacy-legal-compliance-reviewer-audit-prompt.md](privacy-legal-compliance-reviewer-audit-prompt.md)
- [qa-release-engineering-reviewer-audit-prompt.md](qa-release-engineering-reviewer-audit-prompt.md)
- [windows-platform-sre-operations-reviewer-audit-prompt.md](windows-platform-sre-operations-reviewer-audit-prompt.md)
- [m365-entra-administrator-audit-prompt.md](m365-entra-administrator-audit-prompt.md)
- [incident-response-operations-client-delivery-audit-prompt.md](incident-response-operations-client-delivery-audit-prompt.md)
- [licensing-procurement-reviewer-audit-prompt.md](licensing-procurement-reviewer-audit-prompt.md)
- [project-manager-audit-prompt.md](project-manager-audit-prompt.md)
- [governance-officer-audit-prompt.md](governance-officer-audit-prompt.md)
- [ui-engineer-audit-prompt.md](ui-engineer-audit-prompt.md)
- [product-architect-audit-prompt.md](product-architect-audit-prompt.md)

Usage:
- use `base-audit-prompt.md` when you want the shared review contract by itself
- use any role-specific file when you want a ready-to-paste standalone prompt
- if the expert writes a recommendation note, it should first check the current issue map and backlog files; update or reference existing findings when they
  cover the same issue, and create a new file under
  `memory\sensory\Recommendations` only for a materially new review angle

Coverage:
- engineering and implementation
  - code reviewer
  - prompt engineer
  - security engineer
  - DevOps engineer
  - AI engineer
- investigation and delivery
  - DFIR expert
  - incident response operations / client delivery reviewer
  - M365 / Entra administrator
- product and operator experience
  - UI/UX architect frontend implementation
  - product architect implementation planning
- governance and readiness
  - privacy / legal / compliance reviewer
  - QA / release engineering reviewer
  - Windows platform / SRE / operations reviewer
  - licensing / procurement reviewer
  - project manager
  - governance officer

## Related Navigation

- [Recommendation intake folder](../../../memory/sensory/Recommendations/README.md)
- [Expert recommendation issue map](../../../memory/sensory/Recommendations/2026-05-29-expert-recommendation-issue-map.md)
- [Governance standards](../README.md)
