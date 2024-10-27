# Как я запустил Redis в Docker и подключился к нему

## Шаги

1. Попытка подключиться к Redis:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run -it --network some-network --rm redis redis-cli -h some-redis
    docker: Error response from daemon: network some-network not found.
    ```

2. Создание и запуск Redis сервера:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run --name some-redis -d redis redis-server --save 60 1 --loglevel warning
    docker: Error response from daemon: Conflict. The container name "/some-redis" is already in use by container "51f5867cfdfee18d999b15a8ad8962b9382613af027d42c2ed58e43375338257". You have to remove (or rename) that container to be able to reuse that name.
    See 'docker run --help'.
    ```

    Перезапуск Redis сервера:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run --name some-redis -d redis redis-server --save 60 1 --loglevel warning
    df8ddca9d1556000e06937a7fceeee22b90f5e07f8484a4f668c4e8167474981
    ```

3. Создание сети Docker:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker network create some-network
    feb05d3227d2117ee169438e7d169a22d9598a6082a967b695233e2f15be4185
    ```

4. Попытка подключения к Redis через созданную сеть:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run -it --network some-network --rm redis redis-cli -h some-redis
    docker: Error response from daemon: network some-network not found.
    ```

5. Запуск Redis в созданной сети:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run -d --name some-redis --network some-network redis
    docker: Error response from daemon: Conflict. The container name "/some-redis" is already in use by container "df8ddca9d1556000e06937a7fceeee22b90f5e07f8484a4f668c4e8167474981". You have to remove (or rename) that container to be able to reuse that name.
    See 'docker run --help'.
    ```

    Перезапуск Redis в созданной сети:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run -d --name some-redis --network some-network redis
    82e862d5add57013c49a6f1e3d8821b167d305f0fc29e51ecd9c04bb635799a9
    ```

6. Подключение к Redis и проверка его работы:

    ```bash
    sayan@sayan-HP-ENVY-x360-Convertible-15-eu0xxx:~$ docker run -it --network some-network --rm redis redis-cli -h some-redis
    some-redis:6379> ping
    PONG
    some-redis:6379> 
    ```

## Заключение

Теперь Redis работает и доступен через указанную сеть Docker.
#redis #docker #redis-connection #redis-cli