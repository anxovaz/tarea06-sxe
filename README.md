# Tarea 6 - Propuesta de solución de gestión

## Integrantes 

- Anxo Vázquez 

- Antón Seoane

- Edwyn Lezama

## Sistema escogido

El sistema escogido para este proyecto que más se amolda a las necesidades del escenario escogido es `ERP NEXT`.

![logo](./imgs/logo.png)

## Escenario

- Bicis Damián

> Para información más detallada mira la capeta `Docs`

## Despliegue

Utilizamos el archivo `pwd.yml` del repositorio de `frappe-docker` y modificamos únicamente los atributos que están en el `.env.example` para que los recoja por variables de entorno.

Después de tener nuestro archivo `.env` y el `compose.yml` actualizado lo desplegamos con `docker compose up -d`.

```
source .env

docker compose up -d

docker compose logs -f create-site # mira los logs de el contenedor encargado de crear el sitio y esperamos a que finalice

```

Después accedemos a `localhost:8080` en un navegador web.

Después accedemos a `localhost:8080` en un navegador web y creamos nuestro primer sitio.

![inicio](./imgs/inicio.png)

