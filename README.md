# l4d2coop

### 概要

Left 4 dead 2で8人coop用のプラグイン、設定ファイルをまとめて入れるだけ（ついでに難易度ぶち上げ）

-----------------

### インストール方法

#### サーバーの設定

##### ①[steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD)をダウンロード

##### ②適当な場所でSteamCMD.exeを起動しL4D2サーバーをインストール

```
login anonymous
force_install_dir l4d2server
app_update 222860
```

##### ③サーバーをインストールしたフォルダ`force_install_dir `にて指定したフォルダに移動してgitる

```
git init
git remote add origin https://github.com/neohral/l4d2coop.git
git fetch origin
git reset --hard origin/master
```

##### ④サーバー系の設定をする。

・left4dead2\cfg\server.cfg

→プレイヤー数とか、RCONのパスとか

→特殊感染者の部分はかなりきつめなので普通にやるなら要調整

・start.bat

→プレイヤー数とか、ポートとか

あたりを編集(ポートはデフォルト27016、RCONのパスくらいは変えたほうがいいかな)

##### ⑤start.batを起動する。

起動オプションを設定し、srcds.exeを起動するやつ。

起動オプションについては↓

| オプション                   | 概要                               |
| ---------------------------- | ---------------------------------- |
| -autoupdate                  | 起動時にアップデートチェックをする |
| -console                     | CUIコンソールで起動する            |
| +hostport                    | IPポート番号を指定する             |
| +map "マップ名 ゲームモード" | マップとゲームモードを指定         |



##### ⑥コンソールから接続

connect `ローカルのIPアドレス`:`ポート`

※ローカルのIPアドレスはループバックアドレス(127.0.0.1)じゃなかった

確認方法はサーバーをGUIで起動して出るやつ

#### クライアントの設定

##### ①コンソールから接続

connect `グローバルのIPアドレス`:`ポート`

------------------

### 設定内容のメモ

そのうち



### その他メモ

ログは`left4dead2\addons\sourcemod\logs`あたりに出てそう

---------------------------

### 参考

http://gengen5656.blog46.fc2.com/blog-entry-34.html

2011年の記事なので、インストールするものとかは最新のやつを取ってきたほうがいい。