# api_development_template

Rails開発テンプレ

```
$ docker-compose run --rm frontend npm install
```

## frontend
```
$ docker-compose run --rm front yarn create next-app .
```

## backend
$ docker-compose run --rm api bundle exec rails new . --api -d mysql
```

## api/config/database.ymlを書き換え
```api/config/database.yml
default: &default
  adapter: postgresql
  encoding: unicode
  username: root←ここを追加
  password: password←ここを追加
  host: db←ここを追加

  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>

development:
  <<: *default
  database: postgres←ここを変更
```

## start containers
```
$ docker-compose up -d
```
imageを書き換えて更新したいとき
```
$ docker-compose up -d --build
```

* frontend
  * http://localhost:3000/
* backend
  * http://localhost:8000/
