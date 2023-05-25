# Guion Instruccional del Módulo 1: Introducción a Python y Variables

Duración Total: 3 horas

## I. Introducción a Python: conceptos básicos y sintaxis (1 hora)
   ### A. ¿Qué es Python?
      1. Definición de Python
      2. Historia de Python
   ### B. Características de Python
      1. Interpretado
      2. Tipado dinámico
      3. Multiplataforma
      4. Sintaxis clara y sencilla
   ### C. Entorno de desarrollo
      1. Instalación de Python
      2. Interprete de Python
      3. Editores de código
   ### D. Primeros pasos en Python
      1. Hello World!
      2. Variables y asignación
      3. Comentarios
      4. Operadores básicos
      5. Entrada y salida de datos

## II. Variables y tipos de datos: tipos numéricos, cadenas, booleanos (2 horas)
   ### A. Variables y tipos de datos
      1. Variables y asignación
      2. Tipos de datos en Python
      3. Conversión de tipos
   ### B. Tipos numéricos
      1. Enteros
      2. Flotantes
      3. Operaciones numéricas
   ### C. Cadenas
      1. Creación de cadenas
      2. Operaciones con cadenas
      3. Métodos de cadenas
   ### D. Booleanos
      1. Definición de booleanos
      2. Operaciones lógicas
      3. Condiciones y estructuras de control de flujo

## Recursos adicionales:
- Documentación oficial de Python
- Tutoriales en línea
- Ejercicios prácticos
- Plataformas en línea de aprendizaje de programación.

# Introducción a Python: conceptos básicos y sintaxis (1 hora)

## ¿Qué es Python?

1. Definición de Python: Python es un lenguaje de programación de alto nivel, interpretado, dinámicamente tipado y multiplataforma, que se caracteriza por tener una sintaxis clara y sencilla.

2. Historia de Python: Python fue creado por Guido van Rossum a finales de los años 80. El nombre de Python proviene de la afición de Guido por el grupo de comedia británico Monty Python.

## Características de Python

1. Interpretado: Python es un lenguaje interpretado, lo que significa que el código fuente es ejecutado directamente por un intérprete, sin necesidad de ser compilado previamente.

2. Tipado dinámico: En Python, no es necesario definir el tipo de una variable antes de asignarle un valor. El tipo de una variable es determinado dinámicamente durante la ejecución del programa.

3. Multiplataforma: Python puede ser utilizado en diferentes sistemas operativos, como Windows, Linux o Mac OS X.

4. Sintaxis clara y sencilla: La sintaxis de Python es sencilla y fácil de leer, lo que hace que el código sea más legible y fácil de mantener.

## Entorno de desarrollo

1. Instalación de Python: Para utilizar Python es necesario instalarlo en el equipo. Existen diferentes versiones de Python, por lo que es importante elegir la versión adecuada para el proyecto en el que se va a trabajar.

2. Intérprete de Python: El intérprete de Python es el programa que se encarga de ejecutar el código fuente escrito en Python. Existen diferentes intérpretes de Python, como CPython, Jython o IronPython.

3. Editores de código: Existen diferentes editores de código que pueden ser utilizados para escribir código en Python, como Visual Studio Code, PyCharm o Sublime Text.

## Primeros pasos en Python

1. Hello World!: El programa Hello World! es el primer programa que se escribe en cualquier lenguaje de programación. En Python, el programa Hello World! se escribe de la siguiente manera:

```python
print("Hello World!")
```

2. Variables y asignación: En Python, una variable es un espacio de memoria reservado para almacenar un valor. Para asignar un valor a una variable se utiliza el operador "=", como en el siguiente ejemplo:

```python
x = 5
```

3. Comentarios: Los comentarios son texto que se añade al código para hacerlo más legible para los humanos. En Python, los comentarios se escriben utilizando el símbolo "#" al inicio de la línea.

```python
# Esto es un comentario
```

4. Operadores básicos: Python cuenta con diferentes operadores que permiten realizar operaciones aritméticas y lógicas. Algunos de los operadores más comunes son:

- Suma: "+"
- Resta: "-"
- Multiplicación: "*"
- División: "/"
- Módulo: "%"
- Igualdad: "=="
- Mayor que: ">"
- Menor que: "<"

5. Entrada y salida de datos (continuación):
- `print()`: Para mostrar información en la pantalla. Por ejemplo:

```python
print("Hola, ¿cómo estás?")
```

- `input()`: Para leer información desde el teclado. Por ejemplo:

```python
nombre = input("Por favor, introduce tu nombre: ")
print("Hola " + nombre + ", bienvenido a Python!")
```

En este ejemplo, la función `input()` se utiliza para leer el nombre del usuario desde el teclado, y la función `print()` se utiliza para mostrar un mensaje de bienvenida en la pantalla, que incluye el nombre del usuario.

Es importante destacar que la función `input()` devuelve siempre una cadena de caracteres (string), por lo que si se quiere utilizar el valor introducido por el usuario como un número, es necesario convertirlo previamente a un tipo numérico, utilizando una de las funciones de conversión disponibles en Python, como `int()` o `float()`.

## Conclusión

En resumen, en esta clase hemos aprendido los conceptos básicos de Python, como su definición, historia y características principales. También hemos visto cómo instalar Python en nuestro equipo, y cómo utilizar diferentes editores de código para escribir programas en Python. Finalmente, hemos realizado nuestros primeros pasos en Python, escribiendo el programa Hello World!, trabajando con variables, comentarios, operadores y funciones de entrada y salida de datos. Con esta base, estamos listos para seguir aprendiendo y explorando las posibilidades que ofrece Python como lenguaje de programación.

