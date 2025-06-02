

# King Zeus Motor Part Inventory Management System

## Setup & Run Instructions

Welcome! This guide will help you get the system up and running locally.

---

## Prerequisites

Make sure you have the following installed on your machine:

* **Node.js** (v14+ recommended)
* **npm** (comes with Node.js) or **yarn**
* **PHP** (v8+ recommended)
* **Composer** (PHP dependency manager)
* **MySQL** (or compatible database)

---

## Step 1: Clone the Repository

```bash
git clone <your-repository-url>
cd king-zeus-motor-part-inventory
```

---

## Step 2: Setup Backend

### 2.1 Install PHP dependencies

```bash
cd backend
composer install
```

### 2.2 Configure Environment Variables

* Copy `.env.example` to `.env`

```bash
cp .env.example .env
```

* Update `.env` with your database and other settings (example values are provided below):

```
APP_NAME=Laravel
APP_ENV=local
APP_TIMEZONE=Asia/Manila
APP_KEY=base64:P5gY5B0j8B0QQO7fI5I7fqi2N1LyKwTOmBwVlfV7vd4=
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=backend_database
DB_USERNAME=root
DB_PASSWORD=

# Other variables as needed
```

### 2.3 Generate Application Key

```bash
php artisan key:generate
```

### 2.4 Run Database Migrations & Seeders

```bash
php artisan migrate --seed
```

*(This will create necessary tables and seed sample data.)*

### 2.5 Start the Backend Server

```bash
php artisan serve
```

By default, the backend will run on:
`http://localhost:8000`

---

## Step 3: Setup Frontend

### 3.1 Navigate to frontend folder and install dependencies

```bash
cd ../frontend
npm install
```

### 3.2 Start the Frontend Development Server

```bash
npm run dev
```

The frontend will typically be available at:
`http://localhost:3000` (or as specified by Vite)

---

## Additional Notes

* Make sure your database service (MySQL) is running.
* If you want to change ports or environment settings, update `.env` files accordingly.
* Frontend uses Vite with React and TailwindCSS.
* Backend is a Laravel application.

---

## Summary Commands

```bash
# Backend
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
php artisan serve

# Frontend (in a new terminal)
cd frontend
npm install
npm run dev
```

---

If you encounter any issues, please check logs or open an issue on the repository.

---

Would you like me to help format this as a full markdown-ready README.md file with badges and headings?
