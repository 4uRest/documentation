# Ingredientes

Entidad utilizada para representar ingredientes de recetas de productos y productos semi-elaborados. Un conjunto de ingredientes forman una receta.

### **Tabla en base de datos.**

|  | Ingredient |
|-|-|
| **PK** | ingredient_id |
|  | ingredient_name |
| **FK** | category_id |
|  | ingredient_left |
|  | limit_value |
|  | time_notif |
|  | ingredient_unit |
|  | ingredient_weight |
|  | ingredients_losses_clear |
|  | ingredients_losses_cook |
|  | ingredients_losses_fry |
|  | ingredients_losses_stew |
|  | ingredients_losses_bake |
|  | ingredients_type |
|  | partial_write_off |
|  | hidden |
|  | created_at |
|  | updated_at |
|  | deleted_at |
| **FK** | subsidiary_id |

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G1TR1Q9nC36PcOae7jeaJIxgDLTjUUpkfL).

### **Descripción de campos.**

La descripción de los campos se representa de la siguiente manera:

| Parámetro | Descripción | Tipo de dato |
|-|-|-|
| ingredient_id | ID del ingrediente. | Número entero |
| ingredient_name | Nombre del ingrediente. | Texto |
| category_id | ID de la categoría donde el ingrediente se encuentra. | Número entero |
| ingredient_left | Inventario del ingrediente. | Decimal |
| limit_value | Umbral de alerta de stock bajo del ingrediente en almacenamiento. | Decimal |
| time_notif | La fecha y hora de la última notificación del umbral de alerta de stock bajo del ingrediente almacenado. | Fecha y hora |
| ingredient_unit | Unidad del ingrediente: kg — kilogramos, p — piezas, l — litros. | Texto |
| ingredient_weight | Peso del ingrediente si el ingrediente se vende por pieza. | Decimal |
| ingredients_losses_clear | Tasa de pérdida en la limpieza del ingrediente, si el ingrediente no se vende por pieza. | Decimal |
| ingredients_losses_cook | Tasa de pérdida en el horneado del ingrediente si el ingrediente no se vende por pieza. | Decimal |
| ingredients_losses_fry | Tasa de pérdida en el ingrediente que se fríe si el ingrediente no se vende por pieza. | Decimal |
| ingredients_losses_stew | Tasa de pérdida en el guisado de ingredientes si el ingrediente no se vende por pieza. | Decimal |
| ingredients_losses_bake | Tasa de pérdida en la cocción del ingrediente si el ingrediente no se vende por pieza. | Decimal |
| ingredients_type | Tipo de ingrediente: 1 — ingrediente, 2 — ingrediente sistémico. | Número entero |
| partial_write_off | El estado de un ingrediente vendido por pieza que se permite desperdiciar como el que se vende por fracciones: 0 - no permitido, 1 - permitido. | Número entero |
| hidden | El estado de un ingrediente oculto: 0 — no oculto, 1 — oculto. Valor por defecto 0. | Número entero |
| createdAt | Fecha en la que se crea la categoría. | Fecha y hora |
| updatedAt | Fecha en la que se actualiza el ingrediente. | Fecha y hora |
| deletedAt | Fecha en la que se elimina el ingrediente. Null—No eliminado. Valor por defecto null. | Fecha y hora |
| subsidiary_id | ID de la sucursal a la que pertenece el ingrediente. | Número entero |

📝 [Editar Documento](https://github.com/4uRest/documentation)