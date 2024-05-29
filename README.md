# Activity8:API-OLIQUINO
 For EDP Activity 8

To ensure the code works please add the following:
Run XAMPP and add the following databases in SQL With these codes:

**CREATE HR DATABASE**

CREATE DATABASE IF NOT EXISTS hr;
USE hr;

**CREATE USER TABLE**

CREATE TABLE IF NOT EXISTS users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL
);

**CREATE ORDERS TABLE**

CREATE TABLE IF NOT EXISTS orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    product_name VARCHAR(255) NOT NULL,
    price DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE
);

Once the database and the tables have been added, please add the php.api in your xampp/htdocs folder.