# Permiso

Entidad en esquema **Config**. Un permiso representa una acción en el sistema de las empresas, los permisos se asignan a un seed role, o un rol, según el caso.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al permiso. |
| string | description | Descripción de apoyo para entender el alcance del permiso. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Master Super Permission Table](/images/ConfigPermissionTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

📝 [Editar Documento](https://github.com/4uRest/documentation)