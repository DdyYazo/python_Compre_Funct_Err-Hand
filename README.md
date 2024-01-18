# Python_Compre_Funct_Err-Hand


Este repositorio es una excelente fuente de información para cualquier persona que quiera aprender o revisar estos conceptos de Python.


## El Zen de Python
 El [Zen_python.py](Zen_python.py) muestra el Zen de Python, que es una colección de 19 "aforismos" que sirven como principios guía para escribir programas en Python. Aquí hay un resumen de estos aforismos:

1. Hermoso es mejor que feo.
2. Explícito es mejor que implícito.
3. Simple es mejor que complejo.
4. Complejo es mejor que complicado.
5. Plano es mejor que anidado.
6. Espaciado es mejor que denso.
7. La legibilidad cuenta.
8. Los casos especiales no son lo suficientemente especiales como para romper las reglas.
9. Aunque la practicidad le gana a la pureza.
10. Los errores nunca deberían pasar silenciosamente.
11. A menos que se silencien explícitamente.
12. Frente a la ambigüedad, rechaza la tentación de adivinar.
13. Debería haber una, y preferiblemente solo una, manera obvia de hacerlo.
14. Aunque esa manera puede no ser obvia al principio a menos que seas holandés.
15. Ahora es mejor que nunca.
16. Aunque nunca es a menudo mejor que *ahora* mismo.
17. Si la implementación es difícil de explicar, es una mala idea.
18. Si la implementación es fácil de explicar, puede ser una buena idea.
19. Los espacios de nombres son una gran idea, ¡hagamos más de esos!




# Estructura de datos 1: Conjuntos `(sets)`

## [01_set.py](python/01_set.py): Creación y manipulación de conjuntos en Python

Los conjuntos en Python son estructuras de datos que representan una colección de elementos únicos en un orden no garantizado. Se definen de manera similar a las listas y las tuplas, pero en lugar de usar corchetes `[]` o paréntesis `()`, se usan llaves `{}`. 

### Características de los conjuntos en Python:

1. **Únicos**: Los conjuntos automáticamente eliminan los duplicados.
2. **Desordenados**: Los conjuntos no mantienen un orden de los elementos.
3. **Inmutables**: Los elementos dentro de un conjunto deben ser de un tipo de dato inmutable, como números, cadenas y tuplas.
4. **Mutables**: Aunque los elementos dentro del conjunto son inmutables, el conjunto en sí es mutable. Podemos agregar o eliminar elementos de él.
5. **No soportan indexación**: Debido a que los conjuntos son desordenados, no puedes acceder a los elementos de un conjunto por un índice.

### Sets en estructuras de datos 
Los conjuntos en Python también pueden ser creados a partir de otras estructuras de datos como cadenas, tuplas o listas

**Ejemplos**

1. Se crea un conjunto a partir de la cadena "HolaaaMundo". El conjunto resultante contiene cada carácter único de la cadena. Los caracteres duplicados, como las tres 'a', se eliminan en el conjunto resultante.
```python
# Crear un conjunto a partir de una cadena
cadena = "HolaaaMundo"
conjunto_cadena = set(cadena)
print(conjunto_cadena)  # Output: {'a', 'd', 'H', 'l', 'n', 'o', 'M', 'u'}
```

2. Se crea un conjunto a partir de la tupla ('abc', 'cbv', 'as','abc'). El conjunto resultante contiene cada elemento único de la tupla. Los elementos duplicados, como 'abc', se eliminan en el conjunto resultante.

```python
# Crear un conjunto a partir de una tupla
tupla = ('abc', 'cbv', 'as','abc')
conjunto_tupla = set(tupla)
print(conjunto_tupla)  # Output: {'as', 'abc', 'cbv'}
```
3. Además, se puede crear un conjunto a partir de una lista. Cuando se crea un conjunto a partir de una lista, el conjunto contiene los elementos únicos de la lista. Los elementos duplicados se eliminan en el conjunto resultante.

```python
# Crear un conjunto a partir de una lista
lista = ['manzana', 'banana', 'cereza', 'manzana', 'cereza']
conjunto_lista = set(lista)
print(conjunto_lista)  # Output: {'manzana', 'banana', 'cereza'}
```
### Transformación de `(sets)` a estructuras como `(list)` 

Por otro lado, los conjuntos en Python pueden ser convertidos de nuevo a listas. Esto es útil cuando necesitas restaurar el orden de los elementos, ya que los conjuntos no mantienen un orden específico. Para convertir un conjunto a una lista, puedes usar la función `list()`.

