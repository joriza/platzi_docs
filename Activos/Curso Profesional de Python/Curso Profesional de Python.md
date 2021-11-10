# [Curso Profesional de Python](https://platzi.com/clases/python-profesional/)

## 3 [Cómo organizar las carpetas de tus proyectos](https://platzi.com/clases/2397-python-profesional/39542-organiza-los-archivos-de-tus-proyectos/)

__init __.py
Cuando se crea un nuevo objeto, se inicializa llamando al método init en el objeto.

__init__ 

is pronounced “dunder init”: dunder is short for “double-underscore”.

![Cuadro](https://static.platzi.com/media/user_upload/paquettes-5a4095f3-0811-4e56-8f06-296b42b2e497.jpg)

## 4 [¿Qué son los tipados?](https://platzi.com/clases/2397-python-profesional/39543-que-son-los-tipados/)

Hay 4 clasificaciones.
- Estático
- Dinámico
- Débil
- Fuerte

## 5 [Tipado estático en Python](https://platzi.com/clases/2397-python-profesional/39524-tipado-estatico-en-python/)

Como implementarlo.
**Nota:** Solo funciona a partir de la versión 3.6  
Al declarar las variables indicar su tipo.  

``` python
a: int = 5
print(a)

b: str = "Hola"
print(b)

c: bool = True
print(c)
```

**Para un función:**

``` python
def suma(a: int, b: int) -> int :
	return a + b

print(suma(1,2))
```

con `-> int` indico que la función debe devolver un valor del tipo int.  
**Nota:** Así como está indicado en la función, si le paso 2 parámetros string, va a concatenar ambos string.


Existe una librería de fabrica que viene preinstalada con Python que se llama typing, que es de gran utilidad para trabajar con tipado con estructuras de datos entre la versión 3.6 y 3.9, entonces:


``` python
from typing import Dict, List

positives: List [int] = [1,2,3,4,5]

users: Dict [str, int] = {
	"argentina": 1.
	"mexico": 34,
	"colombia": 45,
}

countries: List[Dict[str, str]] = [
	{
		"name" : "Argentina",
		"people" : "45000",
	},
	{
		"name" : "México",
		"people" : "9000000",
	},
	{
		"name" : "Colombia",
		"people" : "99999999999",
	}
]
``` 

**Para Tuplas**

``` python
from typing import Tuple, Dict, List

CoordinatesType = List[Dict[str, Tuple[int, int]]]

coordinates: CoordinatesType = [
	{
		"coord1": (1,2),
		"coord2": (3,5)
	},
	{
		"coord1": (0,1),
		"coord2": (2,5)
	}
]
```

**Ejemplo complejo **

``` python
from typing import Tuple, Dict, List

CoordinatesType = List[Dict[str, Tuple[int, int]]]

#Una variable que es de tipo CoordinatesType 🤯
coordinates: CoordinatesType = [
  {
    'coord1': (1,2),
    'coord2': (3,5),
  },
  {
    'coord1': (0,1),
    'coord2': (2,5),
  },
]
```

CoordinatesType es un alias que contiene el tipo de datos que luego se va a asignar a una variable.

Para que este tema de los tipos sea tenido en cuenta por Python se debe cargar el módulo mypy.

Ventajas de aplicar el tipado stático:  
- Aporta claridad al código.
- Aporta calidad al código.
- Devuelve los errores antes que el programa se ejecute.

## 6 [Practicando el tipado estático](https://platzi.com/clases/2397-python-profesional/39525-practicando-el-tipado-estatico/)

