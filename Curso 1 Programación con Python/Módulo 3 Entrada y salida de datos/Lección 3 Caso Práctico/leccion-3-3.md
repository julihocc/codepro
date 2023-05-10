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