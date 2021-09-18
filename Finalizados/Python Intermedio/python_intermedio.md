- [Python Intermedio](#python-intermedio)
  - [2 El Zen de Python](#2-el-zen-de-python)
  - [3 ¿Qué es la documentación?](#3-qué-es-la-documentación)
  - [4 ¿Qué es un entorno virtual?](#4-qué-es-un-entorno-virtual)
    - [venv](#venv)
  - [5 El primer paso profesional: creación de un entorno virtual](#5-el-primer-paso-profesional-creación-de-un-entorno-virtual)
  - [6 Instalación de dependencias con pip](#6-instalación-de-dependencias-con-pip)
  - [7 Una alternativa: Anaconda](#7-una-alternativa-anaconda)
  - [8 Listas y diccionarios anidados](#8-listas-y-diccionarios-anidados)
  - [9 Listas y diccionarios anidados](#9-listas-y-diccionarios-anidados)
  - [9 List comprehensions](#9-list-comprehensions)
  - [10 Dictionary comprehensions](#10-dictionary-comprehensions)
  - [11 Funciones anónimas: lambda](#11-funciones-anónimas-lambda)
  - [12 High order functions: filter, map y reduce](#12-high-order-functions-filter-map-y-reduce)
  - [13 Proyecto: filtrando datos](#13-proyecto-filtrando-datos)
  - [14 Los errores en el código](#14-los-errores-en-el-código)
  - [15 Debugging](#15-debugging)
  - [16 Manejo de excepciones](#16-manejo-de-excepciones)
  - [17 Poniendo a prueba el manejo de excepciones](#17-poniendo-a-prueba-el-manejo-de-excepciones)
  - [18 Assert statements](#18-assert-statements)
  - [19 ¿Cómo trabajar con archivos?](#19-cómo-trabajar-con-archivos)
  - [20 Trabajando con archivos de texto en Python](#20-trabajando-con-archivos-de-texto-en-python)
  - [21 Reto final: Juego del Ahorcado o Hangman Game](#21-reto-final-juego-del-ahorcado-o-hangman-game)
  - [22 Continúa tu camino profesional con Python](#22-continúa-tu-camino-profesional-con-python)

# [Python Intermedio](https://platzi.com/clases/python-intermedio/)
Ruta: https://platzi.com/backend-python/

## 2 [El Zen de Python](https://platzi.com/clases/2255-python-intermedio/36456-el-zen-de-python/)


- **Bello es mejor que feo:**
Pyhton es estéticamente superior a cualquier otro lenguaje de programación. Al momento de escribir código, es mejor que sea de manera limpia y estética.

- **Explícito es mejor que implícito:**
Hacer más fácil que las otras personas entiendan el código.

- **Simple es mejor que complejo:**
Es mejor tener una implementación simple, que ocupe pocas lineas de código y sea entendible, a que sea una larga y complicada.

- **Complejo es mejor que complicado:**
Si tenemos que extendernos en la implementación y hacerla más compleja para que el código si se entienda, esto es mejor que hacerlo simple y mal.

- **Plano es mejor que anidado:**
El anidamiento es cuando tenemos un bloque de código dentro de otro bloque de código (dependiendo de este). Esto se nota en Python por la identación, nos quedarían estos bloques muy corridos a la derecha.
Es mejor evitar el anidamiento, y hacer las cosas de manera plana.

- **Espaciado es mejor que denso:**
Por la identación de Python (sus sangrías), este principio se nos hace imposible de esquivar. El código inevitablemente es espaciado.

- **La legibilidad es importante:**
Es importante que otros programadores puedan entender lo que estamos escribiendo. Esto hace más fáciles las cosas cuando trabajemos con otros en los proyectos.

- **Los casos especiales no son lo suficientemente especiales cpmo para romper las reglas (sin embargo, la practicidad le gana a la pureza):**
Siempre que podamos respetar estas reglas que nos plantea Python, es mejor así. Sin embargo, si por el hecho de hacer un código muy puro o muy ‘Pythonista’, este pierde legibilidad, es mejor ser más prácticos y romper o saltearnos algunas de estas reglas para que el código sea más eficiente. Por lo tanto, llegado el momento debermos decidir si es mejor hacer las cosas de manera pura o práctica.

- **Los errores nunca deberían pasar silenciosamente (a menos que se silencien explícitamente):**
Manejar los erroes es fundamental. Cada error nos dice algo y hay que prestarle atención. A menos que seas capaz de silenciar un error explícitamente, aunque para esto hay que tener criterio.
Frente a la ambiguedad, evitar la tentación de adivinar:
Nuestro código debería solamente tener una interpretación. Si en un contexto significa algo, y en otro otra cosa, es mejor que lo revisemos y busquemos una solución.

- **Debería haber una, y preferiblemente sola, una manera obvia de hacerlo. (A pesar de que esa manera no sea obvia a menos que seas holandés):**
Esto hace referencia al creador de Python ''Guido van Rossum", que de manera muy inteligente encontrar las soluciones precisas a los problemas, y deberíamos imitarlo.

- **Ahora es mejor que nunca:**
Es mejor desarrollar nuestra solución cuánto antes, no dejarlo para mañana o para mas adelante.

- **A pesar de que nunca es muchas veces mejor que ahora mismo:**
Si por hacer las cosas ya y tenemos poco tiempo, si es mejor dejarlo para después y no hacerlo apurado y mal.

- **Si la implementación es díficil de explicar, es una mala idea, y si es fácil de explicar, es una buena idea:**
Si somos capaces de explicar nuestra implementación a otros desarrolladores paso a paso, es una buena idea. En cambio si no podemos hacerlo, significa que ni nosotros entendemos la implementación y deberíamos repensar nuestra forma de encarar la solución.

- **Los espacios de nombres son una gran idea, ¡Tengamos más de esos! (namespaces):**
Es el nombre que se ha indicado luego de la palabra import, es decir la ruta (namespace) del módulo. (Lo veremos a profundidad más adelante).

## 3 [¿Qué es la documentación?](https://platzi.com/clases/2255-python-intermedio/36457-que-es-la-documentacion/)

Enlace a la documentación oficial.  
https://docs.python.org/es/3/

## 4 [¿Qué es un entorno virtual?](https://platzi.com/clases/2255-python-intermedio/36458-que-es-un-entorno-virtual/)

### venv

Crear  
activar  
desactivar

Sin usar entorno virtual

<img src = "https://static.platzi.com/media/user_upload/Screenshot%20from%202021-04-06%2015-17-31-98f9a6fa-3e6c-4353-9644-31a4e7208737.jpg" width = "57%" height = "57%" alt = "ejemplo" align = "center" />

con entornos virtuales

![En Español](https://static.platzi.com/media/user_upload/Screenshot%20from%202021-04-06%2015-10-22-1804c0b6-79d2-40bd-aced-f859f86c5309.jpg  "Texto del popup")

## 5 [El primer paso profesional: creación de un entorno virtual](https://platzi.com/clases/2255-python-intermedio/36459-el-primer-paso-profesional-creacion-de-un-entorno-/)


https://platzi.com/tutoriales/1751-webscraping/4981-crear-un-entorno-virtual-en-python/

## 6 [Instalación de dependencias con pip](https://platzi.com/clases/2255-python-intermedio/36460-instalacion-de-dependencias-con-pip/)

Crear archivo requirements.txt

`pip freeze > requirements.txt`

Cargar las dependencias del requirements.txt

`pip install -r requirements.txt`

## 7 [Una alternativa: Anaconda](https://platzi.com/clases/2255-python-intermedio/36461-una-alternativa-anaconda/)

Distribución orientada a ciencias de datos

<img src = "https://static.platzi.com/media/user_upload/Conda-9450dd76-6a83-475c-a1dd-b9ea9241dd24.jpg" width = "57%" height = "57%" alt = "ejemplo" align = "center" />

## 8 [Listas y diccionarios anidados](https://platzi.com/clases/2255-python-intermedio/36462-listas-y-diccionarios-anidados/)

## 9 [Listas y diccionarios anidados](https://platzi.com/clases/2255-python-intermedio/36462-listas-y-diccionarios-anidados/)

- Estando en la carpeta de trabajo  
Iniciar repostitorio con git init  
- Crear Entorno virtual  
py -m venv venv
- Ingresar al entorno virtual

- Ignorar el entorno virtual dentro del repositorio.
En .gitignore escribir  
escribir solo el nombre de la carpeta finalizado con un barra  
venv/  
- deactivate para salir del entorno virtual.

Ejemplo donde lista el diccionario.
``` python
def run():
    my_list = [1, "Hello", True, 4.5]
    my_dict = {"firstname": "Facundo", "lastname": "García"}

    super_list = [
        {"firstname": "Facundo", "lastname": "García"},
        {"firstname": "Miguel", "lastname": "Rodriguez"},
        {"firstname": "Pablo", "lastname": "Trinidad"},
        {"firstname": "Susana", "lastname": "Martinez"},
        {"firstname": "José", "lastname": "Fernandez"},
    ]

    super_dict = {
        "natural_nums": [1, 2, 3, 4, 5],
        "integer_nums": [-1, -2, 3, 0, 1],
        "floating_nums": [1.1, 4.55, 6.43],
    }

    for key, value in super_dict.items():
        print(key, ">", value)


if __name__ == '__main__':
    run()
```

## 9 [List comprehensions](https://platzi.com/clases/2255-python-intermedio/36463-list-comprehensions/)

Elevar al cuadrado cada item de la lista que no es divisible por 3.
``` python
def run():
    # squares = []

    # for i in range(1, 101):
    #     if i % 3 != 0:
    #         squares.append(i**2)

    squares = [i**2 for i in range(1, 101) if i % 3 != 0]
    
    print(squares)


if __name__ == "__main__":
    run()
``` 

Detalle de como esta compuesta la estructura.

![Cuadro](https://static.platzi.com/media/user_upload/List_comprehensions1-bacd6262-4bc3-40c8-8c71-3da952e30b41.jpg)


## 10 [Dictionary comprehensions](https://platzi.com/clases/2255-python-intermedio/36464-dictionary-comprehensions/)

``` python
def run():
    # my_dict = {}

    # for i in range(1, 101):
    #     if i % 3 !=0:
    #         my_dict[i] = i**2

    # print(my_dict)

    my_dict = {i: i**3 for i in range(1, 101) if i % 3 != 0}
    print(my_dict)


if __name__ == "__main__":
    run()
``` 

## 11 [Funciones anónimas: lambda](https://platzi.com/clases/2255-python-intermedio/36465-funciones-anonimas-lambda/)

Pueden tener solo una línea de código.
![Cuadro](https://static.platzi.com/media/user_upload/lambda.png-c06b5ab0-03d2-42c2-a442-19559fee74d6.jpg)

## 12 [High order functions: filter, map y reduce](https://platzi.com/clases/2255-python-intermedio/36466-high-order-functions-filter-map-y-reduce/)

Ejemplos de uso.
Filter: Extraer los impares de una lista.
Map: Elevar al cuadrado cada item de la lista
Reduce: Realizar una misma operaión con todos los items de una lista.
Son formas de realizar de forma eficiente iteraciones con datos estructurados.

``` python
from functools import reduce
def main():

    #Filter
    myList = [1,4,5,7,9,13,19,21]

    odd = list(filter(lambda x: x % 2 != 0, myList))
    print(odd)

    #Map
    myList2 = [1, 2, 3, 4, 5]

    squares = list(map(lambda x: x**2, myList2))
    print(squares)

    myList3 = [2, 2, 2, 2, 2]
    
    allMultiplied = reduce(lambda a, b: a * b, myList3)
    print(allMultiplied)

if __name__ == '__main__':
    main()
```

La diferencia entre filter y map:

- filter devuelve True or False según el valor esté dentro de los criterios buscados o no. En caso de que no cumpla con la condición, no será devuelto y la lista se verá reducida por este filtro.
Map funciona muy parecido, pero su diferencia radica en que no puede eliminar valores de la lista del array entregado. Es decir, el output tiene la misma cantidad de valores que el input.
Cómo funciona reduce:

- Reduce toma 2 valores entregados como parámetros y el iterador como otro parámetro. Realiza la función con estos 2 valores, y luego con el resultado de esto y el valor que le sigue en el array. Y así hasta pasar por todos los valores de la lista.

## 13 [Proyecto: filtrando datos](https://platzi.com/clases/2255-python-intermedio/36467-proyecto-filtrando-datos/)

Nota: Las constantes por convención se colocan en mayúsculas.
Los datos son una lista de diccionarios.

``` python
DATA = [
    {
        'name': 'Facundo',
        'age': 72,
        'organization': 'Platzi',
        'position': 'Technical Coach',
        'language': 'python',
    },
    {
        'name': 'Luisana',
        'age': 33,
        'organization': 'Globant',
        'position': 'UX Designer',
        'language': 'javascript',
    },
    {
        'name': 'Héctor',
        'age': 19,
        'organization': 'Platzi',
        'position': 'Associate',
        'language': 'ruby',
    },
    {
        'name': 'Gabriel',
        'age': 20,
        'organization': 'Platzi',
        'position': 'Associate',
        'language': 'javascript',
    },
    {
        'name': 'Isabella',
        'age': 30,
        'organization': 'Platzi',
        'position': 'QA Manager',
        'language': 'java',
    },
    {
        'name': 'Karo',
        'age': 23,
        'organization': 'Everis',
        'position': 'Backend Developer',
        'language': 'python',
    },
    {
        'name': 'Ariel',
        'age': 32,
        'organization': 'Rappi',
        'position': 'Support',
        'language': '',
    },
    {
        'name': 'Juan',
        'age': 17,
        'organization': '',
        'position': 'Student',
        'language': 'go',
    },
    {
        'name': 'Pablo',
        'age': 32,
        'organization': 'Master',
        'position': 'Human Resources Manager',
        'language': 'python',
    },
    {
        'name': 'Lorena',
        'age': 56,
        'organization': 'Python Organization',
        'position': 'Language Maker',
        'language': 'python',
    },
]

def run():

    # Comprehensions solutions
    all_python_devs = [worker["name"] for worker in DATA if worker["language"] == "python"]
    all_Platzi_workers = [worker["name"] for worker in DATA if worker["organization"] == "Platzi"]
    adults =  [worker["name"] for worker in DATA if worker["age"] > 18]
    old_people = list(map(lambda worker: worker | {"old": worker["age"] > 70}, DATA))

    for worker in all_python_devs:
        print(worker)


if __name__ == '__main__':
    run()
```

## 14 [Los errores en el código](https://platzi.com/clases/2255-python-intermedio/36468-los-errores-en-el-codigo/)

Cuando python nos avisa pueden ser 2 tipos de errores.
![Cuadro](https://static.platzi.com/media/user_upload/error-62a56437-8b39-4cd9-85da-0dac5854ee3d.jpg)

Python tiene mas de 50 tipos de execciones.

## 15 [Debugging](https://platzi.com/clases/2255-python-intermedio/36469-debugging/)

Como resolver errores de lógica.

## 16 [Manejo de excepciones](https://platzi.com/clases/2255-python-intermedio/36470-manejo-de-excepciones/)

- TRY: En el try se coloca código que esperamos que pueda lanzar algún error.
- EXCEPT: En el except se maneja el error, es decir, si ocurre un error dentro del bloque de código del try, se deja de ejecutar el código del try y se ejecuta lo que se haya definido en el Except.
- ELSE: El else se ejecuta sólo si no hubo ninguna excepción lanzada desde el try
- FINALLY: Se ejecuta SIEMPRE, haya sido lanzada la excepción o no haya sido lanzada.

![Cuadro](https://static.platzi.com/media/user_upload/python-a0d427c5-4e5b-49cd-8e69-3e3b118f37ce.jpg)

Jerarquía de las excepciones y errores más comunes:
![Cuadro](https://static.platzi.com/media/user_upload/Selection_333-c63590c2-26a7-4d31-91e0-0913c2e83497.jpg)

## 17 [Poniendo a prueba el manejo de excepciones](https://platzi.com/clases/2255-python-intermedio/36471-poniendo-a-prueba-el-manejo-de-excepciones/)

``` python
def divisors(num):
    divisors = []
    for i in range(1, num + 1):
        if num % i == 0:
            divisors.append(i)
    return divisors


def run():
    try: 
        num = int(input('Ingresa un número: '))
        print(divisors(num))
        print("Terminó mi programa")
    except ValueError: 
        print("Debes ingresar un número")


if __name__ == '__main__':
    run()
```
## 18 [Assert statements](https://platzi.com/clases/2255-python-intermedio/36472-assert-statements/)

Cuando usamos assert además de imprimirse el mensaje de error que escribimos, se muestra también todo el TRACEBACK  
En cambio, cuando usamos try-except solo se muestra el mensaje de error que escribimos en el código

``` python
def divisors(num):
    divisors = []
    for i in range(1, num + 1):
        if num % i == 0:
            divisors.append(i)
    return divisors


def run():
    num = input('Ingresa un número: ')
    assert num.isnumeric(), "Debes ingresar un número"
    print(divisors(int(num)))
    print("Terminó mi programa")


if __name__ == '__main__':
    run()
```

## 19 [¿Cómo trabajar con archivos?](https://platzi.com/clases/2255-python-intermedio/36473-como-trabajar-con-archivos/)

Si no escriben el modo de apertura, Python lo toma por Default como si fuera rt  
Read and Text.
 
Modos de Apertura
- r   Read-Lectura, es el modo default de apertura que tiene la función open().
- w   Write-Escritura, este modo trunca el archivo desde el inicio.
- x   Abierto para creación exclusiva, falla si el archivo ya existe previamente.
- a   Write Append - Añadiendo contenido al final del archivo si este ya existe.
- b   Binary Mode - Apertura de modo binario.
- t   Text mode - Modo texto que es el default.
- +   Read-Write, Apertura para actualización (lectura-escritura) - (Puede combinarse con otros modos)

Modos combinados:
- w+   Escritura con actualización, este modo trunca el archivo inicialmente.
- w+b   Escritura/actualización binaria, este modo trunca el archivo inicalmente.
- r+   Lectura con actualización, este modo no trunca el archivo.
- r+b   Lectura/Actualizacion binaria, este modo no trunca el archivo.
 
Estándo en la documentación encontrarán una palabra especial, truncate o truncar esto significa que el archivo existente que queremos abrir será limpiado internamente, o sea su contenido será borrado para dar apertura al nuevo contenido por completo.

https://docs.python.org/3/library/functions.html#open

## 20 [Trabajando con archivos de texto en Python](https://platzi.com/clases/2255-python-intermedio/36474-trabajando-con-archivos-de-texto-en-python/)

``` python
def read():
    numbers = []
    with open("./archivos/numbers.txt", "r") as f: 
        for line in f:
            numbers.append(int(line))
    print(numbers)


def write():
    names = ["Facundo", "Gregorio", "Marta", "Susana", "Jose"]
    with open("./archivos/names.txt", "w") as f:
        for name in names: 
            f.write(name)
            f.write("\n")


def run():
    write()


if __name__ == '__main__':
    run()
```

## 21 [Reto final: Juego del Ahorcado o Hangman Game](https://platzi.com/clases/2255-python-intermedio/36475-reto-final-juego-del-ahorcado-o-hangman-game/)

``` python
import random
import os


def read_data(filepath="./archivos/data.txt"):
    words = []
    with open(filepath, "r", encoding="utf-8") as f:
        for line in f:
            words.append(line.strip().upper())
    return words


def run():
    data = read_data(filepath="./archivos/data.txt")
    chosen_word = random.choice(data)
    chosen_word_list = [letter for letter in chosen_word]
    chosen_word_list_underscores = ["_"] * len(chosen_word_list)
    letter_index_dict = {}
    for idx, letter in enumerate(chosen_word):
        if not letter_index_dict.get(letter): 
            letter_index_dict[letter] = []
        letter_index_dict[letter].append(idx)
    
    while True:
        os.system("cls") # Si estás en Unix (Mac o Linux) cambia cls por clear
        print("¡Adivina la palabra!")
        for element in chosen_word_list_underscores:
            print(element + " ", end="")
        print("\n")

        letter = input("Ingresa una letra: ").strip().upper()
        assert letter.isalpha(), "Solo puedes ingresar letras"

        if letter in chosen_word_list:
            for idx in letter_index_dict[letter]:
                chosen_word_list_underscores[idx] = letter
        
        if "_" not in chosen_word_list_underscores:
            os.system("cls") # Si estás en Unix (Mac o Linux) cambia cls por clear
            print("¡Ganaste! La palabra era", chosen_word)
            break


if __name__ == '__main__':
    run()
```

## 22 [Continúa tu camino profesional con Python](https://platzi.com/clases/2255-python-intermedio/36476-continua-tu-camino-profesional-con-python/)


