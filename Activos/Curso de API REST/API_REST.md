# Curso de API REST

## 3 [Qué es y cómo funciona el protocolo HTTP](https://platzi.com/clases/1638-api-rest/21614-que-es-y-como-funciona-el-protocolo-http/)

HTTP son las siglas de Hypertext Transfer Protocol o protocolo de transferencia de hipertexto, es el conjunto de reglas en las que se van a comunicar dos entidades, en este caso dos computadoras.

Así como nosotros nos comunicamos en español gracias a poder mover las cuerdas vocales, producir y escuchar sonidos, las computadoras se pueden comunicar a través de HTTP gracias al modelo de TCP/IP.

## 4 [¿Qué significa REST? y ¿qué es una API RESTful?](https://platzi.com/clases/1638-api-rest/21611-que-significa-rest-y-que-es-una-api-restful/)

REST es un acrónimo de Representational State Transfer o transferencia de estado representacional, le agrega una capa muy delgada de complejidad y abstracción a HTTP. Mientras que HTTP es transferencia de archivos, REST se basa en la transferencia de recursos.

Una API RESTful es una API diseñada con los conceptos de REST:

- Recurso: todo dentro de una API RESTful debe ser un recurso.
- URI: los recursos en REST siempre se manipulan a partir de la URI, identificadores universales de recursos.
- Acción: todas las peticiones a tu API RESTful deben estar asociadas a uno de los verbos de HTTP: GET para obtener un recurso, POST para escribir un recurso, PUT para modificar un recurso y DELETE para borrarlo.
REST es muy útil cuando:

- Las interacciones son simples.
- Los recursos de tu hardware son limitados.
No conviene cuando las interacciones son muy complejas.

---

Es decir, que el REST es un protocolo que se basa en el intercambio de recursos, http usualmente se basa en el intercambio de archivos aquí es como que se le va un poco el nivel de abstracción.  
Entonces, que es una API RESTfull? Sencillamente es una API que está diseñada alrededor de los conceptos de rest.
Cuáles son estos conceptos entonces? Básicamente de trata de hablar de recursos, de URI y acciones.  
Es decir, una petición REST se basa en decir cuál es el recurso sobre el que queremos realizar alguna acción, Cuál es la acción que queremos realizar, y el URI es lo que nos permite identificar exactamente cuál es efectivamente el recurso sobre el que vamos a actuar.  
De modo que una petición REST completa se basa en una URL que, a diferencia de una URI, incluye el dominio, el protocolo y demás y un verbo http. Estos verbos GET, PUT, POST, DELETE, que mapean a las acciones básicas de obtener un
recurso, crear un recurso nuevo, eliminar un recurso o modificar un recurso existente en el servidor.  
Aquí me quiero detener un momento para explicar un poco mejor el recurso. Puede ser cualquier cosa. Realmente esto depende de un poco en la lógica de la aplicación. Un ejemplo que me viene a la mente es el de una librería donde tales un recurso podría ser un libro o un autor, o tal vez un género de los libros.  
Esto es un ejemplo de peticiones que se podrían realizar aún. Servidor vía red donde, por ejemplo, hacemos el GET/books/1. Eso estamos diciendo que queremos obtener la información del libro que se identifica con el número uno. El segundo ejemplo que dice DELETE/books/50. Lo que estamos haciendo es solicitar el servidor que elimine de su propia base de datos el libro identificado con el número cincuenta.  
Entonces veamos cómo funciona el flujo de una petición REST. Es bastante similar a lo que veíamos en una petición http pero veamos un poquito el detalle para ver la complejidad agregada.  
Empezamos porque un cliente realiza una petición http aún servidor. Esta petición, al igual que lo que habíamos antes, viaja tras de internet y llega al servidor. El servidor comienza a interpretar esta petición y a generar la respuesta y en algún momento determina que ciertos recursos no les son propios. O sea, no los tiene disponibles, sino que debe solicitarse los a otros servidor más. Entonces genera una nueva petición http que viaja nuevamente a través Internet llega a este servidor auxiliar, digamos, este servidor responde con http Y ese http vuelve al servidor original. Esta petición que está marcada en amarillo es la que sería la petición res- propiamente dicha. 
Una vez que el servidor original tomó esos de esos datos que vinieron del otro servidor, continúa el procesamiento de su petición original, agregando esta información genera su respuesta http y esa respuesta viaja nuevamente hacia el cliente que hará lo que tenga que hacer con ella.
En casos, conviene realmente utiliza el REST? Pues esta pregunta viene a cuento de Qué REST no es la única forma que se puede utilizar para el desarrollo de servicios web. Existen otras Usualmente RESTfull conviene cuando las interacciones son simples, como el caso que mostrábamos donde lo que queremos hacer son las operaciones básicas básicas de agregar recursos, quitar recursos, modificarlos y también viene muy bien cuando los recursos de hardware en general son limitados.
Porque como el protocolo está tan cercano al http realmente, no hay mucho más que necesitemos instalar para que todo esto sea posible. Cuando no conviene utilizar REST es cuando las interacciones son un poco más complejas. Como decir no nos alcanza con el mero intercambio de recursos, sino que necesitamos que el servidor aporte más lógica. Un ejemplo que me viene a la mente seríal la de pronto; validación de algún documento. Cuando necesitamos que el servidor aporte la lógica de validación ya RESTfull. Por ahí nos va a quedar un poco chico.

## 5 [Cómo realizar una petición REST e interpretar sus resultados](https://platzi.com/clases/1638-api-rest/21615-como-realizar-una-peticion-rest-e-interpretar-sus-/)

















