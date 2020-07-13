# Rails6 Quick Starter

---

## 概要

Docker-compose を利用した Rails6 のクイックスタートパッケージです。
React の webpack も bash スクリプト（qs/quick-starter）で対応しております。

## 構成

Ruby 2.6（初期）
Rails 6.0 以上
PostgresSQL

## インストール手順

先に Docker をインストールして下さい。
[Docker](https://docs.docker.com/install/)

## リポジトリのクローン

下記コマンドを打ち込み GitHub よりクローンしてください。

```
git clone -b rails6  <Project name>
cd <Project name>
```

## セットアップ

下記コマンドを打つだけです。
＊bash スクリプトが走ります。

```
./qs setup
```

React を使用される場合は下記で行ってください。

```
./qs setup -T --webpack=react
```

ローカルホスト 3000 番にアクセスしてみてください。
`http://localhost:3000`
Rails が立ち上がるはずです。

---

## 他のセットアップ可能パッケージ

### Spring service

最初に `./qs up spring` のコマンドを打ってください。
次に下記のコマンドを打ってください。
`./qs spring rails c`, `./qs spring rails db:migrate`.

### Solargraph service

gem ファイルを追加後に bundle し、up してください。
`gem 'solargraph', group: :development`
`./qs bundle install`
`./qs up solargraph`

### Redis service

下記コマンドを打ってください。
`./qs up redis`

### Chrome service

下記コマンドを打ってください。
`./qs up chrome`
