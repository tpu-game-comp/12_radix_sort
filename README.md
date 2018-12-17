# 基数ソートの演習

# 進め方
## はじめてのとき
* [GitHub](https://github.com/)のアカウントを作成してください
* [Travis CI](https://travis-ci.org/) のアカウントを作成してください
* GitHubのアカウントを[こちらのフォーム](https://goo.gl/forms/anAdoxqPKVt8sJGZ2)から教えてください。
## 毎回の進め方
* このリポジトリをforkしてください
* Travis CI を設定して、自動ビルドが通るようにしてください
   * Travis CI のGitHubアカウントでの登録とforkしたリポジトリをTravisCI側で許可する
   * 参考サイト：[Travis CIで自動テストして、結果をGitHubのトップページに表示する](https://qiita.com/hoshimado/items/4090d8e64beb8a7f95e1)
* forkしたリポジトリの README.md ファイルの「t-kougei-game-comp」の部分を自分のGitHubアカウント名に差し替えてください(2箇所)
* 問題を解いて、テストを通るようにしてください。
* fork 元の master ブランチにプルリクエストを投げてください

# テスト結果

[![Build Status](https://travis-ci.org/t-kougei-game-comp/12_radix_sort.svg?branch=master)](https://travis-ci.org/t-kougei-game-comp/12_radix_sort)

# 今回の問題

基数ソートの勉強です。

入力される数字群を基数ソートで整列してください。

input?.txt ファイルを標準入力として読み込んで、標準出力の結果を output?.txt ファイルと一致するか比較するテストをします。

main.c ファイルだけを書き換えて下さい。

## 入力される値
入力は以下のフォーマットで与えられます。
~~~
n
n
n
~~~

nは数字です。

## 期待する出力

全ての入力を読み込んだ後、入力順に空白で区切って出力してください。
その後、基数ソートを行ってください。

ソート時は、各桁ごとにソートを終えた時点で、並び替え後の数字の列を空白区切りで表示してください。

最後は改行し、余計な文字、空行を含んではいけません。

## 条件
基数は10とします。

すべてのテストケースで数字は以下の条件を満たします。
* 0 <= n <= 1000

入力される行数は100行以内とします。

## 入力例1
~~~
013
022
012
~~~

## 出力例1
~~~
013 022 012
022 012 013
012 013 022
012 013 022
~~~
* 1行目がソート前の状態です
* 2行目が1の位で並び替えた結果になります
* 3行目が10の位で並び替えた結果になります
* 4行目が100の位で並び替えた結果になります。100の位の数字は全て等しいので、前の行と同じ結果です

## 入力例2
~~~
123
231
312
213
132
321
~~~

## 出力例2
~~~
123 231 312 213 132 321
231 321 312 132 123 213
312 213 321 123 231 132
123 132 213 231 312 321
~~~
