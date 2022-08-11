# api_development_template

Rails開発テンプレ

## frontend
```
$ docker-compose run --rm front npm install
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
