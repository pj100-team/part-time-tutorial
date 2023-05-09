#　Infrastructure

## ネットワークのキホンのキ

ネットワークに関しては、以下の記事に書かれている単語の意味がわかるようになると良いです。

https://masassiah.web.fc2.com/contents/20ap/note10.html

一つ一つ調べていきましょう！

本であれば[マスタリングTCP/IP](https://www.amazon.co.jp/%E3%83%9E%E3%82%B9%E3%82%BF%E3%83%AA%E3%83%B3%E3%82%B0TCP-IP%E2%80%95%E5%85%A5%E9%96%80%E7%B7%A8%E2%80%95-%E7%AC%AC6%E7%89%88-%E4%BA%95%E4%B8%8A-%E7%9B%B4%E4%B9%9F/dp/4274224473/ref=asc_df_4274224473/?tag=jpgo-22&linkCode=df0&hvadid=342397001181&hvpos=&hvnetw=g&hvrand=10440745021831075600&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1009507&hvtargid=pla-847853186623&psc=1&th=1&psc=1&tag=&ref=&adgrpid=72867581430&hvpone=&hvptwo=&hvadid=342397001181&hvpos=&hvnetw=g&hvrand=10440745021831075600&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1009507&hvtargid=pla-847853186623)が非常によくまとまっているのでおすすめです。


## Checkpoint1

Q1. 以下の用語について説明してください。

- IPアドレス(IPv4)
- `127.0.0.1`と`0.0.0.0`アドレスの意味
- IPアドレスとポート番号の違い
- HTTP, HTTPS, SSH　それぞれのウェルノウンポート
- DNSの仕組み
- Aレコード、CNAME

Q2. IPアドレスが 172.16.255.164，サブネットマスクが 255.255.255.192 であるホストと同じサブネットワークに属するホストのIPアドレスはどれか。

1. 172.16.255.128
2. 172.16.255.129
3. 172.16.255.191
4. 172.16.255.192

## コンテナ技術(Docker)

以下の公式資料がわかりやすいです。

https://docs.docker.jp/get-started/index.html

## Chceckpoint2

Q1. Dockerイメージとコンテナの違いは何でしょうか？お互いはどういう関係でしょうか？

Q2. ホストPCの意味とは？

Q3. Dockerを使って`postgresql`のDBコンテナを立てて、接続してみましょう

参考: https://qiita.com/zaburo/items/7ab51a7a4d9e1b2d1ec4

## AWSキホンのキ

インフラではAWSを使用することが多いです。
こちらでまとまっている、公式の資料を見ると良いです。

https://qiita.com/toma_shohei/items/b7a001d26bd988d52021

概念やサービスの名前を知っていることが大事です。
特に`IAM`などは必須です。


