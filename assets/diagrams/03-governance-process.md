# Governance Process

この図は、Issueから [Proposal](../../proposals/ja/README.md)、Pull Request、[Decision](../../decisions/ja/README.md) までの初期運用フローです。変更前に [Non-goals](../../docs/ja/04-non-goals.md)、[SAFETY](../../SAFETY.md)、[Threat Model](../../docs/ja/05-threat-model.md) を通す流れを含めます。

```mermaid
flowchart TD
  Idea["Idea Issue<br/>新しいアイデア"]
  Problem["Problem Issue<br/>問題・矛盾・リスク"]
  Translation["Translation Issue<br/>翻訳・用語"]
  NonGoals["Non-goals Check<br/>目指さないものの確認"]
  Safety["Safety Check<br/>悪用・法務・監視化の確認"]
  Threat["Threat Model Check<br/>腐敗・支配・離脱不能性の確認"]
  Proposal["Proposal<br/>変更案・リスク・代替案"]
  PullRequest["Pull Request<br/>具体的な変更"]
  Review["Review<br/>原則・用語・悪用ケース確認"]
  Decision["Decision<br/>重要判断の記録"]
  Docs["docs / modules / glossary"]
  Reopen["再検討 / 異議申し立て"]
  Rollback["Rollback<br/>問題発生時の戻し方"]

  Idea --> Proposal
  Problem --> Proposal
  Translation --> PullRequest
  Proposal --> NonGoals
  NonGoals --> Safety
  Safety --> Threat
  Threat --> PullRequest
  Proposal --> PullRequest
  PullRequest --> Review
  Review --> Docs
  Review --> Decision
  Decision --> Docs
  Review --> Reopen
  Reopen --> Proposal
  Reopen --> Rollback
  Rollback --> Review

  click NonGoals "../../docs/ja/04-non-goals.md" "Non-goals"
  click Safety "../../SAFETY.md" "Safety"
  click Threat "../../docs/ja/05-threat-model.md" "Threat Model"
  click Proposal "../../proposals/ja/README.md" "Proposals"
  click Decision "../../decisions/ja/README.md" "Decisions"
  click Docs "../../docs/ja/README.md" "docs / modules / glossary"
```
