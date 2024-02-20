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




# Módulo 1: Estructura de datos p1: Conjuntos `(sets)`

## [01_set.py](Mod_1_2_Python_Sets_Compren/01_set.py): Creación y manipulación de conjuntos en Python

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

Por ejemplo, en [01_set.py](Mod_1_2_Python_Sets_Compren/01_set.py), se muestra cómo crear un conjunto, agregar elementos a él, y realizar operaciones de conjunto. También se muestra cómo los conjuntos pueden ser utilizados para eliminar duplicados de una lista.


## [02_crud-set.py](Mod_1_2_Python_Sets_Compren/02_crud-set.py): Operaciones CRUD en conjuntos de Python

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


## [03_set-operations.py](Mod_1_2_Python_Sets_Compren/03_set-operations.py): Operaciones de conjuntos en Python

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




# Módulo 2: Estructuras de datos p2: Listas `(list)` y Diccionarios `(dict)` con Comprenhentions

## [04_list-compren.py](Mod_1_2_Python_Sets_Compren/04_list-compren.py): Comprensión de listas en Python

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


## [05_dict-compren.py](Mod_1_2_Python_Sets_Compren/05_dict-compren.py): Comprensión de diccionarios en Python

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


## [06_dict-compren-condi.py](Mod_1_2_Python_Sets_Compren/06_dict-compren-condi.py): Comprensión de diccionarios con condiciones en Python

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
character_count = {character: text.lower().count(character) for character in 'aeiou' if text.lower().count(character) > 0} # Se incluye una condición para solo agregar las vocales al diccionario si aparecen en el texto (es decir, su conteo es mayor a 0).
print(character_count)
print(unique)
```
> [!IMPORTANT]
>
> **En el siguiente Módulo se exploran las funciones con el fin de profundizar mas acerca de los diccionarios con condicionales**


## Diferencias entre `List` vs `Tuples` vs `Sets`
![](https://i.postimg.cc/B6TvLHvk/imagen-2024-01-17-180952810.png)




# Módulo 3: Funciones en Python (Las mas utilizadas y sus diferencias)


## [07_fuctions.py](Mod_3_Python_Functions/07_fuctions.py): Funciones `def` en Python

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


## [08_func-return.py](Mod_3_Python_Functions/08_func-return.py): Funciones con retorno de variables

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


## [09_func-returnMul.py](Mod_3_Python_Functions/09_func-returnMul.py): Funciones con retorno de multiples valores y valores por defecto

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

## [10_scope.py](Mod_3_Python_Functions/10_scope.py): Alcance de variables o `scope` en Python

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


## [12_lambda-func.py](Mod_3_Python_Functions/12_lambda-func.py): Funciones `lamba` o anónimas

Las funciones lambda se definen con la palabra clave `lambda`, seguida de los parámetros y una expresión que constituye el cuerpo de la función.

### Sintaxis 

```python
 lambda argumentos: expresion
```
En donde:
- `lambda`: es la palabra reservada para indicar que es una funcion lambda
- `argumentos`: son los parametros que recibe la funcion, estos son opcionales
- `expresion`: es el cuerpo de la funcion, es decir, lo que hace la funcion 

### Uso de Funciones Lambda
Las funciones lambda son útiles cuando se quiere crear una función que se va a usar una sola vez.

### Función declarativa vs Función Lambda
<p align="center">
  <img src="https://i.postimg.cc/ncpXBkwm/imagen-2024-01-24-171139328.png" alt="Aquí va el texto del enlace">
</p>

### Función declarativa
```python
 def increment(n):
    return n + 1

result = increment(10)
print(result)
### En este caso una función declarativa requiere mas lineas de codigo que una función lambda
```

### Función lambda
```python
## Crear una lambda que devuelve el nombre completo
full_name = lambda first, last: f'The fullname is {first.title()} {last.title()}'

