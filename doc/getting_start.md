## 開発のはじめ方

### はじめに

* middleman

[middleman](https://middlemanapp.com/) を使ってサイトを構築していきます。
middleman は公式の日本語サイトが充実していて、基本的に公式を見たら出来そうな感じです。
ちょっと困っても、 github に上がっている source を参考にできます。

### 開発環境の作り方(Mac)

* コンパイルツール

```
$ xcode-select --install
```

* Homebrew

Middleware を含めたパッケージを管理

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

* irb(Interactive Ruby)

```bash
$ brew install readline
```

* https

```bash
$ brew install openssl
```

* ruby-build, rbenv

Ruby バージョン切り替えツール

```bash
$ brew install ruby-build
$ brew install rbenv
```

* Set up path

```bash
$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> .bash_profile
$ echo 'eval "$(rbenv init -)"' >> .bash_profile
$ source .bash_profile
```

* Ruby

rbenv を使って Ruby をインストールします。

```bash
$ rbenv install 2.3.0
```

* 標準で使う ruby のバージョンを切り替える

```bash
$ rbenv global 2.3.0
```

* 確認

```bash
$ rbenv versions
$ ruby -v
```

* Bundler

[Bundlerを使ったGemパッケージの管理](http://www.rubylife.jp/rails/ini/index2.html)

Ruby で使われるライブラリやアプリケーションは Gem と呼ばれる形式のパッケージにすることができます。 Bundler はアプリケーションに必要となる Gem パッケージの種類やバージョンを管理し、複数のPCで必要なGemパッケージをインストールする仕組みを提供してくれます。

```bash
$ gem install bundler
```

## 実際に動かす

```bash
$ git clone https://github.com/jtf-2016/jtf-2016.github.io.git
$ cd jtf-2016.github.io
$ git checkout develop
$ bundle install
$ script/server
$ open http://127.0.0.1:4567
```
