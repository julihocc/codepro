# **Generadores en Python**

Los generadores son una herramienta poderosa en Python para controlar el flujo de datos en un programa. Son una forma especial de iterador, que es cualquier objeto en Python que se puede recorrer (es decir, puedes "recorrer" todos los elementos en el objeto, uno por uno).

A diferencia de las listas o los arrays, los generadores no almacenan todos sus valores en la memoria a la vez, sino que generan cada valor en el momento. Esto los hace extremadamente eficientes en términos de memoria para trabajar con grandes conjuntos de datos.

Un generador se define como una función, pero en lugar de usar la palabra clave `return`, usa `yield`. Cuando una función que contiene `yield` es llamada, devuelve un objeto generador, pero no comienza a ejecutarse de inmediato. Aquí tienes un ejemplo de un generador muy simple:

```python
def simple_generador():
    yield 1
    yield 2
    yield 3
```

## **Uso de generadores con bucles for**

Los generadores son iterables, por lo que puedes utilizarlos en un bucle for de la misma manera que lo harías con una lista o cualquier otro iterable:

```python
mi_generador = simple_generador()

for num in mi_generador:
    print(num)
```

Este código imprimirá:

```sh
1
2
3
```

Cuando el código llama a la función `simple_generador()`, se crea un objeto generador. Este objeto generador mantiene su estado interno para que sepa qué es lo próximo que necesita generar. 

Cuando el bucle for solicita el siguiente valor del generador, el generador se "despierta", ejecuta el código hasta el siguiente `yield`, produce el valor requerido, y luego se "duerme" de nuevo, recordando dónde se quedó para la próxima vez que se le solicite un valor.

Es importante tener en cuenta que una vez que un generador ha sido completamente iterado (es decir, ha "agotado" todos sus valores), no puede ser reiniciado o reutilizado. Si intentas iterar nuevamente sobre el generador, no devolverá ningún valor:

```python
for num in mi_generador:
    print(num)  # No se imprime nada
```

Para iterar nuevamente sobre los mismos valores, tendrías que crear un nuevo objeto generador llamando nuevamente a la función `simple_generador()`.

## La función `range`

La función `range()` en Python es una función incorporada que se utiliza para generar una secuencia de números. Esta es usada frecuentemente en bucles `for` para repetir una acción un cierto número de veces.

Aquí están los tres modos de uso:

1. `range(n)`: Crea un objeto que representa una secuencia de números desde 0 hasta n-1. Por ejemplo, `range(5)` generaría la secuencia 0, 1, 2, 3, 4.

```python
for i in range(5):
    print(i)
```

Salida:

```sh
0
1
2
3
4
```

2. `range(a, b)`: Crea un objeto que representa una secuencia de números desde a hasta b-1. Por ejemplo, `range(2, 5)` generaría la secuencia 2, 3, 4.

```python
for i in range(2, 5):
    print(i)
```

Salida:

```sh
2
3
4
```

3. `range(a, b, step)`: Crea un objeto que representa una secuencia de números desde a hasta b-1, pero incrementando los números en el tamaño de `step`. Por ejemplo, `range(0, 10, 2)` generaría la secuencia 0, 2, 4, 6, 8.

```python
for i in range(0, 10, 2):
    print(i)
```

Salida:

```sh
0
2
4
6
8
```

Es importante recordar que `range()` en Python 3 no produce una lista explícita de números en memoria. En lugar de eso, crea un objeto "range" que genera los números a medida que se necesitan. Si necesitas una lista explícita de números, puedes convertir el objeto "range" en una lista usando la función `list()`.

```python
numbers = list(range(5))
print(numbers)  # Salida: [0, 1, 2, 3, 4]
```

Esto es especialmente útil si estás trabajando con un rango de números muy grande, ya que el objeto "range" consume mucha menos memoria que una lista equivalente.

### ¿Es la función range un generador? 

No, la función `range()` en Python no es un generador, aunque puede parecerlo porque no genera todos sus valores al mismo tiempo.

La función `range()` devuelve un objeto de tipo `range`, que es un tipo especial de objeto iterable. Aunque `range` produce valores a demanda al igual que un generador (lo que significa que puede generar una secuencia de números muy grande sin consumir una gran cantidad de memoria), no es un generador en el sentido técnico.

Una de las diferencias clave es que los generadores no pueden ser reutilizados una vez que se han agotado, mientras que los objetos `range` pueden ser iterados tantas veces como se desee:

```python
r = range(5)

for i in r:
    print(i)

for i in r:
    print(i)
```

Este código imprimirá los números del 0 al 4 dos veces. Si `r` fuera un generador, la segunda iteración no imprimiría nada, porque el generador ya se habría agotado.

Además, los objetos `range` admiten operaciones que los generadores no admiten, como la indexación y la determinación de su longitud con la función `len()`. Por ejemplo, puedes hacer `r[2]` para obtener el tercer elemento de `r`, o `len(r)` para obtener la longitud de `r`. Estas operaciones no serían posibles con un generador.

### Simulación de la función range

Puedes simular el comportamiento de `range()` usando un generador en Python. Aquí hay un ejemplo simple que imita a `range()` con un solo argumento (es decir, comienza en 0 y se detiene antes del número dado):

```python
def mi_range(fin):
    num = 0
    while num < fin:
        yield num
        num += 1
```

Puedes usarlo de la misma manera que usarías `range()`:

```python
for i in mi_range(5):
    print(i)
```

Esto imprimirá los números del 0 al 4, al igual que `range(5)`.

Si deseas imitar completamente la funcionalidad de `range()`, puedes agregar argumentos adicionales para permitir un inicio, un fin y un paso:

```python
def mi_range_completo(inicio, fin=None, paso=1):
    if fin is None:
        inicio, fin = 0, inicio
    num = inicio
    while num < fin:
        yield num
        num += paso
```

Ahora, puedes usar `mi_range_completo()` de la misma manera que usarías `range()` con uno, dos o tres argumentos:

```python
for i in mi_range_completo(5):
    print(i)

for i in mi_range_completo(2, 5):
    print(i)

for i in mi_range_completo(0, 10, 2):
    print(i)
```

Esto imprimirá las mismas secuencias que los equivalentes `range()`. Recuerda que este generador, a diferencia de `range()`, no puede ser reiniciado o reutilizado una vez que se ha agotado.