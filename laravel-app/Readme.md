1. Install composer

```bash
   curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
```

2. Create a laravel app using composer

```bash
   composer create-project laravel/laravel docker-laravel-app
```

To run the app

```bash
    php artisan serve
```

3. Create a docker file

```bash
   touch Dockerfile
```

4. Build the container

```bash
   docker build -t laravel-app . 
```

5. Run the container

```bash
   docker run -p 80:80 laravel-app
```