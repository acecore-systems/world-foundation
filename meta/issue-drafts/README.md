# Issue Drafts

このディレクトリには、[GitHub Issue](https://github.com/acecore-systems/world-foundation/issues) として作成する前の下書きを置きます。

Issue下書きは正式な設計決定ではありません。実際に採用する場合は、[Issue](https://github.com/acecore-systems/world-foundation/issues)、[Proposal](../../proposals/ja/README.md)、[Pull Request](https://github.com/acecore-systems/world-foundation/pulls)、[Decision](../../decisions/ja/README.md) の流れで扱います。

## 位置づけ

```mermaid
flowchart LR
  Draft["Issue Draft<br/>作成前の下書き"]
  Issue["GitHub Issue<br/>議論の開始"]
  Proposal["Proposal<br/>設計変更案"]
  PullRequest["Pull Request<br/>具体的な変更"]
  Decision["Decision<br/>重要判断の記録"]
  Docs["docs / modules<br/>反映先"]

  Draft --> Issue
  Issue --> Proposal
  Proposal --> PullRequest
  PullRequest --> Docs
  Proposal --> Decision
  Decision --> Docs

  click Draft "https://github.com/acecore-systems/world-foundation/blob/main/meta/issue-drafts/README.md" "Issue下書き"
  click Issue "https://github.com/acecore-systems/world-foundation/issues" "GitHub Issues"
  click Proposal "https://github.com/acecore-systems/world-foundation/blob/main/proposals/ja/README.md" "Proposal"
  click PullRequest "https://github.com/acecore-systems/world-foundation/pulls" "Pull Request"
  click Decision "https://github.com/acecore-systems/world-foundation/blob/main/decisions/ja/README.md" "Decision"
  click Docs "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/README.md" "docs / modules"
```
