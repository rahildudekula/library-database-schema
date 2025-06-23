-- Create schema
CREATE SCHEMA IF NOT EXISTS ecommerce;

-- Create customers table
CREATE TABLE ecommerce.customers (
    customer_id SERIAL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Create products table
CREATE TABLE ecommerce.products (
    product_id SERIAL PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price NUMERIC(10, 2) NOT NULL,
    stock_quantity INT DEFAULT 0
);

-- Create orders table
CREATE TABLE ecommerce.orders (
    order_id SERIAL PRIMARY KEY,
    customer_id INT NOT NULL,
    order_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    total_amount NUMERIC(10, 2),
    FOREIGN KEY (customer_id) REFERENCES ecommerce.customers(customer_id)
);

-- Create order_items table
CREATE TABLE ecommerce.order_items (
    order_item_id SERIAL PRIMARY KEY,
    order_id INT NOT NULL,
    product_id INT NOT NULL,
    quantity INT NOT NULL,
    item_price NUMERIC(10, 2) NOT NULL,
    FOREIGN KEY (order_id) REFERENCES ecommerce.orders(order_id),
    FOREIGN KEY (product_id) REFERENCES ecommerce.products(product_id)
);
