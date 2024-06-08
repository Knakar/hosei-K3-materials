# 第一回 環境構築

## WSLのインストール(Windows Only)
powershell(admin)
```
wsl.exe install -d Ubuntu
```
再起動

VSCodeもしくはJetBrians Fleetを立ち上げる
WSLを選択し起動
### FleetでWSL(ubuntu)に接続
![](https://resources.jetbrains.com/help/img/fleet/1.35/f-wsl-1.png)

Pless`Ctrl+Shift+A`and input `terminal`
then, Select `New Terminal Tool`




## Pythonのインストール(WSL, Ubuntu)
パッケージリストを更新
```
sudo apt update && sudo apt upgrade - y
```
pythonをインストール
```
sudo apt install python3
```
virtualenvをインストール
```
sudo apt install python{version}-venv
```
#### `{version}`の調べ方
```
python3 --version
```
出力が`Python 3.12.3`のとき
`{version}=3.12`


## 仮想環境を作成
プロジェクトファイルに移動し([参考: コマンド基礎(Qiita)](https://qiita.com/Umeda-East45/items/6beaf53bdc24d0736ec7))
### 作成
```
python3 -m venv {env_name}
```
個人的におすすめな`{env_name}`は`.venv`

### 入る
```
source {env_name}/bin/activate
```
### 仮想環境内でパッケージをインストール
```
pip install {package_name e.g.) numpy}
```

### 出る
```
deactivate
```

