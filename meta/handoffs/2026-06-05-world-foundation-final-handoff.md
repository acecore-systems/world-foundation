# World Foundation Design - Codex最終引継ぎ書

このファイルを、次のCodex作業・別スレッド・別担当者への引継ぎとしてそのまま渡してください。  
対象リポジトリは `acecore-systems/world-foundation` です。

---

## 0. この引継ぎ書の目的

この引継ぎ書は、これまでの長い設計会話で固めた思想・設計方針・安全境界・未反映事項を、次のCodexが誤解しないように1ファイルへ集約したものです。

重要なのは、単なるREADME更新ではありません。

このリポジトリは、通常のOSSソフトウェアではなく、**全ての人が好きなことに集中できる世界を目指すための、OSS型の社会設計リポジトリ**です。

社会制度、協力基盤、組織連盟、生活基盤、信用、福祉、経済、仲裁、インフラ、腐敗耐性、安全境界を、ソフトウェア設計のようにIssue、Pull Request、Proposal、Decision、Glossary、Moduleへ分解して扱います。

---

## 1. 現在の最重要コンセプト

### 1.1 主語は `World Foundation Design`

現在のリポジトリでは、主語を `Acecore` から `World Foundation Design` へ整理しています。  
これは非常に重要です。

`Acecore` は初期コードネームとして扱います。  
特定の組織名、ブランド名、創設者、単一実装が世界設計の中心になってはいけません。

今後の文書では、原則として以下の表現を優先してください。

望ましい表現:

- World Foundation Design
- この設計
- 世界設計
- 協力基盤
- 連盟型アーキテクチャ
- 組織連盟
- 自由参加型の協力基盤
- レビュー可能でフォーク可能な社会設計
- 複数組織が共通プロトコルで協力する基盤

避ける表現:

- Acecoreが世界を支配する
- Acecoreが国家を倒す
- Acecoreが政府を置き換える
- Acecoreが唯一の統治者になる
- Acecoreに従わせる
- Acecoreが人々を管理する
- Acecoreが国家を征服する

### 1.2 最終目的

この設計の目的は、**全ての人が好きなことに集中できる世界**を作ることです。

そのために、以下を減らします。

- 生存不安
- 強制的な労働
- 国境による分断
- 不透明な権力
- 戦争インセンティブ
- 離脱できない所属
- 法定通貨や国家制度への過剰な日常依存
- 巨大組織や国家だけに生活基盤を依存する構造

ただし、目的は国家転覆、暴力、違法回避、閉鎖共同体化、カルト化、支配ではありません。

### 1.3 国家との関係

この設計は、国家を力で置き換えることを目指しません。

目指すのは、より便利で、透明で、参加自由で、離脱可能で、フォーク可能な協力基盤を広げることで、国家が現在担っている多くの機能を段階的に不要化・軽量化していくことです。

表現方針:

- 「国家を壊す」ではなく「国家の必要性を段階的に減らす」
- 「政府を倒す」ではなく「国家以外でも担える機能を増やす」
- 「国家と戦う」ではなく「既存制度と接続しながら依存を減らす」
- 「単一世界政府」ではなく「組織連盟、共通プロトコル、多重所属」

### 1.4 支配ではなく協力

ユーザーの明確な意図は、支配ではありません。

重要な発言の要約:

- 単一支配組織にしたいわけではない
- 全ての人が好きなことだけをできる世界を作りたい
- 達成したら創設者自身は組織から降りるつもり
- 組織からの利益を受け取るつもりはない
- 腐敗耐性を十分に整えてから権限を手放す意図がある
- 国家を力で倒すのではなく、国家の必要性が自然に薄れる状態を目指す
- 自由と平和が矛盾しない世界を目指す

この意図は今後の文書にも残す必要があります。

---

## 2. 現在リポジトリに反映済みの内容

現在、以下は反映済みです。  
次のCodexは、これらを消したり弱めたりしないでください。

### 2.1 README

READMEには以下が反映されています。

