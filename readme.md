# Laravel as Clever Cloud demo

This sample project is a fork from [GitHub](https://github.com/evercode1/sample-project).

## Configuration

To use a database (like PostgreSQL), you can link your application with an addon or manually set the following environment variables will be set.

```bash
POSTGRESQL_ADDON_HOST
POSTGRESQL_ADDON_PORT
POSTGRESQL_ADDON_DB
POSTGRESQL_ADDON_USER
POSTGRESQL_ADDON_PASSWORD
```

To update your database schema, add this environment variable to your Clever Cloud application:

```bash
CC_POST_BUILD_HOOK=php artisan migrate --force
```

To enable logs retrieving on Clever console or Clever CLI, you have to specify the following value in `./config/app.php`:

```php
'log' => env('APP_LOG', 'syslog'),
```

Finally, you have to manually set the `APP_KEY=base64:X` with `X` the result of `php artisan key:generate` on your local project.