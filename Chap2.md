# Backend

[Back to README](/README.md)

[Back to Previous Chapter](/Chap1.md)
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

```
poetry --version
```
が実行できればOKです！

## Checkpoint1

Q1. `pyenv`と`poetry`を使用して、python3.11を使用したプロジェクトを作ってみましょう！

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

Q2. Classを使ったなんかいい課題を教えて下さい(help!)

Q3. is-a関係とhas-a関係の違いは？


## DB
Webアプリケーションにおけるデータを保管するデータベース(以下DB)について勉強していきましょう。

実際のWebアプリケーションではORM(Model)と呼ばれるDBを抽象化(細かい操作は見えなくして簡単に扱えるようにすること)したライブラリが使われます。

しかし、実際のサービスではORMしか知らないと、N+1問題やクエリの実行計画を見れないなどのWebアプリケーションのパフォーマンスを十分なものにすることはできません。

そこで、まず最初はDBとはどういうものか、そしてDBを操るSQLとはどういったものなのかをさらっと理解しておきましょう。

- [DB入門](http://www.isc.meiji.ac.jp/~ri03037/ICTdb1/step01.html)
- [Progate SQL入門](https://prog-8.com/courses/sql)
- +1 [適切なIndexを張るために](https://qiita.com/kodai-saito/items/541e4fe46c2d3edc9634)

## Checkpoint3

Q1. DBにIndexを張るメリットとデメリットとは何でしょうか？
Q2. デッドロックになる場合はどのような場合でしょうか？
Q3. N+1問題とは何でしょうか？
Q4. SQL100本ノックをやりましょう(1~30番ぐらいまではやってみましょう。それ以降はお好みで)(Google Colaboratoryで実行できます。)
https://note.com/nmt_rootassist/n/nf70b6e73f673

## FastAPI

いよいよWebアプリケーションのバックエンドを開発していきます！

まずは公式のチュートリアルやドキュメントを読んでみましょう！

https://fastapi.tiangolo.com/ja/tutorial/

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



[Go to Next Chapter](/Chap3.md)