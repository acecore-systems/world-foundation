# World Foundation設計文書

このディレクトリには、理想的な世界の基本設計文書を配置します。

日本語版は初期の正本として扱います。英語版は `docs/en/` に置き、重要な文書から順に翻訳・更新します。

## 全体構成

基本設計は、目的、原則、構造、モジュール、安全境界、運用、移行、調査を相互に接続して扱います。

図から読みたい場合は、クリック可能な [ビジュアルリンクマップ](../../assets/diagrams/visual-link-map.svg) または各項目の「さらに見る」から入れます。

```mermaid
flowchart TB
  Index["World Foundation Design"]
  ビジョン["目的<br/>ビジョン"]
  設計原則["原則<br/>設計原則"]
  アーキテクチャ["構造<br/>アーキテクチャ"]
  モジュール["モジュール<br/>アイデンティティ / 経済 / 福祉 / ガバナンス..."]
  安全方針["安全境界<br/>対象外 / 安全方針 / 脅威モデル"]
  Operation["運用<br/>Issue / 提案 / 意思決定"]
  ロードマップ["移行<br/>ロードマップ"]
  LifeAccess["生活アクセス<br/>福祉 / 経済 / 共有資源"]
  翻訳["翻訳<br/>日本語正本と英語版"]
  調査["調査<br/>調査索引"]

  Index --> ビジョン
  ビジョン --> 設計原則
  設計原則 --> アーキテクチャ
  アーキテクチャ --> モジュール
  アーキテクチャ --> ロードマップ
  モジュール --> LifeAccess
  モジュール --> 安全方針
  モジュール --> Operation
  Operation --> 安全方針
  ロードマップ --> 調査
  翻訳 --> Operation
  調査 -. "前提を検証" .-> 設計原則
  安全方針 -. "逸脱を防ぐ" .-> Operation

  click Index "README.md" "設計文書"
  click ビジョン "00-vision.md" "ビジョン"
  click 設計原則 "01-principles.md" "設計原則"
  click アーキテクチャ "02-architecture.md" "アーキテクチャ"
  click モジュール "../../modules/ja/README.md" "モジュール"
  click 安全方針 "05-threat-model.md" "安全境界"
  click Operation "../../proposals/ja/README.md" "運用"
  click ロードマップ "03-roadmap.md" "ロードマップ"
  click LifeAccess "06-life-access-sustainability.md" "生活アクセス"
  click 翻訳 "07-translation-status.md" "翻訳"
  click 調査 "../../research/ja/index.md" "調査"
```

## 詳細への導線

| 項目 | まず読む | さらに見る |
| --- | --- | --- |
| 目的 | [00-vision.md](00-vision.md) | [00-world-design-overview.md](../../assets/diagrams/00-world-design-overview.md), [ビジュアルリンクマップ](../../assets/diagrams/visual-link-map.svg) |
| 原則 | [01-principles.md](01-principles.md) | [08-non-coercive-adoption.md](../../assets/diagrams/08-non-coercive-adoption.md), [04-non-goals.md](04-non-goals.md) |
| 構造 | [02-architecture.md](02-architecture.md) | [01-cooperation-foundation-layers.md](../../assets/diagrams/01-cooperation-foundation-layers.md), [modules/ja](../../modules/ja/README.md) |
| モジュール | [modules/ja](../../modules/ja/README.md) | [02-module-relationships.md](../../assets/diagrams/02-module-relationships.md), [09-expanded-module-map.md](../../assets/diagrams/09-expanded-module-map.md), [05-threat-model.md](05-threat-model.md) |
| 安全境界 | [04-non-goals.md](04-non-goals.md), [05-threat-model.md](05-threat-model.md) | [安全方針](../../SAFETY.md), [05-risk-and-safety-loops.md](../../assets/diagrams/05-risk-and-safety-loops.md) |
| 運用 | [proposals/ja](../../proposals/ja/README.md), [decisions/ja](../../decisions/ja/README.md) | [03-governance-process.md](../../assets/diagrams/03-governance-process.md), [ガバナンスモジュール](../../modules/ja/governance/README.md) |
| 移行 | [03-roadmap.md](03-roadmap.md) | [04-transition-roadmap.md](../../assets/diagrams/04-transition-roadmap.md), [08-non-coercive-adoption.md](../../assets/diagrams/08-non-coercive-adoption.md) |
| 生活アクセス | [06-life-access-sustainability.md](06-life-access-sustainability.md) | [07-life-access-model.md](../../assets/diagrams/07-life-access-model.md), [福祉モジュール](../../modules/ja/welfare/README.md), [経済モジュール](../../modules/ja/economy/README.md), [05-threat-model.md](05-threat-model.md) |
| 翻訳 | [07-translation-status.md](07-translation-status.md) | [06-multilingual-document-flow.md](../../assets/diagrams/06-multilingual-document-flow.md), [用語集](../../glossary/README.md), [英語版文書](../en/README.md) |
| 調査 | [research/ja/index.md](../../research/ja/index.md) | [research/ja](../../research/ja/README.md) |

## 文書一覧

- `00-vision.md`: 目指す世界
- `01-principles.md`: 設計原則
- `02-architecture.md`: 全体アーキテクチャ
- `03-roadmap.md`: 段階的な移行計画
- `04-non-goals.md`: この設計が目指さないもの
- `05-threat-model.md`: 腐敗、支配、悪用、法務衝突、監視化などのリスク整理
- `06-life-access-sustainability.md`: 生活アクセスと資源配分の持続可能性
- `07-translation-status.md`: 日本語正本と翻訳ステータス管理
