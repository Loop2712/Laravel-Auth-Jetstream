**Install Laravel 8:**
```
composer create-project --prefer-dist laravel/laravel Laravel-Auth-Jetstream
```
**Install Jetstream:**
```
composer require laravel/jetstream
```
**Create Auth with Livewire:**
```
php artisan jetstream:install livewire
OR
php artisan jetstream:install livewire --teams
```
Now, let’s node js package:
```
npm install && npm run dev
```
now, we need to run the migration command to create a database table:
```
php artisan migrate
```
**config/fortify.php**

```
  
'features' => [
        Features::registration(),
        Features::resetPasswords(),
        Features::emailVerification(),
        Features::updateProfileInformation(),
        Features::updatePasswords(),
        Features::twoFactorAuthentication(),
    ],
```
**config/jetstream.php**

```
  
'features' => [
        Features::profilePhotos(),
        Features::api(),
        Features::teams(),
    ],
```
**Now you can run your application by below command:**
```
php artisan serve
```
