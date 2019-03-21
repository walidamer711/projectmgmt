# projectmgmt

Web application for simple project management wirtten in Django.

First create a shared docker volume to be shared between both web and nginx containers, so nginx has access to the staticfiles.

```shell
docker volume create --name DataVolume1
```
then, bring prjectmgmt docker containers up first
```shell
 sudo docker-compose up -d --build
```
then, go to nginx dirctory and execute the same 
```shell
 sudo docker-compose up -d --build
```
access the web container and execute migartions and user creation
```shell
docker exec -it projectmgmt_web_1 /bin/bash

python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```
access the application on http://localhost:1337
