# Codex Bootstrap Prompt

この文書は、world-foundationリポジトリの初期土台を生成するために使ったCodex向け指示書です。

これは設計本文ではなく、初期生成過程の記録として保存します。

---

# Acecore World Design - Codex一括実装指示書

このファイルだけをCodexに渡してください。  
Codexは、この指示に従って `acecore-world-design` リポジトリの初期土台を実装してください。

---

## 0. このタスクの目的

`acecore-world-design` は、通常のソフトウェアリポジトリではありません。

これは、Acecoreが目指す「全ての人が好きなことに集中できる世界」を設計するための、OSS型の社会設計リポジトリです。

社会制度・協力基盤・組織連盟・生活基盤・信用・福祉・経済・腐敗耐性などを、ソフトウェア設計と同じように、Issue、Pull Request、Proposal、Decision、Glossary、Moduleに分解して管理します。

目的は、思想をただ文章で語ることではなく、複数人がレビュー・改善・翻訳・再設計できる形にすることです。

---

## 1. Acecoreの基本思想

Acecoreは、国家、政府、社会、個人を支配するための組織ではありません。

Acecoreが目指すのは、全ての人が生存不安・強制・不透明な権力・国境による分断・戦争インセンティブから解放され、自分が本当にやりたいことに集中できる世界です。

Acecoreは、単一支配組織ではなく、自律した組織同士が共通プロトコルで協力するための基盤を目指します。

重視する価値は以下です。

- 自由参加
- 離脱可能性
- フォーク可能性
- 多重所属
- 透明性
- 腐敗耐性
- モジュール化
- 単一責任
- オープンソース
- 多言語対応
- 国家との敵対ではなく、国家の必要性を段階的に減らす設計
- 強制ではなく、利便性による普及
- 人類全体の協力効率の向上
- 戦争が合理的選択肢にならない構造の形成

Acecoreの最終的な理想は、国家を力で置き換えることではありません。  
むしろ、国家が現在担っている機能をより透明で、分散的で、参加自由な協力基盤へ段階的に移し、結果的に国家が「地域単位の運営主体」程度の役割に縮小されていくことです。

---

## 2. 表現上の注意

以下のような表現は避けてください。

- Acecoreが世界を支配する
- Acecoreが国家を征服する
- Acecoreが政府を倒す
- Acecoreが唯一の統治者になる
- Acecoreに従わせる
- Acecoreに強制参加させる
- Acecoreが人類を管理する

代わりに、以下のような表現を使ってください。

- 協力基盤
- 組織連盟
- 生活OS
- 世界共通の協力プロトコル
- 自由参加型の社会基盤
- 分散的な制度設計
- 透明な意思決定
- 腐敗耐性のある運営
- 多重所属可能な社会
- 国家の必要性を段階的に減らす
- 人類協力のためのオープンな基盤

Acecoreはカルト、帝国、政府、独裁組織、閉鎖共同体のように見えてはいけません。  
常に、自由・透明性・離脱可能性・フォーク可能性を重視してください。

---

## 3. 実装方針

以下の方針で実装してください。

- MarkdownとYAMLだけで構成する
- Webアプリ、ビルド環境、package.json、フレームワーク設定はまだ作らない
- 空ファイルは禁止
- 各Markdownには最低限意味のある初期文章を入れる
- 日本語を初期の主言語にする
- 英語版も置くが、初期は簡潔でよい
- 用語集は言語別ファイルに分けず、1つのYAMLで管理する
- IssueテンプレートとPRテンプレートを作る
- ProposalとDecisionのテンプレートを作る
- 将来拡張しやすいが、初期参加者が迷わない構造にする
- 過剰なRFC/ADR/CIはまだ入れない
- ただし将来的にRFC/ADR/CIへ拡張しやすい命名にする

---

## 4. 作成するディレクトリ構造

以下の構造を作成してください。

