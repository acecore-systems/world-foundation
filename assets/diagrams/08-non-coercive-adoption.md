# Non-coercive Adoption

この図は、[Principles](../../docs/ja/01-principles.md) の「強制ではなく利便性」を、[Roadmap](../../docs/ja/03-roadmap.md) 上の普及モデルとして表したものです。便利さが実質的強制へ変わるリスクは [Threat Model](../../docs/ja/05-threat-model.md) で確認します。

```mermaid
flowchart LR
  Useful["便利である"]
  Transparent["透明である"]
  Fair["公平に見える"]
  Voluntary["自由参加"]
  Trust["信頼"]
  Adoption["自然な採用"]
  Exit["離脱可能性"]
  Feedback["フィードバック"]
  Improvement["改善"]

  Useful --> Voluntary
  Transparent --> Trust
  Fair --> Trust
  Voluntary --> Adoption
  Trust --> Adoption
  Adoption --> Feedback
  Exit --> Trust
  Feedback --> Improvement
  Improvement --> Useful
  Improvement --> Transparent
  Improvement --> Fair

  click Voluntary "../../docs/ja/01-principles.md" "Principles"
  click Exit "../../docs/ja/01-principles.md" "Exit capability"
  click Adoption "../../docs/ja/03-roadmap.md" "Roadmap"
  click Feedback "../../docs/ja/05-threat-model.md" "Threat Model"
```
