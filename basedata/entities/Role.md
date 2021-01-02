# Rol

Entidad utilizada para gestionar roles de usuario en el sistema. Estos roles son creados por super usuarios con los permisos necesarios.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla |
| string | name | Representa el nombre del rol. |
| guid | creator_super_user_guid | Campo que registra el guid del super usuario que crea el rol. |
| guid | updater_super_user_guid | Campo que registra el guid del super usuario que actualiza algún dato del rol. |
| guid | deletor_super_user_guid | Campo que registra el guid del super usuario que elimina el rol. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del rol. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización de algún dato del rol. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del rol. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Company table](/images/RoleTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

📝 [Editar Documento](https://github.com/4uRest/documentation)