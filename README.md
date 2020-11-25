# palmin-albert333_microservices
palmin-albert333 microservices repository

## Homework#12

1. Был создан совой образ на базе ubuntu18.04.

2. С помощью docker-machine была запущена ВМ на Yandex.Cloud.

3. Был описан Dockerfile и на его основе создан docker образ.

4. Образ был залит на Docker Hub.

5. Новый docker обрал был развернут на Yandex.Cloud и локально.

## Homework#13

1. Был установлен linter - hadolint.

2. Был скачен архив приложения и созданы Dockerfile в каждом каталоге.

3. Были собраны образы и запущены контейнеры
   ```
   docker run -d --network=reddit --network-alias=post_db --network-alias=comme>
   docker run -d --network=reddit --network-alias=post albertpalmin1988/post:1.0
   docker run -d --network=reddit --network-alias=comment albertpalmin1988/comment:1.0
   docker run -d --network=reddit -p 9292:9292 albertpalmin1988/ui:1.0
   ```
