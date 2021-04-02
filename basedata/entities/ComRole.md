# Rol.

Entidad en esquema **Company**. Utilizada para gestionar permisos y alcances de usuarios en el sistema de las empresas.


---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al rol. |
| string | description | Descripción de apoyo para entender el alcance del rol. |
| guid | subsidiary_group_guid | Guid del grupo de sucursales donde se creo el rol. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Role Table](/images/ComRoleTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3. Asignación de permisos al rol.

La asignación de permisos al rol se ejecuta a través de una tabla relacional entre la tabla **Permission** y **Role** surgiendo **RolePermission** de la siguiente manera.

![RolePermission Table](/images/ComRolePermissionTable.png)

Donde la descripción de los campos quedaría.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| guid | role_guid | Guid del rol. |
| guid | permission_guid | Guid del permiso. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

📝 [Editar Documento](https://github.com/4uRest/documentation)