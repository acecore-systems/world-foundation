# 図表

このディレクトリには、World Foundation Designの構造、モジュール関係、ガバナンスフロー、移行ロードマップなどを説明する図表を置きます。

図表は、設計文書、モジュール、運用記録、調査への参照索引として扱います。図だけで完結させず、説明文や図のノードから本文へ戻れるようにします。

## ビジュアルリンクマップ

Mermaidが見づらい場合の入口として、クリック可能なSVG索引も置きます。

[![World Foundation ビジュアルリンクマップ](visual-link-map.svg)](visual-link-map.svg)

SVG内の各ノードは、主要な設計文書、モジュール索引、提案、意思決定、用語集へリンクします。GitHub上で画像としてだけ見える場合は、[visual-link-map.svg](visual-link-map.svg) を直接開いて使います。

## 索引構成

```mermaid
flowchart TB
  Overview["00<br/>全体像"]
  Layers["01<br/>層構造"]
  モジュール["02 / 09<br/>モジュール関係"]
  ガバナンス["03<br/>運用フロー"]
  ロードマップ["04<br/>移行ロードマップ"]
  安全方針["05<br/>安全装置"]
  翻訳["06<br/>翻訳フロー"]
  LifeAccess["07<br/>生活アクセス"]
  Adoption["08<br/>非強制の普及"]

  Overview --> Layers
  Layers --> モジュール
  モジュール --> ガバナンス
  モジュール --> LifeAccess
  モジュール --> 安全方針
  ガバナンス --> 安全方針
  Layers --> ロードマップ
  ロードマップ --> Adoption
  翻訳 --> ガバナンス

  click Overview "00-world-design-overview.md" "全体像"
  click Layers "01-cooperation-foundation-layers.md" "層構造"
  click モジュール "02-module-relationships.md" "モジュール関係"
  click ガバナンス "03-governance-process.md" "運用フロー"
  click ロードマップ "04-transition-roadmap.md" "移行ロードマップ"
  click 安全方針 "05-risk-and-safety-loops.md" "安全装置"
  click 翻訳 "06-multilingual-document-flow.md" "翻訳フロー"
  click LifeAccess "07-life-access-model.md" "生活アクセス"
  click Adoption "08-non-coercive-adoption.md" "非強制の普及"
```

## 図表一覧

| 図 | 役割 | 主な詳細文書 |
| --- | --- | --- |
| [00-world-design-overview.md](00-world-design-overview.md) | 世界設計の全体像 | [00-vision.md](../../docs/ja/00-vision.md), [01-principles.md](../../docs/ja/01-principles.md), [visual-link-map.svg](visual-link-map.svg) |
| [01-cooperation-foundation-layers.md](01-cooperation-foundation-layers.md) | 協力基盤の層構造 | [02-architecture.md](../../docs/ja/02-architecture.md), [modules/ja](../../modules/ja/README.md), [09-expanded-module-map.md](09-expanded-module-map.md) |
| [02-module-relationships.md](02-module-relationships.md) | モジュール関係図 | [modules/ja](../../modules/ja/README.md), [02-architecture.md](../../docs/ja/02-architecture.md), [05-threat-model.md](../../docs/ja/05-threat-model.md) |
| [03-governance-process.md](03-governance-process.md) | Issueから意思決定までの流れ | [proposals/ja](../../proposals/ja/README.md), [decisions/ja](../../decisions/ja/README.md), [modules/ja/governance](../../modules/ja/governance/README.md) |
| [04-transition-roadmap.md](04-transition-roadmap.md) | 既存制度から協力基盤への段階的移行 | [03-roadmap.md](../../docs/ja/03-roadmap.md), [08-non-coercive-adoption.md](08-non-coercive-adoption.md), [research/ja](../../research/ja/README.md) |
| [05-risk-and-safety-loops.md](05-risk-and-safety-loops.md) | 腐敗耐性と安全装置 | [05-threat-model.md](../../docs/ja/05-threat-model.md), [04-non-goals.md](../../docs/ja/04-non-goals.md), [SAFETY.md](../../SAFETY.md) |
| [06-multilingual-document-flow.md](06-multilingual-document-flow.md) | 日本語正本と翻訳の管理フロー | [07-translation-status.md](../../docs/ja/07-translation-status.md), [英語版文書](../../docs/en/README.md), [用語集](../../glossary/README.md) |
| [07-life-access-model.md](07-life-access-model.md) | 生活アクセスの設計モデル | [06-life-access-sustainability.md](../../docs/ja/06-life-access-sustainability.md), [modules/ja/welfare](../../modules/ja/welfare/README.md), [modules/ja/economy](../../modules/ja/economy/README.md) |
| [08-non-coercive-adoption.md](08-non-coercive-adoption.md) | 非強制の普及モデル | [01-principles.md](../../docs/ja/01-principles.md), [00-vision.md](../../docs/ja/00-vision.md), [04-transition-roadmap.md](04-transition-roadmap.md) |
| [09-expanded-module-map.md](09-expanded-module-map.md) | 規範 / 公共安全 / 連合を含む拡張モジュール関係図 | [02-architecture.md](../../docs/ja/02-architecture.md), [modules/ja](../../modules/ja/README.md), [02-module-relationships.md](02-module-relationships.md) |

## 表現形式の検討

Mermaidは、GitHub上で表示でき、差分レビューしやすい初期形式として使います。ただし、読みやすい公開図、クリック可能な索引、議論用の手描き図までMermaidだけで済ませません。図の目的に応じて、次の形式を使い分けます。

| 形式 | 使う場面 | このリポジトリでの扱い |
| --- | --- | --- |
| Mermaid | フロー、関係図、レビュー中の設計メモ | Markdown内の軽量な図として使う。見た目を詰めすぎない |
| SVG | 主要な全体図、クリック可能な索引、公開向けの清書 | Markdown図が読みにくい場合の代替入口にする |
| Excalidraw | 構想段階の手描き風整理、議論中の概念図 | 議論用。採用する場合は `.excalidraw` と書き出し画像をセットで置く |
| diagrams.net / draw.io | 複雑な構造図、公開資料用の清書 | XML差分が大きいため、更新理由と書き出し先を明記する |
| D2 / Graphviz | 大きな依存関係、モジュール間関係の自動レイアウト | 生成手順を残せる場合に採用する |
| Markdown table | 図と本文の対応表、読み順、責任範囲 | リンクの正本として扱う。図だけではなく表でも辿れるようにする |

当面は、Markdownページを正本にし、Mermaidはその中の図表現として扱います。中心となる図はSVGやExcalidrawなどを併用できます。併用する場合は、正本ファイル、書き出しファイル、更新手順を同じディレクトリ内に明記します。

## リンク方針

リンクは、独立したリンク一覧として積み上げるのではなく、できる限り説明文、表、Mermaidの `click`、SVGノードの中へ埋め込みます。

図と本文のどちらから読んでも同じ設計判断へ戻れるようにします。Mermaidを使う場合も、単なる挿絵にせず、ノードを対応する本文、図表、[Issue](https://github.com/acecore-systems/world-foundation/issues)、[Pull Request](https://github.com/acecore-systems/world-foundation/pulls) へ接続します。リンク集は索引ページや表が必要な場合だけにします。

## 方針

現時点の図表は、レビューしやすいMermaid入りMarkdownを中心に管理します。ただし、Mermaidが読みづらい場面ではSVG索引やMarkdown表を優先して補います。

図は完成図ではなく、議論のための設計メモです。構造が変わった場合は、対応するdocs、modules、glossary、提案、意思決定と一緒に更新します。Mermaid以外の形式を採用する場合も、変更理由と更新手順を残します。
