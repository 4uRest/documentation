# Auditoría de Esquema Master

Entidad en esquema **Master** utilizada llevar un registro de movimientos en tablas importantes del esquema. Ésta permitirá tener el historial de movimientos con un mensaje personalizado de cada uno de ellos.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | entity | Representa el nombre de la entidad de la tabla donde se registra la modificación de datos. |
| guid | reg_guid | Guid del registro modificado en la tabla original. |
| string | message | Mensaje autogenerado en función de la entidad y operación realizadas. |
| guid | creator_super_user_guid | Campo que registra el guid del creador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Master Master Activity Log](/images/MasterMasterActivityLog.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

Tabla aquí

---

📝 [Editar Documento](https://github.com/4uRest/documentation)