# World Design Overview

この図は、World Foundation Designが何を中心に置くかを示します。目的は [Vision](../../docs/ja/00-vision.md)、設計原則は [Principles](../../docs/ja/01-principles.md)、構造は [Architecture](../../docs/ja/02-architecture.md) に分けます。クリック可能な全体索引は [visual-link-map.svg](visual-link-map.svg) です。

```mermaid
flowchart TB
  Vision["全ての人が好きなことに集中できる世界"]
  Principles["設計原則"]
  Architecture["連盟型アーキテクチャ"]
  Modules["機能モジュール"]
  Governance["透明な意思決定"]
  Experiments["小さな実験"]
  Records["Proposal / Decision / Glossary"]
  Feedback["レビューと改善"]

  Vision --> Principles
  Principles --> Architecture
  Architecture --> Modules
  Modules --> Experiments
  Experiments --> Records
  Records --> Feedback
  Feedback --> Principles
  Governance --> Records
  Governance --> Feedback

  click Vision "../../docs/ja/00-vision.md" "Vision"
  click Principles "../../docs/ja/01-principles.md" "Principles"
  click Architecture "../../docs/ja/02-architecture.md" "Architecture"
  click Modules "../../modules/ja/README.md" "Modules"
  click Governance "../../modules/ja/governance/README.md" "Governance"
  click Records "../../proposals/ja/README.md" "Proposal / Decision / Glossary"
```
