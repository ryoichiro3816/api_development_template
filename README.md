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
```
$ docker-compose run --rm api bundle exec rails new . --api -d mysql
```

## api/config/database.ymlを書き換え
```api/config/database.yml
default: &default
  adapter: postgresql
  encoding: unicode
```diff_ruby
+ username: root
+ password: password
+ host: db
```
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>

development:
  <<: *default
```diff_ruby
- database: app_development  
+ database: postgres
```
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
