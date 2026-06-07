# Handoffs

このディレクトリには、次の作業者や次回Codexへ渡すための引継ぎ記録を置きます。

引継ぎ書は設計本文ではありません。設計に反映する場合は、[Issue](https://github.com/acecore-systems/world-foundation/issues)、[Proposal](../../proposals/ja/README.md)、[Pull Request](https://github.com/acecore-systems/world-foundation/pulls)、[Decision](../../decisions/ja/README.md) の流れで扱います。

## 位置づけ

```mermaid
flowchart LR
  Work["作業中の文脈"]
  Handoff["Handoff<br/>次回作業への引継ぎ"]
  Issue["Issue<br/>未反映事項の整理"]
  Proposal["Proposal<br/>設計変更案"]
  PullRequest["Pull Request<br/>本文への反映"]
  Decision["Decision<br/>重要判断"]

  Work --> Handoff
  Handoff --> Issue
  Issue --> Proposal
  Proposal --> PullRequest
  Proposal --> Decision

  click Work "https://github.com/acecore-systems/world-foundation/blob/main/README.md" "作業中の文脈"
  click Handoff "https://github.com/acecore-systems/world-foundation/blob/main/meta/handoffs/README.md" "Handoff"
  click Issue "https://github.com/acecore-systems/world-foundation/issues" "Issue"
  click Proposal "https://github.com/acecore-systems/world-foundation/blob/main/proposals/ja/README.md" "Proposal"
  click PullRequest "https://github.com/acecore-systems/world-foundation/pulls" "Pull Request"
  click Decision "https://github.com/acecore-systems/world-foundation/blob/main/decisions/ja/README.md" "Decision"
```
