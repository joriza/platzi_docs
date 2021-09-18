# Programación Orientada a Objetos: POO

## 1 [¿Por qué aprender Programación Orientada a Objetos?](https://platzi.com/clases/1474-oop/16669-por-que-aprender-programacion-orientada-a-objetos/)

Permite desarrollas más ráṕido.

La programación orientada a objetos tiene cuatro características principales:
- Encapsulamiento. Quiere decir que oculta datos mediante código.
- Abstracción. Es como se pueden representar los objetos en modo de código.
- Herencia. Es donde una clase nueva se crea a partir de una clase existente.
- Polimorfismo. Se refiere a la propiedad por la que es posible enviar mensajes sintácticamente iguales a objetos de tipos distintos.

## 2 [¿Qué resuelve la Programación Orientada a Objetos?](https://platzi.com/clases/1474-oop/16668-que-resuelve-la-programacion-orientada-a-objetos/)

- Principalmente esos problemas y huecos que nos deja la programación estructurada tales como:   
1 - Código muy largo:  
2 - Si algo falla todo se rompe  
3 - Código Spaguetti: Muchas sentencias de control anidadas y pérdida de control sobre el código.  

## 3 [Paradigma Orientado a Objetos](https://platzi.com/clases/1474-oop/16670-paradigma-orientado-a-objetos/)

**Paradigma:** Teoría que suministra la base y modelo para resolver problemas.

Resumen:
![Cuadro](https://static.platzi.com/media/user_upload/Paradigma%20de%20Programacion-POO-cc9b03f3-09ac-4b5d-ab22-18c5a2ab698c.jpg)

![Cuadro](https://static.platzi.com/media/user_upload/%C2%BFQu%C3%A9%20es%20la%20Programaci%C3%B3n%20orientada%20a%20objetos_-ffb6955d-ae7d-4446-96e2-66f071517a77.jpg)

**4 Elementos**  
Clases  
Propiedades  
Métodos  
Objetos  

**4 Pilares**  
Encapsulamiento  
Abstracción  
Herencia  
Polimorfismo  

## 6 [Diagramas de Modelado](https://platzi.com/clases/1474-oop/16673-diagramas-de-modelado/)

OMT: Object Modeling Techniques. Es una metodología para el análisis orientado a objetos.

UML: Unified Modeling Language o Lenguaje de Modelado Unificado. Tomó las bases y técnicas de OMT unificándolas. Tenemos más opciones de diagramas como lo son Clases, Casos de Uso, Objetos, Actividades, Iteración, Estados, Implementación.

![Cuadro](https://static.platzi.com/media/user_upload/UML-a235cec9-9058-46e6-adf3-978742e0b001.jpg)

## 8 [Objetos](https://platzi.com/clases/1474-oop/16675-objetos9415/)

Los Objetos son aquellos que tienen propiedades y comportamientos, también serán sustantivos.

Pueden ser Físicos o Conceptuales
Las Propiedades también pueden llamarse atributos y estos también serán sustantivos. Algunos atributos o propiedades son nombre, tamaño, forma, estado, etc. Son todas las características del objeto.

Los Comportamientos serán todas las operaciones que el objeto puede hacer, suelen ser verbos o sustantivos y verbo. Algunos ejemplos pueden ser que el usuario pueda hacer login y logout.

# 9 [Abstracción y Clases](https://platzi.com/clases/1474-oop/16677-abstraccion-y-clases/)

Una Clase Es el modelo sobre el cual nuestros objetos se construyen.

Es decir si tenemos un objeto llamado perro y este tiene sus atributos que lo describen generalmente y a su vez tiene métodos donde se define las acciones que pueda hacer ese perrito. Una clase me permite generar mas objetos (mas perros) con mismos atributos y métodos pero con resultados diferentes. ej:

Objeto #1 llamado “Rocky”:
tributo_1: color = marrón
atributo_2: taman’o = pequen’o
atributo_3: raza = chiguagua

metodo_1: ladrar
metodo_2: comer
metodo_3: dormir

Objeto #2 llamado "Max"
atributo_1: color = blanco
atributo_2: taman’o = grande
atributo_3: raza = hunky siberiano

metodo_1: ladrar
metodo_2: comer
metodo_3: dormir

Para no repetir esto muchas veces de acuerdo a la cantidad de perros que es mi ejemplo de objeto, la idea es analizar todos estos objetos extraemos todos esos atributos y entonces generamos modelos. Esos modelos se le llaman Clases.

Una Clase son los modelos sobre los cuales construiremos Objetos

A este análisis se le conoce como Abstracción, simplemente consiste en generar un molde en base a esas propiedades y métodos de los objetos, abstraemos todos esos datos para generar dicho molde.

Resumen: Una clase es un molde para generar un objeto y este análisis se llama Abstracción

## 10 [Modularidad](https://platzi.com/clases/1474-oop/16679-modularidad/)

Modular: Dividir un sitema y así crear módulos independientes, lo que permite evitar un colapso masivo en nuestro código y mejorar la legibilidad.

La modularidad va muy relacionada con las clases y es un principio de la Programación Orientado a Objetos y va de la mano con el Diseño Modular que significa dividir un sistema en partes pequeñas y estas serán nuestros módulos pudiendo funcionar de manera independiente.

La modularidad de nuestro código nos va a permitir

- Reutilizar
- Evitar colapsos
- Hacer nuestro código más mantenible
- Legibilidad
- Resolución rápida de problemas
- Una buena práctica es separando las clases en archivos diferentes.

## 11 [Analizando Uber en Objetos](https://platzi.com/clases/1474-oop/16678-analizando-uber-en-objetos/)

![Cuadro](https://static.platzi.com/media/public/uploads/analizando-uber-en-objetos_7648b008-b099-4b0c-a511-a8be36bcd240.png)