```txt
acecore-world-design/
├─ README.md
├─ CONTRIBUTING.md
├─ GOVERNANCE.md
├─ LICENSE
│
├─ .github/
│  ├─ ISSUE_TEMPLATE/
│  │  ├─ idea.yml
│  │  ├─ problem.yml
│  │  ├─ proposal.yml
│  │  └─ translation.yml
│  └─ PULL_REQUEST_TEMPLATE.md
│
├─ docs/
│  ├─ ja/
│  │  ├─ README.md
│  │  ├─ 00-vision.md
│  │  ├─ 01-principles.md
│  │  ├─ 02-architecture.md
│  │  └─ 03-roadmap.md
│  └─ en/
│     ├─ README.md
│     ├─ 00-vision.md
│     ├─ 01-principles.md
│     ├─ 02-architecture.md
│     └─ 03-roadmap.md
│
├─ modules/
│  ├─ ja/
│  │  ├─ identity/README.md
│  │  ├─ economy/README.md
│  │  ├─ welfare/README.md
│  │  ├─ governance/README.md
│  │  ├─ arbitration/README.md
│  │  └─ infrastructure/README.md
│  └─ en/
│     ├─ identity/README.md
│     ├─ economy/README.md
│     ├─ welfare/README.md
│     ├─ governance/README.md
│     ├─ arbitration/README.md
│     └─ infrastructure/README.md
│
├─ glossary/
│  ├─ README.md
│  └─ terms.yml
│
├─ proposals/
│  ├─ ja/
│  │  └─ README.md
│  ├─ en/
│  │  └─ README.md
│  └─ template.md
│
├─ decisions/
│  ├─ ja/
│  │  └─ README.md
│  ├─ en/
│  │  └─ README.md
│  └─ template.md
│
├─ research/
│  ├─ ja/
│  │  └─ README.md
│  └─ en/
│     └─ README.md
│
└─ assets/
   └─ diagrams/
```

---

## 5. 多言語管理方針

初期は日本語ファーストです。  
理由は、初期メンバーの議論速度を落とさないためです。

ただし、将来的に世界中の人が参加できるように、最初から英語版の置き場を用意します。

方針:

- `docs/ja/` を初期の正本にする
- `docs/en/` は英語版
- `modules/ja/` を初期の正本にする
- `modules/en/` は英語版
- `proposals/` や `decisions/` は最初から全て翻訳しなくてよい
- 重要なProposalやDecisionだけ後から翻訳する
- Issueは日本語で作成してよい
- ラベル名は将来的に英語ベースを想定する
- Glossaryは1つのYAMLファイルで全言語を管理する

---

## 6. Glossary方針

`glossary/terms.yml` は全言語共通の用語辞書です。

用語は以下の形式で管理してください。

```yaml
- id: life_os
  ja: 生活OS
  en: Life OS
  description:
    ja: 人間の生活基盤を抽象化し、統合するための協力基盤。
    en: A cooperation infrastructure that abstracts and integrates the foundations of human life.
```

初期用語として、最低でも以下を登録してください。

