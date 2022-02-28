```
@startuml
ブラウザ -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
TeamduelController -> memcache : unlock
TeamduelController -> ブラウザ : 結果表示
@enduml
```
