# Introducción a Python 


## Conceptos básicos y sintaxis 

### ¿Qué es Python?

1. Definición de Python: Python es un lenguaje de programación de alto nivel, interpretado, dinámicamente tipado y multiplataforma, que se caracteriza por tener una sintaxis clara y sencilla.

2. Historia de Python: Python fue creado por Guido van Rossum a finales de los años 80. El nombre de Python proviene de la afición de Guido por el grupo de comedia británico Monty Python.

### Características de Python

1. Interpretado: Python es un lenguaje interpretado, lo que significa que el código fuente es ejecutado directamente por un intérprete, sin necesidad de ser compilado previamente.

2. Tipado dinámico: En Python, no es necesario definir el tipo de una variable antes de asignarle un valor. El tipo de una variable es determinado dinámicamente durante la ejecución del programa.

3. Multiplataforma: Python puede ser utilizado en diferentes sistemas operativos, como Windows, Linux o Mac OS X.

4. Sintaxis clara y sencilla: La sintaxis de Python es sencilla y fácil de leer, lo que hace que el código sea más legible y fácil de mantener.

### Entorno de desarrollo

1. Instalación de Python: Para utilizar Python es necesario instalarlo en el equipo. Existen diferentes versiones de Python, por lo que es importante elegir la versión adecuada para el proyecto en el que se va a trabajar.

2. Intérprete de Python: El intérprete de Python es el programa que se encarga de ejecutar el código fuente escrito en Python. Se puede acceder al intérprete a través de la línea de comandos o utilizando un entorno de desarrollo integrado (IDE).

3. Editores de código: Existen diferentes editores de código y entornos de desarrollo integrado (IDE) que facilitan la escritura y depuración de código Python. Algunos de los más populares son Visual Studio Code, PyCharm, Jupyter Notebook y Sublime Text.

### Primeros pasos en Python

1. Hello World!: La forma más sencilla de comenzar a programar en Python es escribir un programa que muestre "Hello, World!" en la pantalla. Para ello, basta con escribir el siguiente código:

```python
print("Hello, World!")
```

2. Variables y asignación: Las variables son contenedores en los que se almacenan datos. Para asignar un valor a una variable, se utiliza el operador `=`. Por ejemplo:

```python
mensaje = "Hello, World!"
print(mensaje)
```

3. Comentarios: Los comentarios son líneas de texto que no son ejecutadas por el intérprete de Python. Se utilizan para explicar el funcionamiento del código y facilitar su comprensión. En Python, se pueden utilizar comentarios de una línea utilizando el símbolo `#`. Por ejemplo:

```python
# Este es un comentario
print("Hello, World!")  # Este es otro comentario
```

4. Operadores básicos: Python incluye una serie de operadores básicos para realizar operaciones matemáticas como suma (`+`), resta (`-`), multiplicación (`*`), división (`/`), módulo (`%`) y potencia (`**`). Por ejemplo:

```python
a = 5 + 3
b = 8 - 2
c = 3 * 7
d = 10 / 2
e = 7 % 3
f = 2 ** 3
```

5. Entrada y salida de datos: Para recibir datos del usuario, se puede utilizar la función `input()`. Para mostrar datos en pantalla, se utiliza la función `print()`. Por ejemplo:

```python
nombre = input("Introduce tu nombre: ")
print("Hola, " + nombre + "!")
```

## Variables y tipos de datos 

### Variables y tipos de datos

1. Variables y asignación: Ya se introdujeron las variables y cómo asignarles valores. Es importante recordar que en Python el tipo de una variable se determina dinámicamente en tiempo de ejecución.

2. Tipos de datos en Python: Python admite varios tipos de datos, como números, cadenas de texto y valores booleanos. Algunos de los tipos de datos más comunes son: `int`, `float`, `str` y `bool`.

3. Conversión de tipos: Es posible convertir entre diferentes tipos de datos utilizando funciones como `int()`, `float()`, `str()` y `bool()`. Por ejemplo:

```python
numero = int("123")
texto = str(456)
```

### Tipos numéricos

1. Enteros: Los enteros son números sin decimales. En Python, se representan con el tipo de dato `int`.

2. Flotantes: Los flotantes son números con decimales. En Python, se representan con el tipo de dato `float`.

3. Operaciones numéricas: Además de los operadores básicos mencionados anteriormente , existen otros operadores y funciones que se pueden utilizar para realizar operaciones matemáticas más avanzadas:

1. División entera: La división entera (`//`) devuelve el cociente de la división sin decimales. Por ejemplo:

```python
resultado = 7 // 2  # resultado = 3
```

2. Funciones matemáticas: Python incluye el módulo `math`, que proporciona funciones matemáticas adicionales, como raíz cuadrada, seno, coseno, tangente, logaritmos y muchas más. Para utilizar estas funciones, primero es necesario importar el módulo:

```python
import math

raiz_cuadrada = math.sqrt(9)  # raiz_cuadrada = 3.0
seno = math.sin(math.pi / 2)  # seno = 1.0
```

### Cadenas

1. Cadenas de caracteres: Las cadenas de caracteres (o simplemente, cadenas) son secuencias de caracteres. En Python, se representan con el tipo de dato `str`. Se pueden crear utilizando comillas simples (`'`) o dobles (`"`):

```python
cadena1 = 'Hola, mundo!'
cadena2 = "¡Adiós, mundo!"
```

2. Concatenación de cadenas: Se pueden unir dos o más cadenas utilizando el operador `+`. Por ejemplo:

```python
saludo = "Hola, " + "mundo!"  # saludo = "Hola, mundo!"
```

3. Métodos de cadenas: Las cadenas tienen varios métodos útiles para realizar operaciones como convertir a mayúsculas o minúsculas, reemplazar caracteres, dividir cadenas, etc. Algunos ejemplos:

```python
texto = "Hello, World!"
texto_en_mayusculas = texto.upper()  # "HELLO, WORLD!"
texto_en_minusculas = texto.lower()  # "hello, world!"
```

### Booleanos

1. Valores booleanos: Los valores booleanos representan verdadero o falso. En Python, se representan con el tipo de dato `bool` y los valores `True` y `False`.

2. Operadores de comparación: Python incluye operadores de comparación para determinar si dos valores son iguales (`==`), diferentes (`!=`), mayores (`>`), menores (`<`), mayores o iguales (`>=`) o menores o iguales (`<=`). Estos operadores devuelven un valor booleano:

```python
a = 5
b = 3
resultado = a > b  # resultado = True
```

3. Operadores lógicos: Los operadores lógicos permiten combinar valores booleanos utilizando operaciones como `and`, `or` y `not`. Por ejemplo:

```python
verdadero = True
falso = False

resultado1 = verdadero and falso  # resultado1 = False
resultado2 = verdadero or falso   # resultado2 = True
resultado3 = not verdadero        # resultado3 = False
```

En el próximo módulo, se abordarán estructuras de control de flujo, como condicionales y bucles.

### Estructuras de control de flujo

1. Condicionales: Los condicionales permiten ejecutar bloques de código solo si se cumple una condición determinada. La estructura básica de un condicional en Python es la siguiente:

```python
if condicion:
    # Bloque de código que se ejecuta si la condición es verdadera
```

También se pueden utilizar `elif` (abreviatura de "else if") y `else` para comprobar múltiples condiciones:

```python
if condicion1:
    # Bloque de código que se ejecuta si la condición1 es verdadera
elif condicion2:
    # Bloque de código que se ejecuta si la condición2 es verdadera
else:
    # Bloque de código que se ejecuta si ninguna de las condiciones anteriores es verdadera
```

2. Bucles `while`: Los bucles `while` permiten repetir un bloque de código mientras se cumpla una condición:

```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

3. Bucles `for`: Los bucles `for` permiten iterar sobre una secuencia (como una lista o una cadena de caracteres) y ejecutar un bloque de código para cada elemento de la secuencia:

```python
for letra in "Python":
    print(letra)
```

También se puede utilizar la función `range()` para generar una secuencia numérica y recorrerla con un bucle `for`:

```python
for i in range(5):  # Itera desde 0 hasta 4
    print(i)
```

4. Control de bucles: Python proporciona las palabras clave `break` y `continue` para modificar el comportamiento de los bucles:

- `break`: Termina el bucle y sale de él.
- `continue`: Salta a la siguiente iteración del bucle, sin ejecutar el resto del código dentro del bucle para la iteración actual.

```python
for i in range(10):
    if i == 5:
        break
    print(i)  # Imprime los números del 0 al 4
```

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # Imprime los números impares del 1 al 9
```

En el siguiente módulo, aprenderemos sobre estructuras de datos, como listas, tuplas y diccionarios.

## Estructuras de datos

### Estructuras de datos: Listas y Tuplas

1. Listas: Las listas son colecciones ordenadas y mutables de elementos en Python. Se pueden crear utilizando corchetes `[]` y separando los elementos por comas.

```python
lista = [1, 2, 3, 4]
```

2. Tuplas: Las tuplas son colecciones ordenadas e inmutables de elementos en Python. Se pueden crear utilizando paréntesis `()` y separando los elementos por comas.

```python
tupla = (1, 2, 3, 4)
```

#### Operaciones con listas y tuplas

- Listas:

```python
lista.append(5)  # Añade el elemento 5 al final de la lista
lista.extend([6, 7, 8])  # Añade los elementos 6, 7 y 8 al final de la lista
lista.pop()  # Elimina el último elemento de la lista
lista.remove(2)  # Elimina el elemento 2 de la lista
lista.insert(0, 0)  # Inserta el elemento 0 en la posición 0 de la lista
lista.sort()  # Ordena los elementos de la lista
lista.reverse()  # Invierte el orden de los elementos de la lista
```