```yaml
- id: acecore
  ja: Acecore
  en: Acecore
  description:
    ja: 全ての人が好きなことに集中できる世界を目指すための協力基盤構想。
    en: A cooperation infrastructure concept for a world where everyone can focus on what they truly want to do.

- id: life_os
  ja: 生活OS
  en: Life OS
  description:
    ja: 人間の生活基盤を抽象化し、統合するための協力基盤。
    en: A cooperation infrastructure that abstracts and integrates the foundations of human life.

- id: world_federation
  ja: 世界連盟
  en: World Federation
  description:
    ja: 単一支配組織ではなく、自律した組織同士が共通プロトコルで協力する連盟。
    en: A federation where autonomous organizations cooperate through shared protocols, rather than a single ruling organization.

- id: cooperation_infrastructure
  ja: 協力基盤
  en: Cooperation Infrastructure
  description:
    ja: 個人や組織が国境や所属の違いを超えて協力するための共通基盤。
    en: A common foundation that enables individuals and organizations to cooperate across borders and affiliations.

- id: multi_affiliation
  ja: 多重所属
  en: Multi-affiliation
  description:
    ja: 個人が複数の組織や共同体へ同時に所属できる状態。
    en: A state where an individual can belong to multiple organizations or communities simultaneously.

- id: right_to_exit
  ja: 離脱権
  en: Right to Exit
  description:
    ja: 個人や組織が不利益や強制を受けずに共同体から離脱できる権利。
    en: The right of individuals or organizations to leave a community without coercion or unfair penalty.

- id: forkability
  ja: フォーク可能性
  en: Forkability
  description:
    ja: 既存の仕組みが腐敗・停滞した場合に、別の実装や組織へ分岐できる性質。
    en: The ability to branch into another implementation or organization when an existing system becomes corrupt or stagnant.

- id: corruption_resistance
  ja: 腐敗耐性
  en: Corruption Resistance
  description:
    ja: 権力集中、不透明性、利益固定化などによる腐敗を防ぐための設計特性。
    en: A design property that prevents corruption caused by concentration of power, opacity, or entrenched interests.

- id: modularity
  ja: モジュール性
  en: Modularity
  description:
    ja: 機能や責任を分割し、独立して改善・交換できるようにする設計思想。
    en: A design principle that separates functions and responsibilities so they can be independently improved or replaced.

- id: single_responsibility
  ja: 単一責任
  en: Single Responsibility
  description:
    ja: 1つの組織、制度、モジュールが過剰な機能や権限を持たないようにする考え方。
    en: The principle that one organization, institution, or module should not hold excessive functions or authority.

- id: transparency
  ja: 透明性
  en: Transparency
  description:
    ja: ルール、意思決定、会計、権限、変更履歴が確認可能である状態。
    en: A state where rules, decisions, accounting, authority, and change history are inspectable.

- id: open_protocol
  ja: オープンプロトコル
  en: Open Protocol
  description:
    ja: 特定組織に閉じず、複数の組織が相互接続できる公開仕様。
    en: A public specification that enables multiple organizations to interoperate without being locked into a single entity.

- id: voluntary_participation
  ja: 自由参加
  en: Voluntary Participation
  description:
    ja: 個人や組織が強制されず、自らの意思で参加できること。
    en: The ability of individuals or organizations to participate by choice, without coercion.

- id: federation
  ja: 連盟
  en: Federation
  description:
    ja: 独立性を持つ複数の組織が、共通ルールやプロトコルによって協力する構造。
    en: A structure where multiple autonomous organizations cooperate through shared rules or protocols.

- id: identity
  ja: 身分
  en: Identity
  description:
    ja: 個人や組織が誰であるか、どのような所属や権限を持つかを表す仕組み。
    en: A mechanism representing who a person or organization is, including affiliations and permissions.

- id: reputation
  ja: 信用
  en: Reputation
  description:
    ja: 行動履歴、貢献、信頼性などに基づく社会的評価。
    en: Social evaluation based on behavior history, contribution, and reliability.

- id: welfare
  ja: 福祉
  en: Welfare
  description:
    ja: 人が生存不安から解放され、自由に活動するための生活支援。
    en: Life support that frees people from survival anxiety and enables voluntary activity.

- id: arbitration
  ja: 仲裁
  en: Arbitration
  description:
    ja: 紛争や対立を暴力ではなく、透明な手続きによって解決する仕組み。
    en: A mechanism to resolve disputes through transparent procedures rather than violence.

- id: governance
  ja: ガバナンス
  en: Governance
  description:
    ja: 組織や連盟がどのように意思決定し、権限を管理し、変更されるかの仕組み。
    en: The mechanism by which an organization or federation makes decisions, manages authority, and evolves.

- id: transition
  ja: 移行
  en: Transition
  description:
    ja: 現在の国家・企業・社会制度から、新しい協力基盤へ段階的に移っていく過程。
    en: The gradual process of moving from current state, corporate, and social systems toward a new cooperation infrastructure.
```

---

## 7. 各ファイルの内容方針

### README.md

ルートREADMEには以下を書く。

- Acecore World Designとは何か
- このリポジトリの目的
- 日本語ファーストであること
- 貢献方法
- ディレクトリ概要
- 注意: Acecoreは支配組織ではなく協力基盤であること

初期本文例:

```md
# Acecore World Design

Acecore World Designは、全ての人が好きなことに集中できる世界を目指すための、オープンな社会設計リポジトリです。

このリポジトリでは、Acecoreの思想、原則、アーキテクチャ、モジュール、提案、意思決定、調査資料を管理します。

Acecoreは、国家や社会を支配するための組織ではありません。  
目的は、個人や組織が自由に参加し、協力し、離脱し、必要であればフォークできる協力基盤を設計することです。

## 初期方針

- 日本語ファースト
- 英語対応を最初から想定
- IssueとPull Requestによる設計レビュー
- 用語集による思想の一貫性維持
- モジュールごとの責任分離
- 透明性と腐敗耐性の重視

## ディレクトリ

- `docs/`: 基本文書
- `modules/`: 機能モジュール
- `glossary/`: 用語集
- `proposals/`: 提案
- `decisions/`: 意思決定ログ
- `research/`: 調査資料
```

---

### CONTRIBUTING.md

貢献ルールを書く。

初期本文例:

