# Subject

[Back to README](/README.md)

[Back to Previous Chapter](/Chap3.md)

研修修了課題として、TODOアプリを作ってもらいます。

基本的にChap1 ~ Chap3までの内容でできるようになっていますし、それらの技術を使用して作成してください。

## 技術要件

- API -> FastAPI (poetry管理)
- DB -> お好みのDBを使用してください。sqlite3でも可能
- FrontEnd -> React

<img src='todolist.png'></img>

作成してもらうのは上のような簡単なTODOアプリです。

要件
1. ユーザーはTODOリストを追加することができる。(認証機能は無し)
    1. TODOリストにはタイトルと締切、メモを追加することができる。
    2. TODOリストにはそれぞれ、子タスク(図中ではステップ)を作成することができる。子タスクはその下に子タスクを持つことはできない。子タスクには、名前だけを持たせる。
2. タスクは古い順に上から並べて表示する。
3. ユーザーは上の検索ボタンからタスクの名前で検索を行うことができる。
4. TODOリストのデータはDBに保存されている。

<img src='todolist_search.png'></img>

参考にしたのはMicroSoftのTODOリストです。機能を絞ってありますが、もしも動作を確認したい場合は、以下のリンクからアクセスできます。
もしも要件でわからないところがあれば参考にしてください。

https://to-do.live.com/tasks

## 進め方

1. まずgithubで1つリポジトリを作成する。
2. 1で作成したリポジトリの中に、Backend・Frontendの環境構築を行う。
3. API
    1. TODOListの機能を満たすのに必要なエンドポイントのURIとHTTPメソッドを列挙する。
    2. 必要なDBのテーブルを列挙し、ER図を書いてみる。
    3. 実装を行う
4. FrontEndの実装を行う。
5. 完了したら、下のPRを出す。

## 次のChapterを始める前に

本リポジトリを`clone`し、改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットします。改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap5.md)
