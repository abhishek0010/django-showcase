# django-showcase

A django web app for showcasing its most prominent features and usecases

## Docker Dev Setup

- Create `.env.dev` from `.env.dev.sample` with appropriate modifications
- Run the command

```shell
$ docker compose up -d --build
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
```

## Docker Production setup

- Create `.env.prod` & `.env.prod.db` from samples with appropriate modifications
- Run the command

```shell
$ docker compose -f docker-compose.prod.yml up -d --build
$ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate
$ docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic
$ docker-compose -f docker-compose.prod.yml exec web python manage.py createsuperuser
```