print(full_name('juan', 'perez'))
```
- La sintaxis de la lambda es la misma que la de una funcion pero en este caso se compone por:
1. `full_name`: es el nombre de la funcion
2. `lambda`: es la palabra reservada para indicar que es una funcion lambda
3. `first, last`: son los parametros de la funcion
4. `f'The fullname is {first.title()} {last.title()}'`: es el cuerpo de la funcion, es decir, lo que hace la funcion, utilizando la función title() para poner la primera letra en mayuscula



## [13_HOF.py](Mod_3_Python_Functions/13_HOF.py): HOF `(Higher Order Functions)` implementando Funciones Declarativas y Funciones Lambda

Son funciones que pueden tomar otras funciones como argumentos o devolver funciones como resultado.

### Funciones declarativas que reciben como paramatro una función
```python
def increment(n): # Esta funcion recibe como parametro un numero
    return n + 1 # Esta funcion retorna el numero ingresado mas 1

def high_order_function(x, func): # Esta funcion recibe como parametro un numero y una funcion
    return x + func(x) # Esta funcion retorna el numero ingresado mas el resultado de la funcion que se ingreso como parametro

result = high_order_function(2, increment) # Esta funcion retorna el numero 2 mas el resultado de la funcion increment y no es neceario ejecutar la funcion increment sino definirla como parametro
print(result) # Output: operacion 2 + (2 + 1) = 5
```

### Función que Retorna Otra Función Utilizando Funciones `Lambda`
```python
increment_V2 = lambda x : x + 1 # Esta lambda permite hacer lo mismo que la funcion increment sin necesidad de definir una función usando def o declarar su retorno con return

high_order_function_V2 = lambda x, func: x + func(x) # Emplea el mismo comportamiento que la función declarativa

result = high_order_function_V2(2, increment_V2) # 
print(result) # la salida seria la operacion 2 + (2 + 1) = 5 
```

### Declarar Lambdas Directamente al Designar los Argumentos de una Función
```python
## Primero es necesario definir la función inicial como lambda
high_order_function_V2 = lambda x, func: x + func(x) # Esta funcion recibe como parametro un numero y una funcion y retorna el numero ingresado mas el resultado de la funcion que se ingreso como parametro
result = high_order_function_V2(2, lambda x: x + 1) # Al declararse la variable permite establecer como parametro una función lambda
print(result)
```

# Funciones más utilizadas en Python y su comportamiento
<p align="center">
  <img src="https://i.postimg.cc/h4sX8YQB/imagen-2024-01-24-181612046.png" alt="Aquí va el texto del enlace">
</p>



## [14_map-func.py](Mod_3_Python_Functions/14_map-func.py): Función `map`

La función `map`  es una funcion que recibe como parametro una funcion y un iterable y retorna un objeto map que es un iterador que permite recorrer cada elemento del iterable y aplicarle la funcion que se ingreso como parametro a cada elemento del iterable

### Sintaxis 

```python
  map(funcion, iterable)
```
En donde:
- `map`: es la palabra reservada para indicar que es una funcion map
- `funcion`: es la funcion que se va a aplicar a cada elemento del iterable
- `iterable`: es el iterable que se va a recorrer

### Ejemplo contextual para las función `map`
```python
numbers = [2, 4, 6, 8, 10] # Se crea una lista con numeros
numbers_plus_one = [] # Se crea una lista vacia
for number in numbers: # Se recorre la lista numbers
    numbers_plus_one.append(number * 2) # Se agrega a la lista numbers_plus_one el numero de la lista numbers multiplicado por 2