- `World Foundation Design` を主語にする
- 全ての人が好きなことに集中できる世界を目指す
- 社会制度や協力基盤をIssue、Pull Request、Proposal、Decision、Glossary、Moduleで管理する
- 特定名称やブランドを広めるためのものではない
- 個人や組織が自由に参加し、協力し、離脱し、必要ならフォークできる協力基盤を設計する
- `Acecore` は初期コードネーム
- 日本語ファースト
- 英語対応を想定
- 透明性、離脱可能性、フォーク可能性、腐敗耐性
- 国家との敵対ではなく、国家が担う必要のある機能を段階的に減らす
- Code of Conduct、Safety、Non-goals、Threat Model、Reputation、Audit、metaへの導線

### 2.2 Vision

Visionには以下が反映されています。

- 全ての人が好きなことに集中できる世界
- 生存不安、強制労働、国境分断、不透明な権力、戦争インセンティブからの解放
- 特定組織名やブランドを広めるためではない
- 国家や社会を支配する仕組みではない
- 人類がレビューし、修正し、分岐し、改善し続けられる世界
- 生活、信用、経済、福祉、ガバナンス、仲裁、インフラを分けて設計する
- 1つの組織や制度が過剰な機能を持つと腐敗や支配が起きやすい
- 国家を力で置き換えず、より開かれた選択肢を増やす

### 2.3 Principles

Principlesには以下が反映されています。

- 自由参加
- 離脱可能性
- フォーク可能性
- 透明性
- モジュール化
- 腐敗耐性
- 多重所属
- 国家との非敵対
- 強制ではなく利便性

### 2.4 Architecture

Architectureには以下が反映されています。

初期モジュール:

- Identity
- Reputation
- Economy
- Welfare
- Governance
- Arbitration
- Infrastructure
- Audit

重要な安全境界:

- Reputationは人間の価値を固定するものではない
- Reputationは階級化や全面的な排除につなげない
- Auditは監視社会を作るためのものではない
- Auditは定義された範囲を検証する仕組み
- モジュール間の関係は支配ではなく、参照、連携、検証
- 各モジュールは接続するが、責任範囲を侵食しない

### 2.5 Roadmap

RoadmapにはPhase 0〜5があり、各Phaseに完了条件が追加されています。

特に反映済みの内容:

- Phase 0: Non-goals、Safety、Threat Model、Code of Conduct、初期モジュールREADME
- Phase 1: 初期組織、ガバナンス実験、小さな生活支援や協力実験
- Phase 2: Identity、Reputation、Economy、Welfare、Governance、Arbitration、Infrastructure、Audit
- Phase 3: 組織連盟
- Phase 4: 世界共通協力基盤
- Phase 5: 国家機能の縮小

Phase 5は「特定組織が国家を支配する」のではなく、人々が国家を意識しなくても協力し生活できる状態を作ることとして定義されています。

### 2.6 Safety

`SAFETY.md` には以下が反映されています。

- 国家転覆を目的にしない
- 暴力、武装組織化、私的制裁を目的にしない
- 税回避、労働法回避、金融規制回避、資金決済規制回避を目的にしない
- 閉鎖共同体、カルト、支配組織を目指さない
- 生活、思想、通信、経済活動を一元管理しない
- 仲裁やガバナンスを私刑や思想統制にしない
- 内部ポイントや生活アクセスは法制度、税務、労務、金融規制、資金決済規制との関係を慎重に整理する
- 実装前に専門家レビューが必要な領域を明示
- 透明性とプライバシーの境界を分ける

### 2.7 Non-goals

`docs/ja/04-non-goals.md` には以下が反映されています。

- 国家を力で置き換えない
- 政府を倒さない
- 単一支配組織にならない
- 特定名称や創設者を中心とした運動にしない
- 思想統制しない
- 強制参加を前提にしない
- 離脱不能な共同体や経済圏を作らない
- 税回避、労働法回避、金融規制回避を目的にしない
- 違法な給与代替や疑似通貨運用を目的にしない
- 軍事組織化しない
- 私的制裁や自警団化しない
- 閉鎖共同体化しない
- 創設者、管理者、メンテナーを神格化しない
- 福祉や生活支援を服従の条件にしない
- 信用スコアで人間の価値を固定しない
- 透明性を口実に私生活や思想を監視しない

