# Database

#### Available Database Types

* SQLite: Doesn't require any database server and works without setting anything up.
* MySQL: We recommend using MySQL, if you need to connect your database to an external system, or you use a backup system that requires it. If you want to use MySQL: Make sure that your MySQL server is set up correctly (up-to-date MySQL server version, connection limits, utf8mb4\_0900\_as\_cs as table encoding etc.).
*   MySQL-v2: Better table schemas and supports \[synchronizing claim data across multiple servers].(https://github.com/Angeschossen/Lands/wiki/Database#synchronizing-claims-across-servers)

    ```
    # It is highly recommended to set a unique table prefix if the plugin
    # shares a database with other plugins or Lands instances.
    table-prefix: 'lands_'
    ```

We recommend using MySQL-v2 over SQLite, if possible.

#### Backups

If you want to take backups of your database, you may want to use MySQL and set up a backup service or just a simple script of your choice. This is specific to your environment.

#### Migrate your Database to MySQL, SQLite

1. If you use MySQL, make sure that there are no tables with the same table-prefix!
2. Also, if you want to convert to MySQL, make sure the credentials and database name is set up correctly in your Lands config.
3. Make sure to take a backup of your current database. After you have followed these steps, execute this command: `/lands admin migratedb [sqlite, mysql]`

#### Synchronizing Claims across Servers

A MySQL database and Redis instance is required. It won't work properly without Redis! If you want to synchronize claim data between servers, make sure to configure the following sections in config.yml.

**MySQL:**

If you're currently using the old SQL schema, please make sure to migrate to the new one using `/lands admin migratedb mysql-v2`. Before migration, make sure to use a different `table-prefix` for `mysql-v2`, if you're currently using `mysql`. In case it's the same, adjust it and then reload the configuration before migration.

```
  mysql-v2:
    enabled_19: true
    address_2: 'localhost'
    port_2: '3306'
    username_2: 'minecraft'
    password_2: 'password'
    database_2: 'lands'

    # It is highly recommended to set a unique table prefix if the plugin shares a database with other plugins.
    table-prefix_2: 'lands_'
```

**Redis:**

It is very important to properly configure the `server-name` and `master` option properly.

```
  redis:
    enabled_6: true
    address_3: "redis://127.0.0.1"
    port_3: 6379
    username_3: "default"
    password_3: "password"
    # This should be the name that you configured for this server in your BungeeCord or Velocity config.
    server-name: "server-1"
    # This option should only be enabled on ONE of the servers that are connected to the same Lands database and Redis.
    # If true: This server will execute tasks, such as upkeep, taxes etc. for all lands across all servers that are 
    # connected to the same Lands database and Redis.
    master: true
```

## Schema Migration

You might have gotten a warning in console that you should migrate to the new SQL schema.

### SQLite

To migrate to the new SQL schema with SQLite, follow these instructions:

1. Make sure that sqlite-v2 is **disabled** in config.yml and you currently still use the old database.
2. Execute `/lands admin migratedb sqlite-v2`
3. **Enable** `sqlite-v2` in config.yml:

```
  # Use SQLite for the database. Doesn't require a database server.
  sqlite-v2: true
```

4. Restart the server.

### MySQL

To migrate to the new SQL schema with MySQL, follow these instructions:

1. Configure the mysql-v2 section in config.yml. **Make sure that mysql-v2 is disabled, and you currently still use the old database. Also, make sure to use a different table prefix or database than your current MySQL config!**

```
  # MySQL database
  # To use this without issues, your connection limits etc. need to be configured properly in your MySQL server configuration.
  # If you want to synchronize lands and claims across servers, please read the setup instructions: https://github.com/Angeschossen/Lands/wiki/Database#synchronizing-claims-across-servers
  mysql-v2:
    enabled_19: false
    address_2: 'localhost'
    port_2: '3306'
    username_2: 'minecraft'
    password_2: 'password'
    database_2: 'lands'

    # It is highly recommended to set a unique table prefix if the plugin shares a database with other plugins.
    table-prefix_2: 'lands_'
```

2. Execute `/lands admin migratedb mysql-v2` and check for any error messages, in case you provided the wrong credentials etc.
3. Enable mysql-v2 in config.yml.
4. Restart the server.
