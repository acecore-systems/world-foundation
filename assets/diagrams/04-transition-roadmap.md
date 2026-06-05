# Transition Roadmap

この図は、[Roadmap](../../docs/ja/03-roadmap.md) のフェーズを、既存制度から協力基盤へ段階的に移行する流れとして示します。普及は [Principles](../../docs/ja/01-principles.md) の「強制ではなく利便性」に従い、前提検証は [research/ja](../../research/ja/README.md) に戻します。

```mermaid
flowchart LR
  Current["現在の社会<br/>国家・企業・地域・家族・雇用への強い依存"]
  P0["Phase 0<br/>設計基盤<br/>Safety / Non-goals / Threat Model"]
  P1["Phase 1<br/>初期組織と運用実験"]
  P2["Phase 2<br/>モジュール実験<br/>Reputation / Audit / Norms / Public Safety / Federationを含む"]
  P3["Phase 3<br/>組織連盟"]
  P4["Phase 4<br/>世界共通協力基盤"]
  P5["Phase 5<br/>国家依存の縮小"]
  Future["好きなことに集中しやすい世界"]

  Current --> P0 --> P1 --> P2 --> P3 --> P4 --> P5 --> Future

  P0 -. "用語・原則・Safety・Decision" .-> P1
  P1 -. "小さな失敗の記録" .-> P2
  P2 -. "相互運用性・信用・監査・ルール・安全境界" .-> P3
  P3 -. "国境を超えた協力" .-> P4
  P4 -. "便利さによる自然な採用" .-> P5

  click P0 "../../docs/ja/03-roadmap.md" "Roadmap"
  click P2 "../../modules/ja/README.md" "Modules"
  click P3 "../../modules/ja/federation/README.md" "Federation"
  click P5 "../../assets/diagrams/08-non-coercive-adoption.md" "Non-coercive adoption"
  click Future "../../docs/ja/00-vision.md" "Vision"
```