### 2.8 Threat Model

`docs/ja/05-threat-model.md` には以下のリスクが反映されています。

- 権力集中
- 管理者の腐敗
- 創設者の神格化
- カルト化
- 透明性の低下
- 透明性を口実にした監視
- 離脱不能性
- 経済的囲い込み
- 内部ポイントの悪用
- 税務・労務・金融規制との衝突
- 信用スコアによる差別
- 福祉の支配化
- 仲裁の私刑化
- インフラ提供者による監視・検閲
- 翻訳の歪みによる思想の変質
- 国家や社会との不要な敵対
- 外部からの乗っ取り
- 議論の荒廃
- 目的の形骸化
- モジュール間の責任侵食
- 便利さによる実質的強制
- 多重所属の名目化

### 2.9 Economy Module

Economy Moduleには、会話で出た「円を消すのではなく、円を意識しないUXにする」「内部ポイントを慎重に扱う」「税務・労務・金融規制と衝突しない」が反映されています。

反映済みの区別:

- 法定通貨
- 内部ポイント
- 生活アクセス
- 貢献記録

重要な方針:

- 法定通貨を否定しない
- 給与、税務、会計処理などは既存法制度に従う
- 内部ポイントは名前だけで法的論点を避けられるものではない
- 換金性、移転性、報酬性、投資性、前払い性は慎重に扱う
- 法務・税務・労務・資金決済・消費者保護等の論点を早めに洗い出す
- 生活アクセスを離脱不能性や服従要求につなげない

### 2.10 Welfare Module

Welfare Moduleには以下が反映されています。

- 生存不安を減らす
- 人が好きなことに集中できる状態を支える
- 食、住、通信、教育、医療・健康支援、生活アクセス、相互扶助
- 支援は参加者を縛るためではなく、自由な活動の土台を増やすため
- 強制的な共同生活、離脱不能な福祉制度、特定思想への依存、支援を条件にした服従要求を範囲外にする

### 2.11 Governance Module

Governance Moduleには以下が反映されています。

- 管理者や意思決定者は支配者ではない
- 透明な手続きを維持する責任を持つ参加者
- Issue、Pull Request、Proposal、Decisionによる軽量運用
- 権限の明示
- 判断理由の記録
- 権限の分離
- 異議申し立て
- 任期と見直し
- 利益相反の開示
- フォーク可能性の維持
- 最小権限
- 公開可能な範囲の透明性
- 小さく試して記録する

### 2.12 Arbitration Module

Arbitration Moduleには以下が反映されています。

- 紛争や対立を暴力ではなく透明な手続きで解決する
- 国家司法をただ置き換えるものではない
- 組織間・参加者間の対立を低コストで、記録可能で、再検討可能にする
- 暴力による執行、国家司法の完全代替、密室裁判、参加者の権利を無視した強制処分を範囲外にする

### 2.13 Infrastructure Module

Infrastructure Moduleには以下が反映されています。

- 通信、計算資源、データ、生活インフラ
- 単一巨大インフラではなく、複数組織や地域が相互接続できる基盤
- 単一組織による全インフラ独占、監視インフラ、離脱不能な依存構造、参加者の生活や通信の一元管理を範囲外にする

### 2.14 Reputation Module

Reputation Moduleには以下が反映されています。

- 信用、貢献、行動履歴、信頼性
- 人間の価値を固定するものではない
- 協力しやすくするための補助情報
- 身分階級や排除の仕組みにしない
- 文脈ごとの評価
- 評価根拠、評価者、利用範囲、訂正手続き、異議申し立て
- 匿名性や仮名性が必要な参加者を不必要に露出しない
- 経済・福祉・ガバナンスを支配しすぎない境界を未解決の問いとして扱う

### 2.15 Audit Module

Audit Moduleには以下が反映されています。

