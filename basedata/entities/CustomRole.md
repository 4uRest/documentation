# Rol Personalizado

Un rol personalizado es un rol creado por un usuario y asignado a un grupo de sucursales con la intención de ser usado en todas las sucursales que pertenezcan al grupo de sucursales.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al rol personalizado. |
| string | description | Descripción de apoyo para entender el alcance del rol personalizado. |
| int | subsidiary_group_id | Id del grupo de cucursales donde se creo el rol personalizado. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Custom Role Table](/images/CustomRoleTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| CustomRole | name, subsidiary_group_id | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ningun usuario del grupo de sucursales tenga el registro asignado. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |

---

## 4.  Asignación de permisos al rol.

La asignación de permisos al rol se ejecuta a través de una tabla relacional entre la tabla **Permission** y **CustomRole** surgiendo **CustomRolePermission** de la siguiente manera.

![Custom Role Permission Table](/images/CustomRolePermissionTable.png)

Donde la descripción de los campos quedaría de la siguiente manera.

| Tipo | Campo | Descripción |
|-|-|-|
| int | id | Registro único y auto incrementable de la tabla. |
| guid | custom_role_guid | Guid del rol personalizado. |
| guid | permission_guid | Guid del permiso. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

---
Reglas base de la tabla.

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| CustomRolePermission | custom_role_guid, permission_guid | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | No se puede ejecutar la operación. | El usuario eliminador debe tener el rol autorizado para la acción. Se aplica Hard Delete. |

📝 [Editar Documento](https://github.com/4uRest/documentation)