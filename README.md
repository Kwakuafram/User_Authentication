# Laravel Sanctum Authentication

## Introduction
This project implements user authentication using Laravel Sanctum. It includes features such as user registration, login, logout, and authentication-protected routes.

## Requirements
- PHP >= 8.0
- Composer
- Laravel Framework
- MySQL 

## Installation Steps
1. Clone the repository.
2. Run `composer install` to install dependencies.
3. Configure the `.env` file with database and app settings.
4. Run `php artisan migrate` to create database tables.
5. Install Laravel Sanctum using `composer require laravel/sanctum`.
6. Publish Sanctum configuration using `php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"`.
7. Run `php artisan serve` to start the development server.

## Authentication Routes
- **Register**: Users can sign up with name, email, and password.
- **Login**: Users can log in and receive a token.
- **Logout**: Users can invalidate their token.
- **User Profile**: Retrieve authenticated user details.

## Testing with Postman
1. Register a user by sending a POST request with name, email, and password.
2. Log in using valid credentials and retrieve the authentication token.
3. Use the token in the Authorization header for accessing protected routes.
4. Log out by sending a POST request with the token included in the Authorization header.

## Notes
- Ensure the `sanctum` middleware is applied to protect routes.
- Tokens are invalidated upon logout to prevent unauthorized access.
- Use environment variables for sensitive configurations like database credentials.

## Conclusion
This setup provides a secure authentication system using Laravel Sanctum, enabling token-based authentication for API-driven applications.

