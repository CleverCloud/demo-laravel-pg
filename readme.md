# Laravel as Clever Cloud demo

## Configuration

To use a databse (like PostgreSQL), you can link your application with an addon or manually set the following environment variables will be set.

```bash
POSTGRESQL_ADDON_HOST
POSTGRESQL_ADDON_PORT
POSTGRESQL_ADDON_DB
POSTGRESQL_ADDON_USER
POSTGRESQL_ADDON_PASSWORD
```

To update your database schema, add this environment variable to your Clever Cloud application:

`CC_POST_BUILD_HOOK=php artisan migrate --force`

Finally, you have to manually set the `APP_KEY=base64:X` with `X` the result of `php artisan key:generate` on your local project.