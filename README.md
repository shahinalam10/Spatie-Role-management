# Laravel 11 ACL (Roles & Permissions) with Spatie

This project demonstrates how to implement **User Roles and Permissions** in a Laravel 11 application using the [`spatie/laravel-permission`](https://github.com/spatie/laravel-permission) package.

---

## 🚀 Features
- Role-Based Access Control (ACL)
- User, Role, and Product Management modules
- Assign roles & permissions via seeders
- Restrict access using middleware
- Authentication scaffold

---

## 📦 Requirements
- **PHP** >= 8.x
- **Composer**
- **Node.js & NPM**
- **Database** (MySQL, SQLite, etc.)

---

## ⚙️ Installation

### 1️⃣ Create a Laravel 11 project
```bash
composer create-project laravel/laravel example-app "11.*"
cd example-app

composer require spatie/laravel-permission
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
php artisan migrate

composer require laravel/ui
php artisan ui bootstrap --auth
npm install
npm run build

php artisan make:seeder RoleSeeder
php artisan db:seed --class=RoleSeeder

