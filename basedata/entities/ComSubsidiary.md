# Sucursales.

Entidad en esquema **Company** utilizada para representar una subsidiaria(sucursal) de un grupo de subsidiarias. Ésta será un elemento del grupo al que pertenece y por ende compartirá características como menú, productos, datos fiscales, inventario, donde parte de estos elementos en común son a su vez personalizables por sucursal, por ejemplo una sucursal comparte el menú del grupo, pero en esta sucursal puede que no se maneje un producto en específico por lo que se podrá deshabilitar sólo en ésta sucursal sin afectar a las demás.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado a la sucursal. |
| string | phone_number | Representa el número de teléfono de la sucursal. |
| string | email | Represeta  el correo electrónico de la sucursal. |
| string | alias | Represeta  el alias de la sucursal. |
| byte | flag_inherits_tax_data | Bandera que indica si se heredan los datos fiscales del grupo de sucursales donde pertenece la sucursal: 0—No hereda datos fiscales, 1—Sí hereda datos fiscales. Por defecto es 1. |
| byte | flag_inherits_menu | Bandera que indica si se heredan el menú asignado al grupo de sucursales donde pertenece la sucursal: 0—No hereda menú, 1—Sí hereda menú. Por defecto es 1. |
| byte | hidden | Representa la visibilidad en el sistema: 0—visible, 1—oculto en el sistema. Por defecto es 0. |
| json | address | Dirección de la sucursal. |
| guid | subsidiary_group_guid | Guid de registro del grupo de sucursales donde pertenece la sucursal. |
| guid | tax_data_guid | Campo que registra el guid de registro de los datos fiscales asignados a la sucursal. |
| guid | menu_guid | Campo que registra el guid de registro del menú asignado a la sucursal. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Subsidiary Table](/images/ComSubsidiaryTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

📝 [Editar Documento](https://github.com/4uRest/documentation)