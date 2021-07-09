# node-auth
A NodeJS web app that uses JWT for authorization and uses postgreSQL for user information.

## Tutorial
Followed tutorial [Node.js JWT Authentication with PostgreSQL example](https://bezkoder.com/node-js-jwt-authentication-postgresql/)

## To run on local machine

Make sure you have npm installed.

Create a .env file at the root directory with the following content:
```conf
DB_HOST= #postgres host
DB_USER= # postgres user
DB_PASS= # postgres password
DB_NAME= # postgres database
SECRET= # self-defined secret key
```
Open a terminal at the root directory
```bash
npm install
```
When running the app, the app will drop all records in user, role, and user-role table.

Run the app
```bash
node server.js
```

## Endpoints
**Methods** | **Urls** | **Actions**
--- | --- | ---|
POST | /api/auth/signup | Sign up new account
POST | /api/auth/sign | Log in an account
GET | /api/test/all | Retrive public content
GET | /api/test/user | Access User's Content
GET | /api/test/mod | Access Moderator's Content
GET | /api/test/admin | Access Admin's Content