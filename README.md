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

Archivo `package.json`

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
  "keywords": ['fullstack', 'node', 'express'],
  "author": "José Antonio Muñoz Jiménez",
  "license": "ISC"
}

```


