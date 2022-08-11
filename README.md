# api_development_template

Rails開発テンプレ

```
docker-compose run --rm frontend npm install
```

## frontend
```
docker-compose run --rm front yarn create next-app .
```

## backend
backend/.env
```
SECRET_KEY=xxxx
DEBUG=True
```

## start containers
```
docker-compose up -d
```
* frontend
  * http://localhost:3000/
* backend
  * http://localhost:8000/
