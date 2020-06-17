---
title: "Fundamentos de Tipado en Typescript Parte 1"
excerpt: " Un tipado (type) es un conjunto de valores. En JavaScript (no en TypeScript), hay 8 types...
."
coverImage: "/assets/blog/typescript/types.jpeg"
date: "2020-06-16T06:35:07.322Z"
author:
  name: Juan Millord
  picture: "/assets/blog/authors/millord.jpg"
ogImage:
  url: "/assets/blog/typescript/typescript.png"
---

## ¿Que es el tipado en TypeScript?

Un tipado (type) es un conjunto de valores que determinan el uso del dato en memoria. En JavaScript (no en TypeScript), hay 8 types:

1- Undefined: El conjunto con un solo elemento llamado undefined.

2- Null: El conjunto con un solo elemento null

3- Boolean: El conjunto con dos elementos false y true

4- Number: El conjunto de todos los números

5- BigInt: El conjunto de todos los enteros de precisión-arbitraria

6- String: El conjunto de todos los strings

7- Symbol: El conjunto de todos los símbolos

8- Object: El conjunto de todos los objetos (el cual incluye funciones y arrays).

Es importante saber que todos estos types son dinámicos.

TypeScript trae consigo una capa adicional a JavaScript: static types. La cual solo existe al tiempo del compilado o type-checking del código. Cada variable, propiedad, etc, tiene un tipado (type) estático que predice sus valores dinámicos. Esto es posible a traves de lo que se llama type-checking.

Lo que se puede verificar estáticamente es mucho. Esto sin tener que correr el código. Si por ejemplo el parámetro num de la función toString(num) tiene el tipo estático number, si se le da el argumento toString('abc') arrojará un error. Esto porque 'abc' tiene el tipo incorrecto.

![tsconfig.json](/assets/blog/typescript/tipado.png)

## ¿Que es Type annotation en TypeScript?

Es cuando se asignan explicitamente el tipo de dato en typescript:

![tsconfig.json](/assets/blog/typescript/annotation.png)

Hay dos tipos de anotaciones en esta función

1-El parametro num: dos puntos seguidos por number.
2-Result de toString(): dos puntos seguidos por string

Ambos number y string son type expressions que especifican los tipos datos.

## ¿Que es Type inference en TypeScript?

Es cuando TypeScript determina el tipo de datos sin tener que depender de un type annotation. Si por ejemplo se omite el tipo de datos que se retornará, Typescript infiere que es un string:

![tsconfig.json](/assets/blog/typescript/inference.png)

## Conclusiones

Por medio del tipado de datos nos podemos dar cuenta de errores antes que
el código corra. Lo que hace un mejor developer experience y es mejor forma de escalar los proyectos.
