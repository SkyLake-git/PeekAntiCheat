# 基本的なAPIのドキュメント

todo:
- [x] Basic API
- [ ] Advanced API

***
クラスを使います。
```
use Lyrica0954\PeekAntiCheat\api\PeekAntiCheat;
```

## プレイヤーをUnique-BANする
```
PeekAntiCheat::addBanPlayer($player, "BANの理由", "BANしたプレイヤーの名前(なんでもok)", $until, $autoBan);
```
$player - プレイヤーのオブジェクト  
$until - BANの期限(unix time)  
$autoBan - これを実行した際にキックするか (true/false)  

返り値: ($banid/null)  
$banid: Unique-BANのid    
null: プレイヤーがまだサーバーに参加していない、またはプレイヤーチェックが無効化されている  

## プレイヤーのUnique-BANデータを検索して取得する
```
PeekAntiCheat::searchBanData($info);
```

$info - Unique-BANのIDまたはプレイヤー名  

返り値: (Array/null)  
Array: BANデータのArray  
null: 見つからなかった  

## プレイヤーのUnqiue-BANデータを編集する
```
PeekAntiCheat::changeBanData($bps, "BANの理由", "BANしたプレイヤーの名前(なんでもok)", $until)
```

$bps - Unique-BANのIDまたはプレイヤー名  
$until - BANの期限(unix time)  

返り値: (true/null)  
true: 成功  
null: 見つからなかった

## プレイヤーのUnique-BANを解除する
```
PeekAntiCheat::removeBanPlayer("プレイヤーの名前またはBANのid");
```

返り値: (true/false)  
true: 成功  
false: 失敗  

## プレイヤーのチェックオブジェクトを取得する
```
PeekAntiCheat::getPlayerCheck($player);
```
$player - プレイヤーのオブジェクト  

返り値: (PlayerCheck/null)  
PlayerCheck - PlayerCheck(Lyrica0954\PeekAntiCheat\PlayerCheck) オブジェクト  
null - プレイヤーがまだサーバーに参加していない、またはプレイヤーチェックが無効化されている

## Unique-BANされているプレイヤーのデータを取得
```
PeekAntiCheat::getBanData($bps);
```

$bps - Unqiue-BANのIDまたはプレイヤー名  

返り値: ($banData/null)  
$banData - Unique-BANのデータ  
null - 見つからなかった  

## Unique-BANされているプレイヤーのデータを全て取得
```
PeekAntiCheat::getBans();
```

返り値: Array

## プレイヤーを安全にキックする
```
PeekAntiCheat::addKickPlayer($player, "キックの理由");
```

$player - プレイヤーのオブジェクト  

返り値: なし

## プレイヤーのチェックオブジェクトを全て取得する
```
PeekAntiCheat::getPlayerChecks();
```

返り値: Array

## プレイヤーのチェックを一部無効にする
```
PeekAntiCheat::disablePlayerTest($player, "チェックの名前", $seconds);
```

$player - プレイヤーのオブジェクト  
$seconds - 無効にする秒数  

返り値: なし

## プレイヤーがアンチチートによってキックされるかを変更する
```
PeekAntiCheat::setPlayerKick($player, $kick);
```

$player - プレイヤーのオブジェクト  
$kick - (true/false)  

返り値: なし

## プレイヤーがアンチチート検知されるかを変更する
```
PeekAntiCheat::setPlayerTest($player, $test);
```

$player - プレイヤーのオブジェクト  
$test - (true/false)  

返り値: なし

## プレイヤーがアンチチート検知された際にロールバックするかを変更する
```
PeekAntiCheat::setPlayerSetback($player, $setback);
```

$player - プレイヤーのオブジェクト  
$setback - (true/false)  

返り値: なし

## プレイヤーのデバイスを取得する
```
PeekAntiCheat::getPlayerDevice($player);
```

$player - プレイヤーのオブジェクト  

返り値: デバイスの種類

## プレイヤーのクライアントデータを取得する
```
PeekAntiCheat::getPlayerClientData($player);
```

$player - プレイヤーのオブジェクト  

返り値: クライアントデータ

## プレイヤーにWatchdogをスポーンさせる
```
PeekAntiCheat::spawnWatchdogTo($player, $silent);
```

$player - プレイヤーのオブジェクト  
$silent - 通知を表示しないか (true/false)  

返り値: なし

## プレイヤーをクラッシュさせる
```
PeekAntiCheat::crashPlayer($player);
```

$player - プレイヤーのオブジェクト  

返り値: なし
