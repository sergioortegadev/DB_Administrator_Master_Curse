# Sistema de Autenticación

## Listado de Entidades

### users | **(DE)**

- user_id **(PK)**
- user_name **(UQ)**
- password
- email **(UQ)**
- name
- last_name
- avatar
- active
- date_creation
- date_update

### roles | **(CE)**

- role_id **(PK)**
- role_name
- description

### permissions | **(CE)**

- permission_id **(PK)**
- name
- description

### roles_x_usuario | **(PE)**

Si pusiera el atributo rol en la entidad usuarios, solo podría ponerle un rol a cada usuario, y podría tener relaciones de Muchos a Muchos, con esta entidad pivote "roles_x_usuario" puedo asignar más de un rol a cada usuario.

- rxu_id **(PK)**
- user_id **(FK)**
- role_id **(FK)**

### permisos_x_roles | **(PE)**

- pxr_id **(PK)**
- role_id **(FK)**
- permission_id **(FK)**

---

## Relaciones

En esta base, las entidades de datos no tienen relaciones, sino que se concentran en las tablas pivote, dando solo dos relaciones M a M

- **Users** tienen **roles**
- **Roles** tienen **perissions**
