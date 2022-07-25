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
-Ejemplo

```
docker pull postgres:14.4
```

## Ejecutar la imagen descargada de Postgres

Revisar documentación de postgres sobre las varibles de entorno

```
docker run -e POSTGRES_PASSWORD=ASIGNAR_CONTRASEÑA postgres
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
