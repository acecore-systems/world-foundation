# Proposals

This directory contains design proposals for World Foundation Design.

Proposals are used before changing core documents or modules.

## Position

```mermaid
flowchart LR
  Issue["Issue<br/>problem / idea / translation"]
  Proposal["Proposal<br/>change / impact / risk"]
  Review["Review<br/>principles / safety / terms"]
  PullRequest["Pull Request<br/>concrete change"]
  Docs["docs / modules<br/>target documents"]
  Decision["decisions<br/>important rationale"]

  Issue --> Proposal
  Proposal --> Review
  Review --> PullRequest
  PullRequest --> Docs
  Review --> Decision
  Decision --> Docs

  click Issue "https://github.com/acecore-systems/world-foundation/issues" "GitHub Issues"
  click Proposal "README.md" "Proposals"
  click Review "../../docs/en/01-principles.md" "Review"
  click PullRequest "https://github.com/acecore-systems/world-foundation/pulls" "GitHub Pull Requests"
  click Docs "../../docs/en/README.md" "docs / modules"
  click Decision "../../decisions/en/README.md" "Decisions"
```

## Scope

- Design changes
- New modules or operating procedures
- Policy changes that affect core documents
- Risks, alternatives, and affected documents
- Impact on docs, modules, glossary, or decisions

Early proposals may be written only in Japanese. Important accepted proposals can be translated later.
