# Decision: 用語集を単一YAMLで管理する

## Status

Accepted

## Context

用語の揺れは思想の揺れにつながる。特に多言語化する場合、言語ごとに用語集を分けると整合性が崩れやすい。

World Foundation Designでは、自由参加、離脱可能性、フォーク可能性、腐敗耐性、Non-goals、Threat Modelなど、意味のずれが安全性に直結する用語を扱う。

## Decision

用語集は言語別に分けず、`glossary/terms.yml` で一元管理する。

## Rationale

表形式化、自動処理、多言語展開、翻訳整合性、レビューのしやすさを優先する。

同じIDに日本語と英語を置くことで、用語追加や定義変更のレビュー範囲を明確にする。

## Consequences

用語追加時はYAMLを更新する。重要用語の変更はDecisionへ記録する。

YAML構文を壊すと用語集全体の利用に影響するため、重複IDと構文の確認を行う。

## Alternatives Considered

- 言語別glossary
- Markdown表のみ
- 各文書内で個別定義
