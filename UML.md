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
ブラウザA -> TeamduelControllerA  : バトルを挑む 
ブラウザB -> TeamduelControllerB  : バトルを挑む 
TeamduelControllerA -> memcache : user情報取得
TeamduelControllerB -> memcache : user情報取得
TeamduelControllerA -> TeamduelControllerA : 戦闘処理
TeamduelControllerA -> memcache : user情報保存
TeamduelControllerA -> mysql : user情報保存
TeamduelControllerA -> ブラウザA : 結果表示
TeamduelControllerB -> TeamduelControllerB : 戦闘処理
TeamduelControllerB -> memcache : user情報保存
TeamduelControllerB -> mysql : user情報保存
TeamduelControllerB -> ブラウザB : 結果表示
@enduml
```
