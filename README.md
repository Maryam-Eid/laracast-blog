# Laracast Blog

A small Laravel blog for listing posts and opening a single post by its slug. Posts can also be filtered by category and author.

## Features

- Home page lists posts, newest first
- Post page at `/posts/{slug}`
- Category page at `/categories/{category}`
- Author page at `/authors/{username}`
- Each post belongs to one category and one author
- Eager loads the category and author with every post

## Tech Stack

- PHP ^8.0.2
- Laravel 9
- Blade
- Vite
- MySQL

## Requirements

- PHP ^8.0.2
- Composer
- Node.js and npm
- MySQL

## Installation

```bash
composer install
cp .env.example .env
php artisan key:generate
```

Create a MySQL database, then set these values in `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=
```

Then run:

```bash
php artisan migrate --seed
npm install
npm run build
php artisan serve
```

For local development with Vite:

```bash
npm run dev
```

## Seed Data

The seeder creates one user named Michael Scott and five posts. Categories are created with those posts. The factory password for generated users is `password`.
