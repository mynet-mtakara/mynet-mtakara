```
@startuml
ブラウザA -> TeamduelController  : バトルを挑む 
TeamduelController -> memcache : lock
@enduml
```
