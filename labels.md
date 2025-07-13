# Labeling System Guidelines

This document defines the official label system used across Tokari Works repositories to manage issues, pull requests, and workflows consistently. Labels help clarify scope, status, priority, and team ownership.

## Label Categories

### 1. `type/*`
Describes the nature of the issue or contribution.

| Label             | Description                              |
|------------------|------------------------------------------|
| `type:feature`    | New functionality or enhancement         |
| `type:bug`        | Defect or unintended behavior            |
| `type:refactor`   | Code or script cleanup, non-functional   |
| `type:design`     | Visual/UI-related task                   |
| `type:documentation` | Docs, guidelines, READMEs, etc.      |
| `type:localization` | Translation or language adaptation     |
| `type:audio`      | Soundtrack, SFX, voice, etc.             |

### 2. `status/*`
Represents workflow stage or resolution status.

| Label             | Description                              |
|------------------|------------------------------------------|
| `status:triage`   | Needs initial review or assignment       |
| `status:in-progress` | Actively being worked on              |
| `status:blocked`  | Waiting on external or unresolved input  |
| `status:review`   | Awaiting code/design/narrative review    |
| `status:complete` | Task or PR is complete                   |
| `status:duplicate`| Already tracked in another issue         |
| `status:invalid`  | Not a valid task or error                |

### 3. `priority/*`
Indicates urgency and criticality.

| Label             | Description                              |
|------------------|------------------------------------------|
| `priority:high`   | Critical or time-sensitive               |
| `priority:medium` | Important but not urgent                 |
| `priority:low`    | Minor enhancement or fix                 |

### 4. `team/*`
Specifies the responsible team.

| Label               | Applied When...                                       |
|--------------------|--------------------------------------------------------|
| `team:art`          | Task is owned by the visual/design team               |
| `team:narrative`    | Task involves writing, scripting, emotional structure |
| `team:engineering`  | Task involves tools, engine, or infrastructure        |
| `team:sound`        | Task is related to music, audio, or voice             |
| `team:production`   | Task involves coordination, integration, or QA        |
| `team:localization` | Task involves translation or cultural adaptation      |

### 5. `scope/*`
Optional — describes affected part of the project.

| Label                 | Description                            |
|----------------------|----------------------------------------|
| `scope:ui`            | UI, UX, or frontend experience         |
| `scope:engine`        | Engine internals or backend systems    |
| `scope:script`        | Narrative script or dialogue           |
| `scope:media`         | Images, audio, or promotional assets   |
| `scope:tools`         | Build tools, pipelines, automation     |

## Label Usage Conventions

- Each issue **must have one `type`** and one `team`.
- `priority` is optional, but required for sprint-based planning.
- `status` should be updated throughout the issue lifecycle.
- Use `scope` for technical filtering when needed (optional).
- Keep labels lowercase and kebab-case (e.g. `type:feature`, not `Type: Feature`).

By standardizing labels, Tokari Works ensures clear task ownership, clean board visualization, and potential for future automation (e.g. GitHub Actions or project boards).
