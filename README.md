# Hoe kun je starten met laravel-blade standalone
Dit is een stappenplan waarin je alle stappen doorloopt om de template engine "Laravel Blade" te gebruiken.

- zorg dat je composer kunt starten vanaf een commandline  (zie ook: www.getcomposer.org)

- maak een nieuwe map
- plaats daarin een nieuw bestand composer.json met de volgende inhoud:
```
{
    "require": {
        "philo/laravel-blade": "3.*"
    }
}
```
- open een commandline en ga naar de map waarin je project staat
- geef het commando composer install
- composer gaat nu een nieuwe map aanmaken `vendor` met daarin alle benodigde bestanden
- maak nieuwe mappen `cache` en `views`
- plaats in de map views een nieuw bestand `hello.blade.php` met deze inhoud:
```
<!doctype html>
<html>
<head>
    <title>GithubScraper</title>
    <link rel="stylesheet" type="text/css" href="css/style.css">
</head>
<body>

{{ $message }}

</body>
</html>
```
- voorzie index.php van de volgende inhoud:
```
<?php

// configure blade engine
require 'vendor/autoload.php';
use Philo\Blade\Blade;
$views = __DIR__ . '/views';		
$cache = __DIR__ . '/cache';		
$blade = new Blade($views, $cache);


echo $blade->view()->make('index')->with('message', 'Hallo wereld')->render();
```

