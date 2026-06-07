# Decisions

This directory records important design decisions and their rationale.

## Position

```mermaid
flowchart LR
  Context["Context<br/>Issue / Proposal / Review"]
  Decision["Decision<br/>choice / rationale / impact"]
  Docs["docs / modules<br/>affected documents"]
  Future["Future changes<br/>revisit / update / retire"]

  Context --> Decision
  Decision --> Docs
  Decision --> Future
  Future --> Context

  click Context "https://github.com/acecore-systems/world-foundation/blob/main/proposals/en/README.md" "Issue / Proposal / Review"
  click Decision "https://github.com/acecore-systems/world-foundation/blob/main/decisions/en/README.md" "Decisions"
  click Docs "https://github.com/acecore-systems/world-foundation/blob/main/docs/en/README.md" "docs / modules"
  click Future "https://github.com/acecore-systems/world-foundation/issues" "revisit / update / retire"
```

## Scope

- Important design policies
- Accepted architecture choices
- Rejected alternatives and rationale
- Governance decisions
- Definitions that affect terms or principles

Early decisions may be written only in Japanese. Important decisions can be translated later.
