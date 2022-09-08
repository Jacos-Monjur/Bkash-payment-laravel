## bKash Payment Gateway Integration with Laravel 8

## Clone this repo

```
https://github.com/Jacos-Monjur/Bkash-payment-laravel.git
```

## Install composer packages

```
$ cd laravel-bkash
```

```
$ composer install

```

## Create and setup .env file

```
$ cp .env.example .env
```

```
$ php artisan key:generate

```

change database name

## Migrate and insert records

```
$ php artisan migrate
```

```
$ php artisan tinker
```

```
$ factory(App\Order::class, 20)->create();
```

```
$ exit
```

## Put bKash sandbox credentials to config.json

```
create config.json file to storage/app/public
put credentials your merchant


{
        "createURL" :"https://checkout.sandbox.bka.sh/v1.2.0-beta/checkout/payment/create",
        "executeURL" :"https://checkout.sandbox.bka.sh/v1.2.0-beta/checkout/payment/execute/",
        "tokenURL" : "https://checkout.sandbox.bka.sh/v1.2.0-beta/checkout/token/grant",
        "script" : "https://scripts.sandbox.bka.sh/versions/1.2.0-beta/checkout/bKash-checkout-sandbox.js",
        "app_key": "",
        "proxy" : "",
        "app_secret": "",
        "username" : "",
        "password" : "",
        "token" : ""
}

```

```
php artisan storage:link

```
