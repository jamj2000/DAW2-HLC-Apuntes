# Desarrollo FullStack con MERN


## INTRODUCCIÓN



## INSTALACIÓN DEL ENTORNO

```bash 
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs build-essential

npm install -g concurrently
```

> Referencia: 
> -  https://github.com/nodesource/distributions  (Distribución de binarios desde NodeSource)


## INICIANDO PROYECTO

```bash
mkdir  fullstack1  &&  cd  fullstack1
npm  init  --yes
```

**Archivo `package.json`**

```json
{
  "name": "fullstack1",
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
  ip         : process.env.HOST || '0.0.0.0',
  port       : process.env.PORT || 3000
};
```
