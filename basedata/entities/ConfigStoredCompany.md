# Empresas Registradas

Entidad en esquema **Config** utilizada para llevar un registro de las empresas que completaron el proceso de confirmación del sistema y por ende cuentan con un esquema propio que se genera automáticamente y el nombre se almacena en esta tabla.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | schema_name | Representa el nombre del esquema generado por el sistema correspondiente a la empresa |
| guid | company_sign_up_guid | Representa el guid del registro inicial de la empresa. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Master Stored Company Table](/images/ConfigStoredCompanyTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---


📝 [Editar Documento](https://github.com/4uRest/documentation)