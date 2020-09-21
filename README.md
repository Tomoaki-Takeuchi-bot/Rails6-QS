# Rails6 Quick Starter

## 概要

Docker-compose を利用した Rails6 のクイックスタートパッケージです。<br>
React の webpack も bash スクリプト（qs/quick-starter）で対応しております。

---

## 構成

- Ruby 2.7
- Rails 6.0 以上
- PostgreSQL

---

## インストール手順

先に Docker をインストールして下さい。<br>
[Docker](https://docs.docker.com/install/)

## リポジトリのクローン

下記コマンドを打ち込み GitHub よりクローンしてください。

```
git clone https://github.com/Tomoaki-Takeuchi-bot/Rails6-QS.git <Project name>
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

## 開発時の対応方法

- gem update 時
  gem によっては再起動処理が必要なものもあります。<br>
  その際は `docker-compose down` でコンテナダウンさせ<br>
  `docker-compose up -d web db` で web, db 等のサービスを指定し<br>
  立ち上げしてください。

- 中断時
  `docker-compose stop` で OK です。

- 再開時
  `docker-compose start` で OK です。

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
