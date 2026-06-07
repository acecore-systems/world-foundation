# 拡張モジュール関係

この図は、[アーキテクチャ](../../docs/ja/02-architecture.md) の拡張後モジュール、特に [規範](../../modules/ja/norms/README.md)、[公共安全](../../modules/ja/public-safety/README.md)、[連合](../../modules/ja/federation/README.md) を含む関係を示します。

矢印は支配関係ではなく、参照・連携・検証・相互接続を示します。中央支配化や自警団化などのリスクは [脅威モデル](../../docs/ja/05-threat-model.md) へ戻して確認します。

```mermaid
flowchart TB
  People["個人 / 組織 / 地域"]
  連合["連合<br/>組織間プロトコル"]
  アイデンティティ["アイデンティティ<br/>本人性・所属・権限"]
  評判["評判<br/>信用・貢献"]
  規範["規範<br/>ルール・権利・義務"]
  ガバナンス["ガバナンス<br/>意思決定"]
  仲裁["仲裁<br/>紛争解決"]
  PublicSafety["公共安全<br/>暴力予防・通報"]
  経済["経済<br/>価値交換"]
  福祉["福祉<br/>生活支援"]
  基盤["基盤<br/>通信・計算・データ"]
  監査["監査<br/>検証・記録"]

  People --> アイデンティティ
  People --> 連合
  連合 --> アイデンティティ
  連合 --> 評判
  連合 --> 規範
  アイデンティティ --> 評判
  規範 --> ガバナンス
  規範 --> 仲裁
  ガバナンス --> 監査
  仲裁 --> 監査
  PublicSafety --> 仲裁
  PublicSafety --> 規範
  経済 --> 福祉
  評判 -. "補助情報" .-> ガバナンス
  評判 -. "慎重な参照" .-> 経済
  監査 -. "定義範囲の検証" .-> 評判
  基盤 --> アイデンティティ
  基盤 --> 監査
  基盤 --> 連合

  click People "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/00-vision.md" "個人 / 組織 / 地域"
  click 連合 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/federation/README.md" "連合"
  click アイデンティティ "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/identity/README.md" "アイデンティティ"
  click 評判 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/reputation/README.md" "評判"
  click 規範 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/norms/README.md" "規範"
  click ガバナンス "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/governance/README.md" "ガバナンス"
  click 仲裁 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/arbitration/README.md" "仲裁"
  click PublicSafety "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/public-safety/README.md" "公共安全"
  click 経済 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/economy/README.md" "経済"
  click 福祉 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/welfare/README.md" "福祉"
  click 基盤 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/infrastructure/README.md" "基盤"
  click 監査 "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/audit/README.md" "監査"
```
