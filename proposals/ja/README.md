# 提案

このディレクトリには、World Foundation Designの設計変更や新しい仕組みに関する提案を置きます。

提案は、いきなり本体文書を変更するのではなく、まず提案として議論するために使います。重要な提案では [対象外](../../docs/ja/04-non-goals.md)、[脅威モデル](../../docs/ja/05-threat-model.md)、[ガバナンスプロセス](../../assets/diagrams/03-governance-process.md) を確認し、採用された判断は [意思決定](../../decisions/ja/README.md) に残します。

## 位置づけ

```mermaid
flowchart LR
  Issue["Issue<br/>問題・アイデア・翻訳"]
  提案["提案<br/>変更案・影響・リスク"]
  Review["Review<br/>原則・安全境界・用語"]
  PullRequest["Pull Request<br/>具体的な変更"]
  Docs["docs / modules<br/>反映先"]
  意思決定["decisions<br/>重要判断の記録"]

  Issue --> 提案
  提案 --> Review
  Review --> PullRequest
  PullRequest --> Docs
  Review --> 意思決定
  意思決定 --> Docs

  click Issue "https://github.com/acecore-systems/world-foundation/issues" "GitHub Issues"
  click 提案 "https://github.com/acecore-systems/world-foundation/blob/main/proposals/ja/README.md" "提案"
  click Review "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/01-principles.md" "レビュー観点"
  click PullRequest "https://github.com/acecore-systems/world-foundation/pulls" "GitHub Pull Requests"
  click Docs "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/README.md" "docs / modules"
  click 意思決定 "https://github.com/acecore-systems/world-foundation/blob/main/decisions/ja/README.md" "意思決定"
```

## 扱う内容

- 設計変更
- 新しいモジュールや運用手続き
- 既存文書に影響する方針変更
- 重要なリスクや代替案の整理
- docs、modules、glossary、decisionsへの影響

## 命名

初期は `0001-short-title.md` のような連番形式を推奨します。

提案の粒度は小さく保ち、影響する文書やモジュールを明記してください。

## 提案一覧

- [初期ガバナンスプロセス](0001-initial-governance-process.md)
