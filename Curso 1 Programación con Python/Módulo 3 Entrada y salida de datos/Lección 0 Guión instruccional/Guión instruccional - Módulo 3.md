# Módulo 3: Entrada y salida de datos, Manejo de excepciones y Proyecto pequeño (3 horas)

## Entrada y salida de datos: input(), print(), archivos (1 hora)

### input()

La función `input()` permite obtener datos ingresados por el usuario en la consola. La función puede recibir un argumento que será el mensaje mostrado al usuario.

```python
nombre = input("Ingrese su nombre: ")
print("Hola,", nombre)
```

### print()

La función `print()` permite mostrar información en la consola. Puede recibir múltiples argumentos separados por comas, que serán concatenados automáticamente.

```python
nombre = "Juan"
edad = 30
print("Mi nombre es", nombre, "y tengo", edad, "años")
```

### Archivos

Python facilita el manejo de archivos, tanto para leer como para escribir en ellos. Se pueden utilizar los modos "r" (lectura), "w" (escritura), "a" (añadir) y "x" (creación exclusiva).

#### Lectura de archivos

```python
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
```

#### Escritura de archivos

```python
with open("nuevo_archivo.txt", "w") as archivo:
    archivo.write("Hola, mundo!")
```

## Manejo de excepciones: try, except, finally (1 hora)

El manejo de excepciones es fundamental para prevenir errores en tiempo de ejecución. Python proporciona bloques `try`, `except` y `finally` para manejar estos casos.

### try-except

```python
try:
    numero = int(input("Ingrese un número: "))
    print("El número ingresado es:", numero)
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
```

### try-except-else

```python
try:
    numero = int(input("Ingrese un número: "))
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
else:
    print("El número ingresado es:", numero)
```

### try-except-finally

```python
try:
    numero = int(input("Ingrese un número: "))
except ValueError:
    print("Ha ocurrido un error. Por favor, ingrese un número válido.")
finally:
    print("Fin del programa.")
```

## Proyecto pequeño: aplicación de los conceptos aprendidos (1 hora)

En esta sección, los estudiantes aplicarán los conceptos aprendidos en un proyecto pequeño. El objetivo es crear un programa que realice las siguientes acciones:

1. Pedir al usuario que ingrese un número entero.
2. Leer el contenido de un archivo de texto que contiene una lista de números enteros (uno por línea).
3. Calcular la suma de todos los números en el archivo y el número ingresado por el usuario.
4. Escribir el resultado en un nuevo archivo de texto.
5. Manejar las excepciones apropiadas.

**Ejemplo de solución:**

```python
def leer_numeros(archivo):
    with open(archivo, "r") as f:
        numeros = [int(line.strip()) for line in f.readlines()]
    return numeros

def escribir_suma(archivo, suma):
    with open(archivo, "w") as f:
        f.write(f"La suma es: {suma}\n")

def main():
    try:
        numero_usuario = int(input("Ingrese un número entero: "))
       