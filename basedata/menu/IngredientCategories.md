# Categorías de ingredientes

Entidad utilizada para clasificar/agrupar ingredientes. El detalle de los campos de la tabla en la base de datos son:

**Generado:** *Valor proporciondo desde el sistema* 

**Requerido tipo 1:** *Valor proporciondo por el usuario* 

**Requerido tipo 2:** *Valor seleccionado por el usuario en un rango de opciones del sistema* 

| Parámetro | Descripción | Tipo de dato | Valor por defecto |
|-|-|-|-|
| id | ID único y autoincrementable de la categoría. | Número entero | Generado |
| name | Nombre único de la categoría. | Texto | Requerido |
| createdAt | Fecha en la que se crea la categoría. | Fecha y hora | Generado |
| updatedAt | Fecha en la que se actualiza la categoría. | Fecha y hora | Generado |
| deletedAt | Fecha en la que se elimina la categoría. Null—No eliminado. Valor por defecto null. | Fecha y hora | NULL |
| subsidiary_id | ID de la sucursal a la que pertenece la categoría. | Número entero | Generado |