## II. Variables y tipos de datos: tipos numéricos, cadenas, booleanos (2 horas)

### A. Variables y tipos de datos
1. Variables y asignación
   * Ejemplo:
   ```python
   x = 5
   nombre = "Juan"
   _edad = 30
   ```

2. Tipos de datos en Python
   * Ejemplo:
   ```python
   entero = 42
   flotante = 3.14
   cadena = "Hola, mundo!"
   booleano = True
   ```

3. Conversión de tipos
   * Ejemplo:
   ```python
   entero_a_float = float(42)
   float_a_str = str(3.14)
   str_a_bool = bool("True")
   ```

### B. Tipos numéricos
1. Enteros
   * Ejemplo:
   ```python
   decimal = 42
   binario = 0b101010
   octal = 0o52
   hexadecimal = 0x2A
   ```

2. Flotantes
   * Ejemplo:
   ```python
   flotante_decimal = 3.14
   flotante_exponencial = 3.14e-2
   ```

3. Operaciones numéricas
   * Ejemplo:
   ```python
   suma = 5 + 3
   resta = 7 - 2
   multiplicacion = 4 * 6
   division = 10 / 3
   exponente = 2 ** 3
   modulo = 9 % 2
   ```

### C. Cadenas
1. Creación de cadenas
   * Ejemplo:
   ```python
   cadena_simple = 'Hola, mundo!'
   cadena_doble = "Hola, mundo!"
   ```

2. Operaciones con cadenas
   * Ejemplo:
   ```python
   concatenacion = "Hola, " + "mundo!"
   repeticion = "Hola! " * 3
   primer_caracter = "Python"[0]
   ```

3. Métodos de cadenas
   * Ejemplo:
   ```python
   minusculas = "HOLA, MUNDO!".lower()
   mayusculas = "hola, mundo!".upper()
   sin_espacios = " Hola, mundo! ".strip()
   lista_de_palabras = "Hola, mundo!".split()
   cadena_unida = ", ".join(["Hola", "mundo"])
   ```

### D. Booleanos
1. Definición de booleanos
   * Ejemplo:
   ```python
   verdadero = True
   falso = False
   resultado = 3 > 1
   ```

2. Operaciones lógicas
   * Ejemplo:
   ```python
   and_result = True and False
   or_result = True or False
   not_result = not True
   ```

3. Condiciones y estructuras de control de flujo
   * Ejemplo:
   ```python
   if 5 > 3:
       print("5 es mayor que 3")
   elif 3 > 5:
       print("3 es mayor que 5")
   else:
       print("5 y 3 son iguales")

   for i in range(3):
       print(i)

   contador = 0
   while contador < 3:
       print(contador)
       contador += 1
   ```

Siguiendo con las notas para la clase, abordaremos más temas relacionados con estructuras de datos y funciones en Python:

### E. Listas y tuplas
1. Creación de listas y tuplas
   * Ejemplo:
   ```python
   lista = [1, 2, 3, 4]
   tupla = (1, 2, 3, 4)
   ```

2. Operaciones con listas y tuplas
   * Ejemplo:
   ```python
   lista.append(5)
   lista.extend([6, 7, 8])
   lista.pop()
   lista.remove(2)
   lista.insert(0, 0)
   lista.sort()
   lista.reverse()
   elemento_tupla = tupla[1]
   ```

### F. Diccionarios
1. Creación de diccionarios
   * Ejemplo:
   ```python
   diccionario = {"clave": "valor", "nombre": "Juan", "edad": 30}
   ```

2. Operaciones con diccionarios
   * Ejemplo:
   ```python
   valor = diccionario["clave"]
   diccionario["nueva_clave"] = "nuevo_valor"
   diccionario.update({"nombre": "Pedro", "altura": 175})
   del diccionario["clave"]
   diccionario_keys = diccionario.keys()
   diccionario_values = diccionario.values()
   diccionario_items = diccionario.items()
   ```

### G. Conjuntos
1. Creación de conjuntos
   * Ejemplo:
   ```python
   conjunto = {1, 2, 3, 4}
   ```

2. Operaciones con conjuntos
   * Ejemplo:
   ```python
   conjunto.add(5)
   conjunto.remove(2)
   union = conjunto | {4, 5, 6, 7}
   interseccion = conjunto & {4, 5, 6, 7}
   diferencia = conjunto - {4, 5, 6, 7}
   ```

### H. Funciones
1. Definición de funciones
   * Ejemplo:
   ```python
   def suma(a, b):
       return a + b
   ```

2. Llamada a funciones
   * Ejemplo:
   ```python
   resultado = suma(3, 4)
   print(resultado)
   ```

3. Argumentos por defecto y argumentos con nombre
   * Ejemplo:
   ```python
   def saludo(nombre, saludo="Hola"):
       return f"{saludo}, {nombre}!"

   mensaje = saludo("Juan", saludo="Buenos días")
   print(mensaje)
   ```

Estas notas adicionales cubren temas como listas, tuplas, diccionarios, conjuntos y funciones en Python. Estas estructuras de datos y funciones son fundamentales para desarrollar programas más complejos y eficientes. Además, se incluyen ejemplos de código para ilustrar cómo crear, manipular y utilizar estos elementos en Python.