# Fundamentos de Bases de Datos

## 2 [Historia de las RDB](https://platzi.com/clases/1566-bd/20196-historia-de-las-rdb/)

Las bases de datos surgen de la necesidad de conservar la información más allá de lo que existe en la memoria RAM.

Las bases de datos basadas en archivos eran datos guardados en texto plano, fáciles de guardar pero muy difíciles de consultar y por la necesidad de mejorar esto nacen las bases de datos relacionales. Su inventor Edgar Codd dejó ciertas reglas para asegurarse de que toda la filosofía de las bases de datos no se perdiera, estandarizando el proceso.

Codd inventó el álgebra relacional.

![Cuadro](https://www.mindmeister.com/es/1079684487/las-12-reglas-de-codd-del-modelo-relacional?fullscreen=1)

## 3 [Entidades y atributos](https://platzi.com/clases/1566-bd/20197-entidades-y-atributos/)

La nomenclatura que se esta usando para representar las entidades se llama Notacion de Chen.

![Cuadro](https://static.platzi.com/media/user_upload/img-2e2fc1ba-ad77-4045-b7a5-f74a65e3f55e.jpg)

Una entidad es algo similar a un objeto (programación orientada a objetos) y representa algo en el mundo real, incluso algo abstracto. Tienen atributos que son las cosas que los hacen ser una entidad y por convención se ponen en plural.
Los atributos compuestos son aquellos que tienen atributos ellos mismos.
Los atributos llave son aquellos que identifican a la entidad y no pueden ser repetidos. Existen:
- Naturales: son inherentes al objeto como el número de serie
- Clave artificial: no es inherente al objeto y se asigna de manera arbitraria.
Entidades fuertes: son entidades que pueden sobrevivir por sí solas.
Entidades débiles: no pueden existir sin una entidad fuerte y se representan con un cuadrado con doble línea.
- Identidades débiles por identidad: no se diferencian entre sí más que por la clave de su identidad fuerte.
- Identidades débiles por existencia: se les asigna una clave propia.

![Cuadro](https://static.platzi.com/media/user_upload/Entidades%20y%20Atributos-09c8f49e-1dc2-48b5-be62-8ad93483fd3d.jpg)

## 4 [Entidades de Platzi Blog](https://platzi.com/clases/1566-bd/20198-entidades-de-platzi-blog/)

Nuestro proyecto será un manejador de Blogpost. Es un contexto familiar y nos representará retos muy interesantes.
- Primer paso: Identificar las entidades
- Segundo paso: Pensar en los atributos

## 4 [Relaciones](https://platzi.com/clases/1566-bd/20199-relaciones/)

Las relaciones nos permiten ligar o unir nuestras diferentes entidades y se representan con rombos. Por convención se definen a través de verbos.

Las relaciones tienen una propiedad llamada cardinalidad y tiene que ver con números. Cuántos de un lado pertenecen a cuántos del otro lado:
- Cardinalidad: 1 a 1
- Cardinalidad: 0 a 1
- Cardinalidad: 1 a N
- Cardinalidad: 0 a N

## 7 [DER](https://static.platzi.com/media/user_upload/diagrama%20ER-ed0a237c-3e8e-4057-83f2-07fbac9c8548.jpg)

Diagrama Entidad Relación del proyecto
![Cuadro](https://static.platzi.com/media/user_upload/diagrama%20ER-ed0a237c-3e8e-4057-83f2-07fbac9c8548.jpg)

## 8 [Diagrama Físico: tipos de datos y constraints](https://platzi.com/clases/1566-bd/20202-diagrama-fisico-y-tipos-datos-y-constraints0863/)

Algo muy importante sobre el ahorro de memoria a la hora de poner el diagrama de la base de datos en el mundo real (En el motor de base de datos ya sea SQLSERVER o Oracle). El Char sirve para declarar un campo rigido de disco que vamos a ocupar y el varchar puede cambiar la longitud dependiento del largo de los datos que metamos en el. Seguramente esten pensando que lo mejor es un varchar para todo ya que es dinamico. Pero que el motor de base de datos haga los procesos de calcular la nueva longitud de cada dato del tipo varchar que ingresemos nos puede dar problemas de rendimiento. Si estamos seguros que un dato solo ocupara un char de 5 ocupemos un char de 5. Estas son algunas de las buenas practicas que se debe tener para el funcionamiento de un motor de base de datos.

Tipos de datos
![Cuadro](https://static.platzi.com/media/user_upload/Tipos%20de%20dato-a19128d2-687f-4655-9a65-ea5deb252697.jpg)

Constraints
![Cuadro](https://static.platzi.com/media/user_upload/Captura%20de%20pantalla%20%2828%29-4e756f67-0052-447f-9dcd-cb9bded3b935.jpg)

## 9 [Diagrama Físico: normalización](https://platzi.com/clases/1566-bd/20203-diagrama-fisico-normalizacion8011/)

La normalización como su nombre lo indica nos ayuda a dejar todo de una forma normal. Esto obedece a las 12 reglas de Codd y nos permiten separar componentes en la base de datos:
- Primera forma normal (1FN): Atributos atómicos (Sin campos repetidos)
- Segunda forma normal (2FN): Cumple 1FN y cada campo de la tabla debe depender de una clave única.
- Tercera forma normal (3FN): Cumple 1FN y 2FN y los campos que NO son clave, NO deben tener dependencias.
- Cuarta forma normal (4FN): Cumple 1FN, 2FN, 3FN y los campos multivaluados se identifican por una clave única.

## 10 [Diagrama Físico: normalizando Platziblog](https://platzi.com/clases/1566-bd/20204-diagrama-fisico-normalizando-platziblog2443/)

![Cuadro](https://static.platzi.com/media/user_upload/blogPost-47d19fa7-958a-4df5-b977-8246dd359890.jpg)

## 12 [RDB ¿Qué?](https://platzi.com/clases/1566-bd/20205-rdb-que4374/)

RDBMS significa Relational Database Management System o sistema manejador de bases de datos relacionales. Es un programa que se encarga de seguir las reglas de Codd y se puede utilizar de manera programática.

## 18 [Historia de SQL](https://platzi.com/clases/1566-bd/20210-historia-de-sql/)

SQL significa Structured Query Language y tiene una estructura clara y fija. Su objetivo es hacer un solo lenguaje para consultar cualquier manejador de bases de datos volviéndose un gran estándar.

Ahora existe el NOSQL o Not Only Structured Query Language que significa que no sólo se utiliza SQLen las bases de datos no relacionales.

## 19 [DDL create](https://platzi.com/clases/1566-bd/20211-ddl-create8613/)

SQL tiene dos grandes sublenguajes:
DDL o Data Definition Language que nos ayuda a crear la estructura de una base de datos. Existen 3 grandes comandos:

- Create: Nos ayuda a crear bases de datos, tablas, vistas, índices, etc.
- Alter: Ayuda a alterar o modificar entidades.
- Drop: Nos ayuda a borrar. Hay que tener cuidado al utilizarlo.

3 objetos que manipularemos con el lenguaje DDL:

- Database o bases de datos
- Table o tablas. Son la traducción a SQL de las entidades
- View o vistas: Se ofrece la proyección de los datos de la base de datos de forma entendible.

## 20 [CREATE VIEW y DDL ALTER](https://platzi.com/clases/1566-bd/20212-create-view-y-ddl-alter/)

## 21 [DDL Drop](https://platzi.com/clases/1566-bd/20213-ddl-drop7001/)

![Cuadro](https://static.platzi.com/media/user_upload/Comandos%20SQL-72cd96bf-3335-40a8-adaa-f5b444efcc4d.jpg)

[¿Qué es DDL, DML, DCL y TCL? + Integridad Referencial](https://platzi.com/blog/que-es-ddl-dml-dcl-y-tcl-integridad-referencial/)

## 23 [¿Qué tan standard es SQL](https://platzi.com/clases/1566-bd/19808-que-tan-standard-es-sql/)

La utilidad más grande de SQL fue unificar la forma en la que pensamos y hacemos preguntas a un repositorio de datos. Ahora que nacen nuevas bases de datos igualmente siguen tomando elementos de SQL.

## 26 [Creando Platziblog: tablas transitivas](https://platzi.com/clases/1566-bd/19811-creando-platziblog-tablas-transistivas/)

- Las tablas transitivas sirven como puente para unir dos tablas. No tienen contenido semántico.
- **Reverse Engineer** nos reproduce el esquema del cual nos basamos para crear nuestras tablas. Es útil cuando llegas a un nuevo trabajo y quieres entender cuál fue la mentalidad que tuvieron al momento de crear las bases de datos.

## 27 [¿Por qué las consultas son tan importantes?](https://platzi.com/clases/1566-bd/19812-por-que-las-consultas-son-tan-importantes/)

Las consultas o queries a una base de datos son una parte fundamental ya que esto podría salvar un negocio o empresa.
Alrededor de las consultas a las bases de datos se han creado varias especialidades como ETL o transformación de datos, business intelligence e incluso machine learning.

## 28 [Estructura básica de un Query](https://platzi.com/clases/1566-bd/19817-estructura-basica-de-un-query/)

Los queries son la forma en la que estructuramos las preguntas que se harán a la base de datos. Transforma preguntas en sintaxis.

El query tiene básicamente 2 partes: SELECT y FROM y puede aparecer una tercera como WHERE.

La estrellita o asterisco (*) quiere decir que vamos a seleccionar todo sin filtrar campos.


ESTRUCTURA DE UN QUERY

- Como le hacemos preguntas a las bases de datos? Los queries transforman nuestras preguntas en el lenguaje que utiliza la base de datos.
- Dos partes mas una tercera opcional:
  - SELECT : que datos queremos obtener (que columnas/campos de la tabla).
  - FROM : de donde los queremos obtener (de que tabla, por ejemplo).
  - WHERE : condicion que deben cumplir o filtro que deben pasar los datos a obtener. Es opcional, pero se suele utilizar, ya que sino se obtienen todos los datos sin filtrar ninguno.
- Otras sentencias:
  - GROUP BY : de que manera agrupamos los datos (en este caso agrupa por ciudad).
  - ORDER BY : de que manera ordenamos los datos (en este caso, por poblacion).
  - HAVING : otra manera de filtrar los datos.

## 20 [SELECT](https://platzi.com/clases/1566-bd/19818-select/)

SELECT se encarga de proyectar o mostrar datos.

- El nombre de las columnas o campos que estamos consultando puede ser cambiado utilizando AS después del nombre del campo y poniendo el nuevo que queremos tener:
``` sql
SELECT titulo AS encabezado
FROM posts;
```
- Existe una función de SELECT para poder contar la cantidad de registros. Esa información (un número) será el resultado del query:
``` sql
SELECT COUNT(*)
FROM posts;
```

## 30 [FROM](https://platzi.com/clases/1566-bd/19819-from/)

![Cuadro](https://static.platzi.com/media/user_upload/joins-bbf371dd-2c73-4de6-996e-bcac7fdca4f1.jpg)

![Cuadro](https://static.platzi.com/media/user_upload/ae6e9906853414a0dedddfe7a6dfd716-21510c4e-f8db-4ad0-8aa9-05080b7c1649.jpg)

## 32 [WHERE](https://platzi.com/clases/1566-bd/19821-where/)

**WHERE** es la sentencia que nos ayuda a filtrar tuplas o registros dependiendo de las características que elegimos.

- La propiedad LIKE nos ayuda a traer registros de los cuales conocemos sólo una parte de la información.
- La propiedad BETWEEN nos sirve para arrojar registros que estén en el medio de dos. Por ejemplo los registros con id entre 20 y 30.

Cabe mencionar que los operadores LIKE y BETWEEN AND, pueden ser negados con NOT
NOT LIKE
NOT BETWEEEN – AND –

## 33 [Utilizando la sentencia WHERE nulo y no nulo](https://platzi.com/clases/1566-bd/19822-utilizando-la-sentencia-where-nulo-y-no-nulo/)

El valor nulo en una tabla generalmente es su valor por defecto cuando nadie le asignó algo diferente. La sintaxis para hacer búsquedas de datos nulos es IS NULL. La sintaxis para buscar datos que no son nulos es IS NOT NULL

## 34 [GROUP BY](https://platzi.com/clases/1566-bd/19823-group-by/)

GROUP BY tiene que ver con agrupación. Indica a la base de datos qué criterios debe tener en cuenta para agrupar.

## 35 [ORDER BY y HAVING](https://platzi.com/clases/1566-bd/19824-order-by-y-having/)

La sentencia ORDER BY tiene que ver con el ordenamiento de los datos dependiendo de los criterios que quieras usar.

    ASC sirve para ordenar de forma ascendente.
    DESC sirve para ordenar de forma descendente.
    LIMIT se usa para limitar la cantidad de resultados que arroja el query.

HAVING tiene una similitud muy grande con WHERE, sin embargo el uso de ellos depende del orden. Cuando se quiere seleccionar tuplas agrupadas únicamente se puede hacer con HAVING.

## 35.1 [mapa mental con el resumen de las 35 clases anteriores y esta incluida](https://www.goconqr.com/mindmap/22606096/fundamentos-de-bases-de-datos)

## 36 [El interminable agujero de conejo - Nested queries](https://platzi.com/clases/1566-bd/19825-el-interminable-agujero-de-conejo-nested-queries/)

Significan que dentro de un query podemos hacer otro query. Esto sirve para hacer join de tablas, estando una en memoria. También teniendo un query como condicional del otro.

Este proceso puede ser tan profundo como quieras, teniendo infinitos queries anidados.
Se le conoce como un producto cartesiano ya que se multiplican todos los registros de una tabla con todos los del nuevo query. Esto provoca que el query sea difícil de procesar por lo pesado que puede resultar.

## 37 [¿Cómo convertir una pregunta en un query SQL?](https://platzi.com/clases/1566-bd/19826-como-convertir-una-pregunta-en-un-query-sql/)

De pregunta a Query

    SELECT: Lo que quieres mostrar
    FROM: De dónde voy a tomar los datos
    WHERE: Los filtros de los datos que quieres mostrar
    GROUP BY: Los rubros por los que me interesa agrupar la información
    ORDER BY: El orden en que quiero presentar mi información
    HAVING: Los filtros que quiero que mis datos agrupados tengan


Quiero obtener todos los post creados por edgar@com

    SELECT: Lo que quieres mostrar
        Nickname
        Titulo del post
    FROM: De dónde voy a tomar los datos
        Tabla usuarios y post
    WHERE: Los filtros de los datos que quieres mostrar
        Deben de ser de edgar@com
    GROUP BY: Los rubros por los que me interesa agrupar la información
        No deseo agrupar
    ORDER BY: El orden en que quiero presentar mi información
        por fecha de publicación
    HAVING: Los filtros que quiero que mis datos agrupados tengan


## 38 [Preguntándole a la base de datos](https://platzi.com/clases/1566-bd/19827-preguntandole-a-la-base-de-datos/)

GROUP_CONCAT toma el resultado del query y lo pone como campo separado por comas.

## 40 [¿Qué son y cuáles son los tipos de bases de datos no relacionales?](https://platzi.com/clases/1566-bd/19813-que-son-y-cuales-son-los-tipos-de-base-datos-no-re/)

Respecto a las bases de datos no relacionales, no existe un solo tipo aunque se engloben en una sola categoría.

Tipos de bases de datos no relacionales:

- Clave - valor: Son ideales para almacenar y extraer datos con una clave única. Manejan los diccionarios de manera excepcional. Ejemplos: DynamoDB, Cassandra.
- Basadas en documentos: Son una implementación de clave valor que varía en la forma semiestructurada en que se trata la información. Ideal para almacenar datos JSON y XML. Ejemplos: MongoDB, Firestore.
- Basadas en grafos: Basadas en teoría de grafos, sirven para entidades que se encuentran interconectadas por múltiples relaciones. Ideales para almacenar relaciones complejas. Ejemplos: neo4j, TITAN.
- En memoria: Pueden ser de estructura variada, pero su ventaja radica en la velocidad, ya que al vivir en memoria la extracción de datos es casi inmediata. Ejemplos: Memcached, Redis.
- Optimizadas para búsquedas: Pueden ser de diversas estructuras, su ventaja radica en que se pueden hacer queries y bú squedas complejas de manera sencilla. Ejemplos: BigQuery, Elasticsearch.

## 41 [Servicios administrados y jerarquía de datos](https://platzi.com/clases/1566-bd/19814-servicios-administrados-y-jerarquia-de-datos/)

Firebase es un servicio de Google donde puedes tercerizar muchos elementos en la nube.
Jerarquía de datos:

    Base de datos
    Colección
    Documento
## 42 [Top level collection con Firebase](https://platzi.com/clases/1566-bd/19815-top-level-collection-con-firebase/)

Como crear una base de datos en Firebase.  
Como crear una colección.
## 43 [Creando y borrando documentos en Firestore](https://platzi.com/clases/1566-bd/19816-creando-y-borrando-documentos-en-firestore/)

Tipos de datos en Firestore:

- String: Cualquier tipo de valor alfanumérico
- Number: Soporta enteros y flotantes.
- Boolenan: Los clásicos valores True y False
- Map: Permite agregar un documento dentro de otro.
- Array: Permite agregar un conjunto de datos (soporte multi type) sin nombre e identificador.
- Null: Indica que no se ha definido un valor.
- Timestamp: Permite almacenar fechas (guarda el año, mes, día y hora).
- Geopoint: Guarda una localización geográfica (coordenadas latitud-longitud).
- Reference: Permite referencia un documento (relaciona dos documentos, no importa su colección).

## 44 [Colecciones vs subcolecciones](https://platzi.com/clases/1566-bd/19828-colecciones-vs-subcolecciones/)
## 48 [Bases de datos en la vida real](https://platzi.com/clases/1566-bd/19829-bases-de-datos-en-la-vida-real/)

Hoy en dia, se utilizan diversos tipos de bases de datos segun el problema que se quiera resolver:

- Las bases de datos relacionales, durante mucho tiempo, fueron utilizadas para resolver todo tipo de situaciones, pero al aumentar enormemente el numero de datos a manejar, se volveron ineficientes en muchos casos.
- Firestore o MongoDB nos permiten obtener los datos actuales de la aplicacion de manera simple. Sin embargo, no nos permite hacer, por ejemplo, queries muy complejos.
- En una misma disciplina, es probable que haya que utilizar mas de un tipo de bases de datos.

## 49 [Big Data](https://platzi.com/clases/1566-bd/19830-big-data/)

la definición ahora muy popular del big data como las tres Vs:

- Volumen. Las organizaciones recopilan datos de diversas fuentes, incluyendo transacciones comerciales, medios sociales e información de sensores o que se transmite de una máquina a otra. En el pasado, almacenarlos habría sido un problema – pero nuevas tecnologías (como Hadoop) han aligerado la tarea.  
- Velocidad. Los datos se transmiten a una velocidad sin precedentes y se deben distribuir de manera oportuna. Etiquetas FID, sensores y la medición inteligente crean la necesidad de distribuir torrentes de datos casi en tiempo real.  
- Variedad. Los datos vienen en toda clase de formatos – desde datos numéricos estructurados en bases de datos tradicionales hasta documentos de texto no estructurados, correo electrónico, video, audio, datos de teletipo bursátil y transacciones financieras.  

Los datos de la actualidad provienen de múltiples fuentes, lo que hace difícil vincular, empatar, depurar y transformar datos entre diferentes sistemas. Sin embargo, es necesario conectar y correlacionar relaciones, jerarquías y múltiples vínculos de datos o sus datos se pueden salir de control en un segundo.

## 50 [Data warehouse](https://platzi.com/clases/1566-bd/19831-data-warehouse/)

En primer lugar, DW no es un producto que pueda ser comprado en el mercado, sino más bien un concepto que debe ser construido. DW es una combinación de conceptos y tecnología que cambian significativamente la manera en que es entregada la información a la gente de negocios. El objetivo principal es satisfacer los requerimientos de información internos de la empresa para una mejor gestión, con eficiencia y facilidad de acceso.  
El DW puede verse como una bodega donde están almacenados todos los datos necesarios para realizar las funciones de gestión de la empresa, de manera que puedan utilizarse fácilmente según se necesiten.

![Cuadro](https://static.platzi.com/media/user_upload/Data-Warehouse-1024x525-a5e0323c-f4a3-4850-a21d-f427a638dd11.jpg)