```md
# Contributing

Acecore World Designへの貢献を歓迎します。

このリポジトリでは、社会設計をソフトウェア設計のように扱います。  
問題提起、提案、翻訳、調査、文章改善はすべて重要な貢献です。

## 貢献方法

1. Issueを作成する
2. 議論する
3. 必要に応じて `proposals/` に提案を書く
4. Pull Requestを作成する
5. レビュー後にマージする

## 言語

初期は日本語ファーストです。  
英語翻訳も歓迎しますが、すべての文書を即時翻訳する必要はありません。

## 重要な原則

- 支配や強制を前提にしない
- 透明性を重視する
- 離脱可能性とフォーク可能性を尊重する
- 用語の一貫性を保つ
- 重要な設計判断は `decisions/` に記録する
```

---

### GOVERNANCE.md

リポジトリ運営方針を書く。

初期本文例:

```md
# Governance

このリポジトリのガバナンスは、Acecoreの思想そのものと一致している必要があります。

## 基本方針

- 透明性
- 自由参加
- 離脱可能性
- フォーク可能性
- 権限集中の回避
- 意思決定理由の記録

## 意思決定

通常の変更はPull Requestで行います。  
思想・原則・アーキテクチャに関わる重要な変更は、Proposalを作成し、レビュー後にDecisionとして記録します。

## 管理者の役割

管理者は支配者ではありません。  
管理者は議論の整理、リポジトリ品質の維持、荒らし対策、透明な意思決定の補助を行います。

## 将来の方針

貢献者が増えた場合、メンテナー制度、レビュー権限、投票制度、Decision Processを段階的に整備します。
```

---

### LICENSE

ライセンスは暫定で以下のようにしてください。  
法務的に確定ではないため、明確に暫定と書いてください。

```txt
License: TBD

This repository is currently in an early design phase.
The final license has not yet been decided.

The intended direction is to use an open license suitable for documentation, translation, and public collaboration.
Candidate licenses include Creative Commons Attribution 4.0 International (CC BY 4.0) or similar open documentation licenses.
```

---

## 8. docs/ja の初期内容

### docs/ja/README.md

```md
# Acecore設計文書

このディレクトリには、Acecoreの基本設計文書を配置します。

## 文書一覧

- `00-vision.md`: 目指す世界
- `01-principles.md`: 設計原則
- `02-architecture.md`: 全体アーキテクチャ
- `03-roadmap.md`: 段階的な移行計画
```

### docs/ja/00-vision.md

```md
# Vision

Acecoreが目指すのは、全ての人が好きなことに集中できる世界です。

そのためには、人々を生存不安、強制的な労働、国境による分断、不透明な権力、戦争インセンティブから解放する必要があります。

Acecoreは、国家や社会を支配するための仕組みではありません。  
Acecoreは、人類がより自由に、透明に、協力できるようにするための基盤です。

## 目指す状態

- 人が生きるためだけに望まない活動を強制されない
- 組織や国境を超えて協力できる
- 複数の組織へ自由に所属できる
- 参加も離脱も自由である
- ルールや意思決定が透明である
- 腐敗した仕組みはフォークできる
- 戦争が合理的な選択肢にならない
- 国家の機能は必要最小限に縮小される

## 最終的な方向性

Acecoreは、国家を力で置き換えることを目指しません。  
より便利で、透明で、参加自由な協力基盤を広げることで、国家が担っていた多くの機能を自然に不要化していくことを目指します。
```

### docs/ja/01-principles.md

```md
# Principles

Acecoreの設計では、以下の原則を重視します。

## 1. 自由参加

Acecoreへの参加は常に自由でなければなりません。  
強制、拘束、退出妨害は認めません。

## 2. 離脱可能性

個人や組織は、不当な不利益を受けずに離脱できなければなりません。

## 3. フォーク可能性

仕組みが腐敗・停滞・中央集権化した場合、別の実装へ分岐できる必要があります。

## 4. 透明性

ルール、意思決定、権限、会計、変更履歴は可能な限り確認可能であるべきです。

## 5. モジュール化

身分、信用、経済、福祉、ガバナンス、仲裁、インフラは分離して設計します。  
1つの機能が過剰な権限を持たないようにします。

## 6. 腐敗耐性

権力集中、不透明性、利益固定化、世襲化、離脱不能性を避けます。

## 7. 多重所属

個人は単一の国家や組織だけに縛られず、複数の共同体へ同時に所属できるべきです。

## 8. 国家との非敵対

Acecoreは国家と正面から敵対するためのものではありません。  
既存法制度を尊重しながら、国家の必要性を段階的に減らします。

## 9. 強制ではなく利便性

Acecoreは強制によって広がるべきではありません。  
便利で、透明で、公平であることによって自然に選ばれるべきです。
```

