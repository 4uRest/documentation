# Rol Semilla

Un rol semilla es un rol creado por un super usuario con la intención de ser genérico para todos los modelos de negocio donde se asigne.

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

![Seed Role Table](/images/SeedRoleTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| SeedRole | name | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | Que ningun usuario de ningún grupo de sucursales tenga el registro asignado. El super usuario eliminador debe tener el super rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |

---

## 4.  Asignación de permisos al rol.

La asignación de permisos al rol se ejecuta a través de una tabla relacional entre la tabla **Permission** y **SeedRole** surgiendo **SeedRolePermission** de la siguiente manera.

![Seed Role Permission Table](/images/SeedRolePermissionTable.png)

Donde la descripción de los campos quedaría de la siguiente manera.

| Tipo | Campo | Descripción |
|-|-|-|
| int | id | Registro único y auto incrementable de la tabla. |
| guid | seed_role_guid | Guid del rol semilla. |
| guid | business_model_id | Guid del modelo de negocio. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

---

Reglas base de la tabla para **SeedRolePermission**.

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| SeedRolePermission | seed_role_guid, permission_guid | El usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | No se puede ejecutar la operación. | El super usuario eliminador debe tener el super rol autorizado para la acción. Se aplica Hard Delete. |

---

## 5.  Relación de modelos de negocio con roles semilla.

Existe una relación entre **BusinessModel** y **SeedRole** donde surge **SeedRoleBusinessModel**.

![Seed Role Permission Table](/images/SeedRoleBusinessModelTable.png)

Donde la descripción de los campos quedaría de la siguiente manera.

| Tipo | Campo | Descripción |
|-|-|-|
| int | id | Registro único y auto incrementable de la tabla. |
| guid | seed_role_guid | Guid del rol semilla. |
| id | business_model_id | Id del modelo de negocio. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

---

Reglas base de la tabla para **SeedRoleBusinessModel**.

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| SeedRoleBusinessModel | seed_role_guid, business_model_id | El usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | No se puede ejecutar la operación. | El super usuario eliminador debe tener el super rol autorizado para la acción. Se aplica Hard Delete. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)