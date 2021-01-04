# Super Usuario

Entidad utilizada para gestionar super usuarios en el sistema. Éstos son usuarios principales capaces de gestionar empresas, sucursales etc. El alcance es a nivel empresa 4UREST.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre del super usuario. |
| string | last_name | Representa los apellidos del super usuario. |
| string | phone_number | Representa el número de teléfono del super usuario. |
| datetime | birthday | Representa la fecha de nacimiento del super usuario. |
| string | original_image | Ruta de la imagen original del super usuario. |
| string | processed_image | Ruta de la imagen procesada para el sistema que representa al super usuario. |
| string | email | Representa el correo electrónico del super usuario, éste sirve para accesar al sistema administrativo. |
| string | password | Contraseña registrada por el super usuario, ésta sirve para accesar al sistema administrativo. |
| byte | hidden | Representa la visibilidad en el sistema: 0—visible, 1—sin acceso al sistema. Por defecto es 0. |
| guid | super_role_guid | Campo que registra el guid del super rol asignado al super usuario. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Company table](/images/SuperUserTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

📝 [Editar Documento](https://github.com/4uRest/documentation)