- 透明性、監査ログ、意思決定履歴、会計透明性、権限変更履歴、利益相反記録
- 監視社会を作るものではない
- 検証可能性とプライバシー保護の境界を設計する
- 意思決定ログ、権限変更履歴、会計透明性、Proposal / Decision追跡、監査可能な変更履歴、利益相反、不正検出
- 参加者の私生活監視、全通信の監視、思想監視、監査権限の中央集権化を範囲外にする

### 2.16 Decisions

以下がDecision化されています。

- `0001-japanese-first-policy.md`
- `0002-single-glossary-yaml.md`
- `0003-lightweight-governance-process.md`

これらは重要です。  
今後のCodexは不用意に変更しないでください。変更する場合はProposalとDecisionが必要です。

### 2.17 Proposal

以下が作成されています。

- `proposals/ja/0001-initial-governance-process.md`

Issue → Proposal → Pull Request → Review → Merge → Decision → 必要ならReview/Rollback の軽量プロセスが定義されています。

### 2.18 Templates

以下が改善されています。

- Pull Request Template
- Idea Issue Template
- Problem Issue Template
- Proposal Issue Template
- Translation Issue Template
- Proposal Template
- Decision Template

PRチェックには以下が入っています。

- 支配主体として表現していない
- 自由参加、離脱可能性、透明性に反していない
- 用語集と矛盾していない
- 法務・税務・労務・金融規制回避の意図になっていない
- 国家や社会との不要な敵対を煽っていない
- カルト的、閉鎖共同体的に見えない
- 離脱不能性や経済的囲い込みを強めていない
- 差別につながらない
- プライバシー侵害や監視強化につながらない
- Reputationが人間の価値固定や階級化につながっていない
- Auditが私生活監視や思想監視につながっていない
- Non-goals / Safety / Threat Modelへの影響を確認した

### 2.19 Glossary

Glossaryは単一YAMLで日英管理されています。  
用語数はCodex報告では57件、重複なしです。

反映済みの重要用語:

- World Foundation Design
- Life OS
- World Federation
- Cooperation Infrastructure
- Multi-affiliation
- Right to Exit
- Forkability
- Corruption Resistance
- Modularity
- Single Responsibility
- Transparency
- Open Protocol
- Voluntary Participation
- Federation
- Identity
- Reputation
- Welfare
- Arbitration
- Governance
- Transition
- Audit
- Accountability
- Decision Log
- Proposal
- Module
- Protocol
- Interoperability
- Decentralization
- Subsidiarity
- Non-goals
- Threat Model
- Safety Policy
- Code of Conduct

---

## 3. 現時点でまだ弱い・未反映の領域

ここが今後の最重要引継ぎです。  
会話全体から見ると、以下はまだIssue化・設計化が必要です。

---

### 3.1 Norms Module / Rule Layer

会話では、国家機能のうち「法」も将来的に協力基盤へ統合したいという話がありました。

現在は Governance、Arbitration、Safety、Non-goals に分散して吸収されています。  
しかし、独立した `Norms Module` または `Rule Layer` はまだありません。

今後検討すべき論点:

- ルール
- 規約
- 権利
- 義務
- 契約
- 例外
- 制裁
- 改定手続き
- 国家法との接続
- Arbitrationとの境界
- Governanceとの境界
- 私的法体系化や違法な司法代替に見えない安全境界

推奨Issue:

```txt
Norms Module / Rule Layerを追加するか検討する
```

注意:

この領域は「国家法の違法な代替」に見えないよう、国家法との接続、専門家レビュー、Non-goalsとの整合性を必ず扱うこと。

---

### 3.2 Public Safety / Civil Peace

会話では、国家機能のうち「治安」も将来的な対象として挙がっていました。

現在は Safety、Code of Conduct、Arbitration、Threat Model に一部反映されています。  
ただし、独立した治安設計はまだありません。

今後検討すべき論点:

- 暴力予防
- 私的制裁の禁止
- 自警団化の防止
- 通報
- 国家警察・司法との連携
- コミュニティ安全設計
- 危険兆候の早期発見
- 仲裁との境界
- 公共安全と監視化の境界

推奨Issue:

