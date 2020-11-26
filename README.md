# palmin-albert333_microservices
palmin-albert333 microservices repository
## Homework#14
1. Установлен docker-machine (docker уже был)
2. Поднят docker-host в YC, создан и запушен имайдж в docker hub
```
yc compute instance create --name docker-host --zone ru-central1-a --network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 --create-boot-di>
docker-machine create --driver generic --generic-ip-address=<PUB IP> --generic-ssh-user yc-user --generic-ssh-key ~/.ssh/otusyc docker-host
eval $(docker-machine env docker-host)
```
## Homework#13
1. Был скачан архив приложения и созданы Dockerfile в каждом каталоге.

3. Были собраны образы и запущены контейнеры
   ```
   docker run -d --network=reddit --network-alias=post_db --network-alias=comment_db mongo:latest
   docker run -d --network=reddit --network-alias=post albertpalmin1988/post:1.0
   docker run -d --network=reddit --network-alias=comment albertpalmin1988/comment:1.0
   docker run -d --network=reddit -p 9292:9292 albertpalmin1988/ui:1.0
   ```
