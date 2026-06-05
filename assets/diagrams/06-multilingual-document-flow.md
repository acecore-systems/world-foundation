# Multilingual Document Flow

この図は、[docs/ja](../../docs/ja/README.md) を初期正本とし、[glossary/terms.yml](../../glossary/terms.yml) を通して [docs/en](../../docs/en/README.md) へ反映する流れです。翻訳状態の管理は [Translation Status](../../docs/ja/07-translation-status.md) に置きます。

```mermaid
flowchart TD
  JA["docs/ja<br/>初期正本"]
  Glossary["glossary/terms.yml<br/>日英共通用語"]
  Proposal["Proposal<br/>必要に応じて日本語から開始"]
  Decision["Decision<br/>重要判断を記録"]
  EN["docs/en<br/>英語版"]
  TranslationIssue["Translation Issue<br/>翻訳・用語の揺れ"]
  Review["翻訳レビュー"]

  JA --> Glossary
  JA --> Proposal
  Proposal --> Decision
  Decision --> EN
  Glossary --> EN
  EN --> TranslationIssue
  TranslationIssue --> Review
  Review --> EN
  Review --> Glossary

  click JA "../../docs/ja/README.md" "Japanese docs"
  click Glossary "../../glossary/README.md" "Glossary"
  click Proposal "../../proposals/ja/README.md" "Proposals"
  click Decision "../../decisions/ja/README.md" "Decisions"
  click EN "../../docs/en/README.md" "English docs"
  click Review "../../docs/ja/07-translation-status.md" "Translation Status"
```