print(numbers) # Output: [2, 4, 6, 8, 10]
print(numbers_plus_one) # Output: [4, 8, 12, 16, 20]
```

>[!NOTE]
>
> ### Utilidad de las Función `map` para un codigo mas legible
>
> La función map es una de las funciones más utilizadas en Python, ya que permite aplicar una función a cada elemento de un iterable (lista, tupla, etc.) y retornar un iterador para recorrer los resultados y permite reducir el código y hacerlo más legible utilizando ademas funciones lambda.

### Implementación de la función `map`
```python
# Ejemplo de la funcion map usando una función lambda en una sola linea
numbersv3 = map(lambda number: number * 2, numbers) # Se crea un objeto map que incorpora la funcion lambda que multiplica por 2 cada numero de la lista numbers
print(numbersv3) # Output: <map object at 0x7f1d9f7d7a90>
list_numbersv3 = list(numbersv3) # Se convierte el objeto map en una lista
print(list_numbersv3) # Output: [4, 8, 12, 16, 20]
```

### Ejemplo donde se reemplaza los valores iniciales de una lista por los de otra lista 
En algunos casos una lista puede tener una longitud de datos mayor que otra para ello el output se tomara de la lista con menor cantidad
```python
list1 = [1, 2, 3, 4, 5]# Se crea una lista con numeros
list2 = [6, 7, 8, 9] # Se crea una lista con numeros
list3 = map(lambda a, b: a + b, list1, list2) # Se crea un objeto map que incorpora la funcion lambda que suma los valores de las dos listas
print(list1) # Output: [1, 2, 3, 4, 5]
print(list2) # Output: [6, 7, 8, 9]
print(list3) # Output: <map object at 0x7f1d9f7d7a90>
list3 = list(list3) # Se convierte el objeto map en una lista
print(list3) # Output: [7, 9, 11, 13] debido a que la lista 2 tiene un elemento menos que la lista 1 el resultado es una lista con 4 elemen
```


## [15_map-dicts.py](Mod_3_Python_Functions/15_map-dicts.py): Función `map` en diccionarios

La función `map` tambien se puede usar en diccionarios

### Implementación de función `map` en dictionarys 
Para este ejemplo primero se crea una lista con varios diccionarios 
```python
items = [
    {
     'product': 'laptop',
     'price': 800,
     },
    {
        'product': 'mouse',
        'price': 40,
    },
    {
        'product': 'monitor',
        'price': 400,
    }
]
```

1. Para el primer caso se desea solo imprimir una lista de precios utilizando la función map y el método list
```python
prices = list(map(lambda item: item['price'], items)) # Se crea un objeto map que incorpora la funcion lambda que retorna los precios de los productos del diccionario items
print(prices) # Output: [800, 40, 400]
```

2. Ahora para el segundo caso, se desea agregar un nuevo campo que calcule el impuesto de los precios, lo cual no basta con declararlo en una sola linea sino que se debe definir una función que retorne la operación
```python
# 1. Crear una funcion que calcule el impuesto
def add_taxes(item):
    item['taxes'] = item['price'] * 0.8
    return item

# 2. Definir la funcion en la funcion map
new_item = list(map(add_taxes, items)) # Se crea un objeto map que incorpora la funcion add_taxes que retorba todos los items del diccionario items con el impuesto

print(new_item) # Output: [{'product': 'laptop', 'price': 800, 'impuesto': 640.0}, {'product': 'mouse', 'price': 40, 'impuesto': 32.0}, {'product': 'monitor', 'price': 400, 'impuesto': 320.0}]
```

> [!WARNING]
> 
> ### Condiciones a tener en cuenta cuando se implementa `map` en diccionarios
>
> El utilizar estas funciones se debe tener precación debido a que puede generar un cambio en el array original lo que puede ocasionar problemas en el codigo o errores de logica, entonces para solucionar ello se puede utilizar la biblioteca copy para crear una copia del array original y no modificarlo o otro logica que evite esta excepción

- Antes de crear la función map donde se desea crear un nuevo campo se puede generar una copia en memoria del array original mediante la libreria copy
```python
# 1. Importar la biblioteca copy
import copy
# 2. Crear una copia del array original

## Primer modo de crear una copia del array original
items_cp = copy.copy(items)
print(items_cp) # Output: [{'product': 'laptop', 'price': 800}, {'product': 'mouse', 'price': 40}, {'product': 'monitor', 'price': 400}]

## Segundo modo de crear una copia del array original
items_copy = copy.deepcopy(items)
print(items_copy) # Output: [{'product': 'laptop', 'price': 800}, {'product': 'mouse', 'price': 40}, {'product': 'monitor', 'price': 400}]

## Resto del codigo donde se crea la función map
```

### Diferencia entre `copy` y `deepcopy`
Con respecto al ejemplo anterior al generar una copia del array original con `copy` solo crea una copia superficial del array original, mientras que `deepcopy` crea una copia profunda del array original, es decir, si el array original tiene un array dentro de otro array entonces deepcopy crea una copia de cada array

### Alternativa a copy con otra forma mediante la función `map`
De otro modo tambien se puede añadir una nueva clave valor sin afectar el array original, directamente en la linea del map de la siguiente manera
```python

