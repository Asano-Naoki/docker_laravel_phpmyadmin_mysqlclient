[日本語版 README はこちら](/README_ja.md)

# docker_laravel_phpmyadmin_mysqlclient
docker-compose for Laravel with phpMyAdmin and mysql-client

## Summary
You can create minimum Laravel(LEMP) environment with phpMyAdmin and mysql-client using docker-compose.

## Prerequisites
Before using this repository, prepare your Laravel project directory using mysql.

If you'd like to create a new one, follow the direction at https://github.com/Asano-Naoki/docker_laravel_minimum and execute php artisan migrate command

## Usage
Start docker-compose.
```
docker-compose up -d
```
And you can check your mysql database at http://localhost:8080/

Or you can use mysql-client from the teminal if you prefer.
```
docker-compose exec php sh
...
(after entering sh of php)
...
php artisan db
```
You can also connect mysql without php artisan.
```
docker-compose exec php sh
...
(after entering sh of php)
...
mysql -h mysql -u test_user -p
```

## Author
[Asano Naoki](https://asanonaoki.com/blog/)


## License
Under the MIT License. See [LICENSE](/LICENSE) for details.
