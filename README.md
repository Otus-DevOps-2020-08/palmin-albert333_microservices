# palmin-albert333_microservices
palmin-albert333 microservices repository
## Homework#12
1. Был создан совой образ на базе ubuntu18.04.

2. С помощью docker-machine была запущена ВМ на Yandex.Cloud.

3. Был описан Dockerfile и на его основе создан docker образ.

4. Образ был залит на Docker Hub.

5. Новый docker обрал был развернут на Yandex.Cloud и локально.

## Homework#13

1. Был скачан архив приложения и созданы Dockerfile в каждом каталоге.

3. Были собраны образы и запущены контейнеры
   ```
   docker run -d --network=reddit --network-alias=post_db --network-alias=comment_db mongo:latest
   docker run -d --network=reddit --network-alias=post kvaido/post:1.0
   docker run -d --network=reddit --network-alias=comment kvaido/comment:1.0
   docker run -d --network=reddit -p 9292:9292 kvaido/ui:1.0
   ```

4. Было выполнено задание со звездочкой. Запущены контейнеры с другими сетевыми алиасами.
   ```
   docker run -d --network=reddit --network-alias=my_post_db --network-alias=new_comment_db mongo:latest
   docker run -d --network=reddit --network-alias=post --env POST_DATABASE_HOST=new_post_db albertpalmin1988/post:1.0
   docker run -d --network=reddit --network-alias=comment --env COMMENT_DATABASE_HOST=new_comment_db albertpalmin1988/comment:1.0
   docker run -d --network=reddit -p 9292:9292 albertpalmin1988/ui:1.0

## Homework#14

1. Были изучены сети docker: none, host, bridge.

2. Былз создан и описан docker-compose.

3. Был создан env файл.

4. Выполнено задание со *

## Homework#15
1. Была создана ВМ на Yandex.Cloud с необходимыми параметрами.

2. Был создан docker-compose

3. Были созданы каталоги /srv/gitlab/config, /srv/gitlab/data, /srv/gitlab/logs>
   прописаны в docker-compose.

4. Был настроен Gitlab CI и создан pipeline

## Homework#16

1. Запуск Prometheus

2. Настроен мониторинг микросервисов

## Homework#18

Создал конфиги сервисов reddit для kubernetes

Прошел kubernetes-the-hard-way

##Homework 19
1. Запущен локальный minikube с драйвером VirtualBox
2. Написаны манифесты для деплоя компонентов приложения в кубер
3. Приложение проверено и работает в minikube
4. Развернут кластер кубернетис в Яндекс.Клауд вручную.
5. Развернут кластер кубернетис в Яндекс.Клауд с помощью terraform (для задания со *)
##Homework 20
1. Настроен loadbalancer.
2. Настроен Ingress.
3. Настроен Secret TLS (написан манифест для задания со звездочкой).
4. Настроен NetworkPolicy.
5. Настроен PersistentVolume, PersistentClaim
#Homework 21
1. Установлены и настроены helm, helm2, helm 3.
2. Написаны хелм чарты для деплоя приложения.
3. Изучены, написаны и оттестированы пайплайны для сборки, тестирования и деплоя приложения в гитлабе вн>
4. Пайплайны написаны на разных версиях хелма (непонятно зачем использовать старые хелмы и хелм тиллеры >
5. Для задания со звездочкой в пайпы comment, post, ui добавлен этап trigger_deploy для автоматического >
