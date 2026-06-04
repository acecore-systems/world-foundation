# 翻訳ステータス管理を導入するか検討する

## 背景

日本語ファーストと単一YAML用語集は導入済みだが、各文書の翻訳ステータス管理はまだ初期状態である。

## 目的

日本語正本と英語版の差分、翻訳遅延、意味のズレ、Glossary反映状況を管理する。

## 検討論点

- `draft`
- `translated`
- `reviewed`
- `canonical`
- `outdated`
- front matter管理
- Translation Issueとの接続
- 重要Decisionの翻訳優先度
- Non-goals / Safety / Threat Modelの英語レビュー優先度

## 安全上の注意

翻訳の歪みにより、自由参加、非強制、国家との非敵対、安全境界の意味が変わらないようにする。

## 関連文書

- `docs/ja/07-translation-status.md`
- `docs/en/07-translation-status.md`
- `glossary/terms.yml`
- `.github/ISSUE_TEMPLATE/translation.yml`

## 完了条件

- 翻訳ステータス方針がレビューされている
- 重要文書の初期ステータスが整理されている
- Glossary拡張要否が判断されている
