# Migrating database changes

The following command will run the migrations, this should be run
```
node migrate.js
```

Migrations are found in the /migrations folder in the root. Order is managed by adding a number to it.

When creating a database everyting is generated from the Sequalize model definition. All existing migrations are set to done, so it won't collide with future migrations. Best practice is to write migrations that allow for a table or column to already exists, but mysql doesn't alway make that easy.

```
node reset.js
```

This means that if migrations and the model differ slightly a new database and migrated database is not always the (exactly) same.