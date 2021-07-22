# APIについて
他のプラグインから、PeekAntiCheatの機能を使用したりすることができます。

クラスを使います。
```
use Lyrica0954\PeekAntiCheat\api\PeekAntiCheat;
```

## プレイヤーをUnqiue-BANする
```
PeekAntiCheat::addBanPlayer($player, "BANの理由", "BANしたプレイヤーの名前(なんでもok)", $until, $autoBan);
```
$player - プレイヤーのオブジェクト

$until - BANの期限(unix time)

$autoBan - これを実行した際にキックするか (true/false)


返り値: (true/null)

true: 成功

null: プレイヤーがまだサーバーに参加していない、またはプレイヤーチェックが無効化されている

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

帰り値: PlayerCheck(Lyrica0954\PeekAntiCheat\PlayerCheck) オブジェクト

## Unique-BANされているプレイヤーのデータを全て取得
```
PeekAntiCheat::getBanData();
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

返り値: デバイスの種類

