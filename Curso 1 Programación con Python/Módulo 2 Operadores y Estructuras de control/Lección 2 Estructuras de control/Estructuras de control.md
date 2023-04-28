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