### docs/ja/02-architecture.md

```md
# Architecture

Acecoreは、単一の巨大組織ではなく、複数の自律組織が協力するための連盟型アーキテクチャを目指します。

## 基本構造

Acecoreは以下の層に分けて設計します。

1. Identity: 身分・所属・権限
2. Reputation: 信用・貢献・履歴
3. Economy: 交換・ポイント・生活アクセス
4. Welfare: 生存不安を減らす生活支援
5. Governance: 意思決定・権限管理
6. Arbitration: 紛争解決
7. Infrastructure: 通信・計算・生活基盤
8. Audit: 透明性・監査・ログ

## 設計思想

各機能は単一責任を持つモジュールとして扱います。  
1つの組織や制度が過剰な機能を持つと、腐敗や支配につながるためです。

## 国家機能との関係

Acecoreは、国家の全機能を一気に置き換えるものではありません。  
まずは生活、信用、協力、教育、経済、福祉など、国家以外でも提供可能な領域から始めます。

長期的には、国家が担う必要のある領域を減らし、国家を地域単位の運営主体に近づけることを目指します。
```

### docs/ja/03-roadmap.md

```md
# Roadmap

Acecoreは段階的に設計・実装します。

## Phase 0: 設計基盤

- GitHubリポジトリの整備
- VisionとPrinciplesの作成
- 用語集の整備
- ProposalとDecisionの運用開始

## Phase 1: 初期組織

- 最初の組織運営
- 参加者の募集
- 基本的なガバナンス実験
- 小さな生活支援や協力の仕組みを検証

## Phase 2: モジュール実験

- Identity
- Economy
- Welfare
- Governance
- Arbitration
- Infrastructure

各モジュールを小さく実験します。

## Phase 3: 組織連盟

複数の組織が共通ルールやプロトコルで協力できる状態を作ります。

## Phase 4: 世界共通協力基盤

国境を超えた協力、信用、生活支援、教育、経済圏を形成します。

## Phase 5: 国家機能の縮小

Acecoreが国家を支配するのではなく、人々が国家を意識しなくても協力し生活できる状態を作ります。
```

---

## 9. docs/en の初期内容

英語版は簡潔で構いません。日本語版の意図を保ってください。

### docs/en/README.md

```md
# Acecore Design Documents

This directory contains the core design documents for Acecore.

## Documents

- `00-vision.md`: Vision
- `01-principles.md`: Design principles
- `02-architecture.md`: Architecture
- `03-roadmap.md`: Roadmap
```

### docs/en/00-vision.md

```md
# Vision

Acecore aims to create a world where everyone can focus on what they truly want to do.

Acecore is not a government, empire, or ruling authority.  
It is a cooperation infrastructure for enabling people and organizations to collaborate freely, transparently, and across borders.

## Target State

- People are not forced into unwanted activity merely to survive.
- Individuals can cooperate beyond borders and organizations.
- Participation and exit are voluntary.
- Rules and decisions are transparent.
- Corrupted systems can be forked.
- War becomes structurally irrational.
- The role of states gradually becomes smaller and more local.
```

### docs/en/01-principles.md

```md
# Principles

Acecore is designed around the following principles.

## Voluntary Participation

Participation must be voluntary.

## Right to Exit

Individuals and organizations must be able to leave without coercion or unfair penalty.

## Forkability

If a system becomes corrupt or stagnant, it must be possible to fork it.

## Transparency

Rules, decisions, authority, accounting, and change history should be inspectable.

## Modularity

Identity, economy, welfare, governance, arbitration, and infrastructure should be designed as separate modules.

## Corruption Resistance

The design must avoid concentration of power, opacity, entrenched interests, and exit barriers.

## Multi-affiliation

Individuals should be able to belong to multiple communities and organizations.

## Non-hostility toward States

Acecore does not seek direct conflict with states.  
It aims to reduce the necessity of state functions over time.
```

### docs/en/02-architecture.md

