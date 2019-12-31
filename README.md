# l4d2coop

### インストール方法

#### サーバーの設定

##### �@[steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD)をダウンロード

##### �A適当な場所でSteamCMD.exeを起動しサーバーをインストールする。

```
login anonymous
force_install_dir l4d2server
app_update 222860
```

##### �Bサーバーをインストールしたフォルダ(`force_install_dir `にて指定したフォルダ)に移動してgitる

```
git init
git remote add origin https://github.com/neohral/l4d2coop.git
git fetch origin
git reset --hard origin/master
```

##### �Cサーバー系の設定をする。

・left4dead2\cfg\server.cfg

→プレイヤー数とか、RCONのパスとか

→特殊感染者の部分はかなりきつめなので普通にやるなら要調整

・start.bat

→プレイヤー数とか、ポートとか

あたりを編集(ポートはデフォルト27016、RCONのパスくらいは変えたほうがいいかな)

※設定内容のメモ参照

##### �Dstart.batを起動する。

##### �Eコンソールから接続

connect 【ローカルのIPアドレス】:【ポート】

※ローカルのIPはループバックじゃなくて、**サーバーコンソールのIPアドレス**

#### クライアントの設定

##### �@コンソールから接続

connect 【**グローバル**のIPアドレス】:【ポート】

### 設定内容のメモ