```txt
Public Safetyを国家司法・警察と敵対しない形でどう扱うか検討する
```

注意:

この領域は危険です。  
「治安維持組織」「警察代替」「私的制裁」「武装化」に見える表現は避けること。

---

### 3.3 Founder Non-privilege / Founder Exit Policy

会話では、ユーザーが以下を明言しています。

- 達成したら自分は組織から降りるつもり
- 組織から利益を受け取るつもりはない
- 支配したいわけではない
- 腐敗耐性を整えてから手放したい

現在は、創設者神格化禁止、特定名称中心にしない、管理者は支配者ではない、という形で反映されています。

ただし、創設者の非特権・離脱・利益相反・権限移譲を扱う独立Decisionはまだありません。

推奨Issue:

```txt
Founder Non-privilege / Founder Exit PolicyをDecision化する
```

含めるべき論点:

- 創設者は永久権限を持たない
- 創設者の発言もレビュー対象
- 創設者を神格化しない
- 創設者利益の透明性
- 知財、商標、資産、寄付、報酬の扱い
- 達成後の権限移譲
- 創設者不在でも続く設計
- 創設者が退いた後のガバナンス
- 創設者が戻る場合の条件
- 創設者が利益相反を持つ場合の開示

これは思想の中核に近いので、早めにDecision化する価値があります。

---

### 3.4 Organization Federation Protocol

会話の中心は「組織の連盟が国を不要化する」という考えでした。

現在はArchitectureとRoadmapに連盟型アーキテクチャ、組織連盟、共通プロトコルとして反映されています。

ただし、`Federation Module` または `Organization Federation Protocol` はまだ独立していません。

推奨Issue:

```txt
Organization Federation Protocolを独立モジュール化するか検討する
```

論点:

- 組織間参加
- 多重所属
- 組織間の相互承認
- 組織ごとの自治
- 共通プロトコル準拠
- フォーク時の互換性
- Reputationの組織間共有
- Auditの組織間検証
- Arbitrationの組織間接続
- Federationからの離脱
- Federationの乗っ取り防止
- 連盟標準と地域差の両立

注意:

単一の世界政府や中央支配組織に見えないようにすること。  
連盟は支配機構ではなく、相互接続プロトコルとして扱うこと。

---

### 3.5 Freedom and Peace Principle

会話では「自由と平和が矛盾しない世界」が重要な言葉でした。

現在は以下の形で分散反映されています。

- 戦争が合理的選択肢にならない
- 国家依存を減らす
- 多重所属
- 自由参加
- 組織や国境を超えて協力する
- 国家機能の縮小

ただし、Principlesに「自由と平和の両立」という明示的な原則はありません。

推奨Issue:

```txt
Principlesに「自由と平和の両立」を追加するか検討する
```

書き方の注意:

避ける表現:

- 平和のために自由を制限する
- 管理社会によって争いを防ぐ
- 中央権力で戦争を止める

望ましい表現:

- 自由参加、多重所属、相互依存、透明性、生活不安の低減によって、暴力や戦争が合理的でなくなる構造を目指す
- 平和は強制的な統一ではなく、協力インセンティブの設計によって実現する
- 自由を残したまま、争いの合理性を下げる

---

### 3.6 Life Access Sustainability / Resource Allocation

「全ての人が好きなことに集中できる世界」を目指す場合、生活アクセスの持続可能性が必ず問題になります。

現在は Economy と Welfare に一部反映されていますが、まだ独立Issueとして深掘りが必要です。

推奨Issue:

```txt
生活アクセスと資源配分の持続可能性を検討する
```

論点:

- 食
- 住
- 通信
- 教育
- 健康支援
- 提供原資
- 共同購入
- 寄付
- 会費
- 相互扶助
- 内部ポイント
- フリーライド
- 希少資源
- 支援と依存の境界
- 公平性
- 地域差
- 法制度差
- 透明性とプライバシー
- 生活支援が服従条件にならない設計

---

### 3.7 Translation Status Management

日本語ファーストと単一YAML用語集は反映済みです。

ただし、各文書の翻訳ステータス管理はまだありません。

