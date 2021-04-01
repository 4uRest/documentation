# Preferencias de sistema semilla

Entidad en esquema **Config**. Una preferencia de sistema representa un registro especial de proposito general en las configuraciones del esquema de la empresa en el sistema. Estas preferencias son las configuraciones semilla que se insertan cuando se crea un esquema nuevo.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | type | Tipo/Clasificación de preferencia de sistema. |
| string | name | Nombre de preferencia de sistema. |
| string | value | Valor inicial de preferencia de sistema. |
| string | description | Descripción de preferencia de sistema. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_super_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_super_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Config System Preferences Table](/images/ConfigSeedSystemPreferencesTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:



---

📝 [Editar Documento](https://github.com/4uRest/documentation)