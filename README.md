# My store

Curso de Backend con Node.js: API REST con Express.js


## 1) Configuración del entorno de desarrollo para este curso

- npm init -y
- git init
- npm i nodemon eslint eslint-config-prettier eslint-plugin-prettier prettier -D

## 2) Instalación de Express.js y tu primer servidor HTTP

- npm i express
- npm run dev

## 3) Routing con Express.js

- app.get
- res.json

## 4) ¿Qué es una RESTful API?

| Method    | /products | /products/{id}                |
| :-------- | :-------- | :---------------------------- |
| `GET`     | Get list  | Get                           |
| `PUT`     | Replace*  | Update/Replace                |
| `PATCH`   | No Apply  | Update                        |
| `POST`    | Create    | No Apply                      |
| `DELETE`  | Delete*   | Delete                        |
|           | `*`       | No recomendado                |

## 5) GET: recibir parámetros

| URL                                     | req.params                        |
| :--------                               | :-------------------------------- |
| api.example.com/tasks/:id/              | const id = req.params.id          |
| api.example.com/people/:id/             | const { id } = req.params         |
| api.example.com/users/:id/tasks/:taskId | const { id, taskId } = req.params |

## 6) GET: párametros query

- app.example.com/products
- app.example.com/products?page=1
- app.example.com/products?limit=10&offset=0
- app.example.com/products?region=USA
- app.example.com/products?region=USA&brand=XYZ

- Crear datos ficticios npm i faker@5.5.3 -S

Manejar ruta desde lo especifico a lo dinámico
- /products/filter
- /products/:id

## 7) Separación de responsabilidades con express.Router

Single Responsibility principle

Crear un router para la aplicación
- const router = express.Router();

## 8) POST: método para crear

Router general
- const express = require('express');
- const router = express.Router();
- app.use('/api/v1', router);
POST capturar JSON
- app.use(express.json());

## 9) PUT, PATCH y DELETE
- router.patch
- router.delete

## 10) Códigos de estado o HTTP response status codes
res.status(201).json(.....
- https://http.cat/
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Status

## 11) Introducción a servicios: crea tu primer servicio
Separar router de servicios, en los servicios va la lógica de negocio
- product.service.js

## 12) Crear, editar y eliminar desde un servicio

Crear, editar y eliminar desde un servicio

## 13) Async await y captura de errores
try {
  ...
} catch (error) {
  ...
}

## 14) Middleware para HttpErrors

- function logErrors (err, req, res, next) {...}
- function errorHandler (err, req, res, next) {...}

## 15) Manejo de errores con Boom
- npm i @hapi/boom
- throw boom.notFound('product not found');
- Se crear un nuevo middleware
- function boomErrorHandler (err, req, res, next) { ... }

## 16) Validación de datos con Joi
- npm i joi


## 17) Probando nuestros endpoints
- Validando createProductSchema, updateProductSchema, getProductSchema en products.routers.js

## 18) Consideraciones para producción
- Cors
- Https
- Procesos de Build
- Remover logs
- Seguridad (Helmet)
- Testing

## 19) Problema de CORS
- npm i cors

