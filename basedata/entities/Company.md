_ _ _

# 1. Empresa

Entidad utilizada para registrar empresas en el sistema. Una empresa es capaz de tener entidades como:

* grupos de sucursales,
* usuario,
* menus,
* etc.,

pertenecientes a ella. Un usuario registrado en el sistema siempre pertenece a una empresa.

<!-- Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G1TR1Q9nC36PcOae7jeaJIxgDLTjUUpkfL). -->
_ _ _

## 2.Descripción de campos.

El detalle de los campos de la tabla en la base de datos son:

| Tipo | Campo | Descripción |
|-|-|-|
| guid | guid | Es el identificador único y llave primaria de tipo guid. |
| int | id | Registro único y auto incrementable de la tabla. |
| string | name | Representa el nombre asignado a la compañía. |
| string | phone_number | Representa el número de teléfono de la empresa. |
| string | email | Representa el email de de la empresa. |
| json | address | Dirección de la empresa, en el punto 3 se desglosa y describe su estructura. |
| guid | tax_data_guid | Campo que registra el guid de registro de los datos fiscales de la empresa. |
| guid | creator_user_guid | Campo que registra el guid del creador del registro. |
| guid | updater_user_guid | Campo que registra el guid del editor/modificador del registro. |
| guid | deletor_user_guid | Campo que registra el guid del eliminador del registro. |
| datetime | created_at | Campo que registra la hora y fecha de la creación del registro. |
| datetime | updated_at | Campo que registra la hora y fecha de la actualización/modificación del registro. |
| datetime | deleted_at | Campo que registra la hora y fecha de la eliminación del registro. |


---

## 3.  Descripción del Json "Address".

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

## 4.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![Company table](/images/CompanyTable.png)

_ _ _

📝 [Editar Documento](https://github.com/4uRest/documentation/blob/master/basedata/entities/Company.md)