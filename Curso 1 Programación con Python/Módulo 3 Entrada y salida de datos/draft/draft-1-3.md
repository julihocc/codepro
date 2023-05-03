# Entrada y salida de datos: input(), print(), archivos (1 hora)

## input()

La función `input()` permite obtener datos ingresados por el usuario en la consola. La función puede recibir un argumento que será el mensaje mostrado al usuario.

```python
nombre = input("Ingrese su nombre: ")
print("Hola,", nombre)
```

**Ejemplo:**

```python
numero = int(input("Ingrese un número entero: "))
print("El número ingresado es", numero)
```

## print()

La función `print()` permite mostrar información en la consola. Puede recibir múltiples argumentos separados por comas, que serán concatenados automáticamente.

```python
nombre = "Juan"
edad = 30
print("Mi nombre es", nombre, "y tengo", edad, "años")
```

**Ejemplo:**

```python
x = 5
y = 3
suma = x + y
print(x, "+", y, "=", suma)
```

## Archivos

Python facilita el manejo de archivos, tanto para leer como para escribir en ellos. Se pueden utilizar los modos "r" (lectura), "w" (escritura), "a" (añadir) y "x" (creación exclusiva).

### Lectura de archivos

```python
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
```

**Ejemplo:**

```python
with open("numeros.txt", "r") as archivo:
    numeros = [int(line.strip()) for line in archivo.readlines()]
    print("Números:", numeros)
```

### Escritura de archivos

```python
with open("nuevo_archivo.txt", "w") as archivo:
    archivo.write("Hola, mundo!")
```

**Ejemplo:**

```python
nombres = ["Ana", "Carlos", "Beatriz"]
with open("nombres.txt", "w") as archivo:
    for nombre in nombres:
        archivo.write(nombre + "\n")
```

### Añadir contenido a un archivo

```python
with open("archivo_existente.txt", "a") as archivo:
    archivo.write("Esta línea se añadirá al final del archivo.\n")
```

**Ejemplo:**

```python
nuevos_nombres = ["David", "Elena"]
with open("nombres.txt", "a") as archivo:
    for nombre in nuevos_nombres:
        archivo.write(nombre + "\n")
```

### Lectura de archivos línea por línea

En algunos casos, es útil leer un archivo línea por línea en lugar de cargar todo el contenido en memoria. Esto se puede hacer con un bucle `for`:

```python
with open("archivo.txt", "r") as archivo:
    for line in archivo:
        print(line.strip())
```

**Ejemplo:**

```python
with open("palabras.txt", "r") as archivo:
    for linea in archivo:
        palabra = linea.strip()
        print("Palabra:", palabra)
```

### Operaciones con archivos en modo binario

Para leer o escribir archivos en modo binario, se debe agregar la letra "b" al modo de apertura del archivo. Esto es útil cuando se trabaja con archivos que no son de texto, como imágenes o archivos comprimidos.

**Lectura en modo binario:**

```python
with open("imagen.jpg", "rb") as archivo:
    contenido = archivo.read()
    print("Contenido en bytes:", contenido)
```

**Escritura en modo binario:**

```python
datos_binarios = b'\x48\x6f\x6c\x61\x20\x6d\x75\x6e\x64\x6f\x21'
with open("archivo_binario.bin", "wb") as archivo:
    archivo.write(datos_binarios)
```

## Formateo de cadenas de texto

Python proporciona diferentes maneras de formatear cadenas de texto para facilitar su lectura y presentación.

### Método `format()`

El método `format()` permite reemplazar marcadores de posición en una cadena de texto con valores específicos:

```python
nombre = "Juan"
edad = 30
frase = "Mi nombre es {} y tengo {} años".format(nombre, edad)
print(frase)
```

### F-strings

Las F-strings (cadenas con formato) son una característica de Python 3.6 en adelante que permite incluir expresiones dentro de las cadenas de texto, utilizando llaves y un prefijo "f":

```python
nombre = "Juan"
edad = 30
frase = f"Mi nombre es {nombre} y tengo {edad} años"
print(frase)
```

**Ejemplo:**

```python
x = 5
y = 3
suma = x + y
print(f"{x} + {y} = {suma}")
```
### Uso de archivos temporales

En algunos casos, es útil trabajar con archivos temporales que se eliminan automáticamente una vez que se cierra el archivo. Python proporciona el módulo `tempfile` para manejar este tipo de archivos.

```python
import tempfile

with tempfile.TemporaryFile(mode="w+t") as archivo_temporal:
    archivo_temporal.write("Esta es una línea en un archivo temporal.")
    archivo_temporal.seek(0)
    contenido = archivo_temporal.read()
    print("Contenido del archivo temporal:", contenido)
```

### Conversión de tipos de datos en entrada y salida

A menudo, es necesario convertir tipos de datos al leer o escribir información. Por ejemplo, al leer números de un archivo de texto, estos se encuentran en formato de cadena de caracteres. Es necesario convertirlos a números antes de realizar operaciones matemáticas.

**Ejemplo:**

```python
with open("precios.txt", "r") as archivo:
    precios = [float(line.strip()) for line in archivo.readlines()]

total = sum(precios)
print(f"El total de los precios es: {total}")
```

### Funciones de entrada y salida personalizadas

Para facilitar la reutilización de código y mejorar la legibilidad de los programas, es posible crear funciones personalizadas para operaciones de entrada y salida de datos.

**Ejemplo:**

