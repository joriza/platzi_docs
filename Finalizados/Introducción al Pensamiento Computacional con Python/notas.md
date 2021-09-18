# Introducción al Pensamiento Computacional con Python

## 6 [Asignación de variables](https://platzi.com/clases/1764-python-cs/25231-asignacion-de-variables/)

Las variables son simplemente nombres relacionados con un valor en memoria.
Hacen que los programas sean mas comprensibles.
Los operadores de asignación asocian a estos nombres con los valores en memoria.

## 7 [Cadenas y entradas](https://platzi.com/clases/1764-python-cs/25232-cadenas-y-entradas/)

Las cadenas son tipos no escalares.  
Son secuencias de caracteres.  
Se pueden usar comillas simples o dobles.  
Con el operador '+' se pueden concatenar.  
Con el operador '*' se pueden repetir las cadenas.    
Con slicing se pueden dividir las cadenas convirtiendolas en sub strings.  

variable[ini:fin:paso]  
Los valores que se dejen en blanco es el mas como la pocición.  

Las cadenas son inmutables. Una vez declaradas no se pueden re-asignar.

Con la función input, lo que se obtiene es una cadena de caracteres. Siempre regresa cadenas. Si se necesita que sean numeros, se debe castear.

## 8 [Programas ramificados](https://platzi.com/clases/1764-python-cs/25233-programas-ramificados/)

``` python
num_1 = int(input('Escoge un entero: '))
num_2 = int(input('Escoge otro entero: '))

if num_1 > num_2:
    print('El primer numero es mayor que el segundo')
elif num_1 < num_2:
    print('El segundo numero es mayor que el primero')
else:
    print('Los dos numeros son iguales')
```

## 9 [Iteraciones](https://platzi.com/clases/1764-python-cs/25234-iteraciones/)

``` python
contador_externo = 0
contador_interno = 0

while contador_externo < 5:
    while contador_interno < 6:
        print(contador_externo, contador_interno)
        contador_interno += 1

        if contador_interno >= 3:
            break

    contador_externo += 1
    contador_interno = 0
```

## 10 [Bucles for](https://platzi.com/clases/1764-python-cs/25235-bucles-for/)

```
for (i = 0; i <= 10; i++) {
  <expresión>
}

for <variable> in <iterable>:
    <expresión>
```

``` python
frutas = ['manzana', 'pera', 'mango']
for fruta in frutas:
  print(fruta)

manzana
pera
mango
```

## 12 [Enumeración exhaustiva](https://platzi.com/clases/1764-python-cs/25236-enumeracion-exhaustiva/)



## 13 [Aproximación de soluciones](https://platzi.com/clases/1764-python-cs/25237-aproximacion-de-soluciones/)

Se debe definir que tan cerca se quiere estar de la solución. (Epsilon)
Se debe elegir entre velocidad o presición.

``` python
objetivo = int(input('Escoge un numero: '))
epsilon = 0.0001
paso = epsilon**2 
respuesta = 0.0

while abs(respuesta**2 - objetivo) >= epsilon and respuesta <= objetivo:
    print(abs(respuesta**2 - objetivo), respuesta)
    respuesta += paso

if abs(respuesta**2 - objetivo) >= epsilon:
    print(f'No se encontro la raiz cuadrada {objetivo}')
else:
    print(f'La raiz cudrada de {objetivo} es {respuesta}')
```

## 14 [Búsqueda Binaria](https://platzi.com/clases/1764-python-cs/25238-busqueda-binaria/)

El conjunto de busqueda debe estar ordenado.
Aunque ordenarlo insume mas tiempo que solo buscar, se debe evaluar el tiempo de sucesivas busquedas necesarias es conveniente.
``` python
objetivo = int(input('Escoge un numero: '))
epsilon = 0.001
bajo = 0.0
alto = max(1.0, objetivo)
respuesta = (alto + bajo) / 2

while abs(respuesta**2 - objetivo) >= epsilon:
    print(f'bajo={bajo}, alto={alto}, respuesta={respuesta}')
    if respuesta**2 < objetivo:
        bajo = respuesta
    else:
        alto = respuesta

    respuesta = (alto + bajo) / 2

print(f'La raiz cuadrada de {objetivo} es {respuesta}')
```

