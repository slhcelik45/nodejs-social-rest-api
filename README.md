# REST API

## Project Setup

```
 npm init

```

## Kulanılan Paketler

- express
- mongoose
- dotenv
- helmet
- morgan
- nodemon
- cors
- bcrypt

## Paket yükleme

```
npm i express mongoose dotenv helmet morgan nodemon
```

### Express Tutotial

```
const express = require('express')
const app = express()

app.get('/', function (req, res) {
  res.send('Hello World')
})

app.listen(3000)
```

### dotenv Tutorial

```
require('dotenv').config() ...

DB_HOST=localhost
DB_USER=root
DB_PASS=s1mpl3  .....


const db = require('db')
db.connect({
  host: process.env.DB_HOST,
  username: process.env.DB_USER,
  password: process.env.DB_PASS
}) ....
```

### helmet Tutorial

```
const express = require("express");
const helmet = require("helmet");

const app = express();

app.use(helmet());

// ...is equivalent to this:
app.use(helmet.contentSecurityPolicy());
app.use(helmet.dnsPrefetchControl());
app.use(helmet.expectCt());
app.use(helmet.frameguard());
app.use(helmet.hidePoweredBy());
app.use(helmet.hsts());
app.use(helmet.ieNoOpen());
app.use(helmet.noSniff());
app.use(helmet.permittedCrossDomainPolicies());
app.use(helmet.referrerPolicy());
app.use(helmet.xssFilter());

```

### morgan tutorial

```
var morgan = require('morgan')

morgan(function (tokens, req, res) {
  return [
    tokens.method(req, res),
    tokens.url(req, res),
    tokens.status(req, res),
    tokens.res(req, res, 'content-length'), '-',
    tokens['response-time'](req, res), 'ms'
  ].join(' ')
})

```
