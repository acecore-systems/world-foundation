# リスクと安全性のループ

この図は、[脅威モデル](../../docs/ja/05-threat-model.md) のリスク評価、[対象外](../../docs/ja/04-non-goals.md) と [安全方針](../../SAFETY.md) の安全境界、[監査](../../modules/ja/audit/README.md) と [仲裁](../../modules/ja/arbitration/README.md) による異議申し立てを一つの安全装置として扱う流れです。

```mermaid
flowchart TD
  Change["変更案"]
  Risk["リスク評価"]
  Abuse["悪用ケース"]
  Review["レビュー"]
  意思決定["意思決定記録"]
  Operation["運用"]
  監査["監査・ログ"]
  Appeal["異議申し立て"]
  Fix["修正提案"]
  Fork["フォーク可能性"]

  Change --> Risk
  Risk --> Abuse
  Abuse --> Review
  Review --> 意思決定
  意思決定 --> Operation
  Operation --> 監査
  監査 --> Appeal
  Appeal --> Fix
  Fix --> Review
  Appeal --> Fork
  Fork -. "最後の安全装置" .-> Change

  click Risk "../../docs/ja/05-threat-model.md" "脅威モデル"
  click Abuse "../../docs/ja/04-non-goals.md" "対象外"
  click 意思決定 "../../decisions/ja/README.md" "意思決定"
  click 監査 "../../modules/ja/audit/README.md" "監査"
  click Appeal "../../modules/ja/arbitration/README.md" "仲裁"
  click Fix "../../proposals/ja/README.md" "提案"
```
