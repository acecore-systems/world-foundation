# ガバナンスプロセス

この図は、[Issue](https://github.com/acecore-systems/world-foundation/issues) から [提案](../../proposals/ja/README.md)、[Pull Request](https://github.com/acecore-systems/world-foundation/pulls)、[意思決定](../../decisions/ja/README.md) までの初期運用フローです。変更前に [対象外](../../docs/ja/04-non-goals.md)、[安全方針](../../SAFETY.md)、[脅威モデル](../../docs/ja/05-threat-model.md) を通す流れを含めます。

```mermaid
flowchart TD
  Idea["Idea Issue<br/>新しいアイデア"]
  Problem["Problem Issue<br/>問題・矛盾・リスク"]
  翻訳["翻訳 Issue<br/>翻訳・用語"]
  NonGoals["対象外 Check<br/>目指さないものの確認"]
  安全方針["安全方針 Check<br/>悪用・法務・監視化の確認"]
  Threat["脅威モデル Check<br/>腐敗・支配・離脱不能性の確認"]
  提案["提案<br/>変更案・リスク・代替案"]
  PullRequest["Pull Request<br/>具体的な変更"]
  Review["Review<br/>原則・用語・悪用ケース確認"]
  意思決定["意思決定<br/>重要判断の記録"]
  Docs["docs / modules / glossary"]
  Reopen["再検討 / 異議申し立て"]
  Rollback["Rollback<br/>問題発生時の戻し方"]

  Idea --> 提案
  Problem --> 提案
  翻訳 --> PullRequest
  提案 --> NonGoals
  NonGoals --> 安全方針
  安全方針 --> Threat
  Threat --> PullRequest
  提案 --> PullRequest
  PullRequest --> Review
  Review --> Docs
  Review --> 意思決定
  意思決定 --> Docs
  Review --> Reopen
  Reopen --> 提案
  Reopen --> Rollback
  Rollback --> Review

  click Idea "https://github.com/acecore-systems/world-foundation/issues" "Idea Issue"
  click Problem "https://github.com/acecore-systems/world-foundation/issues" "Problem Issue"
  click 翻訳 "https://github.com/acecore-systems/world-foundation/issues" "翻訳 Issue"
  click NonGoals "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/04-non-goals.md" "対象外"
  click 安全方針 "https://github.com/acecore-systems/world-foundation/blob/main/SAFETY.md" "安全方針"
  click Threat "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/05-threat-model.md" "脅威モデル"
  click 提案 "https://github.com/acecore-systems/world-foundation/blob/main/proposals/ja/README.md" "提案"
  click PullRequest "https://github.com/acecore-systems/world-foundation/pulls" "Pull Request"
  click Review "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/01-principles.md" "レビュー観点"
  click 意思決定 "https://github.com/acecore-systems/world-foundation/blob/main/decisions/ja/README.md" "意思決定"
  click Docs "https://github.com/acecore-systems/world-foundation/blob/main/docs/ja/README.md" "docs / modules / glossary"
  click Reopen "https://github.com/acecore-systems/world-foundation/issues" "再検討 / 異議申し立て"
  click Rollback "https://github.com/acecore-systems/world-foundation/blob/main/assets/diagrams/05-risk-and-safety-loops.md" "Rollback"
```
