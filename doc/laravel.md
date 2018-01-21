# Laravel
***
solves voor problemen die ik ben tegengekomen in laravel

## CORS problem
Gekopieerd van markdown file van **Thomas Van Aken**
1)	composer require barryvdh/laravel-cors
2)	in config/app.php in de providers array deze lijn toevoegen: Barryvdh\Cors\ServiceProvider::class,
3)	in app/Http/Kernel.php in $middelware array deze lijn toevoegen: \Barryvdh\Cors\HandleCors::class,
4)	in app/Http/Kernel.php in $middlewareGroups array in mijn geval onder 'api' deze lijn toevoegen: \Barryvdh\Cors\HandleCors::class,
5)	config publishen: php artisan vendor:publish --provider="Barryvdh\Cors\ServiceProvider"
EXTRA!	When you do a delete, options is sent first, I catch this problem by routing options to an empty function
* Link: https://github.com/barryvdh/laravel-cors
 
 


