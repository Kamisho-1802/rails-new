# rails-new

Ruby on Rails 8 のテンプレートプロジェクトです。

## 使用技術

|カテゴリ   |技術                                                      |
|-------|--------------------------------------------------------|
|言語     |Ruby                                                    |
|フレームワーク|Ruby on Rails 8.0.2                                     |
|データベース |SQLite3                                                 |
|Webサーバー|Puma                                                    |
|フロントエンド|Propshaft / importmap-rails / Hotwire (Turbo + Stimulus)|
|デプロイ   |Kamal / Docker                                          |
|テスト    |Capybara / Selenium WebDriver                           |
|コード品質  |RuboCop (rubocop-rails-omakase) / Brakeman              |

## 必要な環境

- Ruby（`.ruby-version` ファイルに記載のバージョン）
- Bundler
- SQLite3

## セットアップ

```bash
# リポジトリをクローン
git clone https://github.com/Kamisho-1802/rails-new.git
cd rails-new

# gemのインストール
bundle install

# データベースの作成・初期化
bin/rails db:create
bin/rails db:migrate

# サーバーの起動
bin/rails server
```

ブラウザで `http://localhost:3000` にアクセスして動作を確認してください。

## テストの実行

```bash
# 全テストを実行
bin/rails test

# システムテストを実行
bin/rails test:system
```

## Dockerを使った起動

```bash
# イメージのビルド
docker build -t rails-new .

# コンテナの起動
docker run -p 3000:3000 rails-new
```

## デプロイ

このプロジェクトは [Kamal](https://kamal-deploy.org) を使ったデプロイに対応しています。

```bash
kamal deploy
```

## ディレクトリ構成

```
rails-new/
├── app/          # アプリケーションのコア（MVC）
├── bin/          # 実行スクリプト
├── config/       # 設定ファイル
├── db/           # データベース関連
├── lib/          # タスクなど
├── public/       # 静的ファイル
├── test/         # テストコード
├── Gemfile       # gem依存関係
└── Dockerfile    # Dockerの設定
```
