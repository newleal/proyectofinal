<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>
########### PROYECTO FINAL MVC #################
# INTEGRANTES: dIEGO ALEXANDER ARDILA SANCHEZ - MIGUEL ANGEL LEAL BELTRAN
#
#A TENER EN CUENTA:
# 1- Crea una nueva base de datos y conéctala con el proyecto. - LA BASE DE DATOS QUE SE CREO - OK 
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=proyectofinal
DB_USERNAME=root
DB_PASSWORD=
#
#DATOS DE INGRESO:
Ejecuta las migraciones y valida que se hubiesen creado correctamente- OK.
#

1-El sistema debe permitir, desde el back end, la creación de asignaturas por semestres (nombre, cantidad de créditos, nombre docente, asignatura prerrequisito, cantidad de horas de trabajo autónomo y cantidad de horas de trabajo dirigido).

ESTAS SON LAS RUTAS:
Route::get('/materias', 'App\Http\Controllers\MateriasController@index');
Route::post('/materias', 'App\Http\Controllers\MateriasController@store');
Route::get('/materias/{materias}', 'App\Http\Controllers\MateriasController@show');
Route::put('/materias/{materias}', 'App\Http\Controllers\MateriasController@update');
Route::delete('materias/{materias}', 'App\Http\Controllers\MateriasController@destroy');

2-El sistema permite la autenticación de dos tipos de usuarios: estudiantes y coordinador.
 MEDIANTE LA AUTENTICACION CON VUE SE REALIZA LA VALICAION Y AUTENTICACION DESDE EL FRON END

3- El coordinador puede gestionar (CRUD) las asignaturas, pero el estudiante no, únicamente las puede listar y ver información en detalle.
ESTE APARATDO NO SE GENERO ROLES - SE REALIZARON CONSULTAS PERO NO SE LOGRO

4- Genera la API que permita listar todas las asignaturas y consultar su información en detalle.

LA API SE GENERO CON EXITO
Route::get('/programas', 'App\Http\Controllers\ProgramasController@index');
Route::post('/programas', 'App\Http\Controllers\ProgramasController@store');
Route::get('/programas/{programas}', 'App\Http\Controllers\ProgramasController@show');
Route::put('/programas/{programas}', 'App\Http\Controllers\ProgramasController@update');
Route::delete('/programas/{programas}', 'App\Http\Controllers\ProgramasController@destroy');

Route::get('/materias', 'App\Http\Controllers\MateriasController@index');
Route::post('/materias', 'App\Http\Controllers\MateriasController@store');
Route::get('/materias/{materias}', 'App\Http\Controllers\MateriasController@show');
Route::put('/materias/{materias}', 'App\Http\Controllers\MateriasController@update');
Route::delete('materias/{materias}', 'App\Http\Controllers\MateriasController@destroy');

Route::get('/semestres', 'App\Http\Controllers\SemestresController@index');
Route::post('/semestres', 'App\Http\Controllers\SemestresController@store');
Route::get('/semestres/{semestres}', 'App\Http\Controllers\SemestresController@show');
Route::put('/semestres/{semestres}', 'App\Http\Controllers\SemestresController@update');
Route::delete('/semestres/{semestres}', 'App\Http\Controllers\SemestresController@destroy');

5 -Asegúrate que desde el front end se pueda:

 5.1 - Listar las asignaturas, utilizando el componente card.
 
 OK

5.2 - Ver información en detalle de una asignatura, mediante el componente modal
OK


6 - DATOS DE PRUBEBA DESDE LA API
//users
admin
admin@admin.com
password:
$2y$10$Q/dIUM5PjM66a7dRhcTDm.xq/MmMSw/.cxezTufnMOFWVyp1/YbaW
password: 123456789


// Programas
{
    "name":"Contabilidad"
}


// semestres
{
    "name":"Semestre I"
}


//Materias

{
    "name":"Programacion Basica",
    "semestre_id": 1,
    "programa_id":1,
    "cantidad_creditos": "3",
    "name_professor": "Juan Urrego",
    "prerequisito":"Ninguno",
    "cant_hrs_autonomo":"15",
    "cant_hrs_dirigido":"25"
}

##################################
## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 2000 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**
- **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
- **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
