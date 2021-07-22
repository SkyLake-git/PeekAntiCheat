# コマンドについて
ゲーム内から直接PeekAntiCheatの設定をいじくれる素晴らしいものです。
***

## 構文について
§c<> §f内のものは必須引数、 §c{} §f内のものはオプション引数です。 

## フォーマットについて

§2date: §fdateフォーマットが指定されている場合は、§l数-種類§r§f の形で引数を渡します。  
§f例: §7/unique-ban Lyrica0954 generic_reason 1-y 10-mo 31-d 60-m 30-s §f(1年10ヵ月31日60分30秒) 

### /pac check
構文: `/pac check @{player}`  
説明: §7アンチチートがプレイヤーをチェックするかを切り替えます

### /pac notify
構文: `/pac notify @{player}`  
説明: チート検出の通知を切り替えます

### /pac debug
構文: `/pac debug @{player}`  
説明: チート検出のデバッグメッセージ表示を切り替えます

### /pac kick
構文: `/pac kick @{player}`  
説明: アンチチートがプレイヤーをキックするかを切り替えます

### /pac setback
構文: `/pac setback @{player}`  
説明: プレイヤーアンチチートに引っ掛かった際にロールバックするかを切り替えます

### /pac disable
構文: `/pac disable <check> <seconds> @{player}`  
説明: プレイヤーのチェックを特定のものだけ指定した秒数無効にします

### /ackick
構文: `/ackick <player>`  
説明: プレイヤーをアンチチートとしてキックします

### /crash
構文: `/crash <player>`  
説明: プレイヤーにクラッシュさせることを試みます

### /unique-ban
構文: `/unique-ban <player> <reason> {until:date}`  
説明: プレイヤーをユニークBANします、IP-BANと組み合わせると強力です

### /unique-unban
構文: `/unique-unban <player>`  
説明: プレイヤーのユニークBANを解除します

### /unique-banlist
構文: `/unique-banlist`  
説明: プレイヤーのユニークBANを解除します

### /pif
構文: `/pif <player>`  
説明: プレイヤーの情報を取得します
