# docker_laravel_phpmyadmin_mysqlclient
phpMyAdminとmysql-clientを使えるLaravel環境を作るためのdocker-compose


## 概要
docker-composeを使って最小限のphpMyAdminとmysql-client付きLaravel(LEMP)環境を構築することができます。


## 前提条件
このリポジトリを使う前に、mysqlを使っているLaravelプロジェクトディレクトリを用意してください。

新しいLaravelプロジェクトディレクトリを作る場合は、https://github.com/Asano-Naoki/docker_laravel_minimum の手順に従い、php artisan migrateを実行してください。


## 使い方
docker-composeを開始します。
```
docker-compose up -d
```
http://localhost:8080/ でmysqlデータベースを確認できます。

あるいは、好みに応じて、端末からmysql-clientを使えます。
```
docker-compose exec php sh
...
(after entering sh of php)
...
php artisan db
```
php artisanなしでmysqlに接続することもできます。
```
docker-compose exec php sh
...
(after entering sh of php)
...
mysql -h mysql -u test_user -p
```

## 著者
[浅野直樹](https://asanonaoki.com/blog/)


## ライセンス
MITライセンスの元にライセンスされています。詳細は[LICENSE](/LICENSE)をご覧ください。