# --------------- Codigo donde esta declarado el diccionario

# Se puede usar la expresión **nombreDeLaVar para obtener un nuevo diccionario con los mismos elementos del diccionario original
newItems = map(lambda item: {**item, 'tax': item['price'] * .19}, items) # Se crea un objeto map que incorpora la funcion lambda la cual a su vez usa **[NombreDeLaVaria] que en este caso es "item" para desempaquetar el diccionario item y agregarle un nuevo campo llamado tax que es el impuesto del producto

print(list(newItems)) # Output: [{'product': 'tshirt', 'price': 100, 'tax': 19.0}, {'product': 'pants', 'price': 300, 'tax': 57.0}, {'product': 'blue white pants', 'price': 200, 'tax': 38.0}]
print(items) # Output: [{'product': 'tshirt', 'price': 100}, {'product': 'pants', 'price': 300}, {'product': 'blue white pants', 'price': 200}]
```


## [17_filter-func.py](Mod_3_Python_Functions/17_filter-func.py): Función `filter`

Esta función incorporada de Python toma dos argumentos, una función y un iterable, y devuelve un iterable con los elementos del iterable original para los que la función devuelve True.
### Sintaxis 

```python
filter(función, iterable)
```
En donde:
- `función`: es una función que retorna un valor booleano
- `iterable`: es una lista o diccionario

### Función `filter` en listas

 ```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] # Lista de números
even_numbers = list(filter(lambda x: x % 2 == 0, numbers)) # 
print(even_numbers) # output: [2, 4, 6, 8, 10]
print(numbers) # output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]```
```
- En este caso en la función filter se retorna los números  pares de la lista mediante una función lambda filtrada por la función filter en formato de lista

### Función `filter` en diccionarios

 ```python
matches = [
  {
    'home_team': 'Bolivia',
    'away_team': 'Uruguay',
    'home_team_score': 3,
    'away_team_score': 1,
    'home_team_result': 'Win'
  },
  {
    'home_team': 'Brazil',
    'away_team': 'Mexico',
    'home_team_score': 1,
    'away_team_score': 1,
    'home_team_result': 'Draw'
  },
  {
    'home_team': 'Ecuador',
    'away_team': 'Venezuela',
    'home_team_score': 5,
    'away_team_score': 0,
    'home_team_result': 'Win'
  },
] # Esta lista de diccionarios muestra los resultados de los partidos de futbol
print(f'Lista original: {matches} ') 
print(len(matches)) # Output: 3
print('\n')
## Ahora se desea filtrar una lista con solo los partidos que ganó el equipo local
new_list = list(filter(lambda item: item['home_team_result'] == 'Win', matches))
print(f'Lista nueva: {new_list}') 
print(len(new_list)) # Output: 2
```
- En este caso en la función filter se retorna los partidos que ganó el equipo local mediante una función lambda y el iterable item

## [18_reduce-func.py](Mod_3_Python_Functions/18_reduce-func.py): Función `reduce` y uso de la libreria `functools` con el Módulo `reduce`

El archivo 18_reduce-func.py se centra en la demostración del uso de la función reduce en Python. Esta función permite reducir una lista a un solo valor aplicando una función a cada elemento de la lista.

### Sintaxis
La sintaxis de la función reduce es la siguiente:
```python
reduce(función, iterable)
```
Donde:
- `función`: es una función que toma dos argumentos, el acumulador y el elemento actual, y devuelve un nuevo valor para el acumulador.
- `iterable`: es una lista o diccionario.

### Importación de la libreria `functools`
La función reduce no está disponible por defecto en Python, por lo que es necesario importarla del módulo functools.


### Función `reduce` en listas
- En este ejemplo, se utiliza la función reduce con una función lambda para sumar todos los números en una lista.
```python
# Importamos la función reduce del módulo functools
import functools

# Definimos una lista de números
numbers = [1, 2, 3, 4, 5]

# Utilizamos reduce con una función lambda para sumar todos los números en la lista
result = functools.reduce(lambda counter, item: counter + item, numbers) # Retorna la suma de los elementos de la lista que a diferencia de filter y map no retorna una lista sino un solo valor

