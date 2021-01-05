# Permiso

Un permiso representa una acción en el sistema, los permisos se asignan a roles de super usuarios, usuarios o roles personalizados en el sistema.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al permiso |
| string | description | Descripción de apoyo para entender el alcance del permiso. |
| byte | flag_super_permission | Representa el nivel de acceso del permiso: 0—Permiso para usuarios y super usuarios, 1—permiso sólo para super usuarios. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![PERMISSION TABLE](/images/PermissionTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| Permission | name, flag_super_permission | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | No se puede ejecutar la operación. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)