```md
# Architecture

Acecore is designed as a federated architecture, not as a single centralized organization.

## Core Modules

- Identity
- Reputation
- Economy
- Welfare
- Governance
- Arbitration
- Infrastructure
- Audit

Each module should have a clear responsibility and should not accumulate excessive authority.

Acecore begins with areas that can be built outside the state, such as cooperation, education, welfare, trust, and infrastructure.
```

### docs/en/03-roadmap.md

```md
# Roadmap

## Phase 0: Design Foundation

Prepare the repository, glossary, principles, and proposal process.

## Phase 1: Initial Organization

Start with a small organization and governance experiments.

## Phase 2: Module Experiments

Experiment with identity, economy, welfare, governance, arbitration, and infrastructure.

## Phase 3: Federation

Allow multiple organizations to cooperate through shared protocols.

## Phase 4: Global Cooperation Infrastructure

Create cross-border cooperation, trust, welfare, education, and economic layers.

## Phase 5: Reduced State Dependency

Create a world where people can cooperate and live without constantly depending on state boundaries.
```

---

## 10. modules のテンプレート方針

各モジュールREADMEには以下の構造を使ってください。

```md
# Module Name

## 目的

## このモジュールが解決する問題

## 責任範囲

## 責任範囲外

## 他モジュールとの関係

## 初期設計メモ

## 未解決の問い
```

---

## 11. modules/ja の初期内容

### modules/ja/identity/README.md

```md
# Identity Module

## 目的

Identity Moduleは、個人や組織の身分、所属、権限を扱います。

## 解決する問題

現在の身分は国家や企業に強く依存しています。  
Acecoreでは、国境や単一組織に縛られず、多重所属可能な身分基盤を目指します。

## 責任範囲

- 個人ID
- 組織ID
- 所属
- 権限
- 認証
- 多重所属

## 責任範囲外

- 信用評価
- 経済取引
- 紛争解決

## 未解決の問い

- 国家IDとどう連携するか
- 匿名性と信頼性をどう両立するか
- 複数IDや偽装をどう扱うか
```

### modules/ja/economy/README.md

```md
# Economy Module

## 目的

Economy Moduleは、Acecore内部の価値交換、ポイント、生活アクセス、経済圏を扱います。

## 解決する問題

現在の経済は国家通貨に強く依存し、人々が常に法定通貨を意識せざるを得ない構造になっています。  
Acecoreでは、法制度を尊重しつつ、生活上の通貨意識を減らす経済設計を目指します。

## 責任範囲

- 内部ポイント
- 生活アクセス
- 共同購入
- 経済圏
- 価値交換
- 税務・法務との接続方針

## 責任範囲外

- 違法な通貨発行
- 税回避
- 強制的な給与代替

## 未解決の問い

- 法定通貨と内部ポイントの境界
- 税務・労務との整合性
- 換金性をどう制御するか
```

### modules/ja/welfare/README.md

```md
# Welfare Module

## 目的

Welfare Moduleは、生存不安を減らし、人が好きなことに集中できる状態を支えるための生活支援を扱います。

## 解決する問題

多くの人は、生きるために望まない仕事や環境を受け入れざるを得ません。  
Acecoreでは、生活基盤を共同で支え、自由な活動を可能にすることを目指します。

## 責任範囲

- 食
- 住
- 通信
- 教育
- 医療・健康支援
- 生活アクセス
- 相互扶助

## 責任範囲外

- 強制的な共同生活
- 離脱不能な福祉制度
- 特定思想への依存

## 未解決の問い

- 生活支援と依存の境界
- 公平性の設計
- 悪用防止
```

### modules/ja/governance/README.md

```md
# Governance Module

## 目的

Governance Moduleは、Acecoreおよび組織連盟の意思決定、権限管理、変更手続きを扱います。

## 解決する問題

組織は成長すると、権力集中、不透明性、腐敗、形骸化を起こしやすくなります。  
Acecoreでは、透明で、離脱可能で、フォーク可能なガバナンスを設計します。

## 責任範囲

- 意思決定
- 権限管理
- 役割
- 投票
- Proposal
- Decision
- フォーク手続き

## 責任範囲外

- 個人の思想統制
- 強制参加
- 永続的な特権階級

## 未解決の問い

- 意思決定速度と透明性の両立
- 専門性と民主性の両立
- 腐敗した運営をどう検出するか
```

### modules/ja/arbitration/README.md

