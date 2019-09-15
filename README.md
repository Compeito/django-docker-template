# {{ project_name }}

## Usage
```bash
django-admin startproject \
  --template https://github.com/Compeito/django-docker-template/archive/master.zip \
  --extension=env,md \
  {{ project_name }}
cd {{ project_name }}
```

## Setup
```bash
# 必要に応じて環境変数を変更
$ mv .env.example .env
$ vim .env

# Dockerイメージの作成
$ docker-compose build web

# パッケージのインストールとデータベースのマイグレーション
$ docker-compose run web pipenv install --dev
$ docker-compose run web python manage.py migrate
```

## Development
```bash
# Pipfileのdevコマンドで開発サーバーを起動
$ docker-compose run -p 8080:8080 web dev
```
