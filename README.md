<h1 align="center">
    <img src="https://camo.githubusercontent.com/ab9f94b1f47bf05fbf0f99d65a802f638cb38f21/68747470733a2f2f692e696d6775722e636f6d2f613334616f30782e706e67" width="100px" /><br>
    <br>
  <a href="https://github.com/robertokbr/GoBarber-Web">
    GoBarber Frontend Web
  <a/>
</h1>

<h4 align="center">
Complete toolkit to improved the barbershop bussines!
</h4>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/robertokbr/GoBarber-Web.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/robertokbr/GoBarber-Web.svg">

  <a href="https://www.codacy.com/app/robertokbr/GoBarber-Web?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=robertokbr/GoBarber-Web&amp;utm_campaign=Badge_Grade">
    <img alt="Codacy grade" src="https://img.shields.io/codacy/grade/1b577a07dda843aba09f4bc55d1af8fc.svg">
  </a>

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/robertokbr/GoBarber-Web.svg">
  <a href="https://github.com/robertokbr/GoBarber-Web/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/robertokbr/GoBarber-Web.svg">
  </a>

  <a href="https://github.com/robertokbr/GoBarber-Web/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/robertokbr/GoBarber-Web.svg">
  </a>
</p>


 <img src="https://github.com/robertokbr/GoBarber-Web/blob/master/.Github/signin.png"/>
  <img src="https://github.com/robertokbr/GoBarber-Web/blob/master/.Github/signout.png"/>


# 🚧 In progress