推奨Issue:

```txt
翻訳ステータス管理を導入するか検討する
```

候補ステータス:

```txt
draft
translated
reviewed
canonical
outdated
```

論点:

- 日本語正本と英語版の差分
- 翻訳遅延
- 意味のズレ
- Glossary反映状況
- Translation Issueとの接続
- 重要Decisionの翻訳優先度
- Non-goals / Safety / Threat Model の英語レビュー優先度

---

### 3.8 Research Index

会話では、以下の背景が出ていました。

- 戦国時代から近代国家への統合
- 江戸から明治への制度更新
- 村、集落、小国、大国、連邦への統合
- 国家間戦争
- ロシア・ウクライナ、台湾有事、中東などの現代リスク
- OSS
- 単一責任
- オープンソース
- 多中心ガバナンス
- 協同組合
- 生協
- 共済
- 分散ID
- 地域通貨・ポイント
- 資金決済
- 福祉制度
- 仲裁制度
- インターネット標準化
- 相互依存による戦争抑止

現在 `research/` はありますが、研究テーマ一覧や調査インデックスがまだ弱い可能性があります。

推奨Issue:

```txt
Research Indexを作成する
```

---

## 4. 次に作成すべきIssue案

アーカイブ後、まずIssueとして残すべきものは以下です。

```txt
#1 Norms Module / Rule Layerを追加するか検討する
#2 Public Safetyを国家司法・警察と敵対しない形でどう扱うか検討する
#3 Founder Non-privilege / Founder Exit PolicyをDecision化する
#4 Organization Federation Protocolを独立モジュール化するか検討する
#5 Principlesに「自由と平和の両立」を追加するか検討する
#6 生活アクセスと資源配分の持続可能性を検討する
#7 翻訳ステータス管理を導入するか検討する
#8 Research Indexを作成する
#9 Threat Modelの各リスクに具体的な判定基準を追加する
#10 Reputation Moduleで信用スコア差別を防ぐ詳細原則を追加する
#11 Audit Moduleで公開情報と保護情報の境界を整理する
#12 Economy Moduleで内部ポイントの法務レビュー観点を地域別に整理する
#13 Governance Moduleでメンテナー権限の任期・停止・移譲を設計する
#14 Non-goals変更の厳格な手続きをProposal化する
#15 初期組織運用実験の記録テンプレートを作る
```

優先度順に並べるなら、以下です。

```txt
P0: Founder Non-privilege / Founder Exit PolicyをDecision化する
P0: Organization Federation Protocolを独立モジュール化するか検討する
P0: Norms Module / Rule Layerを追加するか検討する
P1: Public Safetyを国家司法・警察と敵対しない形でどう扱うか検討する
P1: Principlesに「自由と平和の両立」を追加するか検討する
P1: 生活アクセスと資源配分の持続可能性を検討する
P2: 翻訳ステータス管理を導入するか検討する
P2: Research Indexを作成する
```

---

## 5. 次回Codexにやらせるなら最初のタスク

次のCodex作業として一番よいのは、**Issue案を実際のIssue下書きMarkdownとして作ること**です。

まだ実際にIssueを作る必要はありません。  
まず `proposals` ではなく、`meta/issue-drafts/` のような場所に下書きを作るのが安全です。

ただし、`meta/issue-drafts/` を新設するかは別途判断してください。  
リポジトリを増やしすぎたくない場合は、この引継ぎファイルをもとに人間が手動でIssue作成してもよいです。

推奨Codexタスク:

```md
# Task

この引継ぎ書をもとに、次に作成すべきIssue本文を8件分作成してください。

対象Issue:

1. Norms Module / Rule Layerを追加するか検討する
2. Public Safetyを国家司法・警察と敵対しない形でどう扱うか検討する
3. Founder Non-privilege / Founder Exit PolicyをDecision化する
4. Organization Federation Protocolを独立モジュール化するか検討する
5. Principlesに「自由と平和の両立」を追加するか検討する
6. 生活アクセスと資源配分の持続可能性を検討する
7. 翻訳ステータス管理を導入するか検討する
8. Research Indexを作成する

制約:

- すべて日本語で書く
- Issue本文はGitHubに貼れる形にする
- 支配、国家転覆、暴力、違法回避に見える表現を避ける
- Non-goals、Safety、Threat Modelと整合させる
- 各Issueに「背景」「目的」「検討論点」「安全上の注意」「関連文書」「完了条件」を入れる
- まだファイル変更はしない
```

