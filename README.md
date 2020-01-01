# l4d2coop

## 概要

Left 4 dead 2で8人coop用のプラグイン、設定ファイルをまとめて入れる（ついでに難易度ぶち上げ）

・[Metamod](http://www.metamodsource.net/)

・[Sourcemod](http://www.sourcemod.net/)

・[L4DToolZ](https://forums.alliedmods.net/showthread.php?t=93600)

・[LEFT12DEAD](https://forums.alliedmods.net/showthread.php?t=126857) 



## インストール方法

### サーバの設定

#### ①[steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD)をダウンロード

#### ②適当な場所でSteamCMD.exeを起動しL4D2サーバをインストール

```
login anonymous
force_install_dir l4d2server
app_update 222860
```

#### ③サーバをインストールしたフォルダにleft4dead2フォルダとstart.batを入れる

gitるなら↓から

```
git init
git remote add origin https://github.com/neohral/l4d2coop.git
git fetch origin
git reset --hard origin/master
```

#### ④サーバ系の設定をする。

・left4dead2\cfg\server.cfg

| 設定項目                     | 設定値                                   | 設定値     |
| ---------------------------- | ---------------------------------------- | ---------- |
| hostname                     | サーバの名前                             | l4d2server |
| sv_allow_lobby_connect_only  | 0にするとコンソールから接続できる        | 0          |
| rcon_password                | サーバ管理者のパスワード                 | "password" |
| sv_lan                       | ネットワーク設定(0:インターネット 1:LAN) | 0          |
| sv_region                    | 地域設定(4:アジア)                       | 4          |
| sv_alltalk                   | ボイチャの設定(0:味方のみ1:全体に)       | 0          |
| sm_cvar sv_force_unreserved  | 直接ゲームに参加する                     | 1          |
| sm_cvar sv_visiblemaxplayers | サーバ画面で見せる参加人数（見た目だけ） | **8**      |
| sm_cvar sv_removehumanlimit  | 参加上限のキックを無効にする             | 1          |
| sm_cvar sv_maxplayers        | 接続可能な最大人数                       | **8**      |
| sm_cvar l4d_maxplayers       | 接続可能な最大人数(いらないかも)         | **8**      |
| sm_cvar l4d_survivor_limit   | BOTを含めた生存者の人数                  | **8**      |
| sm_cvar l4d_infected_limit   | 特殊感染者の最大同時発生数               | 20         |
| sm_cvar l4d_players_delay    | なにこれ(とりあえず必要そう)             | 12         |
| sm_cvar l4d_players_kick     | なにこれ(とりあえず必要そう)             | 0.7        |
| sm_cvar l4d_players_timer    | なにこれ(とりあえず必要そう)             | 1.5        |

人数増やすなら、太字部分を変える

その他特殊感染者の設定あたりはきついので普通にやるなら、要調整

#### ⑤start.batを起動する。

起動オプションを設定し、srcds.exeを起動するやつ。

・start.bat

| 起動オプション               | 概要                               | 設定値            |
| ---------------------------- | ---------------------------------- | ----------------- |
| -autoupdate                  | 起動時にアップデートチェックをする |                   |
| -console                     | CUIコンソールで起動する            |                   |
| +hostport                    | IPポート番号を指定する             | 27016             |
| +map "マップ名 ゲームモード" | マップとゲームモードを指定         | "c1m1_hotel coop" |
| +maxplayers                  |                                    | **8**             |

人数増やすなら、太字部分を変える。

#### ⑥コンソールから接続

connect `ローカルのIPアドレス`:`ポート`

※ローカルのIPアドレスはループバックアドレス(127.0.0.1)じゃなかった

確認方法はサーバをGUIで起動してIPアドレスのとこに出るやつ

### クライアントの設定

#### ①コンソールから接続

connect `グローバルのIPアドレス`:`ポート`

------------------



## メモ

ログは`left4dead2\addons\sourcemod\logs`あたりに出てそう



## 参考

http://gengen5656.blog46.fc2.com/blog-entry-34.html

2011年の記事なので、インストールするものとかは最新のやつを取ってきたほうがいい(1敗)