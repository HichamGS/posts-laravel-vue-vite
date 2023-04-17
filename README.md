## Setup
-- Application key
```
php artisan key:generate --ansi
````

-- Vue packages installation 
```
npm i vue@next vue-loader@next @vitejs/plugin-vue vue-router@4
````


Set up your database (Mysql or Postgres, configure your .env file)



-- Config your vite.config.js
```
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';
import vue from "@vitejs/plugin-vue";

export default defineConfig({
    plugins: [
        vue(),
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
});
```