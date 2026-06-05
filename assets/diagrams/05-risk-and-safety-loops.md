# Risk and Safety Loops

この図は、[Threat Model](../../docs/ja/05-threat-model.md) のリスク評価、[Non-goals](../../docs/ja/04-non-goals.md) と [SAFETY](../../SAFETY.md) の安全境界、[Audit](../../modules/ja/audit/README.md) と [Arbitration](../../modules/ja/arbitration/README.md) による異議申し立てを一つの安全装置として扱う流れです。

```mermaid
flowchart TD
  Change["変更案"]
  Risk["リスク評価"]
  Abuse["悪用ケース"]
  Review["レビュー"]
  Decision["Decision記録"]
  Operation["運用"]
  Audit["監査・ログ"]
  Appeal["異議申し立て"]
  Fix["修正Proposal"]
  Fork["フォーク可能性"]

  Change --> Risk
  Risk --> Abuse
  Abuse --> Review
  Review --> Decision
  Decision --> Operation
  Operation --> Audit
  Audit --> Appeal
  Appeal --> Fix
  Fix --> Review
  Appeal --> Fork
  Fork -. "最後の安全装置" .-> Change

  click Risk "../../docs/ja/05-threat-model.md" "Threat Model"
  click Abuse "../../docs/ja/04-non-goals.md" "Non-goals"
  click Decision "../../decisions/ja/README.md" "Decisions"
  click Audit "../../modules/ja/audit/README.md" "Audit"
  click Appeal "../../modules/ja/arbitration/README.md" "Arbitration"
  click Fix "../../proposals/ja/README.md" "Proposals"
```
