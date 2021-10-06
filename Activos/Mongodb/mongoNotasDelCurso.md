- 4 Crear cuenta en Mongodb Atlas  
[Mongodb Atlas](https://www.mongodb.com/es/cloud/atlas)

- 6 Instalación de Mongo en Linux

- 7 Mongo Shell  
Rel:
[Configuración de Docker para MongoDB](https://platzi.com/clases/2276-nestjs-mongodb/37106-configuracion-de-docker-para-mongodb/https://platzi.com/clases/2276-nestjs-mongodb/37106-configuracion-de-docker-para-mongodb/)

- 9 Bases de datos, Colecciones y Documentos en MongoDB  
BSON soporta mas tipos de datos que el json standard

- 10 Operaciones CRUD desde la consola de MongoDB  
Conecta a mongodb Atlas

- 11 Operaciones CRUD desde Compass

- 12 Tipos de datos

- 13 Qué son los esquemas y las relaciones  
[Otra explicación](https://www.youtube.com/watch?v=b_zr8t2g2Ic)

- 14 [Relaciones entre documentos](https://platzi.com/clases/1533-mongodb/18487-relaciones-entre-documentos/)  
**Interesante Releer**  
En relaciones 1 a 1 utilizar documentos embebidos.  
Los updates no son transaccionales.
Si la relacion es 1 a muchos
es preferible guardarlo en otra colección. Para no repetir muchas veces los datos.

- 15 [Operadores para realizar queries y proyecciones](https://platzi.com/clases/1533-mongodb/18489-operadores-para-realizar-queries-y-proyecciones/)  
**Interesante Releer**  

- 16 [Usando operadores para realizar Updates en arreglos](https://platzi.com/clases/1533-mongodb/18555-usando-operadores-para-realizar-updates-en-arreglo/)  
[MONGODB MANUAL - Operators](https://docs.mongodb.com/manual/reference/operator/)

- 17 [Operaciones avanzadas con Agregaciones](https://platzi.com/clases/1533-mongodb/18492-operaciones-avanzadas-con-agregaciones/)  
Map-Reduce(Totales), count(), estimatedDocumentCount y distinct.

- 18 Configuración e instalación de dependencias para el proyecto PlatziMongo  
Para instalar los requerimientos en un entorno virtual de python
`pip3 install -r requirements.txt`

Mongo Atlas
joriza@gmail.com
pitufo00

Db user Atlas
platzi-admin
jpIudSYHWrdp1KWY


mongodb+srv://platzi-admin:jpIudSYHWrdp1KWY@curso-platzi.f3das.mongodb.net/myFirstDatabase?retryWrites=true&w=majority

export PLATZI_DB_URI="MONGO-URI"
mongodb+srv://platzi-admin:jpIudSYHWrdp1KWY@curso-platzi.f3das.mongodb.net/

export FLASK_APP=platzi-api
export FLASK_ENV=development
export PLATZI_DB_URI="mongodb+srv://platzi-admin:jpIudSYHWrdp1KWY@curso-platzi.f3das.mongodb.net/"


Compass
mongodb+srv://platzi-admin:<password>@curso-platzi.f3das.mongodb.net/test
mongodb+srv://platzi-admin:jpIudSYHWrdp1KWY@curso-platzi.f3das.mongodb.net/test

