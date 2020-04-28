# laravel-api-auth-jwt-boilerplate
Laravel 5.8 API Authentication with JSON Web Token (JWT) Boilerplate

<h3>Installation:</h3>

Clone from git repo

	git clone https://github.com/ric-ez/laravel-api-auth-jwt-boilerplate.git
	
	
Change your directory to project directory

	cd laravel-api-auth-jwt-boilerplate
	
Install composer package

	composer install

Set .env for laravel project

	// Copy .env.example to .env
	
	// Set your DB config
	
	DB_CONNECTION=mysql 			// your DB connection driver
	DB_HOST=127.0.0.1	 			// your DB host
	DB_PORT=3306					// your DB port
	DB_DATABASE=laraveljwt 			// your DB name
	DB_USERNAME=root 				// your DB username
	DB_PASSWORD=root 				// your DB password
	
Generate laravel app key

	php artisan key:generate
	
Generate JWT secret

	php artisan jwt:secret
		
Migrate DB ( Make sure your database is running first before migrating your database )

	php artisan migrate
	
Run the laravel server using php server or using your own workflow ( lamp, valet, vagrant, docker, etc )

	php artisan serve
	
Testing the API using api client software ( postman / insomnia or you can using your own browser )

<h3>Testing:</h3>

Register user

	endpoint: /api/register
	method: POST
	payload:
	
	name, email, password, password_confirmation

Copy token from the request, use bearer token as auth, paste it in, and then send request to

	endpoint: /api/private
	method: GET
	
Public API

	endpoint: /api/public
	method: GET
