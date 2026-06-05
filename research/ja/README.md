# Research

このディレクトリには、理想的な世界の設計に関係する調査資料を置きます。

調査資料は、思想を補強するためだけでなく、設計上のリスク、失敗例、既存制度との関係を検討するために使います。

## 調査領域

```mermaid
flowchart TB
  Research["Research"]
  History["歴史・制度変化"]
  War["戦争・国際関係"]
  OSS["OSS・標準化"]
  Coop["協同組合・相互扶助"]
  Identity["Identity / Reputation"]
  Economy["Economy / Welfare"]
  Governance["Governance / Arbitration / Norms"]
  Safety["Infrastructure / Audit / Safety"]
  Docs["docs / modules<br/>設計への反映"]

  Research --> History
  Research --> War
  Research --> OSS
  Research --> Coop
  Research --> Identity
  Research --> Economy
  Research --> Governance
  Research --> Safety
  History --> Docs
  War --> Docs
  OSS --> Docs
  Coop --> Docs
  Identity --> Docs
  Economy --> Docs
  Governance --> Docs
  Safety --> Docs
```

## 対象例

- 歴史
- 国家制度
- 経済制度
- 協同組合
- OSSガバナンス
- 分散ID
- 福祉
- 紛争解決
- 国際関係
- 法制度

## 方針

調査メモには、出典、要約、世界設計への示唆、未確認事項を分けて書くことを推奨します。

## 索引

調査テーマの一覧は [index.md](index.md) に整理します。
