# projectmgmt

Web application for simple project management wirtten in Django.

First create a shared docker volume to be shared between both web and nginx containers, so nginx has access to the staticfiles.

docker volume create --name DataVolume1

then, bring prjectmgmt docker containers up first

 sudo docker-compose up -d --build

then, go to nginx dirctory and execute the same 

 sudo docker-compose up -d --build

access the application on http://localhost:1337
