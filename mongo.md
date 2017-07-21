## Comandos Globales

| Comando | What do |
| --- | --- |
| use *name* | _Crea o se conecta a una db_
| db | _Muestra las listas de dbs_ |
| show dbs | _Lista las dbs_ |
| show collections | _Lista las colecciones_ |

## Comandos en DB
| Comando | What do |
| --- | --- |
| createCollection(*name*) | Crear una coleccion |


## Comandos en Colecciones
| Command | What do |
| --- | --- |
| drop() | Drop collection |
| insert(*document* ) | Insert a document |

```
.find(criteria, keyBool?)
.findOne()
.update(criteria, data)
.remove(criteria?, number?)
.limit(number)
.skip(number)
.sort({ key: -1|1 })
```
