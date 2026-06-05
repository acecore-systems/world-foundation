# 協力基盤の階層

この図は、[アーキテクチャ](../../docs/ja/02-architecture.md) で説明する協力基盤を層として分けるための初期モデルです。各層の詳細は [モジュール](../../modules/ja/README.md) に置き、責任侵食のリスクは [脅威モデル](../../docs/ja/05-threat-model.md) で扱います。

```mermaid
flowchart TB
  People["個人 / 組織 / 地域"]
  Interface["参加・離脱・多重所属"]
  アイデンティティ["アイデンティティ<br/>本人性・所属・権限"]
  評判["評判<br/>信用・貢献・履歴"]
  経済["経済<br/>価値交換・生活アクセス"]
  福祉["福祉<br/>生存不安を減らす支援"]
  ガバナンス["ガバナンス<br/>意思決定・権限管理"]
  仲裁["仲裁<br/>紛争解決・異議申し立て"]
  基盤["基盤<br/>通信・計算・生活基盤"]
  監査["監査<br/>監査・ログ・透明性"]
  規範["規範<br/>ルール・権利・義務"]
  PublicSafety["公共安全<br/>暴力予防・通報"]
  連合["連合<br/>組織間プロトコル"]

  People --> Interface
  Interface --> アイデンティティ
  アイデンティティ --> 評判
  評判 --> 経済
  経済 --> 福祉
  ガバナンス --> アイデンティティ
  ガバナンス --> 経済
  ガバナンス --> 福祉
  規範 --> ガバナンス
  規範 --> 仲裁
  仲裁 --> ガバナンス
  仲裁 --> 経済
  PublicSafety --> 仲裁
  PublicSafety --> 規範
  連合 --> アイデンティティ
  連合 --> 評判
  連合 --> 監査
  基盤 --> アイデンティティ
  基盤 --> ガバナンス
  基盤 --> 経済
  基盤 --> 連合
  監査 --> ガバナンス
  監査 --> 経済
  監査 --> 仲裁
  監査 --> 評判

  click People "../../docs/ja/00-vision.md" "ビジョン"
  click Interface "../../docs/ja/01-principles.md" "参加・離脱・多重所属"
  click アイデンティティ "../../modules/ja/identity/README.md" "アイデンティティ"
  click 評判 "../../modules/ja/reputation/README.md" "評判"
  click 経済 "../../modules/ja/economy/README.md" "経済"
  click 福祉 "../../modules/ja/welfare/README.md" "福祉"
  click ガバナンス "../../modules/ja/governance/README.md" "ガバナンス"
  click 仲裁 "../../modules/ja/arbitration/README.md" "仲裁"
  click 基盤 "../../modules/ja/infrastructure/README.md" "基盤"
  click 監査 "../../modules/ja/audit/README.md" "監査"
  click 規範 "../../modules/ja/norms/README.md" "規範"
  click PublicSafety "../../modules/ja/public-safety/README.md" "公共安全"
  click 連合 "../../modules/ja/federation/README.md" "連合"
```
