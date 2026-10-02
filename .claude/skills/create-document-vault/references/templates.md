# Document Templates

## Contents

- Frontmatter rules
- WikiLink rules
- ARCHITECTURE.md
- DECISIONS.md
- ADR-NNN — <Title>
- DOMAIN.md
- PROJECT.md
- UI-DESIGN.md
- LOGGING.md
- TOOLS.md
- LEGAL.md

Every vault document uses this frontmatter and cross-linking convention.

### Frontmatter rules

- **title** — `"<Project Name> — <Document Title>"` (e.g. `"MalariaRx — Architecture"`)
- **version** — Start at `1.0`; increment by `0.1` for minor updates, `1.0` for major revisions
- **created** — Date the file was first created (`YYYY-MM-DD`)
- **updated** — Today's date whenever the file is touched (`YYYY-MM-DD`)
- **tags** — Array format (YAML list, not inline); include the project slug and document topic tags

### WikiLink rules

- Use `[[DOCNAME]]` (all-caps, no extension) for cross-references to other vault documents
- Use descriptive link text when the document name alone is ambiguous: `[[DOMAIN|Clinical Domain]]`
- Every document must have a **Related Documents** section at the bottom

---

### ARCHITECTURE.md

```markdown
---
title: <Project Name> — Architecture
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, architecture]
---

# <Project Name> — Architecture

## Overview

<!-- High-level system description -->

## Components

<!-- List and describe major components/services -->

## Data Models

<!-- Key entities, relationships, storage strategy -->

## Integrations

<!-- External systems, APIs, MCP servers -->

## Deployment

<!-- Environments, infrastructure, CI/CD -->

---

## Related Documents

- [[PROJECT]] — Risks, tasks, milestones
- [[DECISIONS]] — Architecture Decision Records
- [[DOMAIN]] — Business domain and glossary
- [[TOOLS]] — Tools and frameworks
```

### DECISIONS.md

```markdown
---
title: <Project Name> — Decisions
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, decisions, adr]
---

# <Project Name> — Architecture Decision Records

## ADR Template

### ADR-NNN — <Title>

- **Date:** YYYY-MM-DD
- **Status:** Proposed / Accepted / Deprecated / Superseded by ADR-NNN
- **Context:** <!-- What is the situation forcing this decision? -->
- **Decision:** <!-- What was decided? -->
- **Rationale:** <!-- Why this option over alternatives? -->
- **Consequences:** <!-- What does this change? What trade-offs are accepted? -->

---

## Related Documents

- [[ARCHITECTURE]] — System design
- [[PROJECT]] — Project context and decisions log
```

### DOMAIN.md

```markdown
---
title: <Project Name> — Domain
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, domain]
---

# <Project Name> — Domain

## Business Context

<!-- What problem this project solves, who it is for -->

## User Personas

<!-- Who uses this system and what they need -->

## Domain Model

<!-- Key concepts, entities, and relationships in the business domain -->

## Glossary

| Term | Definition |
|------|-----------|
|      |           |

---

## Related Documents

- [[ARCHITECTURE]] — System design
- [[PROJECT]] — Project context
- [[UI-DESIGN]] — UX and user flows
```

### PROJECT.md

```markdown
---
title: <Project Name> — Project
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, project-management]
---

# <Project Name> — Project

## Mission

<!-- One sentence: what this project achieves and why it matters -->

## Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
|           |             |        |

## Risks

| ID | Risk | Impact | Likelihood | Mitigation |
|----|------|--------|------------|------------|
|    |      |        |            |            |

## Issues

| ID | Description | Priority | Owner | Status |
|----|-------------|----------|-------|--------|
|    |             |          |       |        |

## Tasks

| ID | Task | Owner | Due | Status |
|----|------|-------|-----|--------|
|    |      |       |     |        |

## Stakeholders

| Name | Role | Contact |
|------|------|---------|
|      |      |         |

## Decisions Log

| Date | Decision | Rationale |
|------|----------|-----------|
|      |          |           |

---

## Related Documents

- [[ARCHITECTURE]] — System design
- [[DECISIONS]] — Architecture Decision Records
- [[DOMAIN]] — Business domain
- [[TOOLS]] — Tools and automation
```

