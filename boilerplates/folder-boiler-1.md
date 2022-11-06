# Boiler 1

> - [Índice](#boiler-1)
>   - [Iniciar Backend](#iniciar-backend)
>     - [Comandos para back](#comandos-para-backend)
>   - [Iniciar Frontend](#iniciar-frontend)
>     - [Comandos Create React App](#con-cra)
>     - [Comandos Vite](#con-vite)
>   - [Boiler general](#boiler-carpetas)
>     - [Boiler back](#backend-boiler)
>     - [Boiler front CRA](#frontend-cra-boiler)
>     - [Boiler front Vite](#frontend-vite-boiler)

## Iniciar Backend

La carpeta que crees cuando inicies el proyecto, recomiendo que se llame con el mismo nombre del proyecto. Esta carpeta será donde haras el `git init` que sugiere Github cuando creas un repositorio.  
Al crear la carpeta **api**, ***ANTES*** de añadir cualquier otra carpeta, a través de la terminal, ejecutar el comando ``npm init` para inicializar un nuevo package y crear el proyecto de node en esa carpeta.  
Te dejo una lista pequeña de comandos (y el orden) que deberías que deberas hacer en la terminal, que van a ser necesarias en el proyecto

### Comandos para backend

```
  npm init
  npm install express cors dotenv morgan nodemon
  npm install pg sequelize (si vas a utilizar PostgrsSQL o una SQL)
  npm install mongodb mongoose (si van a utilizar MongoDB)
  npm install axios (por si hacen pedidos a otra api)
```

## Iniciar Frontend

Para el frontend, hay dos sugerencias si van a utilizar React. 
Opcion 1, utilizar el **create react app**, o utilizar **vite** (Pueden utilizar cualquier otra libreria de frontend)

### Con CRA
Desde la terminal, se ubican sobre la carpeta del proyecto y ejecutan los siguientes comandos
``` 
npx create-react-app client (esto creará la carpeta client y los archivos iniciales de React)
cd client
npm install
```
Finalizado este primer paso, ahora pueden instalar dependencias.

### Con Vite
Desde la termnal, se ubican sobre la carpeta del proyecto y ejecutan los siguientes comandos  
(sugiero leer la documentacion de [vite](https://vitejs.dev/guide/))
```
npm create vite@latest client -- --template react
cd client
npm install
```
Finalizado este primer paso, ahora pueden instalar dependencias

Algunas dependencias que les serán utilez serán `Axios` y `React Router Dom`. Ya, el resto, dependerá de ustedes

# Boiler carpetas

```
📁proyecto
  📁api
  📁client
  📜.gitignore
   ℹ README.md
```

## Backend Boiler

```
📁api (carpeta del backend)
  📁node-modules
  📁src
    📁controllers
      📁xxx-controller (Controladores de la rutas de xxx. Se puede modularizar aún más)
        📜delete-xxx-controller.js 
        📜get-xxx-controler.js
        📜put-xxx-controler.js
        📜post-xxx-controler.js
      📁yyy-controller
      📁...
    📁routes (solo colocaran las rutas. la logica va en los controlers)
      📜index.js (aquí irán las rutas generales, con route.use)
      📜route-xxx.js (aqui van las rutas get/post/put/delete correspondientes)
      📜route-yyy.js
      📜...
    📁models (modelos de la base de datos)
      📜xxx-model.js
      📜yyy-model.js
      📜...
    📁helpers/utils (funciones útiles)
      📜Auth.js
      📜routeProtection.js (jwt)
    📁mails (Si utilizan nodemailer para respuestas)
      📜mail-1.html
      📜mail-2.html
      📜...
    📁api-calls (pedidos a una API externa, si es que la necesitan)
      📜api-a.js (haces el pedido de información y recomiendo guardar en tu base de datos)
      📜api-b.js
      📜...
    📜db.js
    📜app.js
  📜index.js
  ⚙ .env
  📜.env.example (Este archivo es para las variables de entorno para todos sean las mismas)
  📜package-lock.json
  📜package.json
```
## Frontend CRA boiler
```
📁client (carpeta del frontend)
  📁public (esto la crea solo CRA)
  📁src
    📁components (solo componentes, ninguna pagina entera. solo componentes)
      📁component-a
        📜component-a.jsx
        📜component-a.css (este archivo deciden ustedes que tipo de css utilizaran)
      📁component-b
        📜component-b.jsx
        📜component-b.css 
      📁...
    📁pages
      📁landing
        📜landing.jsx
        📜landing.css (este archivo deciden ustedes que tipo de css utilizaran)
      📁page-a
        📜page-a.jsx
        📜page-a.css 
      📁...
    📁utils/helpers (Divide y venceras)
      📜auth.js
      📜passport.js
      📜...
    📁icons (por si tienen iconos aquí)
    📁api-calls
      📁xxx-call
        📜xxx-get.js
        📜xxx-put.js
        📜...
      📁yyy-call
        📜yyy.get.js
        📜yyy.put.js
        📜...
      📁...
    📁redux (el interior dependerá de si usar o no redux-toolkit)
    📜App.js
    📜App.css
    📜index.js
    📜index.css
  📜package.json
  📜package-lock.json
  ⚙ .env
  📜.env.example
```
## Frontend Vite boiler
```
📁client (carpeta del frontend)
  📁public (esto la crea Vite)
    📜vite.svg
  📁src
    📁assets (esto lo crea Vite)
    📁components (solo componentes, ninguna pagina entera. solo componentes)
      📁component-a
        📜component-a.jsx
        📜component-a.css (este archivo deciden ustedes que tipo de css utilizaran)
      📁component-b
        📜component-b.jsx
        📜component-b.css 
      📁...
    📁pages
      📁landing
        📜landing.jsx
        📜landing.css (este archivo deciden ustedes que tipo de css utilizaran)
      📁page-a
        📜page-a.jsx
        📜page-a.css 
      📁...
    📁utils/helpers (Divide y venceras)
      📜auth.js
      📜passport.js
      📜...
    📁icons (por si tienen iconos aquí)
    📁api-calls
      📁xxx-call
        📜xxx-get.js
        📜xxx-put.js
        📜...
      📁yyy-call
        📜yyy.get.js
        📜yyy.put.js
        📜...
      📁...
    📁redux (el interior dependerá de si usar o no redux-toolkit)
    📜App.css
    📜App.jsx
    📜index.css
    📜main.jsx
  📜index.html
  📜package.json
  📜package-lock.json
  ⚙ .env
  📜.env.example
  ⚙ vite.config
```