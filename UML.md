```
@startuml
ブラウザ -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
TeamduelController TeamduelController : 戦闘処理
TeamduelController -> memcache : unlock
TeamduelController -> ブラウザ : 結果表示
@enduml
```