```md
# Arbitration Module

## 目的

Arbitration Moduleは、紛争や対立を暴力ではなく透明な手続きによって解決する仕組みを扱います。

## 解決する問題

国家間や組織間の対立は、最終的に軍事力や強制力に依存しがちです。  
Acecoreでは、合意可能な手続き、記録、第三者仲裁、透明性によって紛争コストを下げることを目指します。

## 責任範囲

- 紛争受付
- 仲裁手続き
- 証拠管理
- 透明な判断
- 再審・異議申し立て
- 組織間紛争

## 責任範囲外

- 暴力による執行
- 国家司法の完全代替
- 密室裁判

## 未解決の問い

- 仲裁結果の実効性
- 国家司法との関係
- AI仲裁の透明性
```

### modules/ja/infrastructure/README.md

```md
# Infrastructure Module

## 目的

Infrastructure Moduleは、Acecoreの協力基盤を支える通信、計算資源、データ、生活インフラを扱います。

## 解決する問題

現代社会では、通信、クラウド、AI、住居、エネルギーなどのインフラが特定企業や国家に強く依存しています。  
Acecoreでは、分散的で相互接続可能なインフラを目指します。

## 責任範囲

- 通信
- 計算資源
- AI基盤
- データ管理
- 生活インフラ
- 可用性
- 相互運用性

## 責任範囲外

- 単一組織による全インフラ独占
- 監視インフラ
- 離脱不能な依存構造

## 未解決の問い

- 分散性と効率性の両立
- プライバシー保護
- 災害や攻撃への耐性
```

---

## 12. modules/en の初期内容

英語版は各モジュールについて簡潔に書いてください。

例:

```md
# Identity Module

## Purpose

The Identity Module handles identity, affiliation, and permissions for individuals and organizations.

## Scope

- Individual identity
- Organizational identity
- Affiliation
- Permissions
- Authentication
- Multi-affiliation

## Open Questions

- How should Acecore interoperate with state-issued identity?
- How can anonymity and trust be balanced?
```

他のモジュールも同程度の簡潔さで作成してください。

---

## 13. proposals

### proposals/ja/README.md

```md
# Proposals

このディレクトリには、Acecoreの設計変更や新しい仕組みに関する提案を置きます。

提案は、いきなり本体文書を変更するのではなく、まずProposalとして議論するために使います。

## 流れ

1. Issueで問題やアイデアを出す
2. Proposalを書く
3. Pull Requestでレビューする
4. 採用された内容をdocsまたはmodulesに反映する
5. 重要な判断はdecisionsに記録する
```

### proposals/en/README.md

```md
# Proposals

This directory contains design proposals for Acecore.

Proposals are used before changing core documents or modules.
```

### proposals/template.md

```md
# Proposal: <title>

## Summary

## Problem

## Motivation

## Proposed Change

## Affected Documents or Modules

## Benefits

## Risks

## Abuse Cases

## Alternatives

## Open Questions

## Related Issues
```

---

## 14. decisions

### decisions/ja/README.md

```md
# Decisions

このディレクトリには、重要な意思決定の記録を置きます。

Decisionは、何を決めたかだけでなく、なぜその判断をしたのかを残すために使います。

## 書くべきもの

- 重要な設計方針
- 採用したアーキテクチャ
- 却下した案と理由
- ガバナンス上の判断
- 用語や思想の定義
```

### decisions/en/README.md

```md
# Decisions

This directory records important design decisions and their rationale.
```

### decisions/template.md

```md
# Decision: <title>

## Status

Proposed / Accepted / Rejected / Superseded

## Context

## Decision

## Rationale

## Consequences

## Alternatives Considered

## Related Proposals or Issues
```

---

## 15. research

### research/ja/README.md

```md
# Research

このディレクトリには、Acecoreの設計に関係する調査資料を置きます。

対象例:

- 歴史
- 国家制度
- 経済制度
- 協同組合
- OSSガバナンス
- 分散ID
- 福祉
- 紛争解決
- 国際関係
- 法制度
```

### research/en/README.md

```md
# Research

This directory contains research notes related to Acecore's design.
```

---

## 16. GitHub Issue Templates

`.github/ISSUE_TEMPLATE/idea.yml`

```yaml
name: Idea
description: 新しいアイデアを提案する
title: "[Idea]: "
labels: ["type:idea"]
body:
  - type: textarea
    id: summary
    attributes:
      label: 概要
      description: アイデアの概要を書いてください。
    validations:
      required: true
  - type: textarea
    id: motivation
    attributes:
      label: なぜ必要か
      description: このアイデアが必要な理由を書いてください。
    validations:
      required: true
  - type: textarea
    id: related
    attributes:
      label: 関連する文書・モジュール
      description: 関連するdocs、modules、glossaryがあれば書いてください。
```