- Tuplas:

```python
elemento_tupla = tupla[1]  # Accede al segundo elemento de la tupla
```

### Estructuras de datos: Diccionarios

1. Diccionarios: Los diccionarios son colecciones no ordenadas de pares clave-valor en Python. Se pueden crear utilizando llaves `{}` y separando las claves y los valores con dos puntos `:`.

```python
diccionario = {"clave": "valor", "nombre": "Juan", "edad": 30}
```

#### Operaciones con diccionarios

```python
valor = diccionario["clave"]  # Obtiene el valor asociado a la clave "clave"
diccionario["nueva_clave"] = "nuevo_valor"  # Añade un nuevo par clave-valor al diccionario
diccionario.update({"nombre": "Pedro", "altura": 175})  # Actualiza los valores de las claves existentes y añade nuevos pares clave-valor
del diccionario["clave"]  # Elimina el par clave-valor con la clave "clave"
diccionario_keys = diccionario.keys()  # Obtiene una vista de las claves del diccionario
diccionario_values = diccionario.values()  # Obtiene una vista de los valores del diccionario
diccionario_items = diccionario.items()  # Obtiene una vista de los pares clave-valor del diccionario
```
### Estructuras de datos: Conjuntos

1. Conjuntos: Los conjuntos son colecciones no ordenadas y sin elementos duplicados en Python. Se pueden crear utilizando llaves `{}` y separando los elementos por comas.

```python
conjunto = {1, 2, 3, 4}
```

#### Operaciones con conjuntos

```python
conjunto.add(5)  # Añade el elemento 5 al conjunto
conjunto.remove(2)  # Elimina el elemento 2 del conjunto
union = conjunto | {4, 5, 6, 7}  # Obtiene la unión de dos conjuntos
interseccion = conjunto & {4, 5, 6, 7}  # Obtiene la intersección de dos conjuntos
diferencia = conjunto - {4, 5, 6, 7}  # Obtiene la diferencia de dos conjuntos
```

### Funciones en Python

1. Definición de funciones: Las funciones son bloques de código reutilizables que realizan una tarea específica. Se pueden definir utilizando la palabra clave `def`, seguida del nombre de la función, paréntesis y dos puntos `:`.

```python
def suma(a, b):
    return a + b
```

2. Llamada a funciones: Las funciones se pueden llamar utilizando su nombre, seguido de paréntesis y los argumentos que se deseen pasar a la función.

```python
resultado = suma(3, 4)
print(resultado)
```

3. Argumentos por defecto y argumentos con nombre: Las funciones en Python pueden tener argumentos con valores por defecto, lo que permite omitir esos argumentos al llamar a la función. También se pueden pasar argumentos utilizando el nombre del argumento, lo que facilita la lectura del código.

```python
def saludo(nombre, saludo="Hola"):
    return f"{saludo}, {nombre}!"

mensaje = saludo("Juan", saludo="Buenos días")
print(mensaje)
```

Con el conocimiento de estas estructuras de datos y funciones, podrás desarrollar programas más complejos y eficientes en Python. Estos conceptos son fundamentales para la programación en Python y te permitirán crear soluciones más sólidas y escalables a medida que continúas aprendiendo.


## Resumen

En este tutorial, se presentó una introducción a Python, incluyendo sus características, instalación y entorno de desarrollo, sintaxis básica, variables y tipos de datos, operaciones con números, cadenas y booleanos, estructuras de control de flujo, y estructuras de datos como listas, tuplas, diccionarios y conjuntos.

## Conclusión

Python es un lenguaje de programación versátil y fácil de aprender, con una amplia gama de aplicaciones y una comunidad activa y en crecimiento. Dominar los conceptos básicos de Python es esencial para comprender y aplicar conceptos más avanzados en áreas como el desarrollo web, la ciencia de datos, la inteligencia artificial y la automatización, entre otras.

## Perspectivas de aprendizaje

Una vez que se haya familiarizado con los conceptos básicos de Python, es importante continuar aprendiendo y practicando para mejorar las habilidades de programación. Algunas ideas para seguir aprendiendo incluyen:

1. Estudiar librerías y módulos de Python para ampliar las capacidades del lenguaje, como NumPy, pandas, matplotlib, Django y Flask.
2. Realizar proyectos personales para aplicar y consolidar los conocimientos adquiridos.
3. Participar en la comunidad de Python a través de foros, grupos de usuarios y conferencias.
4. Leer y estudiar código de otros desarrolladores para aprender de sus enfoques y técnicas.
5. Contribuir a proyectos de código abierto para ganar experiencia y construir un portafolio.

Al seguir aprendiendo y aplicando los conocimientos de Python, se convertirá en un desarrollador más competente y estará mejor preparado para enfrentar desafíos y oportunidades en el mundo de la tecnología.


