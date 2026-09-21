Para poder procesar este documento de manera adecuada tienes que seguir los siguientes pasos:
0.- Crea la siguiente ruta de carpetas: /content/data_lake/raw

1.- Si quieres evitar tener que crear las carpetas manualmente ejecuta el segundo bloque de codigo dentro del propio archivo:

```text
import os

carpetas = [
    "/content/data_lake",
    "/content/data_lake/procesed",
    "/content/data_lake/raw",
    "/content/data_lake/COMPLETADO"
]

for carpeta in carpetas:
    os.makedirs(carpeta, exist_ok=True)

print("Carpetas creadas correctamente.")
````
2.- Subir los siguientes archivos a la siguiente ruta: /content/data_lake/raw

customers.csv
```csv
customer_id,name,city,age
1,Alice,Madrid,25
2,Bob,Chicago,34
3,Charlie,London,29
4,Diana,Chicago,41
5,Eve,Madrid,22
6,Frank,Berlin,37
```

productos.json

```json
[
    {
        "product_id": 101,
        "product": "Laptop",
        "category": "Electronics",
        "price": 1200
    },
    {
        "product_id": 102,
        "product": "Mouse",
        "category": "Accessories",
        "price": 25
    },
    {
        "product_id": 103,
        "product": "Keyboard",
        "category": "Accessories",
        "price": 80
    },
    {
        "product_id": 104,
        "product": "Monitor",
        "category": "Electronics",
        "price": 300
    },
    {
        "product_id": 105,
        "product": "Headphones",
        "category": "Audio",
        "price": 150
    }
]
```
orders.txt

```text
1001|1|101|1
1002|2|102|2
1003|1|103|1
1004|3|104|2
1005|4|101|1
1006|5|105|2
1007|6|103|3
1008|2|105|1
```

