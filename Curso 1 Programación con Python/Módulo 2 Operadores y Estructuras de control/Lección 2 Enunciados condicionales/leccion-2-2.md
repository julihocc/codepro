# Enunciados Condicionales en Python

En Python, los enunciados condicionales se usan para tomar decisiones basadas en ciertas condiciones. Los enunciados condicionales en Python incluyen: `if`, `elif`, y `else`.

## Enunciado `if`

El enunciado `if` se usa para ejecutar un bloque de código si una condición especificada es verdadera.

```python
x = 5
if x > 0:
    print("x es positivo")
```

En este ejemplo, Python imprimirá "x es positivo" porque 5 es mayor que 0.

## Enunciado `else`

El enunciado `else` captura cualquier condición que no haya sido capturada por los enunciados `if` y `elif` anteriores. Se usa para manejar el caso en el que todas las condiciones anteriores son falsas.

```python
x = -5
if x > 0:
    print("x es positivo")
else:
    print("x no es positivo")
```

En este ejemplo, Python imprimirá "x no es positivo" porque -5 no es mayor que 0.

## Enunciado `elif`

El enunciado `elif` es una forma de decir "si las condiciones anteriores no eran verdaderas, entonces prueba esta condición". Se puede usar para manejar múltiples condiciones.

```python
x = 0
if x > 0:
    print("x es positivo")
elif x == 0:
    print("x es cero")
else:
    print("x es negativo")
```

En este ejemplo, Python imprimirá "x es cero" porque x es igual a 0.

Recuerda que los enunciados condicionales pueden ser tan simples o tan complejos como sea necesario para tu programa, y pueden incluir operadores lógicos (`and`, `or`, `not`) para combinar o invertir condiciones.