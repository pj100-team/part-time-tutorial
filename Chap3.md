# Frontend

[Back to README](/README.md)

[Back to Previous Chapter](/Chap2.md)


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

voltaを使用して、nodeをインストールしておきましょう。
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

まず初めにTypeScriptの基本的な文法を以下の資料を読んで理解しましょう。

[読んで学ぶTypeScript](https://typescriptbook.jp/reference)

初心者が理解しておくべき点は以下の項目です。

- [変数宣言: letとconst](https://typescriptbook.jp/reference/values-types-variables/let-and-const)
- [varはもう使わない](https://typescriptbook.jp/reference/values-types-variables/vars-problems)
- [変数宣言の型推論](https://typescriptbook.jp/reference/values-types-variables/type-inference)
- [boolean型 (論理型)](https://typescriptbook.jp/reference/values-types-variables/boolean)
- [number型 (数値型)](https://typescriptbook.jp/reference/values-types-variables/number)
- [string型 (文字列型)](https://typescriptbook.jp/reference/values-types-variables/string)

TODO: @武田 項目を上のように抜き出して羅列してほしい。

チュートリアルを１００％理解することは難しいので、程々にして次に進みましょう。


TypeScript初心者の方には、下記チュートリアルを１００％理解することは難しいので、大体2h~3h程度で軽く目を通しましょう。

また、最低限[こちらの記事](https://typescript-jp.gitbook.io/deep-dive/type-system)で紹介されている型システムは把握しておきましょう。


- [ ] [TypeScript入門 & 環境構築](https://typescript-jp.gitbook.io/deep-dive/getting-started)
- [ ] [JavaScript](https://typescript-jp.gitbook.io/deep-dive/recap)
- [ ] [モダンなJavaScriptの機能](https://typescript-jp.gitbook.io/deep-dive/recap)
- [ ] [プロジェクトの環境設定](https://typescript-jp.gitbook.io/deep-dive/project)
- [ ] [Node.js & TypeScriptのプロジェクト作成](https://typescript-jp.gitbook.io/deep-dive/nodejs)

Classに関しては、Reactでほぼ使わないので、できなくても大丈夫です！
ES6の文法で書くことが多いので、特に

- Arrow関数
- Spread演算子

に関しては書けるようにしておきましょう。

## React

いよいよReactを勉強していきます！公式が一番わかりやすく、非常によくまとまっているのでやっていきましょう！

https://react.dev/learn

#react-v3

ある程度Reactについて理解が深まってきたら実際に練習してみましょう！！

https://github.com/pj100-team/react-v3


## Checkpoint

Q1. `async`, `await`, `Promise`について説明してください。

Q2. `TypeScript`における、ジェネリクスとはどういうものでしょうか？

Q3. `const array1 = [1, 4, 9, 16];`をmap関数を用いて、配列の値を3倍にしてください。

参考: https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/map

Q4. 下記の関数をアロー関数を用いて書き直してください。

```
[1, 2, 3].map(function (n) {
  return n + 1;
});
```

Q5. 以下の参考サイトに従い、React、TypeScriptを使って「いいねボタン」「猫画像ジェネレーター」を作ってみましょう。「ESLintでTypeScriptのコーディング規約チェックを自動化しよう」までやってみてください。

参考：https://typescriptbook.jp/tutorials


Q6. Reactを使ってTODOアプリを作ってみてください。

参考: https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_todo_list_beginning

※(注意事項)上記の参考サイトでは、チュートリアルの序盤で以下のように実行するよう指示があります。
```
cd src
rm -- App.test.js App.css logo.svg reportWebVitals.js setupTests.js
```
しかし、実際にこれを実行するとアプリが機能しなくなる可能性があります。`reportWebVitals.js`と`App.css`は削除せず、まずは以下のように実行するのがオススメです。
```
cd src
rm -- App.test.js logo.svg setupTests.js
```

## 次のChapterを始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap4.md)

