## Pusher integration with laravel

## Step 1
Create Project | laravel 9 

    composer create-project laravel/laravel pusher
## Step 2 
We need to tell Laravel that we are using the Pusher driver in the `.env` file:
```javascript
BROADCAST_DRIVER=pusher
```
## Step 3 
install the Pusher PHP SDK. We can do this using composer:

    composer require pusher/pusher-php-serve
## Step 4 
Then let’s update the `.env` file to contain our Pusher app credentials (noting the added cluster credential, this won’t be in your `.env` file as Laravel has not added this functionality yet:
```javascript
PUSHER_APP_ID=xxxxxx
PUSHER_APP_KEY=xxxxxxxxxxxxxxxxxxxx
PUSHER_APP_SECRET=xxxxxxxxxxxxxxxxxxxx
```
## Step 5
we need to install these dependencies through `NPM`:
```javascript
npm install
```
To subscribe and listen to events, Laravel provides Laravel Echo, which is a JavaScript library that makes it painless to subscribe to channels and listen for events broadcast by Laravel. We’ll need to install it along with the Pusher JavaScript library:
```javascript
npm install --save laravel-echo pusher-js
```

## Step 6 | Authenticating Users
import  laravel/ui

    composer require laravel/ui

After install laravel ui | install bootstrap auth

    php artisan ui bootstrap --auth
  ## step 7 
  go to `resources\views\layouts\app.blade.php`
  
  add cdn bootstrape links css/js
  ```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
```
```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
```

## Step 8 
add Java script code from your account on pusher
