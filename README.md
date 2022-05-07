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