---

## 6. 今後の作業で絶対に守るべき制約

### 6.1 表現制約

以下は禁止です。

- 国家転覆を肯定する表現
- 暴力や武装化を肯定する表現
- 税回避、労働法回避、金融規制回避、資金決済規制回避を肯定する表現
- 疑似通貨給与、違法な給与代替を推奨する表現
- カルト化、閉鎖共同体化、離脱不能性を強める表現
- 創設者や管理者を神格化する表現
- Reputationで人間の価値を固定する表現
- Auditで私生活や思想を監視する表現
- Welfareで服従や思想を条件にする表現
- Arbitrationを私刑や国家司法の完全代替にする表現
- Infrastructureを監視・検閲・離脱不能な依存構造にする表現

### 6.2 設計制約

次の観点を常に確認してください。

- 自由参加を守っているか
- 離脱可能性を弱めていないか
- フォーク可能性を残しているか
- 多重所属を妨げていないか
- 透明性とプライバシーを分けているか
- 権限集中を増やしていないか
- 専門家レビューが必要な領域を見逃していないか
- 国家や社会との不要な敵対を増やしていないか
- 便利さによる実質的強制になっていないか
- 生活支援が依存や服従につながっていないか
- 用語集と矛盾していないか
- 重要判断をDecisionへ残しているか

### 6.3 ファイル運用制約

- 日本語正本を優先する
- 英語版は重要文書から順に翻訳する
- 用語は `glossary/terms.yml` で一元管理する
- 重要用語の変更はDecision対象にする
- Non-goals、Safety、Threat Modelを弱める変更はProposal必須
- 空ファイルは禁止
- MarkdownとYAMLを中心にする
- package.json、CI、Webアプリ、ビルド設定はまだ不要
- 生成用プロンプトは設計本文ではなく `meta/prompts/` に保存する

---

## 7. 現時点の評価

現時点の反映度は 85〜90% です。

主要思想はすでにリポジトリへ移植されています。  
アーカイブしても、設計の芯は失われにくい状態です。

ただし、次フェーズで必ず扱うべき未反映領域は以下です。

1. Norms / Law / Rule Layer
2. Public Safety / Civil Peace
3. Founder Exit / Founder Non-privilege
4. Organization Federation Protocol
5. Freedom and Peace Principle
6. Life Access Sustainability
7. Translation Status
8. Research Index

この8つをIssueとして残せば、これまでの会話で出た重要な未反映部分はほぼ回収できます。

---

## 8. 最終メッセージ

World Foundation Designは、支配や国家転覆の構想ではありません。

これは、全ての人が好きなことに集中できる世界へ向けて、国家・企業・地域・個人が担ってきた機能を分解し、より自由で、透明で、離脱可能で、フォーク可能で、腐敗に強い協力基盤へ移していくための設計です。

最終的に国家が州や地域運営に近い役割へ縮小されるとしても、それは力で奪うものではありません。

よりよい協力基盤が便利で信頼され、自然に選ばれ、既存制度の必要性が段階的に減っていく結果として起こるものです。

この思想を壊さないこと。

今後のCodexは、既存文書を更新する前に、必ず次を確認してください。

```txt
README
SAFETY
CODE_OF_CONDUCT
docs/ja/04-non-goals.md
docs/ja/05-threat-model.md
docs/ja/01-principles.md
docs/ja/02-architecture.md
modules/ja/reputation/README.md
modules/ja/audit/README.md
decisions/ja/0001-japanese-first-policy.md
decisions/ja/0002-single-glossary-yaml.md
decisions/ja/0003-lightweight-governance-process.md
proposals/ja/0001-initial-governance-process.md
glossary/terms.yml
```
