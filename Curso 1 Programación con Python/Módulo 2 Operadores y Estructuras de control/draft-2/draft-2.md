# Operadores y expresiones en Python (1 hora)

## Objetivos:
1. Entender los diferentes tipos de operadores en Python: aritméticos, de comparación y lógicos.
2. Aprender a utilizar estos operadores en expresiones.
3. Practicar la creación de ejemplos de código que utilicen estos operadores.

## Contenido

### I. Introducción (5 minutos)
- Explicar la importancia de los operadores y expresiones en la programación.
- Presentar los tres tipos de operadores que se estudiarán en la clase.

### II. Operadores aritméticos (20 minutos)
- Suma (+)
- Resta (-)
- Multiplicación (*)
- División (/)
- Módulo (%)
- Exponenciación (**)
- División entera (//)

**Ejemplo de código:**
```python
a = 7
b = 3

suma = a + b
resta = a - b
multiplicacion = a * b
division = a / b
modulo = a % b
exponenciacion = a ** b
division_entera = a // b

print("Suma:", suma)
print("Resta:", resta)
print("Multiplicación:", multiplicacion)
print("División:", division)
print("Módulo:", modulo)
print("Exponenciación:", exponenciacion)
print("División entera:", division_entera)
```

### III. Operadores de comparación (15 minutos)
- Igual (==)
- Diferente (!=)
- Mayor que (>)
- Menor que (<)
- Mayor o igual que (>=)
- Menor o igual que (<=)

**Ejemplo de código:**
```python
x = 5
y = 8

igual = x == y
diferente = x != y
mayor_que = x > y
menor_que = x < y
mayor_o_igual = x >= y
menor_o_igual = x <= y

print("Igual:", igual)
print("Diferente:", diferente)
print("Mayor que:", mayor_que)
print("Menor que:", menor_que)
print("Mayor o igual que:", mayor_o_igual)
print("Menor o igual que:", menor_o_igual)
```

### IV. Operadores lógicos (20 minutos)
- AND (and)
- OR (or)
- NOT (not)

**Ejemplo de código:**
```python
verdadero = True
falso = False

conjuncion = verdadero and falso
disyuncion = verdadero or falso
negacion = not verdadero

print("AND:", conjuncion)
print("OR:", disyuncion)
print("NOT:", negacion)
```

### V. Conclusión (5 minutos)
- Resumir los conceptos aprendidos en la clase.
- Recordar la importancia de practicar con ejercicios y proyectos para mejorar el dominio de los operadores y expresiones en Python.

### VI. Ejercicios adicionales (opcional)
- Crear ejercicios prácticos que utilicen operadores aritméticos, de comparación y lógicos para resolver problemas y situaciones reales.

# Lección: Estructuras de control en Python (1 hora)

## Objetivos:
1. Comprender la importancia de las estructuras de control en la programación.
2. Aprender a utilizar las estructuras de control `if`, `while` y `for` en Python.
3. Practicar la creación de ejemplos de código que utilicen estas estructuras de control.

## Contenido

### I. Introducción (5 minutos)
- Explicar la importancia de las estructuras de control en la programación.
- Presentar las tres estructuras de control que se estudiarán en la lección: `if`, `while` y `for`.

### II. La estructura `if` y su uso en la programación (20 minutos)
- Introducción a la estructura `if`
- Uso de `elif` y `else`

**Ejemplo de código:**
```python
edad = 18

if edad < 18:
    print("Menor de edad")
elif edad >= 18 and edad < 65:
    print("Adulto")
else:
    print("Adulto mayor")
```

### III. Uso de la estructura `while` (20 minutos)
- Introducción a la estructura `while`
- Ejemplos de bucles con `while`

**Ejemplo de código:**
```python
contador = 0

while contador < 5:
    print("Contador:", contador)
    contador += 1
```

### IV. La estructura `for` y su aplicación en bucles (20 minutos)
- Introducción a la estructura `for`
- Uso de la función `range`
- Iteración sobre listas y otros objetos iterables

**Ejemplo de código:**
```python
for i in range(5):
    print("Número:", i)

nombres = ["Ana", "Luis", "Carlos", "Sofía"]
for nombre in nombres:
    print("Nombre:", nombre)
```

### V. Conclusión (5 minutos)
- Resumir los conceptos aprendidos en la lección.
- Recordar la importancia de practicar con ejercicios y proyectos para mejorar el dominio de las estructuras de control en Python.

### VI. Ejercicios adicionales (opcional)
- Crear ejercicios prácticos que utilicen las estructuras de control `if`, `while` y `for` para resolver problemas y situaciones reales.

# Lección: Funciones y módulos en Python (1 hora)

## Objetivos:
1. Comprender la importancia de las funciones y módulos en la programación.
2. Aprender a definir y utilizar funciones en Python, así como el uso de parámetros y valores de retorno.
3. Practicar la creación de ejemplos de código que utilicen funciones y módulos en Python.

## Contenido

### I. Introducción (5 minutos)
- Explicar la importancia de las funciones y módulos en la programación.
- Presentar los conceptos clave que se estudiarán en la lección: funciones, parámetros y valores de retorno.

### II. Definición y uso de funciones en Python (20 minutos)
- Introducción a las funciones en Python
- Definición y llamada de funciones
- Uso de la palabra clave `def`

**Ejemplo de código:**
```python
def saludo(nombre):
    print("¡Hola, " + nombre + "!")

saludo("Pedro")
```

### III. Comprender la importancia de los parámetros en una función (20 minutos)
- Introducción a los parámetros en funciones
- Parámetros posicionales y parámetros con nombre
- Parámetros opcionales con valores predeterminados
- Número variable de parámetros (`*args` y `**kwargs`)

**Ejemplo de código:**
```python
def suma(a, b=0, *args, **kwargs):
    total = a + b + sum(args) + sum(kwargs.values())
    return total

resultado = suma(5, 6, 1, 2, 3, x=10, y=20)
print("La suma es:", resultado)
```

### IV. El retorno en Python y su uso en funciones y módulos (20 minutos)
- Introducción al retorno en funciones
- Uso de la palabra clave `return`
- Retorno de múltiples valores con tuplas
- Retorno de funciones como valores

**Ejemplo de código:**
```python
def calculadora(a, b):
    suma = a + b
    resta = a - b
    multiplicacion = a * b
    division = a / b
    return suma, resta, multiplicacion, division

resultados = calculadora(10, 5)
print("Suma, resta, multiplicación y división:", resultados)
```

### V. Conclusión (5 minutos)
- Resumir los conceptos aprendidos en la lección.
- Recordar la importancia de practicar con ejercicios y proyectos para mejorar el dominio de las funciones y módulos en Python.

### VI. Ejercicios adicionales (opcional)
- Crear ejercicios prácticos que utilicen funciones y módulos en Python para resolver problemas y situaciones reales.