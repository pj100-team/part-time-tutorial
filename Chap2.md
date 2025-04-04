# Backend

[Back to README](/README.md)

[Back to Previous Chapter](/Chap1.md)
## プログラミング言語とは
最初にプログラミング言語がどういう物なのかを体験するために以下のページで簡単にPython(無料部分のみ)を触って見ましょう!  
[Pythonって何](https://prog-8.com/lessons/python/study/1)

## 環境構築
本節では主にPythonの学習を行っていきます。
Pythonが使用できるように、`pyenv`と`poetry`を使って環境を構築していきます。

`pyenv`と`poetry`がそれぞれどんなツールなのかは以下の記事を読んで理解しましょう。

[`pyenv`公式](https://github.com/pyenv/pyenv) 

[`poetry`公式](https://python-poetry.org/) 

英語だけど頑張って読みましょう。

### `pyenv`のインストール

#### MacOS

Homebrewを使ってインストールできます。

```
brew update
brew install pyenv
```

```
pyenv -v 
```

が実行できればOKです！

#### Linux(WSL)

まず必要なライブラリを以下のコマンドでインストール

```
sudo apt update
sudo apt install build-essential libffi-dev libssl-dev zlib1g-dev liblzma-dev libbz2-dev \
  libreadline-dev libsqlite3-dev libopencv-dev tk-dev
```

公式からソースコードをclone

```
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

PATHの設定などを`~/.bashrc`に記載して、設定をロードする。

```
echo '' >> ~/.bashrc
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init --path)"' >> ~/.bashrc
source ~/.bashrc
```


```
pyenv -v 
```

が実行できればOKです！

### `Poetry`のインストール

以下のコマンドを打つとインストールすることができます！
もしも、`python3`のコマンドが見つからない場合は、`python`に変えてみたりしてください。

```
curl -sSL https://install.python-poetry.org | python3 -
```

それでもうまくインストールできない場合はHomebrewを使ってPoetryをインストールしてみてください。

```
brew install poetry
```

```
poetry --version
```
が実行できればOKです！

## Checkpoint1

Q1. `pyenv`と`poetry`を使用して、python3.11を使用したプロジェクトを作ってみましょう！

※CheckPoint4で同じ環境を使用するので、プロジェクトは残しておくことをお勧めします。

ヒント: Google検索してやり方を見てみましょう！公式ドキュメントにも色々書いてるので英語を頑張って読んだり、日本語訳したりして、読んでいきましょう！

Q2. なぜ`pyenv`のような仮想環境ツールが必要なのでしょうか？

Q3. `pyproject.toml`に記載されている`tool.poetry.dependencies`と`tool.poetry.group.dev.dependencies`にそれぞれ含まれるライブラリの違いは何でしょうか?

Q4. `poetry.lock`ファイルは`git`で管理すべきでしょうか？しないべきでしょうか？

Q5. `poetry.lock`ファイルが存在せずに、`pyproject.toml`のみが存在する場合に、どのような問題が起こるでしょうか？

Q6. `poetry.lock`ファイルに存在する、`hash`という項目はなぜ必要なのでしょうか？

## Python

Python言語について勉強しましょう！

https://www.tohoho-web.com/python/

特に、基本的な文法(`if`, `for`)と`Class`は重要なのでよく勉強してみてください。

`Class`についてよくわからない場合は以下のサイトを参考にしてみてください！

https://lemon818.com/python-class/

【動画】
https://www.youtube.com/watch?v=F5guF1y7G48

またPythonのデバッガPDBを使えるようにしましょう！

https://qiita.com/kaitolucifer/items/dc58efebd72d72a8feb2

上述の記事でPDBの基本的な使用方法が説明されています。

## Checkpoint2

Q1. Checkpoint1で作成したプロジェクトに、`fizzbuzz.py`というファイルを作成して、以下の仕様を満たすプログラムを書いてみてください。

仕様

1. 以下のコマンドで実行ができること

```
poetry run python fizzbuzz.py <入力したい数字>
```

プログラムが実行されると答えが`print`されること

2. `<入力したい数字>`の部分には1以上の長さの文字列が入る。(以下ではここで入力した文字列を`N`とする。)
3. `N`の値によって`print`される答えを以下のように変える。

    1. `N`が数字の場合

        1. `N`が3で割れる時`Fizz`
        2. `N`が5で割れる時`Buzz`
        3. `N`が15で割れる時`FizzBuzz`
        4. それ以外の場合`N`

    2. `N`が数字ではない場合

        1. `ValueError`例外をスロー


以下は実行例

```
poetry run python fizzbuzz.py 4
4


poetry run python fizzbuzz.py 15
FizzBuzz


poetry run python fizzbuzz.py hoge
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError("hoge is invalid input!")
```

Q2. pdbを使って、作成した処理で`N`の値を確認しましょう。

Q3. Classを使ったなんかいい課題を教えて下さい(help!)

Q4. is-a関係とhas-a関係の違いは？


## DB
Webアプリケーションにおけるデータを保管するデータベース(以下DB)について勉強していきましょう。

実際のWebアプリケーションではORM(Object Relation Mapping)と呼ばれるDBを抽象化(細かい操作は見えなくして簡単に扱えるようにすること)したライブラリが使われます。これによりSQL文を書かなくても、例えばPythonのDjangoフレームワークだと`.save`や`.delete`のような関数みたいに扱うことができます。つまり、いちいち`INSERT INTO`や`UPDATE`のような長い命令を下さなくてもPythonの関数の様に書けるので便利なのです。

しかし、実際のサービスではORMしか知らないと、N+1問題やクエリの実行計画を見れないなどのWebアプリケーションのパフォーマンスを十分なものにすることはできません。

そこで、まず最初はDBとはどういうものか、そしてDBを操るSQLとはどういったものなのかをさらっと理解しておきましょう。
以下のDB入門(応用は興味があれば)、SQL入門の記事に目を通してください。
実際のDBにどのようなものがあるかを知るために、DBエンジンの種類に関しての記事を追加しました。
また、terminalでDBのテーブルを参照して実際に登録されている実感が湧かないため、視覚的に見れるツールDBeaverについても説明追加しました。

- [DB入門](https://qiita.com/higasun/items/0767107dc7100a60f4e4)
  - [DBエンジンの種類](https://zenn.dev/lisras/articles/5ca8dfb5c26e81)
  - [DBとDBエンジンの違い](https://wa3.i-3-i.info/word11570.html)
  - [DBを視覚的に確認するには(DBeaver)](https://zenn.dev/aiq_dev/articles/2629b53f1298bc)
  - [DBeaver使い方](https://qiita.com/12345/items/48f6856e32fd618ea307)
  - [DB用語参考ページ](https://wa3.i-3-i.info/search.html?q=%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9&ln=)
  - [応用:データベース設計](https://qiita.com/KNR109/items/5d4a1954f3e8fd8eaae7)
  - [応用:Cloud上でのDB(AWS Amazon Aurora)](https://business.ntt-east.co.jp/content/cloudsolution/column-71.html)
- [SQL入門(Progate)](https://prog-8.com/courses/sql)
  - [応用:適切なIndexを張るために](https://qiita.com/kodai-saito/items/541e4fe46c2d3edc9634)

## Checkpoint3

Q1. DBにIndexを張るメリットとデメリットとは何でしょうか？

Q2. デッドロックになる場合はどのような場合でしょうか？

Q3. N+1問題とは何でしょうか？

Q4. SQL100本ノックをやりましょう(1~30番ぐらいまではやってみましょう。それ以降はお好みで)

(Google Colaboratoryで実行できます。)
https://note.com/nmt_rootassist/n/nf70b6e73f673

## Django 

いよいよWebアプリケーションのバックエンドを開発していきます！

まずはPythonのフレームワークであるDjango(Web開発のためのPython)の公式のチュートリアルやドキュメントを読んでみましょう！  
https://docs.djangoproject.com/ja/5.1/  
最初にDjangoを自分のPCに[インストール](https://docs.djangoproject.com/ja/5.1/intro/install/)して、
[チュートリアル](https://docs.djangoproject.com/ja/5.1/intro/tutorial01/)
のその7まで読みながら実行しましょう！

ちなみにこれからライブラリやフレームワークという言葉が多用されますが、どちらもよく使われる機能を実装して、その機能を毎回ゼロからコードで書かなくても良いように準備された便利なファイルです！
- [ライブラリ](https://wa3.i-3-i.info/word1473.html)
- [ライブラリとフレームワークの違い](https://wa3.i-3-i.info/diff1146programming.html)

## Checkpoint4

Q1. 以下の単語はどのような意味か説明してください。

1. RestAPI, エンドポイント, URI
3. HTTPリクエスト、レスポンス
4. Session
5. Cookie
6. HTTPステータスコード 例えば(404)
7. HTTPリクエストメソッド
8. CSRFトークン
9. HTTPとHTTPSの違い
10. リクエストボディとリクエストヘッダ

Q2. 以下のサイトを参考にTODOアプリのエンドポイントを作ってみてください。

環境は、Checkpoint1で作成した環境を使用してください。ライブラリ管理は`pip`ではなく、`poetry`を使用してください！

https://dev.to/nditah/develop-a-simple-python-fastapi-todo-app-in-1-minute-8dg

## 次のChapterを始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap3.md)
