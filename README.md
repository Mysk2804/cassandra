Запуск Docker-compose
~~~
docker-compose up -d
~~~
Проверка сети Docker
~~~
docker network ls
~~~
Проверка назначеных IP
~~~
docker network inspect cassandra_mynetwork
~~~
Запуск cqlsh 
~~~
docker run -it --network cassandra_mynetwork --rm cassandra cqlsh cas1
~~~
Для проверки IP адресса в контейнере заходим в bash 
~~~
docker exec -i -t cas1 bash
~~~
Устанавливаем зависимости
~~~
apt update & apt install iputils-ping -y
~~~
Пингуем остальные сервера
~~~
ping 10.5.0.6
~~~