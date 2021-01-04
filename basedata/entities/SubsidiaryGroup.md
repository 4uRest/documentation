# Grupo de Sucursal

Entidad utilizada para gestionar o clasificar un grupo de sucursales que comparten características base en el sistema, por ejemplo, un menú.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado al grupo de sucursales. |
| byte | flag_inherits_tax_data | Bandera que indica si se heredan los datos fiscales de la empresa: 0—No hereda datos fiscales, 1—Sí hereda datos fiscales. Por defecto es 0. |
| guid | tax_data_guid | Guid de los datos fiscales asignados al grupo de sucursales. |
| int | business_model_id | Id del modelo de negocio asignado al grupo de sucursales. |
| int | menu_id | Id del menú asignado al grupo de sucursales. |
| guid | company_guid | Campo que registra el guid de la empresa donde está asignado el grupo de sucursales. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Subsidiary Group table](/images/SubsidiaryGroupTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

📝 [Editar Documento](https://github.com/4uRest/documentation)