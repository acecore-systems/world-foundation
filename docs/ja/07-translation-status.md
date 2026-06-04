# Translation Status

この文書は、日本語正本と英語版の翻訳ステータスを管理するための初期方針です。

## 目的

World Foundation Designは日本語ファーストで始めますが、将来的には世界中の参加者が理解できる必要があります。

翻訳が遅れたり、意味がずれたりすると、Non-goals、Safety、Threat Model、Glossaryの安全境界が弱まる可能性があります。

## ステータス

- `draft`: 下書き
- `translated`: 翻訳済み
- `reviewed`: レビュー済み
- `canonical`: 正本または正本相当
- `outdated`: 原文更新に追従できていない

## 初期方針

- 日本語版を初期正本とする
- 英語版は重要文書から順に翻訳・更新する
- Non-goals、Safety、Threat Model、Code of Conduct、重要Decisionは優先的に英語レビューする
- 用語は `glossary/terms.yml` を参照する
- 翻訳差分や意味のずれはTranslation Issueで扱う
- 自動翻訳だけで安全境界を確定しない

## 初期ステータス表

| 文書 | 日本語 | 英語 | 備考 |
| --- | --- | --- | --- |
| Vision | canonical | reviewed | 英語版は簡潔 |
| Principles | canonical | reviewed | 自由と平和の両立を追加 |
| Architecture | canonical | reviewed | モジュール追加に追従 |
| Roadmap | canonical | reviewed | 完了条件あり |
| Non-goals | canonical | reviewed | 安全境界のため優先 |
| Threat Model | canonical | translated | 英語版は要継続レビュー |
| Safety | canonical | not applicable | ルート文書 |
| Code of Conduct | canonical | not applicable | ルート文書 |
| Decisions | canonical | draft | 英語版Decisionは未整備 |

## 未解決の問い

- 翻訳ステータスを各ファイルのfront matterで管理するか
- Glossaryに `status` や `reviewed_by` を追加するか
- 重要Decisionの英語要約をどこまで作るか
- 翻訳レビュー権限をどう設計するか
