```
@startuml
ブラウザA -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
TeamduelController -> memcache : unlock
@enduml
```
