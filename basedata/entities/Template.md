# Registro de una Empresa.

Entidad en esquema **Company** utilizada para ...

---

## 1.   Descripción de campos.

La descripción de los campos de las entidades se presenta a continuación.

Tabla Aquí

--- 

## 2.  Modelo en base de datos.

El modelo de la entidad en la base de datos con sus llaves foráneas se presenta de la siguiente manera.

![ Table](/images/ComTable.png)

Diagrama de la base de datos [(Link aquí)](https://app.diagrams.net/#G12bfdBfGq1QhoH-HbKd0D5KDiGZxJKMYT).

---

## 3.  Reglas para operaciones básicas.

Las reglas para las operaciones básicas y los campos mínimos requeridos de la entidad son:

Tabla Aquí

---

📝 [Editar Documento](https://github.com/4uRest/documentation)






## 3.  Métodos.

#### permission[POST]: 

**`Request example:`**

Este método espera una 2 campos del permisos que se desea registrar.

```json
{
    "name": "super_user_deletor",
    "description": "Puede eliminar a un super usuarios."
}
```

**`Response example:`**

Si es éxitoso. Este método retorna un código estandar HTTPS .

```
200 OK
``` 

#### permission[GET]: 

**`Request example:`**

Este método espera el campo guid del permiso que se desea consultar.

```
    guid: b57e07fd-c61c-478f-ba8f-61630f4a52ad
```

**`Response example:`**

Este método retorna el permiso registrado.

```json
{
    "guid": "b57e07fd-c61c-478f-ba8f-61630f4a52ad",
    "name": "super_user_viewer",
    "description": "Puede ver los datos de un super usuario."
}
``` 

#### super_permission_list[GET]: 

**`Response example:`**

Este método retorna una lista de permisos registrados.


```json
{  
  "response":[
    {
        "guid": "b57e07fd-c61c-478f-ba8f-61630f4a52ad",
        "name": "super_user_viewer",
        "description": "Puede ver los datos de un super usuario."
    },
    {
        "guid": "02fed7ee-174e-4918-99ae-627b53dff037",
        "name": "super_user_creator",
        "description": "Puede crear super usuarios."
    },
    {
        "guid": "4ca2c838-77c7-452a-92f6-a005f0129c59",
        "name": "super_user_editor",
        "description": "Puede editar los datos de un super usuario."
    },
    {
        "guid": "7edfc905-d0ab-4e5a-b4dd-2aa5737095fe",
        "name": "super_user_deletor",
        "description": "Puede eliminar a un super usuarios."
    }
]
}
``` 

---