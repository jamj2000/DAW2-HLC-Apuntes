# Desarrollo FullStack


## INTRODUCCIÓN

El desarrollo de una Aplicación Web FullStack abarca:

- **BackEnd**
- **FrontEnd**

El Backend es la parte de la aplicación encargada de atender las peticiones HTTP que realiza la parte Frontend de la aplicación así como otros clientes web.

Básicamente el Backend es un servidor HTTP. Además de atender las peticiones de los clientes, el backend también se encarga a menudo de acceder al SGBD que proporciona persistencia de los datos.

El Frontend presenta al usuario la información obtenida del backend, así como proporciona a dicho usuario una interfaz para interactuar con la aplicación.

En proyectos grandes suelen existir puestos laborales específicos para:

- **Desarrollador Backend**
- **Desarrollador Frontend**

No obstante en algunos casos y en ciertos perfiles profesionales puede solicitarse a alguien con conocimientos en ambos cambos. En este caso el perfil es:

- **Desarrollador Fullstack**


## INSTALACIÓN DE SERVIDOR DE BASE DE DATOS (MONGODB)

MongoDB es una base de datos noSQL muy usada actualmente. Se integra muy bien con las aplicaciones escritas en Javascript.





### Operaciones CRUD

| Operación CRUD  | Equivalente HTTP | Equivalente SQL | MongoDB        | Mongoose                                 |
|-----------------|------------------|-----------------|----------------|------------------------------------------|
| C (Create)      | POST             | INSERT          | insert         | objeto.save                              |         
| R (Read)        | GET              | SELECT          | find           | Modelo.find   / Modelo.findOne           |
| U (Update)      | PUT              | UPDATE          | update         | Modelo.update / Modelo.findOneAndUpdate  |
| D (Delete)      | DELETE           | DELETE          | remove         | Modelo.remove / Modelo.findOneAndRemove  |



## INSTALACIÓN DE NODE.JS

```bash 
curl  -sL  https://deb.nodesource.com/setup_10.x  |  sudo  -E  bash  -
sudo  apt-get  install  -y  nodejs  build-essential
```

> Referencia: 
> -  https://github.com/nodesource/distributions  (Distribución de binarios desde NodeSource)


## INICIANDO PROYECTO

```bash
mkdir  proyecto  &&  cd  proyecto
npm  init  --yes
```

**Archivo `package.json`**

```json
{
  "name": "proyecto",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": ["fullstack", "node", "express"],
  "author": "José Antonio Muñoz Jiménez",
  "license": "ISC"
}

```

**Archivo `index.js`**

```js
const express = require('express');
const app     = express();

app.listen (3000);
```

**Instalamos módulo `express` e iniciamos aplicación.**

```bash
npm  install  express
npm  start
```

**Añadimos callback en función `app.listen()`**

```js
const express = require('express');
const app     = express();

app.listen (3000, () => console.log ("Iniciado servidor")  );
```

**Creamos archivo `config.js`**

```js
// El primer valor es el de PRODUCCIÓN. El valor alternativo es el de DESARROLLO

module.exports = {
  port       : process.env.PORT || 3000
};
```


**Actualizamos archivo `index.js`**

```js
const config  = require('./config');
const express = require('express');
const app     = express();

app.listen (config.port,  () => console.log (`Iniciado servidor en puerto ${config.port}`) 
);
```

**Actualizamos de nuevo archivo `index.js`**

```js
const config  = require('./config');
const express = require('express');
const app     = express();

app.get ('/',  (req, res) =>  res.send ({ mensaje: 'Bienvenido'})
);

app.listen (config.port, () => console.log (`Iniciado servidor en puerto ${config.port}`) 
);
```

## FULLSTACK2: INICIANDO PROYECTO

```bash
sudo  npm  install  -g  create-react-app
create-react-app  fullstack2
cd  fullstack2
npm  start 
```

```bash
npm install -g concurrently
```


