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

## [01_set.py](Python_Sets-Compren_Classes/01_set.py): Creación y manipulación de conjuntos en Python

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

Por ejemplo, en [01_set.py](Python_Sets-Compren_Classes/01_set.py), se muestra cómo crear un conjunto, agregar elementos a él, y realizar operaciones de conjunto. También se muestra cómo los conjuntos pueden ser utilizados para eliminar duplicados de una lista.


## [02_crud-set.py](Python_Sets-Compren_Classes/02_crud-set.py): Operaciones CRUD en conjuntos de Python

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


## [03_set-operations.py](Python_Sets-Compren_Classes/03_set-operations.py): Operaciones de conjuntos en Python

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

## [04_list-compren.py](Python_Sets-Compren_Classes/04_list-compren.py): Comprensión de listas en Python

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


## [05_dict-compren.py](Python_Sets-Compren_Classes/05_dict-compren.py): Comprensión de diccionarios en Python

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


## [06_dict-compren-condi.py](Python_Sets-Compren_Classes/06_dict-compren-condi.py): Comprensión de diccionarios con condiciones en Python

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




# Funciones y 


## [07_fuctions.py](Python_Functions_Classes/07_fuctions.py): Funciones en Python

Son un conjunto de instrucciones que realizan una tarea específica y que pueden ser reutilizadas en cualquier parte del programa.

### Definición de Funciones
Las funciones se definen con la palabra clave `def`, seguida del nombre de la función y un par de paréntesis que contienen los parámetros. El cuerpo de la función está indentado y contiene las instrucciones que se ejecutarán cuando se llame a la función.
### Llamada de Funciones
Las funciones se llaman por su nombre, seguido de un par de paréntesis que contienen los argumentos.

>[!TIP]
> - El valor que ingresas cuando llamas la funcion se llama `PARAMETRO`
> 
> - Mientras que el valor que usamos dentro de la funcion se llama `ARGUMENTO`
<p align="center">
  <img src="https://i.postimg.cc/XYV0jZy2/imagen-2024-01-19-185546469.png" alt="Aquí va el texto del enlace">
</p>

### Función sin Parámetros

```python
def saludo(): # Definicion de la funcion
    print("Hola, soy una funcion") # Cuerpo de la funcion
    print("Hola de nuevo, soy una funcion") # Cuerpo de la funcion
saludo()
```
### Función con Parámetros

```python
def suma(number): # Definicion de la funcion
    print(number * 2) # Cuerpo de la funcion
suma(5)
```
### Función dentro de otra función

```python
def suma2(a,b): # Definicion de la funcion
    suma(a+b) # En este caso se llama a la funcion suma() dentro de la funcion suma2()
suma2(5,10) # Al imprimirse muestra la suma de los parametros de la funcion sum2() multiplicados por 2 teniendo en cuenta que la funcion suma() multiplica por 2
suma2(10,10)
```

###  Principio DRY
> [!IMPORTANT]
>
> Las funciones nos ayudan a cumplir con uno de los principios más importantes de la programación como lo es el principio **DRY (don’t repeat yourself)** o (no te repitas).
> 
> Al tener la lógica en una función evitas tener que escribir la misma lógica una y otra vez, de modo que tienes un código más limpio y más escalable.


## [08_func-return.py](Python_Functions_Classes/08_func-return.py): Funciones con retorno de variables

Son un conjunto de instrucciones que realizan una tarea específica, retornan un valor y pueden ser reutilizadas en cualquier parte del programa.

<p align="center">
  <img src="https://i.postimg.cc/L8K02hnJ/imagen-2024-01-19-202454349.png" alt="Aquí va el texto del enlace">
</p>

### Definición de Funciones con Retorno
Las funciones con retorno se definen con la palabra clave `def`, seguida del nombre de la función y un par de paréntesis que contienen los parámetros. El cuerpo de la función está indentado y contiene las instrucciones que se ejecutarán cuando se llame a la función. Al final del cuerpo de la función, se utiliza la palabra clave `return` para indicar el valor que la función retornará.

### Llamada de Funciones con Retorno
Las funciones con retorno se llaman por su nombre, seguido de un par de paréntesis que contienen los argumentos. El valor retornado por la función se puede almacenar en una variable para su uso posterior.

### Comprendiendo la logica del return mediante un ciclo for
```python
sum = 0
for x in range(1,10):
    sum += x
print(sum) # Este codigo imprime la suma de los numeros del 1 al 9 sin embargo si se quiere hacer la suma de los numeros del 1 al 1000 se tendria que modificar el codigo repetidas veces y esto no es eficiente por eso se crean las funciones con retorno
```

