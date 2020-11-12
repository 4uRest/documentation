# Users

| Parámetro | Descripción | Tipo de dato |
|-|-|-|
| user_id | ID único y autoincrementable del registro. | Número entero |
| name | Nombre único del empleado. | Texto |
| last_name | Apellidos del empleado. | Texto |
| phone_number | Número telefónico del empleado. | Texto |
| birthdate | Fecha de nacimiento del empleado | Fecha y hora |
| icon | Url de dirección del empleado. | Texto |
| rol_id | ID del rol asignado al empleado. | Número entero |
| email | Correo electrónico del empleado para acceso al módulo administrativo. | Texto |
| password | Clave del empleado para acceso al módulo administrativo. | Texto |
| pos_pin | Clave del empleado para acceso al módulo POS. | Número entero |
| inactive | Estado del empleado para acceso al sistema administrativo y operativo. 0—Activo en el sistema, 1—inactivo en los sistemas, por lo que no podrá tener acceso. | Número entero |
| createdAt | Fecha en la que se crea el registro. | Fecha y hora |
| updatedAt | Fecha en la que se actualiza el registro. | Fecha y hora |
| deletedAt | Fecha en la que se elimina el registro. Null—No eliminado. Valor por defecto null. | Fecha y hora |
| subsidiary_id | ID de la sucursal a la que pertenece el registro.. | Número entero |

📝 [Edit document](https://github.com/4uRest/documentation)