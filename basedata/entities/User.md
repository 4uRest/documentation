# Usuario

Entidad utilizada para gestionar usuarios en el sistema. Éstos son usuarios que utilizan los módulos del sistema según su rol, son el usuario final.
---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla |
| string | name | Representa el nombre del usuario. |
| string | last_name | Representa los apellidos del usuario. |
| string | phone_number | Representa el número de teléfono del usuario. |
| datetime | birthday | Representa la fecha de nacimiento del usuario. |
| string | original_image | Ruta de la imagen original del usuario. |
| string | processed_image | Ruta de la imagen procesada para el sistema que representa al usuario. |
| string | email | Representa el correo electrónico del usuario. |
| string | password | Representa la clave de acceso al sistema del usuario. |
| int | pos_pin | Pin de acceso a la plataforma punto de venta. |
| byte | hidden | Representa la visibilidad en el sistema: 0—visible, 1—sin acceso al sistema. Por defecto es 0. |
| guid | company_guid | Campo que registra el guid de la empresa a la que pertenece el usuario. |
| guid | subsidiary_guid | Campo que registra el guid de la sucursal a la que es asignado el usuario. |
| guid | role_guid | Campo que registra el guid del rol asignado al usuario. |
| guid | creator_user_guid | Campo que registra el guid del super usuario que crea al nuevo usuario. |
| guid | updater_user_guid | Campo que registra el guid del super usuario que actualiza algún dato del usuario. |
| guid | deletor_user_guid | Campo que registra el guid del super usuario que elimina el usuario. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del usuario. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización de algún dato del usuario. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del usuario. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Company table](/images/UserTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

📝 [Editar Documento](https://github.com/4uRest/documentation)