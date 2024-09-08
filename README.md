
<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

<p align="center">  
  <a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
  <a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
  <a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
  <a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
  <a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
  <a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
  <a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
  <a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>

## Descripción

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

---

# API Florista - Instrucciones de Configuración y Uso

Este proyecto es una API diseñada para la gestión de un catálogo de productos y la administración de pedidos en un vivero o tienda de flores. La API está construida con **NestJS** y utiliza **MongoDB** como base de datos.

## Requisitos Previos

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos en tu entorno de trabajo:

1. **Node.js**: Versión `18.16.0` o superior.  
   - [Descargar Node.js](https://nodejs.org/)
   
2. **npm**: Instalado junto con Node.js.  
   - Puedes verificar la instalación con los siguientes comandos:
   
   ```bash
   node -v
   npm -v
   ```
   
3. **MongoDB**: Base de datos NoSQL. Puedes instalar MongoDB localmente o utilizar **MongoDB Atlas** (una versión de MongoDB en la nube).  
   - [Instalar MongoDB local](https://docs.mongodb.com/manual/installation/)  
   - [Registro en MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

---

## Instrucciones para levantar el proyecto

### Paso 1: Clonar el repositorio

Clona el repositorio del proyecto en tu máquina local.

```bash
git clone https://github.com/usuario/api-florista.git
cd api-florista
```

### Paso 2: Instalar dependencias

Antes de ejecutar el proyecto, es necesario instalar todas las dependencias. Esto se hace con el siguiente comando:

```bash
npm install
```

Este comando leerá el archivo `package.json` e instalará todas las dependencias necesarias para que el proyecto funcione correctamente.

### Paso 3: Configuración del archivo `.env`

El proyecto utiliza un archivo de variables de entorno llamado `.env`. Este archivo contiene configuraciones sensibles como la conexión a la base de datos y el puerto del servidor, entre otros.

Crea un archivo llamado `.env` en la raíz del proyecto.  
Copia y pega el siguiente contenido en el archivo `.env`:

```bash
# Configuración del puerto de la aplicación
PORT=3000

# Conexión a la base de datos MongoDB
MONGODB_URI=mongodb://localhost:27017/florista

# Otras configuraciones
NODE_ENV=development
```

### Paso 4: Levantar la base de datos MongoDB

#### Para MongoDB Local:

- Asegúrate de tener MongoDB instalado en tu sistema.  
- Ejecuta el servicio de MongoDB en tu máquina:

```bash
mongod
```

Esto ejecutará MongoDB en el puerto `27017` de tu máquina local.

#### Para MongoDB Atlas:

- Regístrate en MongoDB Atlas.
- Crea un clúster de base de datos.
- Obtén la URI de conexión de tu clúster y reemplaza el valor de `MONGODB_URI` en tu archivo `.env` con esa URI.

```bash
MONGODB_URI=mongodb+srv://<usuario>:<password>@cluster.mongodb.net/floristaDB?retryWrites=true&w=majority
```

Reemplaza `<usuario>` y `<password>` con tus credenciales.

### Paso 5: Ejecutar la aplicación

Con la base de datos funcionando y el archivo `.env` correctamente configurado, puedes ejecutar el proyecto. Existen varios modos de ejecución:

#### 1. Modo Desarrollo (recomendado para desarrollo):

Este modo recarga automáticamente el servidor cada vez que detecta cambios en el código. Para ejecutar en este modo, usa el siguiente comando:

```bash
npm run start:dev
```

El proyecto estará disponible en [http://localhost:3000](http://localhost:3000).

#### 2. Modo Producción (para despliegue en producción):

Para ejecutar la aplicación en modo producción, primero debes compilarla y luego ejecutarla:

```bash
npm run build
npm run start:prod
```

En este modo, se usa la versión optimizada para producción.

#### 3. Otros modos de ejecución:

- **Modo observador (watch mode)**:
  
  ```bash
  npm run start:dev
  ```

- **Modo depuración (debug mode)**:
  
  ```bash
  npm run start:debug
  ```

---

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest
