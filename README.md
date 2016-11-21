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


