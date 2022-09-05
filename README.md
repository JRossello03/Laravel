<img src="https://desarrolloweb.com/storage/tag_images/actual/XLzFK4Nkfc15A4Qn6emJcyP6DvpvdbD46S2mLfbI.png" align="left" width="150px" height="100px" />

# Laravel con Docker

<br>

## **1. Crear proyecto laravel**

`curl -s "https://laravel.build/example-app" | bash`

### Habilitar interfaz de linia de comandos para interactuar con el entorno de desarrollo Docker predeterminado de Laravel

:bulb: **Tip:** Podemos ejecutar este comando o bien en el directorio donde se encuentra el proyecto o en la carpeta que contiene los proyectos.

`alias sail='bash vendor/bin/sail'`

### Levantar los contenedores

`sail up -d`

### Ejecutar comandos de laravel usando Sail

:memo: **Nota:** Solo podremos ejecutar estos comandos si previamente hemos ejecutado el comando que habilita la interfaz de comandos de Sail

`sail php artisan migrate` // `sail npm install` // `sail npm run build `

:memo: **Nota:** Si no hemos habilitado la interficie de comandos de sail, hay una alternativa para poder ejecutar comandos de laravel.

`docker ps` // buscamos el nombre del contenedor

`docker exec -it <container-name / id-container> bash`

Una vez dentro del contenedor ya podemos ejecutar cualquier comando de Laravel

`php artisan migrate` // `npm install` // `npm run build`

## **2. Instalar Jetstream en nuestro proyecto**

`sail composer require laravel/jetstream`

`sail php artisan jetstream:install livewire/inertia`

`sail npm install`

`sail npm run build`

`sail php artisan migrate`

## 3. Instalar Breeze en nuestro proyecto

`sail composer require laravel/breeze`

`sail php artisan breeze:install`

`sail npm install`

`sail npm run build`

`sail php artisan migrate`