# 生活アクセスモデル

この図は、[生活アクセスの持続可能性](../../docs/ja/06-life-access-sustainability.md) の論点を、[福祉](../../modules/ja/welfare/README.md)、[経済](../../modules/ja/economy/README.md)、共有資源に分けて考える初期モデルです。支援が服従や囲い込みにならない境界は [脅威モデル](../../docs/ja/05-threat-model.md) で扱います。

```mermaid
flowchart TB
  Needs["生活上の必要<br/>食・住・通信・教育・健康"]
  福祉["福祉<br/>相互扶助・生活支援"]
  経済["経済<br/>共同購入・利用枠・内部記録"]
  Commons["共有資源<br/>共有資源・知識"]
  Providers["提供者<br/>個人・組織・地域"]
  Access["生活アクセス"]
  Safeguards["安全装置<br/>離脱可能性・異議申し立て・透明性"]
  Review["レビューと改善"]

  Needs --> 福祉
  Needs --> 経済
  Needs --> Commons
  Providers --> 福祉
  Providers --> 経済
  Providers --> Commons
  福祉 --> Access
  経済 --> Access
  Commons --> Access
  Access --> Safeguards
  Safeguards --> Review
  Review --> 福祉
  Review --> 経済
  Review --> Commons

  click 福祉 "../../modules/ja/welfare/README.md" "福祉"
  click 経済 "../../modules/ja/economy/README.md" "経済"
  click Access "../../docs/ja/06-life-access-sustainability.md" "生活アクセスの持続可能性"
  click Safeguards "../../docs/ja/05-threat-model.md" "脅威モデル"
```
