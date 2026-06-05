# Expanded Module Relationships

この図は、[Architecture](../../docs/ja/02-architecture.md) の拡張後モジュール、特に [Norms](../../modules/ja/norms/README.md)、[Public Safety](../../modules/ja/public-safety/README.md)、[Federation](../../modules/ja/federation/README.md) を含む関係を示します。

矢印は支配関係ではなく、参照・連携・検証・相互接続を示します。中央支配化や自警団化などのリスクは [Threat Model](../../docs/ja/05-threat-model.md) へ戻して確認します。

```mermaid
flowchart TB
  People["個人 / 組織 / 地域"]
  Federation["Federation<br/>組織間プロトコル"]
  Identity["Identity<br/>本人性・所属・権限"]
  Reputation["Reputation<br/>信用・貢献"]
  Norms["Norms<br/>ルール・権利・義務"]
  Governance["Governance<br/>意思決定"]
  Arbitration["Arbitration<br/>紛争解決"]
  PublicSafety["Public Safety<br/>暴力予防・通報"]
  Economy["Economy<br/>価値交換"]
  Welfare["Welfare<br/>生活支援"]
  Infrastructure["Infrastructure<br/>通信・計算・データ"]
  Audit["Audit<br/>検証・記録"]

  People --> Identity
  People --> Federation
  Federation --> Identity
  Federation --> Reputation
  Federation --> Norms
  Identity --> Reputation
  Norms --> Governance
  Norms --> Arbitration
  Governance --> Audit
  Arbitration --> Audit
  PublicSafety --> Arbitration
  PublicSafety --> Norms
  Economy --> Welfare
  Reputation -. "補助情報" .-> Governance
  Reputation -. "慎重な参照" .-> Economy
  Audit -. "定義範囲の検証" .-> Reputation
  Infrastructure --> Identity
  Infrastructure --> Audit
  Infrastructure --> Federation

  click Federation "../../modules/ja/federation/README.md" "Federation"
  click Identity "../../modules/ja/identity/README.md" "Identity"
  click Reputation "../../modules/ja/reputation/README.md" "Reputation"
  click Norms "../../modules/ja/norms/README.md" "Norms"
  click Governance "../../modules/ja/governance/README.md" "Governance"
  click Arbitration "../../modules/ja/arbitration/README.md" "Arbitration"
  click PublicSafety "../../modules/ja/public-safety/README.md" "Public Safety"
  click Economy "../../modules/ja/economy/README.md" "Economy"
  click Welfare "../../modules/ja/welfare/README.md" "Welfare"
  click Infrastructure "../../modules/ja/infrastructure/README.md" "Infrastructure"
  click Audit "../../modules/ja/audit/README.md" "Audit"
```
