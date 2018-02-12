#### This skeleton is based in Laravel 5.6 and comes with AdminLTE working out of the box!

## How to install

First make your storage folder writable. 

```
cp .env.example .env
```

```
composer install
```

```
php artisan key:generate
```

```
php artisan migrate --seed
```

```
php artisan serve
```

and then you can open your browser and navigate to `http://localhost:8000` (or whatever ip/port that you set up in artisan server command) and start your new awesome app!

## Credentials

You can log in using `admin@admin` as username and `admin` as password. 

P.S: you can change this information to whatever you like in `database/seeds/AdminSeeder.php`

## You can disable registration routes

You can enable or disable the registration routes as you like, just use the REGISTRATION_ROUTE in your .env file.

## Auth

This skeleton uses Laravel's Auth scaffold. As you may know, it provides all authentication stuff so you don't have to create routes, controllers and views for login and register.

## AdminLTE

This skeleton uses [jeroennoten's Laravel-AdminLTE](https://github.com/jeroennoten/Laravel-AdminLTE) package to provide AdminLTE out of the box, and you can use all the features provided by this package. 

To use the template, create a blade file and extend the layout with `@extends('adminlte::page')`.
This template yields the following sections:

- `title`: for in the `<title>` tag
- `content_header`: title of the page, above the content
- `content`: all of the page's content
- `css`: extra stylesheets (located in `<head>`)
- `js`: extra javascript (just before `</body>`)

All sections are in fact optional. Your blade template could look like the following.

```html
{{-- resources/views/admin/dashboard.blade.php --}}

@extends('adminlte::page')

@section('title', 'Dashboard')

@section('content_header')
    <h1>Dashboard</h1>
@stop

@section('content')
    <p>Welcome to this beautiful admin panel.</p>
@stop

@section('css')
    <link rel="stylesheet" href="/css/admin_custom.css">
@stop

@section('js')
    <script> console.log('Hi!'); </script>
@stop
```

Note that in Laravel 5.2 or higher you can also use `@stack` directive for `css` and `javascript`:

```html
{{-- resources/views/admin/dashboard.blade.php --}}

@push('css')

@push('js')
```

You now just return this view from your controller, as usual. Check out [AdminLTE](https://almsaeedstudio.com) to find out how to build beautiful content for your admin panel.

To know more, just go to the [package repo page](https://github.com/jeroennoten/Laravel-AdminLTE) here on GitHub.

## Credits
- [Taylor Otwell](https://github.com/taylorotwell) - Creator and maintainer of Laravel.
- [Jeroen Noten](https://github.com/jeroennoten) - Laravel-AdminLTE package.
- [Abdullah Almsaeed](https://github.com/almasaeed2010) - AdminLTE.
- [Simonarde Lima](https://github.com/simonardejr) - maintainer of this skeleton.