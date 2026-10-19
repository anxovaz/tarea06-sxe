# Preparativos

Modifica tu `.env` a tu gusto o simplemente usa el `.env.example` en el repositorio.

```
mv .env.example .env
```

Asegúrate de tener `docker` funcionando en tu equipo.

# Ejecución

Lanza el compose con el siguiente comando.

```
docker compose up -d
```

## Espera a que finalice la instalación de `Frappe` y `ERP NEXT`.

```
docker compose logs -f create-site
```

# Acceso

Accede a `localhost:8080` en tu navegador web de confianza e introduce como usuario `Administrator` y `admin` de contraseña.

# Parar

```
docker compose down -v #-v borra todos los datos del erp ya que borra los volúmenes, omitir si no se necesita
```