### UI-DESIGN.md

```markdown
---
title: <Project Name> — UI Design
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, ui-design]
---

# <Project Name> — UI Design

## Brand

<!-- Visual identity: colours, typography, logo usage rules -->

## Design System

<!-- Spacing scale, grid, elevation, shadows -->

## Component Library

<!-- Key components, variants, usage rules -->

## Screen Inventory

| Screen | Purpose | Notes |
|--------|---------|-------|
|        |         |       |

## User Flows

<!-- Describe key user journeys; embed diagrams from `../../diagrams/` -->

## Accessibility

<!-- WCAG level, contrast ratios, keyboard nav, screen reader requirements -->

---

## Related Documents

- [[DOMAIN]] — User personas and context
- [[ARCHITECTURE]] — Technical constraints on UI
```

### LOGGING.md

```markdown
---
title: <Project Name> — Logging
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, logging]
---

# <Project Name> — Logging Strategy

## Log Levels

| Level | When to use |
|-------|------------|
| ERROR | Unrecoverable failures requiring immediate attention |
| WARN  | Recoverable issues, unexpected but handled states |
| INFO  | Normal operational events (startup, shutdown, key user actions) |
| DEBUG | Detailed diagnostic information (dev/QA only) |
| TRACE | Step-by-step execution traces (dev only) |

## Log Categories

<!-- Domain-specific log categories or tags used to group/filter logs -->

## Audit Logging

<!-- Events that must always be logged for compliance or security -->

## What NOT to Log

- Passwords, tokens, or credentials
- Full PII (mask or truncate where required)
- Sensitive financial or health data in plain text

---

## Related Documents

- [[TOOLS]] — Logging frameworks and tools
- [[LEGAL]] — Data retention and compliance requirements
```

### TOOLS.md

```markdown
---
title: <Project Name> — Tools
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, tools]
---

# <Project Name> — Tools & Automation

## Frameworks & Libraries

| Tool | Version | Purpose |
|------|---------|---------|
|      |         |         |

## Claude Skills Used

| Skill | Purpose |
|-------|---------|
|       |         |

## Claude Plugins / MCPs

| Plugin / MCP | Purpose |
|--------------|---------|
|              |         |

## Scripts & Automation

| Script | Location | Purpose |
|--------|----------|---------|
|        |          |         |

## Vault Index

| Document | Purpose |
|----------|---------|
| [[ARCHITECTURE]] | System design, components, data models |
| [[DECISIONS]] | Architecture Decision Records |
| [[DOMAIN]] | Business domain, personas, glossary |
| [[PROJECT]] | Risks, issues, tasks, milestones |
| [[UI-DESIGN]] | Design system, screens, UX flows, brand |
| [[LOGGING]] | Logging strategy and rules |
| [[TOOLS]] | This document |
| [[LEGAL]] | Copyright, licences |

---

## Related Documents

- [[PROJECT]] — Project context
- [[ARCHITECTURE]] — Technical environment
```

### LEGAL.md

```markdown
---
title: <Project Name> — Legal
version: 1.0
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [<project-slug>, legal]
---

# <Project Name> — Legal

## Copyright

<!-- Owner, year, rights reserved statement -->

## IP Ownership

<!-- Who owns the intellectual property produced by this project -->

## Source File Header

<!-- Standard header to prepend to all source files, if required -->

```
// Copyright (C) YYYY <Owner>. All rights reserved.
```

## Licences

| Dependency | Licence | Obligations |
|------------|---------|-------------|
|            |         |             |

## Compliance Notes

<!-- Regulatory requirements (POPIA, GDPR, HIPAA, etc.) that apply -->

---

## Related Documents

- [[LOGGING]] — Data retention and PII handling
- [[PROJECT]] — Stakeholders and decisions
```