Por ejemplo:

```python
# Tomando de base el output del set anterior

# Convertir el conjunto a una lista con el mismo output
lista = list(lista)
print(lista)  # Output: ['manzana', 'banana', 'cereza']
```

Los conjuntos en Python también soportan operaciones matemáticas como la **unión**, **intersección**, **diferencia** y **diferencia simétrica**.

Por ejemplo, en [01_set.py](python/01_set.py), se muestra cómo crear un conjunto, agregar elementos a él, y realizar operaciones de conjunto. También se muestra cómo los conjuntos pueden ser utilizados para eliminar duplicados de una lista.


## [02_crud-set.py](python/02_crud-set.py): Operaciones CRUD en conjuntos de Python

En Python, los conjuntos permiten realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar). Aquí hay un resumen de los puntos clave:

1. **Crear (Create)**: Se puede crear un conjunto usando llaves `{}` o la función `set()`. Cada elemento debe ser único.

```python
# Crear un conjunto con tres elementos
conjunto = {'manzana', 'banana', 'cereza'}
```
2. **Leer (Read)**: Se puede iterar sobre un conjunto usando un bucle `for`. También se puede comprobar si un elemento existe en un conjunto usando la palabra clave `in`.
```python
# Leer e imprimir cada elemento del conjunto
for fruta in conjunto:
    print(fruta)

# O tambien con solo la consulta
print('manzana' in conjunto)

# Del mismo modo saber el tamaño
size = len(conjunto)
```
3. **Actualizar (Update)**: Se puede agregar un elemento a un conjunto usando el método `add()`. Para agregar varios elementos, se usa el método `update()`.
```python
# Agregar un elemento al conjunto
conjunto.add('naranja')
# Agregar varios elementos al conjunto
conjunto.update(['kiwi', 'mango'])
```
4. **Eliminar (Delete)**: Se puede eliminar un elemento de un conjunto usando los métodos `remove()` o` discard()`. La diferencia es que` remove()` lanzará un error si el elemento no existe, mientras que `discard()` no.
```python
# Eliminar un elemento del conjunto
conjunto.remove('banana')
# Intentar eliminar un elemento que puede no estar en el conjunto
conjunto.discard('kiwi')
```
5. **Limpiar (Clear)**: Se puede eliminar todos los elementos de un conjunto usando el método `clear()`.
```python
# Limpiar un conjunto
conjunto.clear()
```


## [03_set-operations.py](python/03_set-operations.py): Operaciones de conjuntos en Python

El archivo `03_set-operations.py` demuestra cómo realizar operaciones de conjuntos en Python. Aquí hay un resumen de los puntos clave:

### 1. Unión 
La unión de dos conjuntos es un nuevo conjunto que contiene todos los elementos que están en al menos uno de los dos conjuntos. En Python, puedes usar el método `union()` o el operador `|` para obtener la unión de dos conjuntos.
```python
# Unión de conjuntos
unionSet = setCountriesA.union(setCountriesB)
# o también puedes usar el operador |
unionSet = setCountriesA | setCountriesB
```

### 2. Intersección
La intersección de dos conjuntos es un nuevo conjunto que contiene todos los elementos que están en ambos conjuntos. En Python, puedes usar el método `intersection()` o el operador `&` para obtener la intersección de dos conjuntos.
```python
# Intersección de conjuntos
intersectionSet = setCountriesA.intersection(setCountriesB)
# o también puedes usar el operador &
intersectionSet = setCountriesA & setCountriesB
```

### 3. Diferencia
La diferencia de dos conjuntos es un nuevo conjunto que contiene todos los elementos que están en el primer conjunto pero no en el segundo. En Python, puedes usar el método `difference()` o el operador `-` para obtener la diferencia de dos conjuntos.
```python
# Diferencia de conjuntos
differenceSet = setCountriesA.difference(setCountriesB)
# o también puedes usar el operador -
differenceSet = setCountriesA - setCountriesB
```

### 4. Diferencia simétrica
La diferencia simétrica de dos conjuntos es un nuevo conjunto que contiene todos los elementos que están en uno de los conjuntos, pero no en ambos. En Python, puedes usar el método `symmetric_difference()` o el operador `^` para obtener la diferencia simétrica de dos conjuntos.
```python
# Diferencia simétrica de conjuntos
symDifferenceSet = setCountriesA.symmetric_difference(setCountriesB)
# o también puedes usar el operador ^
symDifferenceSet = setCountriesA ^ setCountriesB
```

