# Prueba API REST de Indra

Este proyecto es un servicio API desarrollado con  tecnologias Serverless, Express, TypeScript y MySQL.

## Requisitos Previos

La base de datos está creada para el despliegue de aws. Si deseas probar el proyecto en local, debes tener acceso a la base de datos existente o crear tu propia base de datos. Para ello, ejecuta el script SQL db.sql que se encuentra en la raíz del proyecto en tu base de datos.

Asegúrate de añadir un archivo .env con las variables de entorno basadas en el archivo de ejemplo .env-example.

### Variables de entorno

- `DB_MYSQL`: URL de conexión a la base de datos MySQL

 - DB_MYSQL=mysql://root:@localhost:3306/backend-indra

- `SW_URL_API`: URL de la API de Star Wars

 - SW_URL_API=https://swapi.py4e.com/api

### Elementos necesarios
Asegúrate de tener instalados los siguientes elementos antes de ejecutar la aplicación:
- Node.js v20
- npm o yarn
- serverless


## Configuración

1. **Clona el repositorio:**

   ```bash
   git clone https://github.com/joseyzambranov/backend-indra.git
   cd backend-indra
   ```

2. **Instala las dependencias:**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno:**

   Renombra el archivo .env-example a .env y añade la URL de tu base de datos MySQL o coloca la base de datos ya creada.

 **Ejecutar entorno de desarrollo:**
   ```bash
   npm run dev
   ```

 **Ejecutar entorno de desarrollo serverless:**
   ```bash
   npm run serverless:dev
   ```
   
 **Deploy con serverless:**
   ```bash
   npm run serverless:deploy
   ```

 **Test unitario:**
   ```bash
   npm run test
   ```   


## Endpoints

Base url
- local: http://localhost:4000/dev
- production: https://jv5hgpshn9.execute-api.us-east-1.amazonaws.com/dev

### `GET /dev/api/swapi`

Este endpoint proporciona una lista de personajes.

Ejemplo:

```bash
curl http://localhost:4000/dev/api/swapi
```

### `GET /dev/api/user`

Este endpoint proporciona una lista de usuarios.

Ejemplo:
```bash
curl http://localhost:4000/dev/api/user
```
### `POST /dev/api/user`

Este endpoint crea un nuevo usuarios.

Ejemplo:
```bash
curl http://localhost:4000/dev/api/user