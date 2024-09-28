## HelloWorld 

`docker run hello-world`


## Что такое Docker

Docker - сервис для запуска приложений в контейнерах.  

- Приложения запускаются в изолированной среде
- Все зависимости приложений устанавливается внутри контейнеров

## Компоненты Docker

- Image
- Container
- Storage & Volumes
- Networking

## Image

Компоненты Image

- Metadata
- Layers (Слои)
Layer are immutable (Слои не изменяемы доступны только для чтения)
### Show Images (Показать все образы)

```
docker images
```

### Show MetaInfo About Image (Показать метаинфу образа)

```
docker image inspect <id or name>
```


### Download Image (Варианты загрузки образа)

```
docker pull <regisry:optional>/<repository:optional>/<name>:<tag>
```

Примеры различных вариантов загрузки образов:

```
docker pull <image>
```

```
docker pull <image:tag>
```

```
docker pull <userName>/<image:tag>
```

```
docker pull 192.168.0.1:5000/<image>
```

```
docker pull 192.168.0.1:5000/<userName/<image:tag>
```

## Container

## Create Container (Создать контейнер)

```
docker create --name <containerName> <ImageName:tag>
```

### Start Container (Запуск контейнера)

```
docker start <containerName>
```

### Kill and Stop Container (Остановка контейнера Stop - деликатная остановка, Kill- принудительно)

```
docker kill <container>
```

```
docker stop <container>
```

## Remove Container (Удаление. Перед удалением контейнер должен быть остановлен!)

```
docker rm <container>
```

## Перемещение файлов между хост и контейнером

Из хоста в контейнер

```
docker cp <dirOnHost> <containerID>:<path>
```

Из контейнера в хост

```
docker cp <containerID>:<path_on_container> <path_on_host>
```

## Deleting Unused and Stopped Containers

```
docker container prune
```

- [[MySQL Container]]
- [[Postgres Container]]