### 5. Subconjunto
Un conjunto es un subconjunto de otro si todos sus elementos también están en el otro conjunto. En Python, puedes usar el método `issubset()` para comprobar si un conjunto es un subconjunto de otro.
```python
# Comprobar si un conjunto es un subconjunto de otro
isSubset = setCountriesA.issubset(setCountriesB)
```

### 6. Superconjunto
Un conjunto es un superconjunto de otro si contiene todos los elementos del otro conjunto. En Python, puedes usar el método `issuperset()` para comprobar si un conjunto es un superconjunto de otro.
```python
# Comprobar si un conjunto es un superconjunto de otro
isSuperset = setCountriesA.issuperset(setCountriesB)
```




# Estructuras de datos 2: Listas `(list)` y Diccionarios `(dict)` con Comprenhentions

## [04_list-compren.py](04_list-compren.py): Comprensión de listas en Python

El archivo `04_list-compren.py` aborda el tema de la comprensión de listas en Python, una característica que permite crear y transformar listas de una manera concisa y legible.

### Sintaxis 
La sintaxis es muy similar a la de los conjuntos, pero en lugar de usar llaves, se usan corchetes.

```python
[element for element in iterable]
```
En donde:
- ``element`` es la variable que se va a agregar a la lista
- `iterable` es una colección de elementos como una lista, un conjunto, una tupla, etc.

### Uso del comprenhension
* Un ejemplo de cómo se crearía una lista sin comprensión se muestra a continuación:

```python
# Forma habitual de un ciclo 
numbers = []
for element in range(1, 11):
    numbers.append(element*2)
print(numbers)
```
Este código crea una lista de números del 1 al 10, cada uno multiplicado por 2, sin utilizar la comprensión de listas.

* Luego, se muestra cómo se puede lograr el mismo resultado con la comprensión de listas:
```python
# Forma con la aplicación de la comprensión
numbers_Com = [element*2 for element in range(1, 11)]
print(numbers_Com)
```

