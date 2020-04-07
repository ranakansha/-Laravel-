# -Laravel-
## prerequistes
Php,
Xampp,
Composer

### Go to the tdoc dir and open cmd 

step 1 : Install Laravel using command
composer create-project laravel/laravel <project name>
  
setp 2 : go inside  project dir and run serve command
php artisan serve

for publicly acceble your directory without  http://127.0.0.1:8000 
1 > Go inside public folder
2> copy .htaccess and index.php file inside your home dir 
3> open index.php file that are in home dir in vs code and paste the following code
```
<?php

/**
 * Laravel - A PHP Framework For Web Artisans
 *
 * @package  Laravel
 * @author   Taylor Otwell <taylor@laravel.com>
 */

$uri = urldecode(
    parse_url($_SERVER['REQUEST_URI'], PHP_URL_PATH)
);

// This file allows us to emulate Apache's "mod_rewrite" functionality from the
// built-in PHP web server. This provides a convenient way to test a Laravel
// application without having installed a "real" web server software here.
if ($uri !== '/' && file_exists(__DIR__.'/public'.$uri)) {
    return false;
}

require_once __DIR__.'/public/index.php';




```
4 > run php artisan serve 
5. open browser and type localhost/projectname
