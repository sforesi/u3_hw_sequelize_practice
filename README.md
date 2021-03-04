# Sequelize Practice

![](https://khalilstemmler.com/static/sequelize-banner-aa084fb79fadfa1c0fc483b5092f44f5.png)

## Deliverables

You'll be creating a database with a theme of your choosing. You must have the following:

- Atleast 3 models
- Table names must be lowercased and snakecased
- Crud queries, read, update, create, and delete for each model, You can hard code in information for the create, update and delete. You can either create 3 seperate files or one file for all of these queries.

## Getting Started

These commands should be done in order.

```sh
npm init
```

```sh
npm install sequelize pg
```

```sh
npx sequelize-cli init
```

Modify your `config.json` so that you're creating a database with your chosen name and modify the dialect to `postgres`.

Create your database:

```sh
npx sequelize-cli db:create
```

---

## Creating Models

To create a new model run:

```sh
npx sequelize-cli model:generate --name <Your Model Name Goes Here> --attributes <someattribute>:<somedatatype>,<other stuff...>
```

Remember, there can be no spaces in between each attribute.

Once your model is created don't forget to add the `tableName` field in the model and adjust the migration generated accordingly.

After each model creation, run:

```sh
npx sequelize-cli db:migrate
```

## Requiring Models

In the file you're using for your queries, don't forget to require your models:

```js
const {} = require('./models')
```

#### Made A Mistake?

You can always revert a migration using:

```sh
npx sequelize-cli db:migrate:undo
```

## Generating Seeds

You can generate a seed file using:

```sh
npx sequelize-cli seed:generate --name <Seed Name>
```

Run your seed using:

```sh
npx sequelize-cli db:seed:all
```

Hint: You can also use faker:

```sh 
npm install --save-dev faker
```
