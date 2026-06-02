# UI UX Architect Web UI Implementation Prompt

This file contains the ALFIE web UI design and frontend implementation prompt.
It can be pasted directly into the corresponding chat.

```text
You are a senior UI/UX Architect, Product Designer, and Frontend Engineer.

Your task is to design and implement the ALFIE web UI.

ALFIE means:

Agent-Led Forensic Intelligence Engine

ALFIE is a persistent forensic operations platform for:

- Digital Forensics
- Incident Response
- eDiscovery
- Offensive Security
- Internal Investigations
- Evidence Analysis
- Workflow Automation
- Knowledge Management

The backend architecture, agents, workflows, queue management, state layers,
governance, operating principles, and guardrails already exist elsewhere in
the repository or are being implemented separately.

Your responsibility is ONLY the web UI.

Do not redesign backend architecture.

Do not redesign agent architecture.

Do not implement orchestration logic.

Do not implement queue management.

Do not implement OpenAI integration.

Do not modify governance or guardrails.

Do not modify existing agent definitions.

Focus exclusively on creating a high-quality frontend experience that can later
connect to backend APIs.

Before writing recommendation output, check the current issue map and backlog files.
Update or reference existing findings when they cover the same issue; create a
new recommendation file only for a materially new review angle.

--------------------------------------------------
CRITICAL IMPLEMENTATION CONSTRAINT
--------------------------------------------------

All frontend code must exist inside a single folder at the root of the
repository:

/webUI

Do not scatter frontend code throughout the repository.

Target structure:

repo-root/
\-- webUI/
    |-- package.json
    |-- README.md
    |-- public/
    |-- src/
    |-- components/
    |-- layouts/
    |-- pages/
    |-- services/
    |-- hooks/
    |-- assets/
    |-- styles/
    |-- mock-data/
    \-- etc

Keep everything self-contained.

Only request root-level changes if absolutely required.

--------------------------------------------------
PLATFORM IDENTITY
--------------------------------------------------

ALFIE is not a chatbot.

ALFIE is not a consumer AI assistant.

ALFIE is a forensic command platform.

Analysts operate ALFIE.

Agents work inside ALFIE.

Workflows run inside ALFIE.

Cases are managed through ALFIE.

The user should feel:

"I am operating a forensic operations platform."

NOT:

"I am chatting with an AI."

--------------------------------------------------
VISUAL DIRECTION
--------------------------------------------------

The UI should feel like:

- A cyber operations center
- A forensic command center
- A mission control platform

Inspired by:

- Hackers (1995)
- Ghost in the Shell
- The Matrix operator consoles
- WarGames
- Neuromancer
- Splunk
- Kibana
- Security Onion
- Velociraptor
- Maltego
- Bloomberg Terminal
- NOC/SOC environments

Target balance:

70% operational dashboard
20% analyst workstation
10% retro terminal influence

DO NOT create a fake full-screen terminal.

The platform must remain usable for analysts working all day.

--------------------------------------------------
VISUAL STYLE
--------------------------------------------------

Dark theme first.

Suggested palette:

Background:
- Near black
- Deep charcoal
- Dark graphite

Accent:
- Cyan
- Electric blue
- Teal

Status:
- Green = healthy
- Amber = warning
- Red = critical

Text:
- White
- Light gray

Characteristics:

- Dense information layouts
- Multi-pane interfaces
- Minimal wasted space
- Operational dashboards
- Activity streams
- Timelines
- Graphs
- Evidence chains
- Relationship views
- Status indicators

Avoid:

- Large empty cards
- Excessive whitespace
- Consumer SaaS design
- Generic AI chat interfaces
- Oversized rounded corners
- Playful design language

--------------------------------------------------
TECHNICAL STACK
--------------------------------------------------

Preferred stack:

- React
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- lucide-react
- recharts
- reactflow (where useful)

If a better stack is chosen, explain why.

Frontend should run with:

npm install
npm run dev

--------------------------------------------------
MOCK DATA
--------------------------------------------------

Assume backend APIs do not yet exist.

Create realistic mock data.

Store all mock data under:

/webUI/mock-data

Structure the application so API integration can be added later.

Create service layers and API abstraction where appropriate.

--------------------------------------------------
PRIMARY NAVIGATION
--------------------------------------------------

Top navigation:

- Operations
- Cases
- Agents
- Workflows
- Evidence
- Findings
- Approvals
- Activity
- Knowledge
- Administration

--------------------------------------------------
SCREENS TO IMPLEMENT
--------------------------------------------------

Create a working frontend prototype for:

1. Operations Dashboard
2. Cases Dashboard
3. Case Workspace
4. Agent Control Centre
5. Workflow Centre
6. Evidence Explorer
7. Findings Centre
8. Approval Centre
9. Activity Stream
10. Knowledge Centre
11. Administration

--------------------------------------------------
OPERATIONS DASHBOARD
--------------------------------------------------

Purpose:

Provide immediate visibility into ALFIE.

Display:

- System status
- Active cases
- Active workflows
- Agent activity
- Pending approvals
- Recent findings
- Alerts
- Queue status
- System health

This should feel like mission control.

--------------------------------------------------
CASES DASHBOARD
--------------------------------------------------

Display:

- Case list
- Search
- Filters
- Status
- Priority
- Assigned analysts
- Recent activity
- Workflow progress

--------------------------------------------------
CASE WORKSPACE
--------------------------------------------------

Most important screen.

Use a dense multi-pane layout.

Include:

- Case summary
- Status
- Timeline
- Findings
- Evidence references
- Workflow status
- Agent activity
- Notes
- Pending approvals
- Tool run history

This should feel like a forensic command center.

--------------------------------------------------
AGENT CONTROL CENTRE
--------------------------------------------------

Important:

The platform already has agents.

Do NOT create new agent architecture.

The UI should only represent existing agents.

Use mock data.

Display:

- Agent name
- Role
- Status
- Current task
- Assigned case
- Queue state
- Health
- Last activity
- Recent actions

Agents should appear as specialist operators.

Not chatbot avatars.

--------------------------------------------------
WORKFLOW CENTRE
--------------------------------------------------

Display:

- Workflow library
- Running workflows
- Workflow status
- Execution history
- Workflow relationships

--------------------------------------------------
EVIDENCE EXPLORER
--------------------------------------------------

Evidence must be traceable.

Display:

- Source
- Type
- Path/reference
- Hash
- Ingest time
- Linked findings
- Related evidence
- Timeline references

Include relationship views where appropriate.

--------------------------------------------------
FINDINGS CENTRE
--------------------------------------------------

Each finding should show:

- Finding statement
- Confidence
- Status
- Supporting evidence
- Supporting tools
- Supporting workflow
- Reviewer status
- Approval status

Support:

- Draft
- Reviewed
- Approved
- Final

--------------------------------------------------
APPROVAL CENTRE
--------------------------------------------------

Display:

- Pending approvals
- Approval history
- Risk level
- Impact
- Reasoning
- Related evidence
- Related workflow
- Related findings

Actions:

- Approve
- Reject
- Request changes

--------------------------------------------------
ACTIVITY STREAM
--------------------------------------------------

Should feel like a live mission operations console.

Display:

- Agent actions
- Workflow events
- Tool executions
- Approval events
- Findings updates
- Errors
- Warnings

Real-time style presentation using mock data.

--------------------------------------------------
KNOWLEDGE CENTRE
--------------------------------------------------

Display:

- Runbooks
- SOPs
- Governance
- Operating principles
- Wiki content

Support:

- Search
- Categories
- Recently viewed

--------------------------------------------------
ADMINISTRATION
--------------------------------------------------

Display:

- Platform settings
- User management
- Integrations
- Health
- Audit settings

Use mock data.

--------------------------------------------------
HUMAN-IN-THE-LOOP UX
--------------------------------------------------

The interface must clearly show:

- What ALFIE is doing
- What is running
- What is waiting
- What is blocked
- What requires approval
- What changed recently

Nothing important should happen invisibly.

Analysts should always be able to:

- Review
- Approve
- Reject
- Pause
- Resume
- Investigate

--------------------------------------------------
BRANDING
--------------------------------------------------

Use ALFIE branding throughout.

Examples:

- ALFIE Operations
- ALFIE Cases
- ALFIE Agents
- ALFIE Findings
- ALFIE Activity Stream
- ALFIE Workflows

The AI should feel like a coordinated forensic operating platform.

Not a single assistant.

--------------------------------------------------
DELIVERABLES
--------------------------------------------------

1. Inspect repository structure first.
2. Create /webUI.
3. Build a working frontend prototype entirely within /webUI.
4. Use mocked data.
5. Create reusable components.
6. Create layouts.
7. Create routing/navigation.
8. Create dark theme styling.
9. Create README containing:
   - stack used
   - setup instructions
   - run instructions
   - folder structure
   - mock data explanation
   - future API integration guidance

Do not modify unrelated backend files.

Do not modify agent definitions.

Do not modify workflow logic.

Do not modify orchestration logic.

Keep the frontend isolated, modular, and ready for future backend integration.
```

## Related Navigation

- [Expert audit prompts](README.md)
- [Expert recommendation issue map](../../../memory/sensory/Recommendations/2026-05-29-expert-recommendation-issue-map.md)
