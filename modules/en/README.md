# Modules

This directory contains design notes for the functional modules of World Foundation Design.

Modules are not units of control. They separate responsibilities so each area can connect with others without taking over their scope.

## Module Index

```mermaid
flowchart TB
  Foundation["Cooperation Infrastructure<br/>voluntary / exit-capable / forkable"]
  Identity["Identity<br/>personhood / membership / permissions"]
  Reputation["Reputation<br/>trust / contribution"]
  Economy["Economy<br/>exchange / life access"]
  Welfare["Welfare<br/>life support"]
  Governance["Governance<br/>decisions"]
  Arbitration["Arbitration<br/>dispute resolution"]
  Infrastructure["Infrastructure<br/>communication / compute / data"]
  Audit["Audit<br/>verification / records"]
  Norms["Norms<br/>rules / rights / duties"]
  PublicSafety["Public Safety<br/>violence prevention / reporting boundaries"]
  Federation["Federation<br/>inter-organization protocol"]

  Foundation --> Identity
  Foundation --> Infrastructure
  Identity --> Reputation
  Reputation -. "supporting context" .-> Economy
  Economy --> Welfare
  Norms --> Governance
  Norms --> Arbitration
  Governance --> Audit
  Arbitration --> Audit
  PublicSafety --> Arbitration
  Federation --> Identity
  Federation --> Reputation
  Federation --> Audit
  Infrastructure --> Federation
  Infrastructure --> Audit

  click Foundation "https://github.com/acecore-systems/world-foundation/blob/main/docs/en/00-vision.md" "Cooperation infrastructure"
  click Identity "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/identity/README.md" "Identity"
  click Reputation "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/reputation/README.md" "Reputation"
  click Economy "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/economy/README.md" "Economy"
  click Welfare "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/welfare/README.md" "Welfare"
  click Governance "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/governance/README.md" "Governance"
  click Arbitration "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/arbitration/README.md" "Arbitration"
  click Infrastructure "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/infrastructure/README.md" "Infrastructure"
  click Audit "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/audit/README.md" "Audit"
  click Norms "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/norms/README.md" "Norms"
  click PublicSafety "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/public-safety/README.md" "Public Safety"
  click Federation "https://github.com/acecore-systems/world-foundation/blob/main/modules/en/federation/README.md" "Federation"
```

## Module List

| Module | Role |
| --- | --- |
| [identity/README.md](identity/README.md) | Personhood, membership, and permissions |
| [reputation/README.md](reputation/README.md) | Trust, contribution, and context-specific evaluation |
| [economy/README.md](economy/README.md) | Exchange, internal records, and life access |
| [welfare/README.md](welfare/README.md) | Life support that reduces survival anxiety |
| [governance/README.md](governance/README.md) | Decisions, change processes, and authority management |
| [arbitration/README.md](arbitration/README.md) | Dispute resolution and appeals |
| [infrastructure/README.md](infrastructure/README.md) | Communication, computation, data, and life infrastructure |
| [audit/README.md](audit/README.md) | Verification, records, and public/protected information boundaries |
| [norms/README.md](norms/README.md) | Rules, terms, rights, and duties |
| [public-safety/README.md](public-safety/README.md) | Violence prevention, reporting, and public safety boundaries |
| [federation/README.md](federation/README.md) | Inter-organization protocols, autonomy, and interoperability |

## Related Diagrams

- [02-module-relationships.md](../../assets/diagrams/02-module-relationships.md): Module relationships
- [09-expanded-module-map.md](../../assets/diagrams/09-expanded-module-map.md): Expanded module relationships
- [01-cooperation-foundation-layers.md](../../assets/diagrams/01-cooperation-foundation-layers.md): Cooperation foundation layers
