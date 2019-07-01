# {{ project_name }}

## Usage
```bash
django-admin startproject \
  --template https://github.com/Compeito/django-docker-template/archive/master.zip \
  --extension=env,md \
  {{ project_name }}
cd {{ project_name }}
mv example.env .env
docker-compose build
docker-compose run web pipenv install --dev
docker-compose up -d
```
