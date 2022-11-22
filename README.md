### Change docker-compose.yml
- Line 6 to your current linux username
- Line 8 to Php version you want
- Line 22 to Mysql version you want

### Run Docker Compose UP and Build if you change something in yml file.
- docker-compose build && docker-compose up -d

### Create a laravel project in root folder
- docker-compose exec app composer create-project --prefer-dist laravel/laravel .

### Change Permission root folder ->
#### 7 - Owner can write
#### 7 - Group can write
#### 5 - Others cannot write!
- sudo chmod -R 775 .

### Run Command in /src/storage
- sudo chown -R www-data:www-data .

### Change .env file to
- DB_CONNECTION=mysql
- DB_HOST=db
- DB_PORT=3306
- DB_DATABASE=homestead
- DB_USERNAME=homestead
- DB_PASSWORD=secret

### Phpmyadmin Access
- Server: host.docker.internal
- Username: homestead
- Password: secret