### Implementación de una "Función" para agilizar el código anterior
```python
def sum_with_range(min,max): # Definicion de la funcion
    sum = 0 # Variable que almacena la suma de los numeros
    for x in range(min,max): # Ciclo for que recorre los numeros del 1 al 1000
        sum += x # Esta linea suma los numeros del 1 al 1000
    print(sum)
    
sum_with_range(1,10) # En este caso el resultado seria 10 porque se suman los numeros del 1 al 9 como factorial
sum_with_range(20,30) # Este codigo imprime la suma de los numeros del 20 al 29
sum_with_range(1,100) # Este codigo imprime la suma de los numeros del 1 al 99
```

### Implementación de una "Función con retorno"
```python
def sum_with_range2(min,max): # Definicion de la funcion
    print(f"Entrada de los parametros minimo '{min}' y maximo '{max}' ")
    sum = 0 # Variable que almacena la suma de los numeros
    for x in range(min,max): # Ciclo for que recorre los numeros del 1 al 1000
        sum += x # Esta linea suma los numeros del 1 al 1000
    return sum # Esta linea retorna el valor de la suma

# Luego de esto es necesario declarar una variable que almacene el valor de retorno de la funcion de lo contrario no se podra imprimir el resultado de la funcion

result = sum_with_range2(1,10) # Se declara una variable que almacena el valor de retorno de la funcion
print(f"El resultado de la suma de los parametros es: {result}")

result_2 = sum_with_range2(result,result+10)
print(f"El resultado de la suma de los parametros es: {result_2}")
```


## [09_func-returnMul.py](Python_Functions_Classes/09_func-returnMul.py): Funciones con retorno de multiples valores y valores por defecto

### Funciones con Retorno de Múltiples Valores 
Las funciones pueden retornar múltiples valores, que se pueden almacenar en varias variables.
```python
def find_volume(lenth, width, depth): # En este caso se establecen los argumentos
    return lenth*width*depth # Se retorna el resultado de la operacion

result = find_volume(2,3,4) # Se declara la variable result y se le asigna el valor de la funcion find_volume
print(f"El volumen es: {result}") 
```

### Funciones con Parámetros por Defecto
Las funciones pueden tener parámetros con valores por defecto, que se utilizarán si no se proporciona un argumento para ese parámetro al llamar a la función.
```python
def find_volume2(length=2, width=3, depth=4): # En este caso se establecen los argumentos por defecto
    return length*width*depth, width, 'hola' # Se retorna el resultado de la operacion
print(f"El volumen es: {find_volume2()}") # En este caso se imprime el resultado de la funcion con los valores por defecto
```

### Reasignar un nuevo argumento a un parametro especifico
```python
print(f"El volumen es: {find_volume2(width=5)}") # En este caso se reasigna el valor del width a 5 dando como resultado el volumen de 40
```

### Retornar mas de una función por separado
```python
result2, width, saludo = find_volume2() # En este caso se declara las variables result2, width y saludo y se le asigna el valor de la funcion find_volume2
print(f"El volumen es: {result2}") # Se imprime el valor de la variable result2
print(f"El ancho es: {width}") # Se imprime el valor de la variable width
print(f"El saludo es: {saludo}") # Se imprime el valor de la variable saludo
```

## [09_func-returnMul.py](Python_Functions_Classes/09_func-returnMul.py): Alcance de variables o `scope` en Python

El scope es la visibilidad de una variable dentro de un programa, es decir, en qué partes del programa se puede acceder a una variable o no.

### Variables Globales
Las variables globales se pueden acceder desde cualquier parte del programa.
```python
# En este caso la variable global es 'name' y se puede acceder a ella desde cualquier parte del programa
name = "Juan" # Variable global
print(f"El nombre es: {name}") # Se imprime el valor de la variable global
```

### Variables Locales
Las variables locales solo se pueden acceder desde el bloque de código donde se declararon, generalmente dentro de una función.
```python
# En este caso la variable local es 'name' y solo se puede acceder a ella desde el bloque de codigo donde se declaro es decir dentro de la funcion
def print_name():
    name = "Luisa" # Variable local
    print(f"El nombre es: {name}") # Se imprime el valor de la variable local
print_name() # Se ejecuta la funcion
```

### Conversión de Variables Locales en Globales
Una variable local puede convertirse en global utilizando la palabra clave `global`.
```python
# En este caso se puede acceder a la variable global y local desde cualquier parte del programa
def print_name():
    global name # Se declara la variable global
    name = "Luisa" # Variable local
print_name() # Se ejecuta la funcion
print(f"El nombre es: {name}") # Se imprime el valor de la variable global
```

### Diferencia entre una variable global y una variable local
La variable global se puede acceder desde cualquier parte del programa mientras que la variable local solo se puede acceder desde el bloque de codigo donde se declaro mayormente dentro de una funcion
```python
name = "Juan" # Variable global
def print_name():
    name = "Luisa" # Variable local
    print(f"El nombre es: {name}") # Se imprime el valor de la variable local
print_name() # Se ejecuta la funcion
print(f"El nombre es: {name}") # Se imprime el valor de la variable global
```





