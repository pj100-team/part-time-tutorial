# Introduction

[Back to README](/README.md)

## 環境構築

このセクションではこのチュートリアルを行う上で必要になる環境を構築していきます。
対象は Windows、MacOS、Linux です。

以下のコマンドが動かせる場合はこのセクションは飛ばしてもらっても大丈夫です。

```
git --version
```

### Windows

基本的に開発では Linux 環境を使用することが多いので、まずは WSL という Windows の中で Linux 環境を動かすことができる機能を使用して、Linux 環境を作成する。

[公式ページ](https://learn.microsoft.com/ja-jp/windows/wsl/install)に従ってインストールして下さい。

WSL は wsl2 を使用してください。

使用する Linux 環境は Ubuntu 20.04 LTS を想定しています。

Linux 環境が作成できたら、以下のコマンドで`apt-get`というパッケージマネージャーを使用して、`git`をインストールしていきます。

```
sudo apt-get update
sudo apt-get install git-all
```

もしも、途中でエラーが出た場合は、なにか問題があるはずです。
Google で検索したり、ChatGPT に聞いてみたりしてください。

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.25.1`のような文字列が表示されたら、キホンの環境構築は OK です！

### Mac

Homebrew と呼ばれるパッケージ管理ツールをインストールしましょう。

https://brew.sh/index_ja

インストールできたら、以下のコマンドを打って見ましょう。

```
brew --version
```

結果として

```
Homebrew 4.0.10
Homebrew/homebrew-core (git revision 29f317deb32; last commit 2023-04-03)
Homebrew/homebrew-cask (git revision 4602819837; last commit 2023-04-03)
```

のような文字が画面に表示されれば OK です！

続いて、git をインストールします。

```
brew install git
```

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.30.1 (Apple Git-130)`のような文字列が表示されたら、キホンの環境構築は OK です！

### Linux

以下のコマンドで`apt-get`というパッケージマネージャーを使用して、`git`をインストールしていきます。

```
sudo apt-get update
sudo apt-get install git-all
```

もしも、途中でエラーが出た場合は、なにか問題があるはずです。
Google で検索したり、ChatGPT に聞いてみたりしてください。

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.25.1`のような文字列が表示されたら、キホンの環境構築は OK です！

## Linux コマンドのキホンのキ

続いて、Linux コマンドの使い方を学習していきます。(MacOS でも大体一緒です！)
まず最初に Linux のキホンについて以下のブログにまとまっているので見てみると良いと思います！
(Linux の環境構築ではなく、コマンドを中心に学習すると良いです！)

https://eng-entrance.com/category/linux/linux-basic

続いて、Shell(コマンドを打つ黒い画面)を通じて、ファイル作成や編集といった様々な操作をできるようになりましょう！
以下の漫画でわかりやすく解説されているので、読んでください！

https://xtech.nikkei.com/atcl/learning/column/19/00014/

## エディタ

### Visual Studio Code

使い慣れたエディタ・IDE があればそれをお使いいただいて結構ですが、Visual Studio Code が圧倒的に評価が高いのでおすすめです。
[Visual Studio Code 公式ページ](https://code.visualstudio.com/)

日本語化もしておきましょう。
[VSCode (Visual Studio Code) を日本語化する](https://www.karelie.net/vscode-visual-studio-code-japanese/)

記事を読む
[Visual Studio Code の使い方、基本の「キ」](https://www.atmarkit.co.jp/ait/articles/1507/10/news028.html)

## git とその使い方

続いて、`git`について勉強します。エンジニアとして、働く以上`git`を避けては通れません！

まず以下の資料で`git`の意味と使い方の基礎を学びましょう。

<a href="https://backlog.com/ja/git-tutorial/" target="_blank">サル先生の Git 入門</a>

入門編、発展編、プルリクエスト編の全てに目を通しましょう。

ある程度理解できたら、以下のハンズオンを実際に行ってみて、手を動かして git,github を使えるようになりましょう。

https://qiita.com/TakumaKurosawa/items/79a75026327d8deb9c04

## HTML & CSS

Web 開発を行う基本となる HTML と CSS について学んで行きましょう！

以下の資料の CSS 上級編を除いた

[HTML](https://web-design-textbook.com/html-textbook.html) ~ [Web 制作中級編](https://web-design-textbook.com/makepage-middle.html)

を行いましょう！

[Web デザインの教科書](https://web-design-textbook.com/)

## DevTools

Web 開発を行う上で強力なツールとなる Web ブラウザの開発者ツールについて学んでいきましょう。

https://willcloud.jp/knowhow/dev-tools-01/

上記の資料で HTML＆CSS の挙動を確認できるようにしましょう。

## Checkpoint

この章で勉強したことが使えるようになっているかを確認しましょう！
もしも、わからないことがあったら、もう一度調べてみましょう！

`linux`コマンド

Q1. `home`ディレクトリ(`cd ~`とコマンドを打つと移動できる)に、`tutorial`という名前のディレクトリを作りましょう。

Q2. (Q1 に続いて) `tutorial`ディレクトリの中に、`git-command.txt`という空のファイルを作成してください。

Q3. (Q2 に続いて) Shell で`git`とコマンドを打つと以下のように表示されると思います。

```
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]

~~~ 途中省略 ~~~

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
```

この内、`repository`という文言が含まれている行のみを`git-command.txt`に記載しましょう。

この際に、手動でコピーアンドペーストするのではなく、1 行のコマンドで打てるようにしましょう。

ヒント: `|`とか`grep`を使います。

`git`

Q1. `github`のアカウントは存在しますか？ない場合は作りましょう。

Q2. `ssh`で`github`に接続することができますか？以下のコマンドを打って確認しましょう！

```
ssh -T git@github.com
```

応答として以下の文字列が表示されたら OK です！

```
Hi (account名)! You've successfully authenticated, but GitHub does not provide shell access.
```

できない場合は、https://www.kagoya.jp/howto/it-glossary/develop/github_ssh/を参考にSSHで接続できるようにしましょう！

Q3. `github`で、[こちらの記事](https://docs.github.com/ja/get-started/quickstart/create-a-repo)を参考にしてリポジトリを作成しましょう。また、そのリポジトリに`README.md`を作成しましょう。

Q4. `Visual Studio Code`から、適当なテキストファイルを作成しましょう。
[こちらの記事](`https://yzhums.com/751/`)を参考にして、Q3 で作成したリポジトリにプッシュしましょう。

`HTML` & `CSS`

Q1. 簡単な TODOList を作ってみましょう。[ここ](https://www.w3schools.com/howto/howto_js_todolist.asp)に記載されている通りで、JavaScript はまだやらなくても大丈夫です！見た目だけ再現できるようにしましょう！

Q2. 開発者ツールを使用して、作成した TODO リストの padding や mergin が正しく設定されているかを確認しましょう。

## 次の Chapter を始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PR と省略)を出しましょう！
どんな些細な PR でも構いません！:pray:
改善点の`Pull Request`が出されたら、本 Chapter のフィードバックと次 Chapter のプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap2.md)
