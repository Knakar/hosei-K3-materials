# C言語講座 環境構築 = for mac =
from Knakar
## for M1 Mac
「ターミナル」の「情報を見る」から
![](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2090432%2F1e6bbfa7-9eea-b812-a570-562a90311e23.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&w=1400&fit=max&s=0accade9a5e6bcba3946920f9413fe1b)
「Rosettaを使用して開く」のチェックボックスをクリックして有効化する
![](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2090432%2Fe5542180-73bd-2b4a-e1ed-2e57560fe284.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&w=1400&fit=max&s=d953af9f9e2fd14d0661f65b054ed2d9)
## brewをinstall
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
インストールされているか確認
```sh
brew -v
```
### エラー`brew: command not found`が出た場合
zsh
```zsh
echo "export PATH=$PATH:/opt/homebrew/bin" >> ~/.zshrc
source ~/.zshrc
```
bash
```bash
echo "export PATH=$PATH:/opt/homebrew/bin" >> ~/.bashrc
source ~/.bashrc
```

## Install VSCode
```sh
brew install visual-studio-code
```

## Install gcc
```sh
brew install gcc
```

## [Optional] gccのリンク先をclangからgcc系にする
`{version}`はインストールした`gcc`のバージョン
```sh
ln -s /usr/local/bin/gcc-{version} /usr/local/gcc
ln -s /usr/local/bin/g++-{version} /usr/local/g++
```

## Last Step
```sh
exec $SHELL -l
```
## 何かエラーが起きたとき
xcodeが入ってると起きるっぽい!?
```sh
xcode-select --install
```
