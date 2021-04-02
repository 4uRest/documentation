# Seed Role

Entidad en esquema **Config**. Utilizada para gestionar permisos y alcances de  usuarios en el sistema de las empresas.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al rol semilla. |
| string | description | Descripción de apoyo para entender el alcance del rol semilla. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Config Seed Role table](/images/ConfigSeedRoleTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3. Asignación de permisos al rol semilla.

La asignación de permisos al rol semilla se ejecuta a través de una tabla relacional entre la tabla **Permission** y **SeedRole** surgiendo **SeedRolePermission** de la siguiente manera.

![Config Seed Role Permission Table](/images/ConfigSeedRolePermissionTable.png)

Donde la descripción de los campos quedaría.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| guid | seed_role_guid | Guid del rol semilla. |
| guid | permission_guid | Guid del permiso. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)