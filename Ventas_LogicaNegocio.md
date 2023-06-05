# Ventas

## Listado de Entidades

### customers - **(DE)**

- customer_id INT AUTO **(PK)**
- customer_name VARCHAR(100)
- customer_last_name VARCHAR(100)
- email VARCHAR(100) **(UQ)**
- phone_number INT **(UQ)**
- cuil VARCHAR(100) **(UQ)**
- customer_address VARCHAR(100)
- zip_postal_code VARCHAR(10)
- city VARCHAR(500)
- country VARCHAR(50) **(FK)**

### products - **(DE|CE)**

- product_id INT AUTO **(PK)**
- bar_code INT
- product_name VARCHAR(100)
- description TEXT
- size VARCHAR(4)
- color VARCHAR(10)
- product_price FLOAT
- stock INT
- image VARCHAR(250)

### sales - **(DE)**

- sale_id INT AUTO **(PK)**
- customer_id INT **(FK)**
- date DATETIME
- total FLOAT

### items_sale - **(PE)**

- item_id INT AUTO **(PK)**
- sale_id INT **(FK)**
- product_id INT **(FK)**
- product_quantity INT

### country - **(CE)**

- country_id INT AUTO **(PK)**
- country_name VARCHAR(50)
- domain VARCHAR(2) **(UQ)**

---

## Relaciones

1. Un **customer** tiene **country** (_1 - 1_)
1. Un **customers** puede tener varias **sales** (_1 - M_)
1. Un **sales** puede tener varias **items_sale** (_1 - M_)
   1.Un **items_sale** es un **procuct** (_1 - 1_)

---

## Modelo Relacional de la DB

![Modelo Relacional](./Ventas_LogicaNegocio_ModeloRelacional_DB.png)
