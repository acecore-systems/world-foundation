# モジュール

このディレクトリには、World Foundation Designを構成する機能モジュールの設計メモを置きます。

モジュールは支配単位ではなく、責任範囲を分けるための単位です。各モジュールは接続しますが、他モジュールの責任を侵食しないように設計します。

## モジュール構成

```mermaid
flowchart TB
  Foundation["協力基盤<br/>自由参加・離脱可能・フォーク可能"]
  アイデンティティ["アイデンティティ<br/>本人性・所属・権限"]
  評判["評判<br/>信用・貢献"]
  経済["経済<br/>価値交換・生活アクセス"]
  福祉["福祉<br/>生活支援"]
  ガバナンス["ガバナンス<br/>意思決定"]
  仲裁["仲裁<br/>紛争解決"]
  基盤["基盤<br/>通信・計算・データ"]
  監査["監査<br/>検証・記録"]
  規範["規範<br/>ルール・権利・義務"]
  PublicSafety["公共安全<br/>暴力予防・通報境界"]
  連合["連合<br/>組織間プロトコル"]

  Foundation --> アイデンティティ
  Foundation --> 基盤
  アイデンティティ --> 評判
  評判 -. "補助情報" .-> 経済
  経済 --> 福祉
  規範 --> ガバナンス
  規範 --> 仲裁
  ガバナンス --> 監査
  仲裁 --> 監査
  PublicSafety --> 仲裁
  連合 --> アイデンティティ
  連合 --> 評判
  連合 --> 監査
  基盤 --> 連合
  基盤 --> 監査

  click Foundation "../../docs/ja/00-vision.md" "協力基盤"
  click アイデンティティ "identity/README.md" "アイデンティティ"
  click 評判 "reputation/README.md" "評判"
  click 経済 "economy/README.md" "経済"
  click 福祉 "welfare/README.md" "福祉"
  click ガバナンス "governance/README.md" "ガバナンス"
  click 仲裁 "arbitration/README.md" "仲裁"
  click 基盤 "infrastructure/README.md" "基盤"
  click 監査 "audit/README.md" "監査"
  click 規範 "norms/README.md" "規範"
  click PublicSafety "public-safety/README.md" "公共安全"
  click 連合 "federation/README.md" "連合"
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

全体構造は [アーキテクチャ](../../docs/ja/02-architecture.md)、モジュール間の接続は [02-module-relationships.md](../../assets/diagrams/02-module-relationships.md) と [09-expanded-module-map.md](../../assets/diagrams/09-expanded-module-map.md)、安全境界は [対象外](../../docs/ja/04-non-goals.md) と [脅威モデル](../../docs/ja/05-threat-model.md) を見ながら読みます。
