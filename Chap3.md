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

TypeScript(TS)とは、JavaScriptに型がついた言語です。
普段の開発ではTypeScriptを使用することが多いので、マスターしましょう！

### TypeScriptチュートリアル①
TypeScriptの基本的な文法を以下の資料を読んで理解しましょう。

[読んで学ぶTypeScript](https://typescriptbook.jp/reference)

中でも、初心者が理解しておくべき点は以下のページです。

- [変数宣言: letとconst](https://typescriptbook.jp/reference/values-types-variables/let-and-const)
- [varはもう使わない](https://typescriptbook.jp/reference/values-types-variables/vars-problems)
- [変数宣言の型推論](https://typescriptbook.jp/reference/values-types-variables/type-inference)
- [boolean型 (論理型)](https://typescriptbook.jp/reference/values-types-variables/boolean)
- [number型 (数値型)](https://typescriptbook.jp/reference/values-types-variables/number)
- [string型 (文字列型)](https://typescriptbook.jp/reference/values-types-variables/string)
- [配列の型注釈 (type annotation)](https://typescriptbook.jp/reference/values-types-variables/array/type-annotation-of-array)
- [配列をループする方法](https://typescriptbook.jp/reference/values-types-variables/array/how-to-loop-an-array)
- [配列のスプレッド構文「...」(spread syntax)](https://typescriptbook.jp/reference/values-types-variables/array/spread-syntax-for-array)
- [アロー関数 (arrow function)](https://typescriptbook.jp/reference/functions/arrow-functions)
- [戻り値がない関数とvoid型 (void type)](https://typescriptbook.jp/reference/functions/void-type)
- [Promise<T>](https://typescriptbook.jp/reference/asynchronous/promise)
- [async](https://typescriptbook.jp/reference/asynchronous/async)
- [await](https://typescriptbook.jp/reference/asynchronous/await)

チュートリアルを100％理解することは難しいので、程々にして次に進みましょう。

### TypeScriptチュートリアル②

上のチュートリアルで、TypeScriptのおおまかなルールを理解できたかと思います。

ここでは改めて、[こちらの記事](https://typescript-jp.gitbook.io/deep-dive/type-system)で紹介されている型システムを把握できているか、確認してみましょう。


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

- [] [日本語版](https://ja.react.dev/learn)


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


## 次のChapterを始める前に

本リポジトリを`clone`して,改善点を見つけて`Pull Request`(以下、PRと省略)を出しましょう！
どんな些細なPRでも構いません！:pray:
改善点の`Pull Request`が出されたら、本Chapterのフィードバックと次Chapterのプランを作成するための面談をセットするので改善点の`Pull Request`はどんな内容でもいいので必ず出してください！

[Go to Next Chapter](/Chap4.md)

