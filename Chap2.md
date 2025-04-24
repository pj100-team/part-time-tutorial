# Backend

[Back to README](/README.md)

[Back to Previous Chapter](/Chap1.md)

## 学び方のポイント

- 分からない単語があっても **「読み飛ばしてOK」**。
- 実際に動かして「理解すること」が最優先。
- まずは完走、あとで復習！のスタンスで取り組みましょう 💪


## <font color="Coral">WEB開発における語彙のキャッチアップ</font>
> [!tip]
> - はじめから、全てを完全に理解する必要はありません。
> - 実務を通じて、徐々に深く理解していけば問題ありません。
> - まずは、広く浅く概要を掴むことを目標にしてください。


| カテゴリ     | 知識・技術                     | 参考URL |
|--------------|-------------------------------|-----------------------------------|
| Web知識      | HTTP/HTTPS                    | [httpsとは？httpとの違いやよくある勘違い・セキュリティの基礎まで](https://cybersecurity-jp.com/column/25772) |
| Web知識      | TCP/IP                        | [TCP/IPとは「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word1540.html) |
| Web知識      | SSH                           | [SSHとは？仕組みや認証方法を解説](https://hnavi.co.jp/knowledge/blog/ssh/) |
| Web知識      | API                           | [REST APIとは？特徴やメリットをわかりやすく解説](https://envader.plus/article/83) |
| Web知識      | CORS                          | [CORSについて簡単に説明する](https://tech-lab.sios.jp/archives/37299) |
| Web知識      | HTTPメソッド                  | [Web開発でよく使う4つのHTTPメソッド【REST API】](https://tsuyopon.xyz/2019/01/31/understand-4-http-methods/) |
| Web知識      | ステータスコード               | [api ステータスコードとは？その設計方法は？](https://apidog.com/jp/blog/what-is-api-status-code-and-its-designing/) |
| Web知識      | セキュリティ                  | [セキュリティとは？意味や種類、基本のセキュリティ対策をわかりやすく解説](https://aslead.nri.co.jp/ownedmedia/development/security-001/) |
| プログラミング| Python                        | [Pythonを使ったWebアプリケーションの開発の流れと企業が注意するべきポイント](https://corp.tech.hipro-job.jp/column/175) |
| ミドルウェア  | DB設計                        | ・[データベース設計とは？設計する目的・流れ・ポイントについて詳しく解説！](https://www.incudata.co.jp/magazine/000611.html)<br>・[ER図とは？書き方やテクニックをわかりやすく解説](https://products.sint.co.jp/ober/blog/create-er-diagram) |
| ミドルウェア  | SQL                           | [【SQL入門】データベース言語の基礎知識と実践方法を解説！](https://udemy.benesse.co.jp/development/system/intro-sql.html) |
| ミドルウェア  | Nginx                         | [【超入門】これさえ読めばOK！初心者でもわかる NGINX 解説](https://beyondjapan.com/blog/2024/05/about_nginx/) |
| その他        | Docker                        | [【初心者向け・図解】Dockerとは？現役エンジニアがわかりやすく解説](https://o2mamiblog.com/docker-beginner-1/) |
| その他        | Postman                       | [ワークショップ - API基礎 Documentation](https://www.postman.com/postman/postman-japan-workshop/documentation/aslsdcq/api) |



## 環境構築
本節では主にPythonの学習を行っていきます。
Pythonが使用できるように、`pyenv`と`poetry`を使って環境を構築していきます。

`pyenv`と`poetry`がそれぞれどんなツールなのかは以下の記事を読んで理解しましょう。

[`pyenv`公式](https://github.com/pyenv/pyenv) 

[`poetry`公式](https://python-poetry.org/)

- [基本的な使い方](https://python-poetry.org/docs/basic-usage/)
- [コマンド集](https://python-poetry.org/docs/cli/)

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

## Checkpoint

Q1. `fizzbuzz.py`というファイルを作成して、以下の仕様を満たすプログラムを書いてみてください。

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

Q3. is-a関係とhas-a関係の違いは？


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

## Checkpoint

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

## Django REST Framework
次に、アイフルの実務で利用するDjango REST Frameworkについて学んでいきましょう！
下記のNoteの記事を1~12章まで読み進めましょう！
https://note.com/a_244/n/n0ba924a4a4d3?magazine_key=m058abba754d6

## Checkpoint

Q1. 以下の単語はどのような意味か説明してください！

1. RestAPI, エンドポイント, URI
3. HTTPリクエスト、レスポンス
4. Session
5. Cookie
6. HTTPステータスコード 例えば(404)
7. HTTPリクエストメソッド
8. CSRFトークン
9. HTTPとHTTPSの違い
10. リクエストボディとリクエストヘッダ

Q2 Django REST Framework 課題：TODO一覧APIを作ってみましょう！

## 🎯 目標
- `/api/todos/` にアクセスすると、TODOの一覧が JSON 形式で返ってくるAPIを作成してみましょう！まずは下記の説明を見ずにAPIを作成しましょう！

<details>
<summary>📝 ステップバイステップ解説（解答の一例を見たい場合はこちら）</summary>

## 🪜 ステップバイステップ解説

### ① モデルとテストデータを作成

モデルの作成

```python
# todos/models.py
from django.db import models

class Todo(models.Model):
    title = models.CharField(max_length=100)
    is_done = models.BooleanField(default=False)

    def __str__(self):
        return self.title
```
テストデータの作成

下記でDjangoシェルを開く
```
python manage.py shell
```

下記でTodoデータを入れる
```
from todos.models import Todo
Todo.objects.create(title="牛乳を買う", is_done=False)
Todo.objects.create(title="DRF課題を終わらせる", is_done=True)

```



### ② マイグレーションの実行
```
python manage.py makemigrations
```
```
python manage.py migrate
```

### ③　シリアライザを作成
```python
# todos/serializers.py
from rest_framework import serializers
from .models import Todo

class TodoSerializer(serializers.ModelSerializer):
    class Meta:
        model = Todo
        fields = '__all__'
```
### ④ ビューを作成
```python
# todos/views.py
from rest_framework.views import APIView
from rest_framework.response import Response
from .models import Todo
from .serializers import TodoSerializer

class TodoListView(APIView):
    def get(self, request):
        todos = Todo.objects.all()
        serializer = TodoSerializer(todos, many=True)
        return Response(serializer.data)

```
### ⑤ URLを設定
```python
# todos/urls.py
from django.urls import path
from .views import TodoListView

urlpatterns = [
    path('todos/', TodoListView.as_view()),
]

# config/urls.py（プロジェクト直下）
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('api/', include('todos.urls')),
]

```

</details>

### 確認方法
python manage.py runserverでサーバーを起動し、http://localhost:8000/api/todos/
でTODOの一覧が表示されれば成功です。

## 🧠 おまけ課題（余力があれば挑戦！）

- `POST /api/todos/`：TODOを新しく登録するエンドポイントを追加してみましょう。



## 次のChapterを始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap3.md)
