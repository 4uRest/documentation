# Categorías de ingredientes

Entidad utilizada para clasificar/agrupar ingredientes.

### **Tabla en base de datos.**

|  | Ingredient_category |
|-|-|
| **PK** | category_id |
|  | category_name |
|  | created_at |
|  | updated_at |
|  | deleted_at |
| **FK** | subsidiary_id |

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G1TR1Q9nC36PcOae7jeaJIxgDLTjUUpkfL).

### **Descripción de campos.**

El detalle de los campos de la tabla en la base de datos son:

| Parámetro | Descripción | Tipo de dato |
|-|-|-|
| category_id | ID único y autoincrementable de la categoría. | Número entero |
| category_name | Nombre único de la categoría. | Texto |
| created_at | Fecha en la que se crea la categoría. | Fecha y hora |
| updated_at | Fecha en la que se actualiza la categoría. | Fecha y hora |
| deleted_at | Fecha en la que se elimina la categoría. Null—No eliminado. Valor por defecto null. | Fecha y hora |
| subsidiary_id | ID de la sucursal a la que pertenece la categoría. | Número entero |

📝 [Editar Documento](https://github.com/4uRest/documentation)