# Imprimimos el resultado
print(result) # Output: 15
```

### Función `reduce` en diccionarios

- En este ejemplo, se utiliza la función reduce con una función lambda para sumar los goles de los partidos de fútbol en una lista de diccionarios. Retornando la suma de los goles de los partidos tanto de local como de visitante
```python
# Importamos la función reduce del módulo functools
import functools

# Definimos una lista de diccionarios que representan partidos de fútbol
matches = [
    {
        'home_team': 'Bolivia',
        'away_team': 'Uruguay',
        'home_team_score': 3,
        'away_team_score': 1,
        'home_team_result': 'Win'
    },
    {
        'home_team': 'Brazil',
        'away_team': 'Mexico',
        'home_team_score': 1,
        'away_team_score': 1,
        'home_team_result': 'Draw'
    },
    {
        'home_team': 'Ecuador',
        'away_team': 'Venezuela',
        'home_team_score': 5,
        'away_team_score': 0,
        'home_team_result': 'Win'
    },
]

# Utilizamos reduce con una función lambda para sumar los goles de los partidos de fútbol
total_goals = functools.reduce(lambda counter, item: counter + item['home_team_score'] + item['away_team_score'], matches, 0) # El 0 es el valor inicial de la variable counter
****
# Imprimimos el resultado
print(total_goals) # Output: 11
```

> [!NOTE]
> 
> # La diferencia entre una función `def` y una función `lambda` en cuanto a su legibilidad y mantenibilidad
>
> - `def` se utiliza para definir funciones normales. Pueden tener cualquier número de argumentos y cualquier cantidad de código dentro de ellas. También pueden tener un nombre, lo que permite reutilizarlas en diferentes partes del código.
> 
> - `lambda` se utiliza para definir funciones anónimas pequeñas. Estas funciones son de una sola línea y no tienen un nombre. Son útiles cuando necesitas una función pequeña para una operación única, como pasarla como argumento a funciones como `map()`, `filter()`, etc.
> ### En términos de mantenibilidad:
> - Las funciones `def` son más fáciles de leer y mantener, especialmente para funciones más largas y complejas. Pueden tener un nombre, lo que facilita la comprensión de su propósito. También pueden tener documentación a través de docstrings.
> 
> - Las funciones `lambda` son útiles para operaciones simples y de una sola línea, pero pueden ser difíciles de leer y mantener si se utilizan para operaciones más complejas. No pueden tener un nombre ni docstrings, lo que puede hacer que sea más difícil entender su propósito.

>[!IMPORTANT]
> 
> En resumen, si estás escribiendo una función más larga y compleja que se utilizará en varias partes de tu código, probablemente deberías usar `def`. 
> 
> Por otro lado, si solo necesitas una función simple para una operación única, `lambda` puede ser una buena opción.




# Módulo 4: Módulos en Python

## 1. ¿Que son los modulos?
> [!IMPORTANT]
> 
> Los modulos **son archivos que contienen un conjunto de funciones que pueden ser importadas y utilizadas en otros programas.** 
> - Estos por otro lado tambien pueden ser considerados como todo archivo con la extensión `.py` donde se pueden definir funciones, clases o variables. 
> 
> Es por ello que **los modulos son una forma de organizar y reutilizar código.**

### 1.1 Modulos por defecto en Python y los mas utilizados
- `random`: Genera números aleatorios.
```python
from random import randint
print(randint(1, 10))  # Imprime un número aleatorio entre 1 y 10
```
- `os`: Proporciona funciones para interactuar con el sistema operativo.
```python
import os
print(os.getcwd())  # Imprime el directorio de trabajo actual
```
- `sys`: Proporciona acceso a algunas variables utilizadas o mantenidas por el intérprete de Python.
```python
import sys
print(sys.version)  # Imprime la versión de Python
```
- `re`: Proporciona funciones para trabajar con expresiones regulares.
```python
import re
print(re.match(r'\d+', '123abc'))  # Busca uno o más dígitos al principio de la cadena
```
- `time`: Proporciona funciones para trabajar con tiempos y fechas.
```python
import time
print(time.time())  # Imprime el tiempo actual en segundos desde la época
```
- `collections`: Implementa tipos de contenedores especializados que proporcionan alternativas a los contenedores generales de Python.
```python
from collections import Counter
numbers = [1, 1, 2, 1, 2, 1, 4, 5, 3, 3, 21]
counter = Counter(numbers) # Retorna un diccionario con el conteo de cada elemento de la lista
print(counter) # output: Counter({1: 1, 2: 1, 3: 1, 4: 1, 5: 1, 6: 1, 7: 1, 8: 1, 9: 1, 10: 1})
```
- `datetime`: Proporciona clases para manipular fechas y horas.
```python
from random import randint
print(randint(1, 10))  # Imprime un número aleatorio entre 1 y 10
```
- `math`: Proporciona funciones matemáticas.
```python
import math
print(math.sqrt(16))  # Imprime la raíz cuadrada de 16
```
- `json`: Proporciona funciones para trabajar con datos JSON.
```python
import json
print(json.dumps({"name": "John", "age": 30}))  # Convierte un diccionario a una cadena JSON
```
- `csv`: Proporciona funciones para leer y escribir archivos CSV.
```python
import csv
with open('file.csv', 'r') as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)  # Imprime cada fila del archivo CSV
```



## [20_modules-app](20_modules-app): ¿Como construir modulos en Python?
Para construir módulos debemos tener en cuenta que se deben crear en la misma carpeta a lo cual utilizaremos `import` para ser llamada en el archivo a trabajar

> [!TIP] 
> 
> Una buena practica para nombrar archivos que se consideran modulos es nombrandolos como `utils.py`, `helpers.py`, etc. lo que permitira que otros programadores sepan que son modulos que contienen funciones que pueden ser reutilizadas en otros programas del mismo archivo.

> [!IMPORTANT] 
> 
> Ademas normalmente los archivos que  tienen utilidades solo manejan funciones para que no se mezclen con las variables y clases de otros archivos.

### Sintaxis
Para poder usar las funciones y variables definidas en un módulo se emplea la siguiente sintaxis 
```python
from nombre_modulo import (nombre_funcion, nombre_variable)
```
**Donde**:
- `función`: es una función que toma dos argumentos, el acumulador y el elemento actual, y devuelve un nuevo valor para el acumulador.
- `iterable`: es una lista o diccionario.
- `nombre_modulo` es el nombre del archivo sin la extensión .py
- `nombre_funcion` es el nombre de la función que se va a importar
- `nombre_variable` es el nombre de la variable que se va a importar
"""

### Renombrar un modulo o una función al importarla
- **Para los modulos es**:
```python
import nombre_modulo as nuevo_nombre 
```
- **Para las funciones o variables** 
```python
from nombre_modulo import nombre_funcion as nuevo_nombre
```
### Ejemplos de Funciones y Variables importadas de un `modulo.py`
#### 1 Funciones Importadas
1. Para este ejemplo se define una función que puede ser reutilizada en otros programas.
   
   - La función `get_population()` retorna dos listas, una con las llaves y otra con los valores que se van a emplear en el diccionario
   ```python
    def get_population():

        keys = ["col", "arg"]
        values = ["col", "arg"]
        return keys, values

    ```

    - La forma de llamarlo desde otro archivo se estableceria de la siguiente manera
   ```python
    import utils_1 as u  # De este modo se importa el módulo utils.py y se le asigna el nombre u
    keys, values = (
        u.get_population()
    )  # De este modo se importa la función get_population() del módulo utils.py y se asigna a las variables keys y values
    print(keys, values)
    ```

2. Otro ejemplo de una función de una población basado en un pais llamada `population_by_country()` que utiliza una lambda function para filtrar los paises de la lista de diccionarios data y retorna el pais y su población 

   ```python
    def population_by_country(data, country):
    result = list(filter(lambda item: item['Country'] == country, data))
    return result
    ```

   - Para hacer uso de esta función se debe definir una lista de diccionarios con la población de varios países 
   ```python
    data = [
    {"Country": "Colombia", "Population": 502},
    {"Country": "Argentina", "Population": 400},
    {"Country": "Peru", "Population": 300},
    {"Country": "Mexico", "Population": 700},
    ] 
    result = u.population_by_country(
        data, "Colombia"
    )  # La variable result almacena el resultado de la función population_by_country() del módulo utils.py y solo se le pasa el país "Colombia" junto con su población
    print(result)  # Output: [{'Country': 'Colombia', 'Population': 502}] # Se imprime el resultado de la función population_by_country() del módulo utils.py
    ```
    - Para solo hacer el llamado de la función basta con declarar la sintaxis `from...import`
   ```python
    import utils_1 as u  # De este modo se importa el módulo utils.py y se le asigna el nombre u
    keys, values = (
        u.get_population()
    )  # De este modo se importa la función get_population() del módulo utils.py y se asigna a las variables keys y values
    print(keys, values)
    ```


#### 2 Variables Importadas
3. Al igual que las funciones las variables definidas en un módulo pueden ser reutilizadas en otros programas.
   
   - **Ejemplo**
   ```python
    A = 'Hola'
    ```
    - Para llamarla solo se importa la libreria 
   ```python
    print(u.A)  # De este modo se imprime la variable A del módulo mod.py
    ```



## [21_scripts_modules](21_scripts_modules): ¿Que son y como utilizar los Scripts de modulos en Python?

### ¿Que son los Scripts en Python?
Los scripts de Python son programas que se pueden ejecutar directamente por el intérprete de Python sin necesidad de ser compilados previamente. Esto es posible gracias a la naturaleza interpretada de Python donde comienza toda la ejecución de un programa que se le denomina `"entry point"`.

> [!IMPORTANT]
> 
> ### ¿Que es el punto de entrada `entry point`?
>
> En Python, el punto de entrada suele ser una línea que se ve así:
> ```python
> if `__name__` == `"__main__":`
>    main() # Corresponde al nombre de la función
> ```
> - Aquí, `main()` es una función definida por el usuario que contiene el código que se ejecutará cuando se inicie el programa.
> 
> - La condición `if `__name__` == `"__main__":`` se cumple cuando el script se ejecuta directamente. Esto se debe a que cuando Python ejecuta un archivo directamente, establece la variable especial ``__name__`` en "``__main__``".
> 
> - Si el archivo se importa como un módulo en otro script, ``__name__`` se establece en el nombre del archivo, por lo que el código bajo la condición `if `__name__` == `"__main__"`:` no se ejecuta. 

> [!NOTE]
> 
> Esto es útil cuando quieres que ciertas partes de tu código solo se ejecuten cuando el archivo se ejecute directamente, y no cuando se importe como un módulo.

### Ejemplo practico para comprender el comportamiento de los scripts en Python

- Imagina que tienes dos archivos de Python: `main.py` y `module.py`.

    - El archivo `module.py` contiene lo siguiente:
    ```python
    def hello():
        print("Hola desde module.py!")

    if `__name__` == `"__main__":`
        print("module.py se está ejecutando directamente")
    else:
        print("module.py se ha importado como un módulo")
    ```
    - Y el archivo `main.py` contiene lo siguiente:
    ```python
    import module

    module.hello()
    ```
- Si ejecutas `module.py` directamente desde la línea de comandos con `python module.py`, verás lo siguiente:
    ```python
    module.py se está ejecutando directamente
    ```
    - Esto se debe a que `__name__` es `"__main__"` cuando ejecutas `module.py` directamente, por lo que el código dentro del bloque `if __name__ == "__main__":` se ejecuta.
- Por otro lado, si ejecutas `main.py` con `python main.py`, verás lo siguiente:
     ```python
    module.py se ha importado como un módulo
    Hola desde module.py!
    ```
    - Esto se debe a que `module.py` se importa como un módulo en `main.py`, por lo que `__name__` no es `"__main__"` en `module.py`. Como resultado, el código dentro del bloque `if __name__ == "__main__":` no se ejecuta, pero la función hello que se llama en `main.py` sí se ejecuta.



## [22_mi_paquete](mi_paquete_22): ¿Que son y como utilizar los Paquetes `pkg` de modulos en Python?

Los paquetes en Python son una forma de organizar módulos relacionados en un directorio. Un paquete es simplemente un directorio que contiene uno o más archivos `.py`, junto con un archivo especial llamado `__init__.py`.

El archivo `__init__.py` es necesario para que Python reconozca el directorio como un paquete. Este archivo puede estar vacío, o puede contener código válido de Python. A menudo se utiliza para realizar inicializaciones necesarias para el paquete, o para definir una API específica para el paquete.

### Ejemplo de cómo estructurar un paquete:

```python
mi_paquete/
    __init__.py
    modulo1.py
    modulo2.py
