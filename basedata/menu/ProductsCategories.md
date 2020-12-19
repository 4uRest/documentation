# Categorias de productos 

Entidad utilizada para clasificar/agrupar productos. El detalle de los campos de la tabla en la base de datos son:

| Parámetro | Descripción | Tipo de dato |
|-|-|-|
| id | ID único y autoincrementable de la categoría. | Número entero |
| name | Nombre único de la categoría. | Texto |
| parent_category_id | ID de la categoría padre. | Número entero |
| color | Color de la tarjeta del producto: blanco, naranja, amarillo,verde, azul, azul marino, morado,negro, azul menta, verde lima, rosa. El color predeterminado es blanco. | Texto |
| icon | URL de dirección de la imagen. | Texto |
| hidden | Estado de visibilidad de una categoría: 0 — no oculta, 1 — oculta. El valor predeterminado es 0. | Número entero |
| createdAt | Fecha en la que se crea la categoría | Fecha y hora |
| updatedAt | Fecha en la que se actualiza la categoría | Fecha y hora |
| deletedAt | Fecha en la que se elimina la categoría | Fecha y hora |
| subsidiary_id | ID de la sucursal a la que pertenece el registro | Número entero |

Si el valor “hidden” de la categoría se encuentra en 0. La visibilidad de las categorías se puede personalizar en días y horarios específicos de la semana. Estos datos se guardan en un archivo JSON. Los campos por día son los siguientes

* status: El estado de visibilidad de una categoría en un determinado día, el valor predeterminado es 0:
    * 0 — activa todo el día, 
    * 1 —  activa en horario específico, 
    * 2 — inactiva. 
* start_time: Si el parámetro “status” se encuentra en 1, la categoría se mostrará en la hora indicada en start_time.
* end_time: Si el parámetro “status” se encuentra en 1 la categoría se dejará de mostrar en la hora indicada en end_time.

Ejemplo de una categoría que sólo está activa viernes, sábado y domingo.

```json
{
"availability":[
	{
"subsidiary_id": "2" ,
“schedule_monday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_tuesday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_wednesday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_thursday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_friday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_saturday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_sunday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
}

},
{
"subsidiary_id": "39" ,
“schedule_monday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_tuesday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_wednesday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_thursday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_friday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_saturday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
},
“schedule_sunday”:    {
        "status": "2" ,
        "start_time": "00:00",
        "end_time": "00:00",
}

},

]
}
```

📝 [Editar Documento](https://github.com/4uRest/documentation)