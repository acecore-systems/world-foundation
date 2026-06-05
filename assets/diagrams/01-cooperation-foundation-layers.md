# Cooperation Foundation Layers

この図は、[Architecture](../../docs/ja/02-architecture.md) で説明する協力基盤を層として分けるための初期モデルです。各層の詳細は [modules/ja](../../modules/ja/README.md) に置き、責任侵食のリスクは [Threat Model](../../docs/ja/05-threat-model.md) で扱います。

```mermaid
flowchart TB
  People["個人 / 組織 / 地域"]
  Interface["参加・離脱・多重所属"]
  Identity["Identity<br/>本人性・所属・権限"]
  Reputation["Reputation<br/>信用・貢献・履歴"]
  Economy["Economy<br/>価値交換・生活アクセス"]
  Welfare["Welfare<br/>生存不安を減らす支援"]
  Governance["Governance<br/>意思決定・権限管理"]
  Arbitration["Arbitration<br/>紛争解決・異議申し立て"]
  Infrastructure["Infrastructure<br/>通信・計算・生活基盤"]
  Audit["Audit<br/>監査・ログ・透明性"]
  Norms["Norms<br/>ルール・権利・義務"]
  PublicSafety["Public Safety<br/>暴力予防・通報"]
  Federation["Federation<br/>組織間プロトコル"]

  People --> Interface
  Interface --> Identity
  Identity --> Reputation
  Reputation --> Economy
  Economy --> Welfare
  Governance --> Identity
  Governance --> Economy
  Governance --> Welfare
  Norms --> Governance
  Norms --> Arbitration
  Arbitration --> Governance
  Arbitration --> Economy
  PublicSafety --> Arbitration
  PublicSafety --> Norms
  Federation --> Identity
  Federation --> Reputation
  Federation --> Audit
  Infrastructure --> Identity
  Infrastructure --> Governance
  Infrastructure --> Economy
  Infrastructure --> Federation
  Audit --> Governance
  Audit --> Economy
  Audit --> Arbitration
  Audit --> Reputation

  click Identity "../../modules/ja/identity/README.md" "Identity"
  click Reputation "../../modules/ja/reputation/README.md" "Reputation"
  click Economy "../../modules/ja/economy/README.md" "Economy"
  click Welfare "../../modules/ja/welfare/README.md" "Welfare"
  click Governance "../../modules/ja/governance/README.md" "Governance"
  click Arbitration "../../modules/ja/arbitration/README.md" "Arbitration"
  click Infrastructure "../../modules/ja/infrastructure/README.md" "Infrastructure"
  click Audit "../../modules/ja/audit/README.md" "Audit"
  click Norms "../../modules/ja/norms/README.md" "Norms"
  click PublicSafety "../../modules/ja/public-safety/README.md" "Public Safety"
  click Federation "../../modules/ja/federation/README.md" "Federation"
```