```

En este caso, `mi_paquete` es un paquete que contiene dos módulos: `modulo1` y `modulo2`. Puedes importar estos módulos con la siguiente sintaxis:

```python
from mi_paquete import modulo1, modulo2
```

O puedes importar funciones o clases específicas de los módulos:

```python
from mi_paquete.modulo1 import mi_funcion
```

El archivo `__init__.py` también puede decidir qué módulos se importan por defecto cuando importas el paquete. Por ejemplo, si `__init__.py` contiene la siguiente línea:

```python
from . import modulo1
```

Entonces, cuando importas `mi_paquete`, `modulo1` se importará automáticamente:

```python
import mi_paquete  # Esto importará mi_paquete.modulo1 automáticamente junto con sus funciones o variables declaradas
```

Los paquetes son una característica importante de Python que te permite organizar tu código de manera más efectiva. Te permiten agrupar módulos relacionados juntos, lo que puede hacer que tu código sea más fácil de entender y mantener.

### Paquetes regulares `(regular packages)` y Paquetes de espacio de nombres `(namespaces packages)`

El tipo de paquete que contiene un archivo `__init__.py` se conoce comúnmente como un "paquete regular" o simplemente un "paquete" en Python.

El archivo `__init__.py` es lo que distingue a un paquete de un directorio normal. Este archivo puede estar vacío, pero debe estar presente para que Python reconozca el directorio como un paquete.

> [!NOTE]
> 
> **A partir de Python 3.3, también se introdujo el concepto de "paquetes de espacio de nombres", que son paquetes que no requieren un archivo` __init__.py`. Sin embargo, los paquetes regulares con un archivo `__init__.py` son todavía muy comunes y ampliamente utilizados.**

### Diferencia entre `regular pkg` y `namespaces pkg`
En Python, existen dos tipos de paquetes para organizar módulos relacionados: "Regular Packages" y "Namespace Packages".

**Regular Packages**: Son directorios que contienen un archivo `__init__.py`(que puede estar vacio) y uno o más archivos de módulo Python. Python reconoce estos directorios como paquetes regulares. El archivo `__init__.py` se ejecuta al importar el paquete y puede contener cualquier código Python, a menudo utilizado para inicializar el paquete.
- **Por ejemplo:**
```python
mi_paquete/
    __init__.py
    modulo1.py
    modulo2.py