```python
def leer_numeros(archivo):
    with open(archivo, "r") as f:
        numeros = [int(line.strip()) for line in f.readlines()]
    return numeros

def guardar_numeros(archivo, numeros):
    with open(archivo, "w") as f:
        for numero in numeros:
            f.write(f"{numero}\n")

numeros = leer_numeros("numeros.txt")
numeros_ordenados = sorted(numeros)
guardar_numeros("numeros_ordenados.txt", numeros_ordenados)
```

Con estas notas y ejemplos, los estudiantes podrán comprender y practicar el manejo de entrada y salida de datos en Python, incluyendo el uso de funciones `input()` y `print()`, operaciones con archivos de texto y binarios, manejo de excepciones y formateo de cadenas de texto. Estas habilidades son fundamentales para desarrollar aplicaciones de Python más avanzadas y para trabajar con datos de manera efectiva.

# Manejo de excepciones: try, except, finally (1 hora)

El manejo de excepciones es fundamental para prevenir errores en tiempo de ejecución y mantener la estabilidad de un programa. Python proporciona bloques `try`, `except`, y `finally` para manejar estos casos.

## try-except

El bloque `try-except` permite capturar y manejar excepciones que puedan ocurrir durante la ejecución de un programa.

```python
try:
    numero = int(input("Ingrese un número: "))
    print("El número ingresado es:", numero)
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
```

## try-except-else

El bloque `try-except-else` permite ejecutar un fragmento de código si no se produce ninguna excepción dentro del bloque `try`.

```python
try:
    numero = int(input("Ingrese un número: "))
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
else:
    print("El número ingresado es:", numero)
```

## try-except-finally

El bloque `try-except-finally` permite ejecutar un fragmento de código sin importar si se produce o no una excepción dentro del bloque `try`.

```python
try:
    numero = int(input("Ingrese un número: "))
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
finally:
    print("Fin del programa.")
```

## Capturando múltiples excepciones

Es posible capturar y manejar diferentes tipos de excepciones utilizando varios bloques `except`.

```python
try:
    numerador = int(input("Ingrese el numerador: "))
    denominador = int(input("Ingrese el denominador: "))
    resultado = numerador / denominador
    print("El resultado es:", resultado)
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
except ZeroDivisionError:
    print("No se puede dividir por cero.")
```

## Capturando excepciones y accediendo a la información de error

Al capturar una excepción, es posible acceder a información adicional sobre el error utilizando la palabra clave `as`.

```python
try:
    numero = int(input("Ingrese un número: "))
    resultado = 100 / numero
    print("El resultado es:", resultado)
except (ValueError, ZeroDivisionError) as e:
    print(f"Ha ocurrido un error: {e}")
```

## Levantando excepciones

En ocasiones, es necesario generar excepciones de manera manual utilizando la palabra clave `raise`.

```python
def validar_edad(edad):
    if edad < 0:
        raise ValueError("La edad no puede ser negativa.")

try:
    edad = int(input("Ingrese su edad: "))
    validar_edad(edad)
except ValueError as e:
    print(f"Error: {e}")
```

Con estas notas y ejemplos, los estudiantes podrán comprender y aplicar el manejo de excepciones en Python, incluyendo el uso de bloques `try`, `except`, `else` y `finally`, la captura de múltiples excepciones y la generación manual de excepciones. Estas habilidades son esenciales para desarrollar programas robustos y resistentes a errores en tiempo de ejecución.

# Proyecto pequeño: aplicación de los conceptos aprendidos (1 hora)

El objetivo de este proyecto es crear un programa que realice las acciones especificadas, aplicando los conceptos de entrada y salida de datos y manejo de excepciones.

## Solución

```python
def pedir_numero_entero():
    try:
        numero = int(input("Ingrese un número entero: "))
        return numero
    except ValueError:
        print("Error: Por favor, ingrese un número entero válido.")
        return None

def leer_numeros_de_archivo(nombre_archivo):
    try:
        with open(nombre_archivo, "r") as archivo:
            numeros = [int(line.strip()) for line in archivo.readlines()]
        return numeros
    except FileNotFoundError:
        print(f"Error: No se pudo encontrar el archivo {nombre_archivo}.")
        return None
    except ValueError:
        print("Error: El archivo contiene datos no válidos.")
        return None

def calcular_suma(numeros, numero):
    return sum(numeros) + numero

def escribir_resultado_en_archivo(nombre_archivo, resultado):
    try:
        with open(nombre_archivo, "w") as archivo:
            archivo.write(f"La suma total es: {resultado}\n")
    except IOError:
        print(f"Error: No se pudo escribir en el archivo {nombre_archivo}.")

def main():
    numero = pedir_numero_entero()
    if numero is None:
        return

    numeros = leer_numeros_de_archivo("numeros.txt")
    if numeros is None:
        return

    suma_total = calcular_suma(numeros, numero)
    print(f"La suma total es: {suma_total}")

    escribir_resultado_en_archivo("resultado.txt", suma_total)

if __name__ == "__main__":
    main()
```

En esta solución, hemos dividido el problema en varias funciones para facilitar la comprensión y el mantenimiento del código. La función `pedir_numero_entero` se encarga de solicitar un número entero al usuario y manejar la excepción `ValueError`. La función `leer_numeros_de_archivo` lee los números de un archivo de texto y maneja las excepciones `FileNotFoundError` y `ValueError`. La función `calcular_suma` calcula la suma de todos los números y la función `escribir_resultado_en_archivo` escribe el resultado en un nuevo archivo de texto, manejando la excepción `IOError`. Finalmente, la función `main` se encarga de coordinar todas las operaciones y ejecutar el programa.

Con esta solución, los estudiantes pueden aplicar y reforzar los conceptos aprendidos en las lecciones anteriores, incluyendo la entrada y salida de datos, el manejo de archivos y el manejo de excepciones en Python.