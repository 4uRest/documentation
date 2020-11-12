# Ingredientes

Entidad utilizada para representar ingredientes de recetas de productos y productos semi-elaborados. Un conjunto de ingredientes forman una receta. La descripción de los campos se representa de la siguiente manera:

### Interpretación de la tabla
* Parámetro
    * Representa el campo en la base de datos.

* Descripción
    * Explicación de función del campo.

* Tipo de dato
    * Representación del tipo de dato esperado del campo.

* Valores por defecto
    * **Generado tipo 1:** *Valor generado desde el sistema al momento de la operación ejecutada.* 
    * **Generado tipo 2:** *Valor proporciondo desde el sistema. No es creado al momento de la operación que se esta ejecutando, éste se viene guardando desde alguna operación anterior.*
    * **Requerido tipo 1:** *Valor proporciondo por el usuario.* 
    * **Requerido tipo 2:** *Valor seleccionado por el usuario en un rango de opciones del sistema.* 

Tabla Ingredientes (**Ingredients**)

| Parámetro | Descripción | Tipo de dato | Valor por defecto |
|-|-|-|-|
| ingredient_id | ID del ingrediente. | Número entero | Generado tipo 1|
| ingredient_name | Nombre del ingrediente. | Texto | Requerido tipo 1|
| category_id | ID de la categoría donde el ingrediente se encuentra. | Número entero | 0 - Requerido tipo 1|
| ingredient_left | Inventario del ingrediente. | Decimal | 0 |
| limit_value | Umbral de alerta de stock bajo del ingrediente en almacenamiento. | Decimal | 0 |
| time_notif | La fecha y hora de la última notificación del umbral de alerta de stock bajo del ingrediente almacenado. | Fecha y hora | NULL |
| ingredient_unit | Unidad del ingrediente: kg — kilogramos, p — piezas, l — litros. | Texto | Requerido tipo 2|
| ingredient_weight | Peso del ingrediente si el ingrediente se vende por pieza. | Decimal | 0 |
| ingredients_losses_clear | Tasa de pérdida en la limpieza del ingrediente, si el ingrediente no se vende por pieza. | Decimal | 0 |
| ingredients_losses_cook | Tasa de pérdida en el horneado del ingrediente si el ingrediente no se vende por pieza. | Decimal | 0 |
| ingredients_losses_fry | Tasa de pérdida en el ingrediente que se fríe si el ingrediente no se vende por pieza. | Decimal | 0 |
| ingredients_losses_stew | Tasa de pérdida en el guisado de ingredientes si el ingrediente no se vende por pieza. | Decimal | 0 |
| ingredients_losses_bake | Tasa de pérdida en la cocción del ingrediente si el ingrediente no se vende por pieza. | Decimal | 0 |
| ingredients_type | Tipo de ingrediente: 1 — ingrediente, 2 — ingrediente sistémico. | Número entero | Generado tipo 1|
| partial_write_off | El estado de un ingrediente vendido por pieza que se permite desperdiciar como el que se vende por fracciones: 0 - no permitido, 1 - permitido. | Número entero | 0 |
| hidden | El estado de un ingrediente oculto: 0 — no oculto, 1 — oculto. Valor por defecto 0. | Número entero | 0 |
| createdAt | Fecha en la que se crea la categoría. | Fecha y hora | Generado tipo 1|
| updatedAt | Fecha en la que se actualiza el ingrediente. | Fecha y hora | Generado tipo 1|
| deletedAt | Fecha en la que se elimina el ingrediente. Null—No eliminado. Valor por defecto null. | Fecha y hora | NULL |
| subsidiary_id | ID de la sucursal a la que pertenece el ingrediente. | Número entero | Generado tipo 2|

📝 [Editar Documento](https://github.com/4uRest/documentation)