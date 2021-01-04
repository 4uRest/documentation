# Sucursal

Entidad utilizada para representar una sucursal en el sistema.

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
| byte | flag_inherits_tax_data | Bandera que indica si se heredan los datos fiscales del grupo de sucursales donde pertennece la sucursal: 0—No hereda datos fiscales, 1—Sí hereda datos fiscales. Por defecto es 0. |
| byte | hidden | Representa la visibilidad en el sistema: 0—visible, 1—oculto en el sistema. Por defecto es 0. |
| json | address | Dirección de la sucursal, en el punto 2 se desglosa y describe su estructura. |
| int | subsidiary_group_id | Guid de registro del grupo de sucursales donde pertenece la sucursal. |
| guid | tax_data_guid | Campo que registra el guid de registro de los datos fiscales asignados a la sucursal. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Descripción del Json "Address".

Para el siguiente ejemplo. Se tienen los siguientes datos.

La calle **"Av de los Insurgentes"** tiene como **"id = 15"** por lo tanto, el json quedaría de la siguiente manera:

```json
{
    "place_id": "15",
    "details":"No.16902, Rio Tijuana 3ra Etapa, Tijuana, B.C",
    "reference":"Dentro de la plaza"
}
```

---

## 3.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Subsidiary table](/images/SubsidiaryTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 4.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|:-:|:-:|:-:|:-:|:-:|
| Subsidiary | name, subsidiary_group_id | El usuario creador debe tener el rol autorizado para la acción. Se genera: id, created_at. Se cumple con campos de entrada mínimos y creator_user_guid | El usuario actualizador debe tener el rol autorizado para la acción. Se genera: updated_at. Se cumple con campos de entrada mínimos y updater_user_guid. | Que ningun usuario esté asignado a la sucursal. El usuario eliminador debe tener el rol autorizado para la acción. Se genera: deleted_at. Se cumple con campo deletor_user_guid. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)