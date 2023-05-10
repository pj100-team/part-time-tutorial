#　Frontend

[Back to README](/README.md)

[Back to Previous Chapter](/Chap2.md)
## JavaScript
チュートリアルを使って基本的な文法をマスターしていきましょう！

https://www.w3schools.com/js/

Classに関しては、Reactでほぼ使わないので、できなくても大丈夫です！
ES6の文法で書くことが多いので、特に

- Arrow関数
- Spread演算子

に関しては掛けるようにしておきましょう。

## 環境構築
フロントエンドの環境構築を行っていきます。

https://docs.volta.sh/guide/getting-started

以下のコマンドでインストールが完了します。

```
curl https://get.volta.sh | bash
```

以下のコマンドを打って

```
volta --version
```

1.1.1

のような文字列が表示されればOKです！

voltaを使用して、nodeの最新版をインストールしておきましょう。
今回は16系のnodeを使用します。

```
volta install node@16
```

以下のコマンドを実行して

```
node -v
```

v16.20.0

のような文字列が表示されればOKです！





## TypeScript

JavaScriptに型がついた言語です。
普段の開発ではTypeScriptを使用することが多いので、マスターしましょう！

以下の資料はかなりボリュームがありますが、Reactの部分などは飛ばしましょう。

https://typescript-jp.gitbook.io/deep-dive/


## React

いよいよReactを勉強していきます！公式が一番わかりやすく、非常によくまとまっているのでやっていきましょう！

https://react.dev/learn

## Checkpoint

Q1. `async`, `await`, `Promise`について説明してください。

Q2. `TypeScript`における、ジェネリクスとはどういうものでしょうか？

Q3. Reactを使ってTODOアプリを作ってみてください。

参考: https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_todo_list_beginning

[Go to Next Chapter](/Chap4.md)