`.github/ISSUE_TEMPLATE/problem.yml`

```yaml
name: Problem
description: 問題・矛盾・リスクを報告する
title: "[Problem]: "
labels: ["type:problem"]
body:
  - type: textarea
    id: problem
    attributes:
      label: 問題
      description: 何が問題なのかを書いてください。
    validations:
      required: true
  - type: textarea
    id: impact
    attributes:
      label: 影響
      description: この問題が放置された場合の影響を書いてください。
    validations:
      required: true
  - type: textarea
    id: possible_solution
    attributes:
      label: 解決案
      description: 解決案があれば書いてください。
```

`.github/ISSUE_TEMPLATE/proposal.yml`

```yaml
name: Proposal
description: 設計変更の提案を作成する
title: "[Proposal]: "
labels: ["type:proposal"]
body:
  - type: textarea
    id: summary
    attributes:
      label: 提案概要
      description: 提案内容を簡潔に書いてください。
    validations:
      required: true
  - type: textarea
    id: target
    attributes:
      label: 対象
      description: 影響を受ける文書やモジュールを書いてください。
    validations:
      required: true
  - type: textarea
    id: risks
    attributes:
      label: リスク
      description: この提案のリスクや悪用可能性を書いてください。
  - type: textarea
    id: alternatives
    attributes:
      label: 代替案
      description: 検討した代替案があれば書いてください。
```

`.github/ISSUE_TEMPLATE/translation.yml`

```yaml
name: Translation
description: 翻訳・用語・多言語対応に関するIssue
title: "[Translation]: "
labels: ["type:translation"]
body:
  - type: input
    id: source
    attributes:
      label: 対象ファイル
      description: 翻訳対象または修正対象のファイルパスを書いてください。
    validations:
      required: true
  - type: input
    id: language
    attributes:
      label: 言語
      description: 対象言語を書いてください。例 ja, en
    validations:
      required: true
  - type: textarea
    id: details
    attributes:
      label: 内容
      description: 翻訳内容、表現の問題、用語の揺れなどを書いてください。
    validations:
      required: true
```

---

## 17. Pull Request Template

`.github/PULL_REQUEST_TEMPLATE.md`

```md
# Pull Request

## 概要

## 変更内容

- 

## 変更対象

- [ ] docs
- [ ] modules
- [ ] glossary
- [ ] proposals
- [ ] decisions
- [ ] research
- [ ] GitHub settings/templates

## 関連Issue

Closes #

## チェックリスト

- [ ] Acecoreを支配組織として表現していない
- [ ] 自由参加・離脱可能性・透明性に反していない
- [ ] 用語集と矛盾していない
- [ ] 必要に応じて日本語・英語の対応を考慮した
- [ ] 重要な意思決定がある場合、decisionsへの記録を検討した
- [ ] 悪用リスクや腐敗リスクを考慮した

## 補足
```

---

## 18. 初期Issue案

実装完了後、Codexは以下のIssue案を報告してください。  
実際にIssueを作成する必要はありません。

```txt
#1 docs/ja/00-vision.mdをより詳細化する
#2 glossary/terms.ymlに初期用語を50個まで追加する
#3 modules/ja/economy/README.mdで法定通貨と内部ポイントの関係を整理する
#4 modules/ja/governance/README.mdで腐敗耐性の設計原則を追加する
#5 proposals/ja/0001-initial-governance-process.mdを作成する
#6 decisions/ja/0001-use-japanese-first-policy.mdを作成する
#7 docs/en配下の翻訳品質をレビューする
```

---

## 19. 完了時の報告形式

実装完了後、Codexは以下の形式で報告してください。

```md
## 作成したファイル

- ...

## 設計上の判断

- ...

## 注意点

- ...

## 次に作成すべきIssue案

- ...
```

---

## 20. 最終確認

この実装では、まだ以下は行わないでください。

- Webサイト化
- npm / pnpm / yarn の導入
- CI設定
- 自動翻訳システム
- 認証システム
- 実際のポイント・通貨実装
- 法務文書としての確定
- 政治的宣言文としての過激表現

今回は、あくまでGitHubで共同設計を始めるための、シンプルで拡張可能な土台を作成することが目的です。
