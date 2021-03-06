# laravel-chat-pusher
Pusher Service and Laravel - VueJS


Build a chat app with Laravel and Pusher Service

Signup Pusher Service:
https://pusher.com/signup

### Getting Started

Clone the project repository by running the command below if you use SSH

```
git clone https://github.com/messivite/laravel-chat-pusher.git


After cloning,run terminal:

```
composer install
```

You must editing .env file (Database Connection,Pusher Settings)

Then run:

```
php artisan key:generate
```

### Setup Pusher

If you don't have one already, create a free Pusher account at https://pusher.com/signup then login to your dashboard and create an app.

Set the `BROADCAST_DRIVER` in your `.env` file to **pusher**:

```
BROADCAST_DRIVER=pusher
```

Then fill in your Pusher app credentials in your `.env` file:

```
PUSHER_APP_ID=xxxxxx
PUSHER_APP_KEY=xxxxxxxxxxxxxxxxxxxx
PUSHER_APP_SECRET=xxxxxxxxxxxxxxxxxxxx
```

Also, remember to fill in the `cluster` of your Pusher app and other additional options in `config/broadcasting.php`:

```
// config/broadcasting.php

'options' => [
   'cluster' => 'eu',
   'encrypted' => true
],
```

### Database Migrations

Be sure to fill in your database details in your `.env` file before running the migrations:

```
php artisan migrate
```

And finally, start the application:

```
php artisan serve
```

and visit [http://localhost:8000/](http://localhost:8000/) to see the application in action.
=======
