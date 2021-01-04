# Datos Físcales

Entidad utilizada para gestionar los datos físcales de empresas, grupos de sucursales o sucursales en el sistema.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | tax_identification_number | Clave única de identificación físcal. |
| string | name | Representa el nombre asignado a los datos fiscales. |
| string | phone_number | Representa el número de teléfono de los datos fiscales. |
| string | email | Representa el correo electrónico de los datos fiscales. |
| json | address | Dirección de los datos fiscales. |
| guid | company_guid | Campo que registra el guid de la empresa donde están registrados los datos fiscales. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Tax Data table](/images/TaxDataTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

📝 [Editar Documento](https://github.com/4uRest/documentation)