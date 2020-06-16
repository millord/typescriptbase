---
title: "Configuración básica de Typecript"
excerpt: "Para este tutorial es necesario que tengas node.js instalado.
Con node.js instalado, ve a la consola y escribe... sigue leyendo."
coverImage: "/assets/blog/typescript/config.png"
date: "2020-06-11T06:35:07.322Z"
author:
  name: Juan Millord
  picture: "/assets/blog/authors/millord.jpg"
ogImage:
  url: "/assets/blog/big/big.webp"
---

## Como configurar tu Typescript en poco tiempo

Para este tutorial es necesario que tengas node.js instalado.
Con node.js instalado, ve a la consola y escribe:

```
npm install -g typescript

npm install -g ts-node
```

a. El primero instala a Typescript globalmente y el segundo a ts-node, que será lo que usaremos para conpilar de typescript a javascript.

b. Luego que ya esté instalado todo lo del paso anterior:

1 -crear un directorio, como por ejemplo:

mkdir miProyecto

Dentro de ese directorio creater dos más.

mkdir ts

dentro de ts, crear src y test:

cd ts && mkdir src test

src: donde estara el codigo y test, para los test.

2 -Luego al mismo nivel de ts, crear dist, queria así:

![tsconfig.json](/assets/blog/typescript/structure.png)

y finalmente crear el archivo tsconfig.js, dentro de este espeficiar:

Quedará así

![tsconfig.json](/assets/blog/typescript/tsconfig.png)

rootDir : donde el código en typescript reside

outDir: donde el código se compila a javascript

module: El módulo a usar, en este caso CommonJS

Finalmente, ve al root del proyecto y escribe en la consola:

```
tsc
```

y esto compilará a javascript. Y para correr el código en consola:

```
tsc-node main.ts
```

## Conclusiones

Como puedes ver la configuración de Typescript es muy sencilla. Solo tienes que tener instalado varios paquetes, crear un directorio donde
tengas el código en Typescript y otro de salida del código ya compilado
a Javascript. Es mucho lo que puedes hacer con Typescript y te animo a seguir estudiandolo.
