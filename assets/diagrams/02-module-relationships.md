# モジュール関係

この図は、[モジュール](../../modules/ja/README.md) の初期モジュール同士の関係を示します。矢印は支配関係ではなく、[アーキテクチャ](../../docs/ja/02-architecture.md) が前提にする参照・連携・検証の関係です。

評判は全アクセスを支配するためのものではありません。監査も全てを監視するためのものではなく、定義された範囲を検証可能にするための仕組みです。この境界が崩れるリスクは [脅威モデル](../../docs/ja/05-threat-model.md) と [対象外](../../docs/ja/04-non-goals.md) で扱います。

```mermaid
flowchart LR
  アイデンティティ["アイデンティティ<br/>本人性・所属・権限"]
  評判["評判<br/>信用・貢献・文脈別評価"]
  経済["経済<br/>ポイント・価値交換・生活アクセス"]
  福祉["福祉<br/>食・住・通信・教育・健康支援"]
  ガバナンス["ガバナンス<br/>意思決定・変更手続き"]
  仲裁["仲裁<br/>紛争解決・異議申し立て"]
  基盤["基盤<br/>通信・計算・データ"]
  監査["監査<br/>意思決定・会計・権限変更の検証"]
  規範["規範<br/>ルール・権利・義務"]
  PublicSafety["公共安全<br/>暴力予防・通報境界"]
  連合["連合<br/>組織間プロトコル"]
  用語集["用語集<br/>用語の一貫性"]
  Decisions["Decisions<br/>判断理由の記録"]

  アイデンティティ --> 評判
  アイデンティティ --> ガバナンス
  アイデンティティ --> 福祉
  アイデンティティ --> 経済
  評判 -. "補助情報" .-> ガバナンス
  評判 -. "慎重な参照" .-> 経済
  評判 -. "慎重な参照" .-> 福祉
  評判 --> 仲裁
  経済 --> 福祉
  経済 --> 仲裁
  福祉 --> 仲裁
  ガバナンス --> Decisions
  ガバナンス --> 用語集
  ガバナンス --> 規範
  仲裁 --> Decisions
  仲裁 --> 規範
  規範 --> 連合
  PublicSafety --> 仲裁
  PublicSafety --> 規範
  連合 -. "相互接続" .-> アイデンティティ
  連合 -. "組織間連携" .-> 評判
  連合 -. "組織間検証" .-> 監査
  監査 -. "定義範囲の検証" .-> ガバナンス
  監査 -. "定義範囲の検証" .-> 経済
  監査 -. "定義範囲の検証" .-> 仲裁
  監査 -. "評価根拠の検証" .-> 評判
  基盤 --> アイデンティティ
  基盤 --> 経済
  基盤 --> ガバナンス
  基盤 --> 監査
  用語集 --> アイデンティティ
  用語集 --> 評判
  用語集 --> 経済
  用語集 --> ガバナンス
  用語集 --> 規範

  click アイデンティティ "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/identity/README.md" "アイデンティティ"
  click 評判 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/reputation/README.md" "評判"
  click 経済 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/economy/README.md" "経済"
  click 福祉 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/welfare/README.md" "福祉"
  click ガバナンス "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/governance/README.md" "ガバナンス"
  click 仲裁 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/arbitration/README.md" "仲裁"
  click 基盤 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/infrastructure/README.md" "基盤"
  click 監査 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/audit/README.md" "監査"
  click 規範 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/norms/README.md" "規範"
  click PublicSafety "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/public-safety/README.md" "公共安全"
  click 連合 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/federation/README.md" "連合"
  click 用語集 "https://github.com/acecore-systems/world-foundation/blob/main/glossary/README.md" "用語集"
  click Decisions "https://github.com/acecore-systems/world-foundation/blob/main/decisions/ja/README.md" "意思決定"
```
