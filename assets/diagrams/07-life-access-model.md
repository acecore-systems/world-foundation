# Life Access Model

この図は、[Life Access Sustainability](../../docs/ja/06-life-access-sustainability.md) の論点を、[Welfare](../../modules/ja/welfare/README.md)、[Economy](../../modules/ja/economy/README.md)、共有資源に分けて考える初期モデルです。支援が服従や囲い込みにならない境界は [Threat Model](../../docs/ja/05-threat-model.md) で扱います。

```mermaid
flowchart TB
  Needs["生活上の必要<br/>食・住・通信・教育・健康"]
  Welfare["Welfare<br/>相互扶助・生活支援"]
  Economy["Economy<br/>共同購入・利用枠・内部記録"]
  Commons["Commons<br/>共有資源・知識"]
  Providers["提供者<br/>個人・組織・地域"]
  Access["生活アクセス"]
  Safeguards["安全装置<br/>離脱可能性・異議申し立て・透明性"]
  Review["レビューと改善"]

  Needs --> Welfare
  Needs --> Economy
  Needs --> Commons
  Providers --> Welfare
  Providers --> Economy
  Providers --> Commons
  Welfare --> Access
  Economy --> Access
  Commons --> Access
  Access --> Safeguards
  Safeguards --> Review
  Review --> Welfare
  Review --> Economy
  Review --> Commons

  click Welfare "../../modules/ja/welfare/README.md" "Welfare"
  click Economy "../../modules/ja/economy/README.md" "Economy"
  click Access "../../docs/ja/06-life-access-sustainability.md" "Life Access Sustainability"
  click Safeguards "../../docs/ja/05-threat-model.md" "Threat Model"
```
