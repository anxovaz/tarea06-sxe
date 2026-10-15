# `Compose`

El archivo `compose.yaml` está dividido en estas partes:

- **backend**: ejecuta el servidor principal para procesar solicitudes web. 

- **configurator**: configura los ajustes y genera un archivo de configuración antes de iniciar los servicios.

- **create-site**: el encargado de crear el sitio inicial una vez ya está todo desplegado.

- **db**: la base de datos que utiliza ERPNEXT (mariadb)

- **frontend**: funciona como un servidor web (nginx) y proxy inverso para enrutar el tráfico web.

- **queue-long**: utiliza las colas de Redis para procesar tareas y trabajos de larga duración. 

- **queue-short**: lo mismo que `queue-long` pero para tareas de corta duración.

- **redis-queue**: intermediario que administra colas de tareas asíncronas.

- **redis-cache**: proporciona almacenamiento en caché.

- **scheduler**: gestiona tareas programadas y eventos del sistema. 

- **websocket**: socket que administra la comunicación bidireccional en tiempo real.

Usando los siguientes volúmenes:

- **db-data**: usado por mariadb

- **redis-queue-data**: usado por `redis`

- **sites**: donde se almacenan los sitios.

- **logs**: logs del `ERP`

Y la siguiente red:

- frappe_network: tipo bridge
