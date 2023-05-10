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