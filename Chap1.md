# Introduction

[Back to README](/README.md)


## エディタ[1h]
### Visual Studio Code
Visual Studio Code（通称：VS Code）とは、プログラミングのコードを編集するためのエディタ（編集アプリ）です。
使い慣れたエディタ・IDEがあればそれをお使いいただいて結構ですが、VS Codeの方が圧倒的に評価が高いのでおすすめです。エディタにこだわりのない方は、以下の公式ページよりVS Codeをダウンロードしてください。
[Visual Studio Code 公式ページ](https://code.visualstudio.com/)

日本語化もしておきましょう。
[VSCode (Visual Studio Code) を日本語化する](https://www.karelie.net/vscode-visual-studio-code-japanese/)

記事を読む
[Visual Studio Codeの使い方、基本の「キ」](https://www.atmarkit.co.jp/ait/articles/1507/10/news028.html)


## 環境構築[2h]
このセクションではこのチュートリアルを行う上で必要になる環境を構築していきます。
対象はWindows、MacOS、Linuxです。

以下のコマンドが動かせる場合はこのセクションは飛ばしてもらっても大丈夫です。

```
git --version
```


### Windows
#### WSLおよびUbuntuのインストール
基本的に開発ではLinux環境を使用することが多いので、まずはWSL（Windows Subsystem for Linux）というWindowsの中でLinux環境を動かすことができる機能を使用して、Linux環境を作成します。

[公式ページ](https://learn.microsoft.com/ja-jp/windows/wsl/install)
に従ってLinux環境をインストールします。なお、公式ページにもある通り、Linux環境のインストールにおいて使用するのはVS Codeではなく、WindowsのコマンドプロンプトもしくはPowerShellです。

WSLはwsl2を使用してください。
WSLを使って、Linux環境の一種であるUbuntu 20.04 LTSをインストールしてください。Ubuntuとは、Linuxディストリビューション（Linuxのシステムやソフトウェアを一つにまとめた〝スターターキット〟のようなもの）の一種です。


#### VS CodeとWSLの接続
VS CodeでUbutu内のファイルを編集・実行できるよう、設定します。

[公式ページ](https://learn.microsoft.com/ja-jp/windows/wsl/tutorials/wsl-vscode) に従ってVS CodeにRemote Developmentという拡張機能を追加し、その後、VS CodeにてUbuntuを起動できるように設定してください。

最終的に、VS Codeの編集画面の左下に緑色で「WSL：Ubuntu」と表示されれば成功です。

特に指示がない限り、以降のコマンド（例えば、次節〝Gitのインストール〟のsudo apt-get updateなどのコマンド）は、VS CodeでUbuntuを起動した状態で、VS Codeのターミナルに入力してください。


#### Gitのインストール
Linux環境が作成できたら、以下のコマンドで`apt-get`というパッケージマネージャーを使用して、`git`をインストールしていきます。

```
sudo apt-get update
sudo apt-get install git-all
```

sudoコマンド実行の際にパスワードを求められる場合があります。その場合は、Ubuntuインストールの際に設定したパスワードを入力してください。

もしも、途中でエラーが出た場合は、なにか問題があるはずです。Googleで検索したり、ChatGPTに聞いてみたりしてください。

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.25.1`のような文字列が表示されたら、キホンの環境構築はOKです！

### Mac

Homebrewと呼ばれるパッケージ管理ツールをインストールしましょう。

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

のような文字が画面に表示されればOKです！

続いて、gitをインストールします。

```
brew install git
```

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.30.1 (Apple Git-130)`のような文字列が表示されたら、キホンの環境構築はOKです！

### Linux

以下のコマンドで`apt-get`というパッケージマネージャーを使用して、`git`をインストールしていきます。

```
sudo apt-get update
sudo apt-get install git-all
```

もしも、途中でエラーが出た場合は、なにか問題があるはずです。
Googleで検索したり、ChatGPTに聞いてみたりしてください。

インストールできたら、以下のコマンドを叩いてみてください。

```
git --version
```

結果として`git version 2.25.1`のような文字列が表示されたら、キホンの環境構築はOKです！


## Linuxのキホンのキ[2h]

続いて、Linuxコマンドの使い方を学習していきます。(MacOSでも大体一緒です！)
まず最初にLinuxのキホンについて以下のブログにまとまっているので見てみると良いと思います！

https://eng-entrance.com/category/linux/linux-basic

続いて、Shell(コマンドを打つ黒い画面)を通じて、ファイル作成や編集といった様々な操作をできるようになりましょう！
以下の漫画がわかりやすく解説されているので、読んでください！

https://xtech.nikkei.com/atcl/learning/column/19/00014/


## gitとその使い方[3h]

続いて、`git`について勉強します。エンジニアとして働く以上、`git`を避けては通れません！

まず以下の資料で`git`の意味と使い方の基礎を学びましょう

https://backlog.com/ja/git-tutorial/

入門編、発展編、プルリクエスト編の全てに目を通しましょう。ただし、途中でBacklogを使用したチュートリアルが登場しますが、これらはやらずに飛ばしてください（Backlogに有料登録する必要があるため）。

ある程度理解できたら、以下のハンズオンを実際に行ってみて、手を動かしてgit,githubを使えるようになりましょう。

https://qiita.com/TakumaKurosawa/items/79a75026327d8deb9c04



## HTML & CSS[2h]

Web開発を行う基本となるHTMLとCSSについて学んで行きましょう！

[Webデザインの教科書](https://web-design-textbook.com/)

上記のサイトの以下の項目に取り組みましょう。
- HTML
- CSS(基本編)
- Web制作(準備編)
- Web制作(基本編)



## Checkpoint
この章で勉強したことが使えるようになっているかを確認しましょう！
もしも、わからないことがあったら、もう一度調べてみましょう！

`linux`コマンド

Q1. `home`ディレクトリ(`cd ~`とコマンドを打つと移動できる)に、`tutorial`という名前のディレクトリを作りましょう。

Q2. (Q1に続いて) `tutorial`ディレクトリの中に、`git-command.txt`という空のファイルを作成してください。

Q3. (Q2に続いて) Shellで`git`とコマンドを打つと以下のように表示されると思います。

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

この際に、手動でコピーアンドペーストするのではなく、1行のコマンドで打てるようにしましょう。

ヒント: `|`とか`grep`を使います。

Q4. 本チャプターでは`git`をインストールして使えるようにしました。今後、このチュートリアルを進めていくと様々なソフトウェアをインストールする必要があります。
その中で、`hoge`というソフトをインストールしたはずなのに、Shellで`hoge`(※)と入力しても

```
command not found: hoge
```

というエラーがでしまって使えないということがよくあります。このエラーはインストールしたソフトウェアに`PATH`が正しく通されていないことが原因です。
では、どうすれば`PATH`を正しく通すことができるのでしょうか？

ヒント: https://qiita.com/Naggi-Goishi/items/2c49ea50602ea80bf015

※`hoge`とは、全く意味のない名称を示したい時に使う「メタ構文変数」と呼ばれるものの1つです。実際に`hoge`とターミナルに打ち込んで何かが動作するわけではありません。例えば、郵便局のサイトを訪れると、宛名の書き方のところに「郵便太郎 様」とか「郵便花子 様」とかテキトーな名前が使われていますよね？プログラミング界における「郵便太郎」が`hoge`です。他にも`piyo`、`foo`、`bar`など色々あります。プログラミングの教材サイトなどでちょくちょく登場するので覚えておきましょう。

`git`

Q1. `github`のアカウントは存在しますか？ない場合は作りましょう。

Q2. `ssh`で`github`に接続することができますか？以下のコマンドを打って確認しましょう！

```
ssh -T git@github.com
```

応答として以下の文字列が表示されたらOKです！

```
Hi (account名)! You've successfully authenticated, but GitHub does not provide shell access.
```

できない場合は、[こちらのサイト](https://qiita.com/shizuma/items/2b2f873a0034839e47ce)
を参考にSSHで接続できるようにしましょう！

## 次のChapterを始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap2.md)



