
# Estandares de codificación de WordPress

Para desarrollar aplicaciones en WordPress es necesarios configurar el entorno necesario ya sea para Themes o Plugins.

## Requerimiento
- `PHP`
- `Composer`
- `tmux`


Crea la carpeta necesaria con la estructura a desarrollar en mi caso usare `composer`
luego instalare esta libreria [WordPress Coding Standards for PHP_CodeSniffer](https://github.com/WordPress/WordPress-Coding-Standards).

para composer agregar el siguiente código al archivo `composer.json`.

````  json
{
    "require-dev": {
        "wp-coding-standards/wpcs": "^3.0"
    },
    "config": {
        "allow-plugins": {
            "dealerdirect/phpcodesniffer-composer-installer": true
        }
    }
}
````

Luego usar los siguientes comandos.

````bash
composer install
composer update
````
Tambien es necesario revisar y configurar el archivo `phpcs.xml`.

Lugo ejecutar el comando. Recordar tener configurado `phpcs.xml`.

````bash
./vendor/bin/phpcs -s -p class-fullculqi-ajax.php
./vendor/bin/phpcs --standard=WordPress class-fullculqi-ajax.php
````