## 15 [Funciones y abstracción](https://platzi.com/clases/1764-python-cs/25240-funciones-y-abstraccion/)

- Decompsosicion: Dividir el código en compnentes que colaboran con un fin en común.

``` python
def <nombre>(<parametros>):
    <cuerpo>
    return <espresión>
```

parámetros posicionales, si se utiliza el mismo nombre de parámetros para llamar a la función con los mismos nombres que tiene la función, no es necesario que se respete el orden.

En los parámetros, se puede colocar valores por default, que se pueden omitir.
Se le indica en la definción de la función cual es el valor por omisión.

## 16 [Scope o Alcance](https://platzi.com/clases/1764-python-cs/25241-scope-o-alcance/)

![Cuadro](https://static.platzi.com/media/user_upload/Scope-a97b831f-1adc-4581-816e-722088dc5fe8.jpg)

## 17 [Especificaciones del código](https://platzi.com/clases/1764-python-cs/25242-especificaciones-del-codigo/)

Escribir y leer las especificaciónes dentro de las funciones.

## 18 [Recursividad](https://platzi.com/clases/1764-python-cs/25243-recursividad/)

Una técnica de programar mediante la cual una funciona se llama a sí misma.

sys.setrecursionlimit(limite_de_recursiones)
Limita la cantidad de recursiones.

``` python
def factorial(n)
    if n == 1:
        return 1
    return n * factorial(n - 1)
n = int(input('Escribe un entero: '))

print(factorial(n))
```
## 19 [Fibonnacci y la Recursividad](https://platzi.com/clases/1764-python-cs/25244-fibonnacci-y-la-recursividad/)

## 20 [Funciones como objetos](https://platzi.com/clases/1764-python-cs/25248-funciones-como-objetos/)

![Cuadro](https://runestone.academy/runestone/books/published/fopp/_images/lambda.gif)

En Python las funciones:

- Tienen un tipo
- Se pueden pasar como argumentos de otras funciones
- Se pueden utilizar en expresiones
- Se pueden incluir en varias estructuras de datos (como listas, tuplas, diccionarios, etc.)

Funciones anónimas.

sumar = lambda x, y: x + y

sumar(2, 3)

## 21 [Tuplas](https://platzi.com/clases/1764-python-cs/25245-tuplas/)

Son secuencias inmutables de objetos.
A diferencias de las cadenas pueden contener cualquier tipo de objeto.
Pueden utilizarse para devolver varios valores en una función.

my_tuple = ()

desempaquetar los valores de una tupla. Reasignar una tupla.
x,y,z = my_tuple

## 22 [Rangos](https://platzi.com/clases/1764-python-cs/25246-rangos/)

Representan una secuencia de enteros.
Son inmutables pero se pueden reasignar.
Son muy eficientes en el uso de memoria.

## 23 [Listas y mutabilidad](https://platzi.com/clases/1764-python-cs/25247-listas-y-mutabilidad/)

Mutar una estructura de datos es una posible fuente de errores.
Python permite contener distintos tipos de datos en una misma lista.
pop = extrae y elimina el último elemento.

id(my_list)
devuelve la posición de memoria de la lista.

tener cuidado, que si se copia una lista en otra, ambas listas están en la misma posición de memoria, es como crear un alias.
Esto sucede con las estructuras de datos mutables.

### Clonación
b = list(a)
Son 2 listas con datos igual, pero no apuntan a la misma direccion de memoria.

Tambien se pueden clonar con slices.
b = a[::]

### List comprehension
Una forma concisa de aplicar operaciónes a los valores de una lista.
La condición es optativa.

## 24 [Diccionarios](https://platzi.com/clases/1764-python-cs/25249-diccionarios/)
Son grupos de clave - valor.
No tienen un orden interno.
Son mutables, pueden iterarse.

my_dict = {}

my_dict.get('Nombre',30)
Si no existe la clave, devuelve 30

Modificar o agregar
my_dict['clave']= valor

Borrar un elemento
del my_dict['clave']

Como iterar un diccionario.
por clave
for llave in my_dict.key():

por valor
for valor in my_dict.value():

por clave y valor
for llave, valor in my_dict.items():

Consultar si existe una clave.
'Clave' in my_dict
devuelve un booleano

## 25 [Pruebas de caja negra](https://platzi.com/clases/1764-python-cs/25250-pruebas-de-caja-negra/)

Se basan en la especificación del funcionamiento.
Se envían inputs y se verifican las outputs.
Unit testing, comprueban funcion por función.
Integratión testing, comprueba que todos los módulos funcionan entre sí.

``` python
import unittest


def suma(num_1, num_2):
    return abs(num_1) + num_2


class CajaNegraTest(unittest.TestCase):

    def test_suma_dos_positivos(self):
        num_1 = 10
        num_2 = 5

        resultado = suma(num_1, num_2)

        self.assertEqual(resultado, 15)

    def test_suma_dos_negativos(self):
        num_1 = -10
        num_2 = -7

        resultado = suma(num_1, num_2)

        self.assertEqual(resultado, -17)


if __name__ == '__main__':
    unittest.main()
```

## 26 [Pruebas de caja de cristal](https://platzi.com/clases/1764-python-cs/25251-pruebas-de-caja-de-cristal/)

Se basan en el flujo del programa. Probar los diferentes caminos dentro de la aplicación.

- Si hay un if
Probar el if principal
Elif
Else

- Si hay un loop.
No entrando
Entrando 1 sola vez 
entrando mas de una vez

- Probar todas las excepciones
  
``` python
import unittest


def es_mayor_de_edad(edad):
    if edad >= 18:
        return False
    else:
        return False


class PruebaDeCristalTest(unittest.TestCase):

    def test_es_mayor_de_edad(self):
        edad = 20

        resultado = es_mayor_de_edad(edad)

        self.assertEqual(resultado, True)

    def test_es_menor_de_edad(self):
        edad = 15

        resultado = es_mayor_de_edad(edad)

        self.assertEqual(resultado, False)


if __name__ == '__main__':
    unittest.main()
```
Se le puede agregar el parámetro verbosity=2 al método unittest.main para que el resultado en la consola sea mas detallado.
``` python
if __name__ == '__main__':
    unittest.main(verbosity=2)
```

La diferencia entre las pruebas de Caja Negra y Caja de Cristal es que en las pruebas de caja negra se escriben primero los test para ayudarnos a implementar nuevo código. En las pruebas de caja de cristal se asume que se tiene código escrito y las pruebas se escriben para verificar todas las ramificaciones del programa y probar todos los diferentes caminos posibles.

## 27 [Debugging](https://platzi.com/clases/1764-python-cs/25252-debugging/)

La mejor forma de evitar erroes, es con los tests.

El print statement también sirve.

Debuguear es un proceso de búsqueda. Cada prueba debe acotar el espacio de búsqueda.
Búsqueda binaria con print statement.

**Errores comunes**
Orden de argumentos.
Nombres de funciones.
Inicialización de variables.
Comparar flotantes.
Comparar con value equality en lugar de object equality ( == en lugar de is)
Hay funciones que tienen efecto secundario.
Generar alias con tipos de datos mutables.

Llevar registro de que se ha realizado para corregir un bug, y debe quedar dentro de al menos 1 test.

## 28 [Manejo de excepciones](https://platzi.com/clases/1764-python-cs/25253-manejo-de-excepciones/)

Es aplicar programación defensiva.  
Solo imprimir el mensaje con el error, no es manejarla, es silenciarla.

Excepciones comunes:
```
ImportError : una importación falla;
IndexError : una lista se indexa con un número fuera de rango;
NameError : se usa una variable desconocida ;
SyntaxError : el código no se puede analizar correctamente
TypeError : se llama a una función en un valor de un tipo inapropiado;
ValueError : se llama a una función en un valor del tipo correcto, pero con un valor inapropiado
```

## 29[Excepciones y control de flujo](https://platzi.com/clases/1764-python-cs/25254-excepciones-y-control-de-flujo/)

(Es casi todo el texto. Basicamente, son 2 formas de proceder con el control de flujo, pero terminan con el mismo resultado final.)

## 30 [Afirmaciones](https://platzi.com/clases/1764-python-cs/25255-afirmaciones/)

Es un método de programación defensiva.
Es un método para debuguear.

Palabra reservada `assert`

