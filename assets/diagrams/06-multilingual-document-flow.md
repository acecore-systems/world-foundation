# 多言語ドキュメント運用

この図は、[日本語の設計文書](../../docs/ja/README.md) を初期正本とし、[日英共通用語](../../glossary/terms.yml) を通して [英語版文書](../../docs/en/README.md) へ反映する流れです。翻訳状態の管理は [翻訳ステータス](../../docs/ja/07-translation-status.md) に置きます。

```mermaid
flowchart TD
  JA["docs/ja<br/>初期正本"]
  用語集["glossary/terms.yml<br/>日英共通用語"]
  提案["提案<br/>必要に応じて日本語から開始"]
  意思決定["意思決定<br/>重要判断を記録"]
  EN["docs/en<br/>英語版"]
  翻訳Issue["翻訳 Issue<br/>翻訳・用語の揺れ"]
  Review["翻訳レビュー"]

  JA --> 用語集
  JA --> 提案
  提案 --> 意思決定
  意思決定 --> EN
  用語集 --> EN
  EN --> 翻訳Issue
  翻訳Issue --> Review
  Review --> EN
  Review --> 用語集

  click JA "../../docs/ja/README.md" "日本語文書"
  click 用語集 "../../glossary/README.md" "用語集"
  click 提案 "../../proposals/ja/README.md" "提案"
  click 意思決定 "../../decisions/ja/README.md" "意思決定"
  click EN "../../docs/en/README.md" "英語文書"
  click 翻訳Issue "https://github.com/acecore-systems/world-foundation/issues" "翻訳 Issue"
  click Review "../../docs/ja/07-translation-status.md" "翻訳ステータス"
```
