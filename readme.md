<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>


# Run here

    docker-compose up -d

wait 5 minute, check i success `docker ps`

    docker-compose exec app composer dump-autoload
    docker-compose exec app php artisan key:generate
    docker-compose exec app php artisan config:cache
    docker-compose exec app composer install

Fix user root for database

    docker-compose exec app db
    mysql -p

password: vnutour2022

    ALTER USER 'root'@'%' IDENTIFIED WITH 'mysql_native_password' BY 'vnutour2022';

    docker-compose exec app npm install
    docker-compose exec app npm run watch
    docker-compose exec app chmod -R gu+w storage
    docker-compose exec app chmod -R guo+w storage
    docker-compose exec app php artisan cache:clear