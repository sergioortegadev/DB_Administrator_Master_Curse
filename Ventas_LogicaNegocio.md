# Ventas

## Listado de Entidades

### customers - **(DE)**

- customer_id **(PK)**
- customer_name
- customer_last_name
- cuil
- phone_number
- email
- customer_address
- zip_postal_code
- city
- country **(FK)**

### products - **(DE|CE)**

- product_id **(PK)**
- product_name
- description
- talle
- color
- product_price
- stock
- image

### sales - **(DE)**

- sale_id **(PK)**
- customer_id **(FK)**
- date
- total

### items_sale - **(PE)**

- item_id **(PK)**
- sale_id **(FK)**
- product_id **(FK)**
- product_quantity

### country - **(CE)**

- country_id **(PK)**
- country_name
- domain

---
