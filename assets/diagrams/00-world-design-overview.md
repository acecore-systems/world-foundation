# 世界設計の全体像

この図は、World Foundation Designが何を中心に置くかを示します。目的は [ビジョン](../../docs/ja/00-vision.md)、設計原則は [設計原則](../../docs/ja/01-principles.md)、構造は [アーキテクチャ](../../docs/ja/02-architecture.md) に分けます。クリック可能な全体索引は [visual-link-map.svg](visual-link-map.svg) です。

```mermaid
flowchart TB
  ビジョン["全ての人が好きなことに集中できる世界"]
  設計原則["設計原則"]
  アーキテクチャ["連盟型アーキテクチャ"]
  モジュール["機能モジュール"]
  ガバナンス["透明な意思決定"]
  Experiments["小さな実験"]
  Records["提案 / 意思決定 / 用語集"]
  Feedback["レビューと改善"]

  ビジョン --> 設計原則
  設計原則 --> アーキテクチャ
  アーキテクチャ --> モジュール
  モジュール --> Experiments
  Experiments --> Records
  Records --> Feedback
  Feedback --> 設計原則
  ガバナンス --> Records
  ガバナンス --> Feedback

  click ビジョン "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/00-vision.md" "ビジョン"
  click 設計原則 "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/01-principles.md" "設計原則"
  click アーキテクチャ "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/02-architecture.md" "アーキテクチャ"
  click モジュール "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/README.md" "モジュール"
  click ガバナンス "https://github.com/acecore-systems/world-foundation/blob/main/modules/ja/governance/README.md" "ガバナンス"
  click Experiments "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/03-roadmap.md" "小さな実験"
  click Records "https://github.com/acecore-systems/world-foundation/blob/main/proposals/ja/README.md" "提案 / 意思決定 / 用語集"
  click Feedback "https://github.com/acecore-systems/world-foundation/blob/main/assets/diagrams/05-risk-and-safety-loops.md" "レビューと改善"
```
