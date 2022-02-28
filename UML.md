## 通常
```
@startuml
ブラウザ -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
TeamduelController -> TeamduelController : 戦闘処理
TeamduelController -> memcache : unlock
TeamduelController -> ブラウザ : 結果表示
@enduml
```

## 不具合
```
@startuml
ブラウザA -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
TeamduelController -> TeamduelController : 戦闘処理
TeamduelController -> memcache : unlock
TeamduelController -> ブラウザA : 結果表示
@enduml
```
