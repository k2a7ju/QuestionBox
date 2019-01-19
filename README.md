# 概要
質問箱丸パクリ
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
