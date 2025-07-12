# Collaboration Guidelines

Effective collaboration ensures narrative consistency, production efficiency, and creative alignment across departments. This document outlines the collaborative principles, communication protocols, and task management practices adopted by Tokari Works.

## 1. Team Roles & Interfaces

Collaboration is cross-functional by design. Core roles include:

- **Narrative Team**: Lead Writer, Scene Writers, Narrative Editors  
- **Programming Team**: Systems Writers, Engine Integrators  
- **Art Team**: Character Artists, Background Artists, UI Designers  
- **Production Team**: Project Managers, Producers, QA

Each team is autonomous in its scope, but communication between them is structured and continuous.

## 2. Communication Protocols

### 2.1. Tools

- **GitHub Issues & Pull Requests**: Feature tracking, feedback, and approvals  
- **Notion / Confluence**: Documentation, planning boards, shared calendars  
- **Discord**: Daily async status updates, team channels, direct queries

### 2.2. Meeting Cadence

- **Weekly Syncs**: Interdisciplinary alignment, milestone updates  
- **Bi-weekly Reviews**: Focused on narrative, scene QA, and visual consistency  
- **On-Demand Breakouts**: Issue-specific problem solving

### 2.3. Communication Standards

- Use thread-based discussions for traceability  
- Provide actionable feedback (what/why/how)  
- Keep summaries concise and decisions logged

## 3. Writing Collaboration Practices

### 3.1. Version Control

- Writers push to `feature/write/scene_label` branches  
- Revisions occur via GitHub Pull Requests with proper labels (`draft`, `review`, `finalize`)

### 3.2. Review Protocol

- Minimum two reviewers per PR: Narrative Editor + Systems Writer (if logic involved)  
- Inline comments required for all content suggestions  
- Suggestions must be accepted, modified, or rejected with justification

### 3.3. Draft Ownership

- Scene Writers retain ownership until `finalize/` stage  
- Major rewrites require author consultation  
- Lead Writer resolves deadlocks when consensus fails

## 4. Cross-Team Integration

### 4.1. Art × Narrative

- Art requests initiated via scoped briefs tied to approved scripts  
- Artists flag inconsistencies with narrative cues during review

### 4.2. Programming × Narrative

- Systems Writers assist in logic modeling (flags, conditions, state transitions)  
- Writers provide logic maps and variable definitions alongside scene drafts

### 4.3. QA × All Teams

- QA logs narrative, visual, and logic bugs into GitHub  
- Writers and developers triage issues by type and severity

## 5. Conflict Resolution

- Escalate unresolved issues to the Project Manager or Lead Writer  
- Use written proposals for alternative solutions  
- Prioritize narrative coherence, production feasibility, and player experience

## 6. Documentation & Accountability

- All feedback and approvals must be logged in version control tools  
- Changelogs accompany merges and releases  
- Ownership, contributions, and sign-offs are tracked at the file level