- [ReactJs with Typescript](https://reactjs.org) - A JavaScript library for building user interfaces
- [react-router-dom]()
- [Axios](https://github.com/axios/axios) - Promise based HTTP client for the browser and NodeJs
- [Uuidv4]()
- [Yup]()
- [Styled-components]()
- [React-Spring](https://www.react-spring.io/)
- [Eslint]()
- [Prettier]()
- [EditorConfig]()

## 🎈 Project Style

* EditorConfig
* Eslint -config-airbnb
* Prettier

## :information_source: How To Use

```bash
# Clone this repository
$ git clone https://github.com/robertokbr/GoBarber-Web

# Go into the repository
$ cd GoBarber-Web

# Install dependencies
$ yarn install

# Run the app
$ yarn start
```
---

<h1 align="center">
    <img src="https://camo.githubusercontent.com/ab9f94b1f47bf05fbf0f99d65a802f638cb38f21/68747470733a2f2f692e696d6775722e636f6d2f613334616f30782e706e67" width="100px" /><br>
    <br>
    <a href="https://github.com/robertokbr/GoBarber-API">
      Go Barber API
    <a/>
</h1>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/robertokbr/GoBarber.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/robertokbr/GoBarber.svg">

  <a href="https://www.codacy.com/app/robertokbr/GoBarber?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=robertokbr/GoBarber&amp;utm_campaign=Badge_Grade">
    <img alt="Codacy grade" src="https://img.shields.io/codacy/grade/1b577a07dda843aba09f4bc55d1af8fc.svg">
  </a>

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/robertokbr/GoBarber.svg">
  <a href="https://github.com/robertokbr/GoBarber/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/robertokbr/GoBarber.svg">
  </a>

  <a href="https://github.com/robertokbr/GoBarber/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/robertokbr/GoBarber.svg">
  </a>
  
# 🚧 In progress

## 🕹 Features

* Create User
* Create Session by E-mail and Password, and get a JWT token
* Use Authenticated Routes
* Create Appointments with User - Appointments relation one to many
* Get Appointments
* Upload Avatar
* Update Avatar 
* ...🔧


## 🏗 Architecture:
* `Runtime`: Node.JS with TypeScript 
* `API`: RESTfull
* `Architectural pattern`: Data mapper pattern with DDD
* `ORM`: Typeorm
* `Persistent data store`: Docker Postgres
* `Authentication`: JWT


## 🔧 Other configs

* Global Exception catch class

* Middleware ```ensureAuthenticated``` to compare the auth JWT token with the provided key 

* BcryptJs to store the user key as a hash

## :information_source: How To Use

To clone and run this application, you'll need [Git](https://git-scm.com), Node.js v10.16 or higher + yarn v1.13 or higher installed on your computer. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/robertokbr/GoBarber

# Go into the repository
$ cd GoBarber

# Install dependencies
$ yarn 
```
---

## How to Run Postgres Database at Docker

* [Install Docker](https://www.notion.so/Instalando-Docker-6290d9994b0b4555a153576a1d97bee2)

```bash
# Create a Postgres Image
$ docker run --name gostack_postgres -e POSTGRES_PASSWORD=docker -p 5432:54
32 -d postgres
```

## Docker Alternative
* ``OBS``: If you dont wanna run the database at Docker, and you preferer a simple alternative  I recommend you to change the database to Sqlite3, for this you have to:
```bash
# Install Sqlite3
$ yarn add sqlite3 
```
* Copy and paste it in the ormConfig.json:
```
{
  "name": "default",
  "type": "sqlite",
  "database": "./src/database/db.sqlite3",
  "autoSchemaSync": true,
  "entities": [
    "src/models/*.ts"
  ],
  "logging": {
    "logQueries": true
  },

  "migrations": [
    "./src/database/migrations/*.ts"
  ],
  "cli": {
    "entitiesDir": "src/models",
    "migrationsDir": "./src/database/migrations"
  }
}

```

## How to Run the Server:
```bash
# Run migrations
$ yarn typeorm migratios:run

# Run localhost server
$ yarn dev:server
```

<h1 align="center">
    <img src="https://camo.githubusercontent.com/ab9f94b1f47bf05fbf0f99d65a802f638cb38f21/68747470733a2f2f692e696d6775722e636f6d2f613334616f30782e706e67" width="100px" /><br>
    <br>
    <a href="https://github.com/robertokbr/GoBarber-Mobile">
      GoBarber Mobile
    <a/>
</h1>

<h4 align="center">
 Complete toolkit to improved the barbershop bussines!

</h4>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/robertokbr/GoBarber-Mobile.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/robertokbr/GoBarber-Mobile.svg">

  <a href="https://www.codacy.com/app/robertokbr/GoBarber-Mobile?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=robertokbr/GoBarber-Mobile&amp;utm_campaign=Badge_Grade">
    <img alt="Codacy grade" src="https://img.shields.io/codacy/grade/1b577a07dda843aba09f4bc55d1af8fc.svg">
  </a>

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/robertokbr/GoBarber-Mobile.svg">
  <a href="https://github.com/robertokbr/GoBarber-Mobile/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/robertokbr/GoBarber-Mobile.svg">
  </a>

  <a href="https://github.com/robertokbr/GoBarber-Mobile/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/robertokbr/GoBarber-Mobile.svg">
  </a>
</p>

<p  align="center">
 <img src="https://github.com/robertokbr/GoBarber-Mobile/blob/master/.GIthub/IMG_4947.PNG" width="300"/> <img src="https://github.com/robertokbr/GoBarber-Mobile/blob/master/.GIthub/IMG_4948.PNG" width="300"/> <img src="https://github.com/robertokbr/GoBarber-Mobile/blob/master/.GIthub/IMG_4951.PNG" width="300"/>
</p>


# 🚧 In progress

- [React-Native with Typescript](https://reactjs.org) - A JavaScript library for building user interfaces
- [Expo]()
- [React-hooks]()
- [Context-api]()
- [Styled-components]()
- [Yup]()
- [Expo-vector-icons]()
- [react-native-unimodules]()
- [Eslint]()
- [Prettier]()
- [EditorConfig]()

## 🎈 Objective of the project

* Study the development of a application from the scratch

## :information_source: How To Use

To clone and run this application, you'll need [Git](https://git-scm.com), [Node.js v10.16][nodejs] or higher + [Yarn v1.13][yarn] or higher installed on your computer. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/robertokbr/GoBarber-Mobile

# Go into the repository
$ cd GoBarber-Mobile

# Install dependencies
$ yarn install

# Run the app
$ yarn start
```
---


Roberto Junior :wave: [Join me on Linkedin!](https://www.linkedin.com/in/robertojrcdc/)

[nodejs]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[vc]: https://code.visualstudio.com/
[vceditconfig]: https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig
[vceslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

