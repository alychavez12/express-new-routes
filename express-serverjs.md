# Express

## In Your Terminal

* mkdir nameOfTheFolder
* cd nameOfTheFolder
* touch server.js
* npm init -y (install express)
* npm i express
* git init
* git remote add origin https://github.com/alychavez12/express-new-routes.git
* git add -A
* git commit -m 'wip: adds file system'
* git push origin master
* code .

## VS CODE

## In Server.js

1. require dependencies

* const express = require('express');

2. initialize the express app

* const app = express();

* touch file: .env
* in .env file PORT=3000
* in terminal: npm i dotenv

* mkdir folder: views
* in views folder: touch index.ejs show.ejs edit.ejs
* in terminal: npm i ejs (pluging model)

3. Configure Settings in server.js

* require('dotenv').config();
* const port = process.env.PORT;

4. Configure Database (Creates a model folder and a file.js with data information)

* const fruits = require('./models/fruits.js)

5. Mount Middleware (Give us acces to req.body)

* app.use(express.urlencoded ({extended:false}));

6. Mount Routes (INDUCES).

## CSS

 * in server.js app.use(express.static('public));

 * mkdir folder: public
  - mkdir CSS
   - touch style.css
  - mkdir img
  - mkdir js
   - touch script.js

