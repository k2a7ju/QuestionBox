# 概要
プログラム勉強用
# 実行方法
## Docker
### コンテナ起動
```
$ docker-compose build
$ docker-compose up -d
```
### コンテナ停止
```
$ docker-compose stop
```
## DB 関連
### phpmyadmin接続
`http://localhost:8080/`へアクセス
### mysql接続(root)
```
$ mysql -uroot -P3306 -h127.0.0.1 -p
```
## アプリケーション
### Dockerコンテナ内にssh
```
$ docker-compose exec php bash
```
### 初期設定（Dockerコンテナ内で）
```
$ composer install
$ cp .env.example .env
$ php artisan key:generate
$ php artisan migrate
```
`http://localhost:8000/`へアクセス