```

**Namespace Packages**: Introducidos en Python 3.3, son similares a los paquetes regulares pero no requieren un archivo `__init__.py`. Esto permite que múltiples directorios diferentes contribuyan a un mismo paquete.

- **Por ejemplo, si tienes los siguientes directorios en tu sys.path:**
```python
dir1/
    mi_paquete/
        modulo1.py

dir2/
    mi_paquete/
        modulo2.py
```

Python fusionará estos directorios en un único paquete de espacio de nombres `mi_paquete`.
> [!TIP]
> 
> #### Buena practica de emplear el namespace en python
> - **Ejemplo**
> ```python
> print(mi_paquete.mod_1.func_1()) 
> ```
> En este ejemplo de namespace package, se puede acceder a los modulos y sus funciones de la siguiente manera:
> 
> ` mi_paquete.mod_1.func_1()` o `mi_paquete.mod_2.func_3()` sin necesidad de importarlos directamente y **esto como solución a las importaciones o funciones que pueden estar bajo el mismo nombre**. 
> 
> *Cabe aclarar que no se pueden invocar directamente sin antes haberlos importado en*`mi_paquete/__init__.py`

En resumen, la principal diferencia entre los paquetes regulares y los de espacio de nombres es que los paquetes regulares están contenidos en un solo directorio y requieren un archivo `__init__.py`, mientras que los paquetes de espacio de nombres pueden extenderse a través de múltiples directorios y no requieren un archivo `__init__.py`.

