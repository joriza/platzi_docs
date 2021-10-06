Al menos en versiones viejas no tiene
transacciones
subquieries


[Instalar mongo db usando docker](https://platzi.com/tutoriales/1533-mongodb/4930-instalar-mongo-db-usando-docker/)
[Utiliza MongoDB desde Python](https://www.youtube.com/watch?v=pJO5gKxzsco&t=764s)
[Python Flask & Mongodb REST API](https://www.youtube.com/watch?v=GsCCyN3fRoI&t=1264s)

### Crear contenedor
docker run -d -p 27017:27017 --name mydatabase mongo:4.2

### Ingresar al contenedor
docker exec -it mydatabase bash

### Dockerfile
Sirver para crear un contenedor a partir de una imagen
El archivo debe ser con la primera letra en mayúscula y sin extensión.
El punto indica que debe tomar datos del Dockerfile.
docker build -t <nombre-contenedor> .

La primera línea siempre debe ser el nombre de una imagen.
FROM <nombre-imagen>


### Comandos de consola mongo
show dbs
use <Nombre-db>
show collections
db.<Nombre-collection>
Crear una coleccion
db.createCollection('name');

## Operaciones con documentos

### Altas (Agregar)
- Insertar un documento  
db.mongodb.insert({ejemplo: "cassandra"}) 

db.mongodb.find()  
db.mongodb.find().explain() #Mostrar detalle de la collection.

- Crear indice  
  1 = ascendente
  -1 = descendente
db.mongodb.ensureIndex({ejemplo: 1})

- Mostrar los indices creados  
db.system.indexes.find() 

- Consultar los datos  
db.mongodb.find({ejemplo: "mongodb"})  

### Bajas (Borrar)
db.ho2.remove({b:2})

Desde la version 3
en el sheel se puede asignar un documento a una variable.
y con el comanado insert 
db.collection.insert(variable)
tampbien se pueden insertar varios domucumentos con:
db.collection.insertMany([variable1, variable2])

Mostrar el primer documento
db.coll.findOne()

mostrar los n primeros documentos
db.coll.find().limit(2)

mostrar todos los documentos que cumplan una determinada condicion.
db.personas.find({Edad : {$gte: 25}}).pretty()

además indicando los campos que no quiero que se muestren.
db.personas.find({Edad : {$gte: 25}},{_id: 0})

## Modificaciones 

### Una situacion
- Actulizar una colección
  En este caso agregar una lista vacía
  3to arg. crea un documento si no existe, flase = no crea.
  4to arg. Actualiza todas las ocurrencias o solo 1. true = todas las ocurrencias
db.mongodb.update({}, {"$set": {lista: []}}, false, true )
- agrega una lista
db.mongodb.update({ejemplo: "mongodb"}, {"$set": {lista: [1,2,3]}}, false, true )

### Se puede asignar el resultado de una consulta a un avariable.
luego se puede manejar como una variable.
var1 = db.personas.findOne()
var1.Edad = 22
db.personas.save(var1)
Si no existiera el documento lo agrega.
### Con Update
db.personas.update({<condicion>},{<campos>})
Esto reemplaza la estructura de los documentos que cumplan la condición.
Tener cuidado que se pueden perder campos, pero sirve para eliminar campos.
updateOne() - solo midifica la primer coincidencia que encuentre.
updateMany() - Modifica todas las coincidencias que encuentre.
### De esta forma solo modifica los stributos indicados sin modificar estructura
db.temp.update({Nombre: "Pablo"},{$set:{Edad:34}})
db.temp.update({Nombre: "Pablo"},{$set:{"Identificaciones.DNI":34123456}})
Cuidado que tambien se puede modificar el tipo de dato.
Si el campo no existe, agrega el campo al documento.
- Agrega un campo fecha.
db.temp.update({Nombre: "Pablo"},{$set:{Fnac:ISODate("1971-01-03")}})
- Para eliminar un campo
db.temp.update({},{$unset:{Fnac3:1}})
- De la misma forma que se agrega un campo, se agrega un documento embebido.
- Por default solo modifica al primer registro que cumpla la condición.
db.temp.update({Edad: {$gte: 50}},{$set:{Nivel: 2}},{multi: true})
### Para agregar items a un campo array
https://www.youtube.com/watch?v=fkd_J2imMzc&list=PLpk46uAL3qUG3NYfYJkmREZGCX5yM3P7u&index=9
db.temp.update(
    {Nombre: "Pablo"},
        {$push:{Deporte: 
            {$each:["x3","x4"]}}})
(ver slice), tambien se puede agregar sort

### Post con varios ejemplos de modificaciones de datos.
https://charlascylon.com/2013-07-18-tutorial-mongodb-operaciones-de-actualizaci%C3%B3n-de
https://charlascylon.com/2013-07-25-tutorial-mongodb-operaciones-de-actualizaci%C3%B3n-de-ii

## Regex
db.temp.find({Nombre: /J/i})
La regex va entre // y la i indica que no sea case sensitive
db.temp.find({Nombre: {$in: [a,b,c]})
para que cumpla mas de una condicion
db.temp.find({Nombre: {$regex: /^j.*e/i})
Regex completa

## Count, Distinct y Limit
Falta ver mejor.




### Eliminar documentos
db.collection.remove() - elimina los documentos que cumplen con la colección.
db.collection.drop() - Todos los documentos de una colección.

## Proyecciones
Sin condicion, solo campos nombre
db.temp.find({},{Nombre : 1})
Sin condicion, Que no tenga campo nombre
db.temp.find({},{Nombre : 0})



{
  "Nombre": "Juan",
  "Edad": 20
}
{
  "Nombre": "Pedro"
  "Edad": 25,
}
{
  "Nombre": "Diego"
  "Edad": 30,
},

{
  "Nombre": "Fernando",
  "Edad": 55,
  "Datos":
    {
      "DNI":21735666,
      "Reg":0,
      "CUIL":0
    }
}

Inner Join con MongoDB
https://www.youtube.com/watch?v=N3ny7bvS_IM


### Consultas de un test de UDT
db.ho.find({},{_id: 0, SetupQueries: 0}) // Sin SetupQueries
db.ho.find({},{_id: 0, "TestCases": 1}) // Solo los test Cases
db.ho.find({},{_id: 0, "TestCases.Input": 1}) // Solo los campos input
db.ho.find({},{_id: 0, "TestCases.Input.Input": 1}) // Solo las frases

### Tipo dbxsql para mongodb
La version de Linux se ejecuta sin instalar, solo se descomprime.
www.robomongo.org
cd /home/javier/Descargas/temp/robo3t-1.4.3-linux-x86_64-48f7dfd/bin/

