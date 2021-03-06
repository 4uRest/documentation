# Usuarios

Entidad en esquema **Company**, utilizada para gestionar usuarios en el sistema de las empresas. Éstos son usuarios son capaces de ejercer acciones en la empresa segun el alcance de su rol.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al usuario. |
| string | last_name | Representa los apellidos del usuario. |
| string | phone_number | Representa el número de teléfono del usuario. |
| datetime | birthday | Representa la fecha de nacimiento del usuario. |
| string | original_image | Ruta de la imagen original del usuario. |
| string | processed_image | Ruta de la imagen procesada para el sistema que representa al usuario. |
| string | email | Representa el correo electrónico del usuario. |
| string | password | Representa la clave de acceso al sistema del usuario. |
| int | pos_pin | Pin de acceso a la plataforma punto de venta. |
| byte | hidden | Representa la visibilidad en el sistema: 0—visible, 1—sin acceso al sistema. Por defecto es 0. |
| guid | role_guid | Campo que registra el guid del rol asignado al usuario. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![User Table](/images/ComUserTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

📝 [Editar Documento](https://github.com/4uRest/documentation)