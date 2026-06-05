# 調査

このディレクトリには、理想的な世界の設計に関係する調査資料を置きます。

調査資料は、思想を補強するためだけでなく、設計上のリスク、失敗例、既存制度との関係を検討するために使います。調査結果は [ロードマップ](../../docs/ja/03-roadmap.md)、[脅威モデル](../../docs/ja/05-threat-model.md)、各 [モジュール](../../modules/ja/README.md) へ戻し、設計変更が必要な場合は [提案](../../proposals/ja/README.md) として扱います。

## 調査領域

```mermaid
flowchart TB
  調査["調査"]
  History["歴史・制度変化"]
  War["戦争・国際関係"]
  OSS["OSS・標準化"]
  Coop["協同組合・相互扶助"]
  アイデンティティ["アイデンティティ / 評判"]
  経済["経済 / 福祉"]
  ガバナンス["ガバナンス / 仲裁 / 規範"]
  安全方針["基盤 / 監査 / 安全方針"]
  Docs["docs / modules<br/>設計への反映"]

  調査 --> History
  調査 --> War
  調査 --> OSS
  調査 --> Coop
  調査 --> アイデンティティ
  調査 --> 経済
  調査 --> ガバナンス
  調査 --> 安全方針
  History --> Docs
  War --> Docs
  OSS --> Docs
  Coop --> Docs
  アイデンティティ --> Docs
  経済 --> Docs
  ガバナンス --> Docs
  安全方針 --> Docs

  click 調査 "index.md" "調査索引"
  click History "index.md" "歴史・制度変化"
  click War "index.md" "戦争・国際関係"
  click OSS "index.md" "OSS・標準化"
  click Coop "index.md" "協同組合・相互扶助"
  click アイデンティティ "../../modules/ja/identity/README.md" "アイデンティティ / 評判"
  click 経済 "../../modules/ja/economy/README.md" "経済 / 福祉"
  click ガバナンス "../../modules/ja/governance/README.md" "ガバナンス / 仲裁 / 規範"
  click 安全方針 "../../docs/ja/05-threat-model.md" "基盤 / 監査 / 安全方針"
  click Docs "../../docs/ja/README.md" "設計文書"
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

調査テーマの一覧は [調査索引](index.md) に整理します。
