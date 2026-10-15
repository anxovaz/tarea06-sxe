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

![compose-up](./imgs/compose-up.png)

Después accedemos a `localhost:8080` en un navegador web.

Después accedemos a `localhost:8080` en un navegador web y creamos nuestro primer sitio.

![inicio](./imgs/inicio.png)

## Objetivos

### Inventario

Para crear un inventario primero hay que crear los productos y el almacén, para ello accedemos a la sección `Item` y creamos un nuevo producto llamado `Rueda` con id `001`, para el Almacén lo creamos en la sección `Warehouse`, una vez terminamos de crear el producto y el almacén accedemos a la sección `Stock Entry` y creamos una entrada de la siguiente forma:

![stock](./imgs/stock.png)

### Proveedores

Para crear un proveedor accedemos a la sección `Supplier` y en este caso creamos un Bazar Chino.

![supplier](./imgs/supplier.png)

### Clientes

Para crear una ficha de cliente entramos a la sección `Customer list`:

![customer](./imgs/customer.png)
