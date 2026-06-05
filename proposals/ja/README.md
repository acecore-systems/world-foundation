# Proposals

このディレクトリには、World Foundation Designの設計変更や新しい仕組みに関する提案を置きます。

提案は、いきなり本体文書を変更するのではなく、まずProposalとして議論するために使います。重要な提案では [Non-goals](../../docs/ja/04-non-goals.md)、[Threat Model](../../docs/ja/05-threat-model.md)、[Governance Process](../../assets/diagrams/03-governance-process.md) を確認し、採用された判断は [decisions/ja](../../decisions/ja/README.md) に残します。

## 位置づけ

```mermaid
flowchart LR
  Issue["Issue<br/>問題・アイデア・翻訳"]
  Proposal["Proposal<br/>変更案・影響・リスク"]
  Review["Review<br/>原則・安全境界・用語"]
  PullRequest["Pull Request<br/>具体的な変更"]
  Docs["docs / modules<br/>反映先"]
  Decision["decisions<br/>重要判断の記録"]

  Issue --> Proposal
  Proposal --> Review
  Review --> PullRequest
  PullRequest --> Docs
  Review --> Decision
  Decision --> Docs
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

- [0001-initial-governance-process.md](0001-initial-governance-process.md): 初期ガバナンスプロセス
