# C言語講座 環境構築 = for mac =
from Knakar
## brewをinstall
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
インストールされているか確認
```sh
brew -v
```
### `bash: brew: command not found`が出た場合
```zsh
echo "export PATH=$PATH:/opt/homebrew/bin" >> ~/.zshrc
source ~/.zshrc
```
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
```sh
ln -s /usr/local/bin/gcc-{version} /usr/local/gcc
ln -s /usr/local/bin/g++-{version} /usr/localg++
```

## Step Last
```sh
exec $SHELL -l
```
## 何かエラーが起きたとき
xcodeが入ってると起きるっぽい!?
```sh
xcode-select --install
```
