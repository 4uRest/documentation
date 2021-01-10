# ETAPA I DE DESARROLLO

Espacio destinado para la documentación de las entidades de la base de datos de 4UREST.

---

### VISTAS DE LA ETAPA I

El siguiente [enlace](http://bit.ly/4UREST-VIEWS) presenta las vistas y flujo de la Etapa I

![VIEWS EN ETAPA I](basedata/entities/images/FORM_VIEWS.jpg)

--- 

### MODELO BASE DE LA ETAPA I

El modelo de la base de datos en la etapa 1 se presenta a continuación.

![BD DIAGRAM E1](basedata/entities/images/BD_DIAGRAM_E1.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

### OPERACIONES BÁSICAS DE LA ETAPA I

En la **ETAPA I** del sistema, podrá ser capaz de ejecutar las siguientes operaciones con sus entidades:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| SuperUser | name, last name, phone_number, email, password, super_role_guid | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: guid, id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid. | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | Un super usuario no se puede eliminar a si mismo. El super usuario eliminador debe tener el super rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_super_user_guid. |
| SuperRole | name | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: guid, id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid. | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | Que ningún super usuario tenga asignado  el super rol. El super usuario eliminador debe tener el super rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_super_user_guid. |
| BusinessModel | name | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid. | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | Que ninguna sucursal tenga asignado el business model. El super usuario eliminador debe tener el super rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_super_user_guid. |
| User | name, last name, email, password, company_guid, role_guid | El usuario creador debe tener el rol autorizado para la acción. Se genera: guid, id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Un usuario no se puede eliminarse a si mismo. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| Company | name | El usuario creador debe tener el rol autorizado para la acción. Se genera: guid, id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | No se puede ejecutar la operación. |
| SubsidiaryGroup | name, business_model_id, company_guid | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ninguna sucursal esté asignada al grupo de sucursales. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| Subsidiary | name, subsidiary_group_id | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ningun usuario esté asignado a la sucursal. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| TaxData | tax_identification_number, name,  phone_number, email, address, company_guid | El usuario creador debe tener el rol autorizado para la acción. Se genera: guid, id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ninguna empresa, grupo de sucursales o sucursal tenga asignados los datos fiscales. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| Menu | name, subsidiary_group_id | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ningun grupo de sucursales tenga el registro asignado. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| CustomRole | name, subsidiary_group_id | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ningun usuario del grupo de sucursales tenga el registro asignado. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| SeedRole | name | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | Que ningun usuario de ningún grupo de sucursales tenga el registro asignado. El super usuario eliminador debe tener el super rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |
| Permission | name, flag_super_permission | El super usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | El super usuario actualizador debe tener el super rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_super_user_guid. | No se puede ejecutar la operación. |
| CustomRolePermission | custom_role_guid, permission_guid | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | No se puede ejecutar la operación. | El usuario eliminador debe tener el rol autorizado para la acción. Se aplica Hard Delete. |
| SuperRolePermission | super_role_guid, permission_guid | El usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | No se puede ejecutar la operación. | El super usuario eliminador debe tener el super rol autorizado para la acción. Se aplica Hard Delete. |
| SeedRolePermission | seed_role_guid, permission_guid | El usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | No se puede ejecutar la operación. | El super usuario eliminador debe tener el super rol autorizado para la acción. Se aplica Hard Delete. |
| SeedRoleBusinessModel | seed_role_guid, business_model_id | El usuario creador debe tener el super rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_super_user_guid | No se puede ejecutar la operación. | El super usuario eliminador debe tener el super rol autorizado para la acción. Se aplica Hard Delete. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)