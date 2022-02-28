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
ブラウザA -> TeamduelController A  : バトルを挑む 
ブラウザB -> TeamduelController B  : バトルを挑む 
TeamduelController A -> memcache : user情報取得
TeamduelController A -> TeamduelController : 戦闘処理
TeamduelController A -> memcache : user情報保存
TeamduelController A -> mysql : user情報保存
TeamduelController A -> ブラウザA : 結果表示
@enduml
```