### Uso de condicionales en comprenhension
Por otro lado, tambien es posible agregar condicionales a la lista de comprensión:
```python
[element for element in iterable if condition]
```
En donde:
- `element` es la variable que se va a agregar a la lista
- `iterable` es una colección de elementos como una lista, un conjunto, una tupla, etc.
- `condition` es una condición que se debe cumplir para agregar el elemento a la lista """


* Por ejemplo, el siguiente código crea una lista de los números pares del 1 al 10, cada uno multiplicado por 2:
```python
# Forma habitual de un ciclo 
for i in range(1, 11):
    if i % 2 == 0: # En este caso se crea una condicion para que solo se agreguen los numeros pares
        numbersCon.append(i*2) # Luego cada numero se multiplica por 2
print(numbersCon) # Al imprimirlo se puede ver que se crea una lista con los numeros del 1 al 20 pero solo los pares pero de dos en dos
```

* Luego, se muestra cómo se puede lograr el mismo resultado con la comprensión de listas:
```python
# Forma con la aplicación de la comprensión
numbers_V3 = [i*2 for i in range(1, 11) if i % 2 == 0] 
print(numbers_V3
```


## [05_dict-compren.py](05_dict-compren.py): Comprensión de diccionarios en Python

El archivo `05_dict-compren.py` se centra en la comprensión de diccionarios en Python. La comprensión de diccionarios es una forma concisa de crear diccionarios a partir de estructuras de datos existentes.

###  Comprensión de Diccionarios:

Este archivo muestra cómo usar la comprensión de diccionarios para crear nuevos diccionarios de manera eficiente.

### Sintaxis 
Al igual que las listas los diccionarios tambien permite implementear comprensiones

```python
 {key: value for value in iterable} 
```
En donde:
- `key`: es el nombre de la llave
- `value`: es el valor de la llave
- `iterable`: es el iterable que se va a recorrer

**Ejemplo de un diccionario sin comprension:**
```python
dict1 = {}
for i in range(1, 5):
    dict1[i] = i+3 # En este caso se suma cada numero el numero 3
```
**Ejemplo de un diccionario con comprension:**
```python
dict2 = {i: i+3 for i in range(1, 5)} # En este se emplea la sintaxis de un diccionario con comprension
```

###  Comprensión de Diccionarios a partir de una lista

**Ejemplo sin comprension:**
```python
countries = ["MX", "COL", "ARG", "USA"]
population = {}
for country in countries:
    population[country] = random.randint(1, 100) # Se genera un numero aleatorio entre 1 y 100 para cada pais
```
**Ejemplo con comprension:**
```python
population_v2 = {country: random.randint(1, 100) for country in countries} # En este se emplea la sintaxis de un diccionario con comprension
```

###  Comprensión de Diccionarios a partir de dos listas haciendo uso de la función `zip` y `len`

1. **Primera forma de crear un diccionario a partir de dos listas:**
   
    Este archivo muestra cómo generar un diccionario utilizando la función `zip` para unir dos listas y la comprensión de diccionarios.

```python
# Se crean dos listas: una con nombres y otra con edades
names = ["Juan", "Maria", "Pedro", "Luisa"]
ages = [18, 25, 30, 40, 50]

## En esta forma se crea una lista de tuplas con los nombres y sus respectivas edades
print(list(zip(names, ages)))

# Por otro lado en esta forma, se crea un diccionario con comprensión
new_dict = {names: ages for (names, ages) in zip(names, ages)}
```
- Este código genera un diccionario donde las claves son los nombres y los valores son las edades correspondientes, utilizando la función zip para unir las dos listas

2. **Segunda forma de crear un diccionario a partir de dos listas:**

   El archivo también muestra cómo generar un diccionario utilizando un `iterador` para recorrer las listas y la comprensión de diccionarios pero tambien se utiliza la función `len` para saber la longitud de la lista.

```python
# Se utiliza un iterador para recorrer las listas y se crea un diccionario con comprensión
dict3 = {names[i]: ages[i] for i in range(len(names))}
print(dict3)  # Se imprime el diccionario
```
- Para este caso, es importante el iterador `i` ya que permite recorrer las listas y crear el diccionario. Al imprimirlo, cumple la misma función que el ejemplo anterior.


> [!NOTE]
>
> La primera forma es más eficiente que la segunda para evitar errores de indexación.


## [06_dict-compren-condi.py](06_dict-compren-condi.py): Comprensión de diccionarios con condiciones en Python

En este archivo, exploramos cómo usar la comprensión de diccionarios con condiciones.

### Sintaxis 
Al igual que las listas los diccionarios tambien permite implementear comprensiones

```python
 {key: value for value in iterable} 
```
En donde:
- `key`: es el nombre de la llave
- `value`: es el valor de la llave
- `iterable`: es el iterable que se va a recorrer
- `condition`: es la condicion que se debe cumplir para que se agregue el elemento o no al diccionario

### Ejemplo de Comprensión de Diccionarios con Condiciones

Aquí hay un ejemplo de cómo se puede usar la comprensión de diccionarios para crear un nuevo diccionario que contenga solo los pares clave-valor de un diccionario existente que cumplan con una cierta condición.

1. **Ejemplo de Comprensión de Diccionarios sin Condiciones**
```python
import random
# En este se emplea la sintaxis de un diccionario con comprension para asignar un numero aleatorio entre 1 y 100 a cada pais
countries = ["MX", "COL", "ARG", "USA"]

population_V2 = {country: random.randint(1, 100) for country in countries}
```
2. **Ejemplo de Comprensión de Diccionarios con Condiciones**
   
   En este ejemplo country es la llave y population es el valor de la llave y se emplea la funcion `items()` para recorrer el diccionario de population_V2 y se agrega la condicion de que solo se agreguen los paises con poblacion mayor a 20 al diccionario result

```python
result ={country: population for (country, population) in population_V2.items() if population > 20}
```
3. **Ejemplo de Comprensión de Diccionarios con Condiciones a partir de un Texto**
   
   En este ejemplo a partir de un texto se va a crear un diccionario comprenhension con condicional donde imprima las vocales y la cantidad de veces que aparecen en el texto, para ello se emplea la funcion `upper` para que las vocales aparezcan en mayuscula y se agrega la condicion de que solo se agreguen las vocales al diccionario unique

```python
# 
text = "Hi, my name is Juan and I am a software developer"
# 
unique = { character: character.upper() for character in text if character in "aeiou"}
# Al imprimirlo se puede ver que se crea un diccionario con las vocales y la cantidad de veces que aparecen en el texto
print(unique)
```
> [!IMPORTANT]
>
> **En el siguiente modulo se exploran las funciones con el fin de profundizar mas acerca de los diccionarios con condicionales**


## Diferencias entre `List` vs `Tuples` vs `Sets`
![](https://i.postimg.cc/B6TvLHvk/imagen-2024-01-17-180952810.png)