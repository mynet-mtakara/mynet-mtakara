aaa

```
#0 share/drpr/application/modules/main/models/App/Controller/Abstract.php(1338):
#1 share/drpr/application/modules/main/models/App/Controller/Abstract.php(1229):
#2 share/drpr/application/modules/main/controllers/DuelController.php(688):
#3 framework/framework/php/Synphonie/Framework/Controller/Action.php(258):
#4 framework/framework/php/Synphonie/Framework/Controller/Front.php(313):
#5 share/drpr/public/index.php(103): 
```

PVP
DuelController::processAction()

```
$duel = new App_Duel_PvP( $owner );
App_Duel::handleProcessSkill( $owner, $duel, $data );
$duel->execute( $attack_deck, $defense_deck, $target, $treasure, $use_fight );		
```

<script src="/easeljs-0.6.0.min.js"></script>
<script src="/tweenjs-0.4.0.min.js"></script>
<script src="/movieclip-0.6.0.min.js"></script>
<script src="/preloadjs-0.3.0.min.js"></script>
<script src="/asset/js?f=lib/app/gimmick/duel/6/pvp_battle.js&amp;_v=38&amp;nocache=1"></script>


## 通常のスキル実行
```
#0 share/drpr/application/modules/main/models/App/Duel/DataSet/Ub.php(2740):
#1 share/drpr/application/modules/main/models/App/Duel/DataSet/Ub.php(2199): 
#2 share/drpr/application/modules/main/models/App/Duel/DataSet.php(1345):
#3 share/drpr/application/modules/main/models/App/Duel.php(1240): 
#4 share/drpr/application/modules/main/models/App/Duel.php(998):
#5 share/drpr/application/modules/main/controllers/DuelController.php(531): 
#6 framework/framework/php/Synphonie/Framework/Controller/Action.php(258):
#7 framework/framework/php/Synphonie/Framework/Controller/Front.php(313): 
#8 share/drpr/public/index.php(103):
```
