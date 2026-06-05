# Module Relationships

この図は、[modules/ja](../../modules/ja/README.md) の初期モジュール同士の関係を示します。矢印は支配関係ではなく、[Architecture](../../docs/ja/02-architecture.md) が前提にする参照・連携・検証の関係です。

Reputationは全アクセスを支配するためのものではありません。Auditも全てを監視するためのものではなく、定義された範囲を検証可能にするための仕組みです。この境界が崩れるリスクは [Threat Model](../../docs/ja/05-threat-model.md) と [Non-goals](../../docs/ja/04-non-goals.md) で扱います。

```mermaid
flowchart LR
  Identity["Identity<br/>本人性・所属・権限"]
  Reputation["Reputation<br/>信用・貢献・文脈別評価"]
  Economy["Economy<br/>ポイント・価値交換・生活アクセス"]
  Welfare["Welfare<br/>食・住・通信・教育・健康支援"]
  Governance["Governance<br/>意思決定・変更手続き"]
  Arbitration["Arbitration<br/>紛争解決・異議申し立て"]
  Infrastructure["Infrastructure<br/>通信・計算・データ"]
  Audit["Audit<br/>意思決定・会計・権限変更の検証"]
  Norms["Norms<br/>ルール・権利・義務"]
  PublicSafety["Public Safety<br/>暴力予防・通報境界"]
  Federation["Federation<br/>組織間プロトコル"]
  Glossary["Glossary<br/>用語の一貫性"]
  Decisions["Decisions<br/>判断理由の記録"]

  Identity --> Reputation
  Identity --> Governance
  Identity --> Welfare
  Identity --> Economy
  Reputation -. "補助情報" .-> Governance
  Reputation -. "慎重な参照" .-> Economy
  Reputation -. "慎重な参照" .-> Welfare
  Reputation --> Arbitration
  Economy --> Welfare
  Economy --> Arbitration
  Welfare --> Arbitration
  Governance --> Decisions
  Governance --> Glossary
  Governance --> Norms
  Arbitration --> Decisions
  Arbitration --> Norms
  Norms --> Federation
  PublicSafety --> Arbitration
  PublicSafety --> Norms
  Federation -. "相互接続" .-> Identity
  Federation -. "組織間連携" .-> Reputation
  Federation -. "組織間検証" .-> Audit
  Audit -. "定義範囲の検証" .-> Governance
  Audit -. "定義範囲の検証" .-> Economy
  Audit -. "定義範囲の検証" .-> Arbitration
  Audit -. "評価根拠の検証" .-> Reputation
  Infrastructure --> Identity
  Infrastructure --> Economy
  Infrastructure --> Governance
  Infrastructure --> Audit
  Glossary --> Identity
  Glossary --> Reputation
  Glossary --> Economy
  Glossary --> Governance
  Glossary --> Norms

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
  click Glossary "../../glossary/README.md" "Glossary"
  click Decisions "../../decisions/ja/README.md" "Decisions"
```
