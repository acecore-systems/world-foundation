# Modules

このディレクトリには、World Foundation Designを構成する機能モジュールの設計メモを置きます。

モジュールは支配単位ではなく、責任範囲を分けるための単位です。各モジュールは接続しますが、他モジュールの責任を侵食しないように設計します。

## モジュール構成

```mermaid
flowchart TB
  Foundation["協力基盤<br/>自由参加・離脱可能・フォーク可能"]
  Identity["Identity<br/>本人性・所属・権限"]
  Reputation["Reputation<br/>信用・貢献"]
  Economy["Economy<br/>価値交換・生活アクセス"]
  Welfare["Welfare<br/>生活支援"]
  Governance["Governance<br/>意思決定"]
  Arbitration["Arbitration<br/>紛争解決"]
  Infrastructure["Infrastructure<br/>通信・計算・データ"]
  Audit["Audit<br/>検証・記録"]
  Norms["Norms<br/>ルール・権利・義務"]
  PublicSafety["Public Safety<br/>暴力予防・通報境界"]
  Federation["Federation<br/>組織間プロトコル"]

  Foundation --> Identity
  Foundation --> Infrastructure
  Identity --> Reputation
  Reputation -. "補助情報" .-> Economy
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

  click Identity "identity/README.md" "Identity"
  click Reputation "reputation/README.md" "Reputation"
  click Economy "economy/README.md" "Economy"
  click Welfare "welfare/README.md" "Welfare"
  click Governance "governance/README.md" "Governance"
  click Arbitration "arbitration/README.md" "Arbitration"
  click Infrastructure "infrastructure/README.md" "Infrastructure"
  click Audit "audit/README.md" "Audit"
  click Norms "norms/README.md" "Norms"
  click PublicSafety "public-safety/README.md" "Public Safety"
  click Federation "federation/README.md" "Federation"
```

## モジュール一覧

| モジュール | 役割 |
| --- | --- |
| [identity/README.md](identity/README.md) | 本人性、所属、権限 |
| [reputation/README.md](reputation/README.md) | 信用、貢献、文脈別評価 |
| [economy/README.md](economy/README.md) | 価値交換、内部記録、生活アクセス |
| [welfare/README.md](welfare/README.md) | 生存不安を減らす生活支援 |
| [governance/README.md](governance/README.md) | 意思決定、変更手続き、権限管理 |
| [arbitration/README.md](arbitration/README.md) | 紛争解決、異議申し立て |
| [infrastructure/README.md](infrastructure/README.md) | 通信、計算、データ、生活基盤 |
| [audit/README.md](audit/README.md) | 検証、記録、公開情報と保護情報の境界 |
| [norms/README.md](norms/README.md) | ルール、規約、権利、義務 |
| [public-safety/README.md](public-safety/README.md) | 暴力予防、通報、公共安全境界 |
| [federation/README.md](federation/README.md) | 組織間プロトコル、自治、相互運用性 |

## 読み方

全体構造は [Architecture](../../docs/ja/02-architecture.md)、モジュール間の接続は [02-module-relationships.md](../../assets/diagrams/02-module-relationships.md) と [09-expanded-module-map.md](../../assets/diagrams/09-expanded-module-map.md)、安全境界は [Non-goals](../../docs/ja/04-non-goals.md) と [Threat Model](../../docs/ja/05-threat-model.md) を見ながら読みます。
