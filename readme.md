# Node Postgres

> Mengintegrasikan Javascript(node.js) ke database(postgres)

Agenda:
- Package & npm
- Setup node-postgres
- mini MVC with node-postgres (kalau sempat)

---
## Package di Javascript

- Package merupakan libraries yg dapat digunakan dalam project kita
- Untuk menginstall package dapat menggunakan `npm` atau `Node Package Manager`
- Biasanya node.js kita sudah include `npm`
https://www.npmjs.com/

### Cara menggunakan npm

- `npm init` / `npm init -y` => menginisiasi/membuat package.json
- `npm install <nama package>` => menginstall suatu package
  - `npm install --save-dev <nama package>` / `npm install -D <nama package>` => install dev dependencies
  - `npm install --location=global <nama package>` / `npm install -g <nama package>` => install global
  - `npm install <nama package>@<version>` => install dengan versi spesifik
  - dll
- `npm uninstall <nama package>` => uninstall
- `npm test` => keperluan testing
- dan masih banyak lagi... https://docs.npmjs.com/cli/v7/commands

### Setelah inisiasi npm

- `touch .gitignore` => membuat file `.gitignore`
- memasukan `node_modules` dalam file `.gitignore`

> Langkah ini hukumnya WAJIB dilakukan

---
## Menginstall node-postgres

https://node-postgres.com/
- `npm install pg`
- connection dari javascript ke postgres
  - pool => dynamic/multiple connection to database
  - client => single connection to database
- programmatic connection https://node-postgres.com/features/connecting#programmatic
- membuat file connection => require dari package `pg` 
- test connection

## Setup/Migration
> Create table dan relasinya dsb

- membuat file setup/Migration => require pool yang sudah di test
- membuat query untuk create table
- menjalankan querynya

## Seeding
> me-seed / insert data awal ke table2 yang sudah di migrasi

- membuat file seeding => require pool
- membuat query untuk insert kedalam table
- menjalankan querynya

---
## MVC with node-postgres

### Setup folder dan file untuk MVC

- bikin app index, model dan controller seperti biasa
- require pool dari connection di model
- prosesnya hampir mirip dengan setup/migration dan seeding