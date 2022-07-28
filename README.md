# Postgres-Course

Esta es una pequeña guia acerca de Docker

## Instalación En Linux o Mac Os

```
install docker
```

## Instalación En Windows

Seguir los pasos de instalación de la pagina oficial de Docker

-Recuerda tener Wsl instalado en Windows

```
https://docs.docker.com/desktop/install/windows-install/
```

## Docker Hub

Esta es una página en donde podemos encontrar las imágenes oficiales de las imágenes, con su documentación

```
https://hub.docker.com/
```

# Comandos Docker

![dock](https://user-images.githubusercontent.com/60405554/180707902-256752d1-b4d5-44c0-b4df-4cb0e3684f8a.png)
![dock2](https://user-images.githubusercontent.com/60405554/180707895-58b79d4d-25e4-4b52-8f90-1cef5a9e6bfe.png)
![dock1](https://user-images.githubusercontent.com/60405554/180707903-6528a74f-8d5d-4e3c-8519-b56ac76e5861.png)

## Documentación Docker-Postgresql

```
https://github.com/docker-library/docs/blob/master/postgres/README.md
```

## Descargar la imagen

Este comando nos descargara la última versión disponible de la imagen

```
docker pull postgres
```

Con este comando le asignaremos la versión de la imagen que queremos descargar

```
docker pull postgres:14.4
```

## Ejecutar la imagen descargada de Postgres

Revisar documentación de postgres sobre las varibles de entorno

Obligatoriamente debemos asignar una contraseña

```
docker run -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA postgres
```

Asignar nombre de usuario

```
docker run -e POSTGRES_USER=ASIGNAR_NOMBRE -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA postgres
```

Asignar nombre base de datos

```
docker run -e POSTGRES_USER=ASIGNAR_NOMBRE -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA -e POSTGRES_DB=NOMBRE_DB -d postgres
```

Asignar nombre del contenedor

```
docker run --name NOMBRE_CONTENEDOR -e POSTGRES_USER=ASIGNAR_NOMBRE -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA -e POSTGRES_DB=NOMBRE_DB -d postgres
```

Asignar puerto

```
docker run --name NOMBRE_CONTENEDOR -e POSTGRES_USER=ASIGNAR_NOMBRE -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA -e POSTGRES_DB=NOMBRE_DB -p 5432:5432 -d postgres
```

## Version de Postgres

```
psql --version
```

## Conectarnos a la imagen postgres

```
docker exec -it NOMBRE_IMAGEN bash
```

## Interactuar con Postgres

El usuario por defecto es postgres

```
psql -U USUARIO --password
```

## Listar bases de datos

```
\l
```

## Listar tablas

```
\d
```

## Listar los contenedores

```
docker ps
```

Ver los contenedores en ejecución

```
docker ps -a
```

## Detener contenedor

```
docker stop ID CONTENEDOR O NOMBRE CONTENEDOR
```

## Eliminar contenedores

```
docker rm ID CONTENEDOR O NOMBRE CONTENEDOR
```

## Eliminar imagen

```
docker rmi ID IMAGEN
```

## Levantar imagen en un Docker compose

```
docker compose up
```
