# Registro de una Empresa.

Entidad en esquema **Master** utilizada para primer contacto cuando se intenta registrar una empresa en el sistema. Esta entidad hace un respaldo de los datos del formulario de registro sin crear el esquema a la empresa hasta que cumpla con la confirmación del correo electrónico.

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | company_name | Representa el nombre asignado la empresa. |
| string | subsidiary_name | Representa el nombre asignado la sucursal. |
| guid | business_model_guid | Guid del modelo de negocio asignado. |
| string | user_name | Representa el nombre del usuario. |
| string | user_last_name | Representa los apellidos del usuario. |
| string | user_phone_number | Representa el número de teléfono del usuario. |
| string | user_email | Representa el correo electrónico del usuario. |
| string | user_password | Representa la clave de acceso al sistema del usuario. |
| byte | email_confirmed | Valor que representa el estado de verificación del correo electrónico: 0—no confirmado, 1—confirmado. Por defecto es 0. |
| byte | phone_number_confirmed | Valor que representa el estado de verificación del número teléfonico: 0—no confirmado, 1—confirmado. Por defecto es 0. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Master Company Sign Up Table](/images/MasterCompanySignUpTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

| Entitie | Campos de entrada mínimos | Reglas para Create | Reglas para Update | Reglas para Soft Delete |
|-|-|-|-|-|
| CompanySignUp | company_name, subsidiary_name, business_model_guid, user_name, user_last_name, user_phone_number, user_email, user_password | Se genera: id, created_at. Se cumple con campos de entrada mínimos. | El usuario debe de confirmar el correo electrónico o el número de teléfono. Se genera: updated_at. | No se puede ejecutar la operación. |

---

📝 [Editar Documento](https://github.com/4uRest/documentation)