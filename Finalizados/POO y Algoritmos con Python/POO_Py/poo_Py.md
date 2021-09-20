# [Curso de POO y Algoritmos con Python](https://platzi.com/clases/poo-python/)

## 5 Abstracción
Clases privadas y publicas

``` Python
class Lavadora:

    def __init__(self):
        pass

    def lavar(self, temperatura='caliente'):
        self._llenar_tanque_de_agua(temperatura)
        self._anadir_jabon()
        self._lavar()
        self._centrifugar()

    def _llenar_tanque_de_agua(self, temperatura):
        print(f'Llenando el tanque con agua {temperatura}')

    def _anadir_jabon(self):
        print('Anadiendo jabon')

    def _lavar(self):
        print('Lavando la ropa')

    def _centrifugar(self):
        print('Centrifugando la ropa')


if __name__ == '__main__':
    lavadora = Lavadora()
    lavadora.lavar()
```

## 6 Funciones: base de los decoradores
Estas funciones añaden funcionalidades a otras funciones del programa.  
https://www.youtube.com/watch?v=DQXm6bIZgvk  
[Decoradores con parámetros](https://www.youtube.com/watch?v=_IwlE3Z7U04&list=PLU8oAlHdN5BlvPxziopYZRd55pdqFwkeS&index=74)


## 8 [Encapsulación, getters and setters](https://platzi.com/clases/1775-poo-python/25225-encapsulacion-getters-and-setters/)
Con los metodos getters y setters, podemos invocar a un método como si fuera una propiedad.
https://www.youtube.com/watch?v=RHIRwNcBms8

## 9 [Herencia](https://platzi.com/clases/1775-poo-python/25226-herencia/)

``` Python
lass Rectangulo:

    def __init__(self, base, altura):
        self.base = base
        self.altura = altura

    def area(self):
        return self.base * self.altura

class Cuadrado(Rectangulo):

    def __init__(self, lado):
        super().__init__(lado, lado)


if __name__ == '__main__':
    rectangulo = Rectangulo(base=3, altura=4)
    print(rectangulo.area())

    cuadrado = Cuadrado(lado=5)
    print(cuadrado.area())
```

## 10 [Polimorfismo](https://platzi.com/clases/1775-poo-python/25258-polimorfismo/)
En otros lenguajes, nosotros utilizamos la palabra overwite que significa que vamos a modificar el comportamiento de una superclase En Payton. Lo único que nosotros tenemos que hacer es directamente tomar el nombre del método que nosotros queremos modificar de la super clase e implementarlo de manera distinta en la subclase.

``` Python

class Persona:

    def __init__(self, nombre):
        self.nombre = nombre

    def avanza(self):
        print('Ando caminando')


class Ciclista(Persona):

    def __init__(self, nombre):
        super().__init__(nombre)

    def avanza(self):
        print('Ando moviendome en mi bicicleta')


def main():
    persona = Persona('David')
    persona.avanza()

    ciclista = Ciclista('Daniel')
    ciclista.avanza()


if __name__ == '__main__':
    main()
```

## 15 [Búsqueda lineal](https://platzi.com/clases/1775-poo-python/25263-busqueda-lineal/)
Implementación iterativa.

``` python
import random

def busqueda_lineal(lista, objetivo):
    match = False

    for elemento in lista: # O(n)
        if elemento == objetivo:
            match = True
            break

    return match


if __name__ == '__main__':
    tamano_de_lista = int(input('De que tamano sera la lista? '))
    objetivo = int(input('Que numero quieres encontrar? '))

    lista = [random.randint(0, 100) for i in range(tamano_de_lista)]

    encontrado = busqueda_lineal(lista, objetivo)
    print(lista)
    # uso de operador ternario
    print(f'El elemento {objetivo} {"esta" if encontrado else "no esta"} en la lista')
```


## 16 [Búsqueda binaria](https://platzi.com/clases/1775-poo-python/25264-busqueda-binaria/)
Implementación recursiva.  
Los datos deben estar ordenados.

``` Python
import random

def busqueda_binaria(lista, comienzo, final, objetivo):
    print(f'buscando {objetivo} entre {lista[comienzo]} y {lista[final - 1]}')
    if comienzo > final:
        return False

    medio = (comienzo + final) // 2

    if lista[medio] == objetivo:
        return True
    elif lista[medio] < objetivo:
        return busqueda_binaria(lista, medio + 1, final, objetivo)
    else:
        return busqueda_binaria(lista, comienzo, medio - 1, objetivo)


if __name__ == '__main__':
    tamano_de_lista = int(input('De que tamano es la lista? '))
    objetivo = int(input('Que numero quieres encontrar? '))

    lista = sorted([random.randint(0, 100) for i in range(tamano_de_lista)])

    encontrado = busqueda_binaria(lista, 0, len(lista), objetivo)

    print(lista)
    print(f'El elemento {objetivo} {"esta" if encontrado else "no esta"} en la lista')
```

## 20 [Ambientes virtuales](https://platzi.com/clases/1775-poo-python/25268-ambientes-virtuales/)

### Usando venv, que ya está incluido en Python 3.
- Crear ambiente:  
`python3.7 -m venv <nombre_del_ambiente_virual>`

- Ingresar:  
`source env/bin/activate`

- Salir:
`deactivate`

## 22 [Graficado simple](https://platzi.com/clases/1775-poo-python/25270-graficado-simple/)

bokeh, es más recomendable que otros conocidos.
Entre otras cosas se puede usar con Flask o Dyango.

[enlace:](http://docs.bokeh.org/en/latest/index.html)

```python
from bokeh.plotting import figure, output_file, show

if __name__ == '__main__':
    output_file('graficado_simple.html')
    fig = figure()
    
    total_vals = int(input('Cuantos valores quieres graficar?'))
    x_vals = list(range(total_vals))
    y_vals = []

    for x in x_vals:
        val = int(input(f'Valor y para {x}'))
        y_vals.append(val)

    fig.line(x_vals, y_vals, line_width=2)
    show(fig)
```