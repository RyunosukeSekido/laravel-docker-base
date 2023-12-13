# laravel-docker-base

## 概要

Laravel+Docker環境（nginx, MySQL）でwebアプリケーションを構築する際のベースとして使用できます。

## 使い方
1. リポジトリのクローン
```
git clone https://github.com/RyunosukeSekido/laravel-docker-base.git
```

2. Dockerをビルド
```
docker compose up -d
```
以降のコマンドはappコンテナに入って実行します。
```
docker compose exec app bash
```

3. エラーログを書き込むための権限変更
```
chmod -R 777 storage bootstrap/cache
```
4. プロジェクトの依存関係をインストール
```
composer install
```

5. envファイルの作成
```
cp .env.example .env
```
6. アプリケーションキーの作成
```
php artisan key:generate
```

7. シンボリックリンクの作成
```
php artisan storage:link
```

8. マイグレーション
```
php artisan migrate
```

上記の手順で、[http://localhost:8080/](http://localhost:8080/)にアクセスすると、
Laravelのウェルカムページが表示されます。
