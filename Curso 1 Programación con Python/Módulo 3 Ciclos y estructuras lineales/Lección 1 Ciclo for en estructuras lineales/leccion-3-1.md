# Estructuras Lineales de Datos y Ciclos `for` en Python

Las estructuras de datos lineales son aquellas en las que los elementos están organizados de manera secuencial. Python proporciona varias estructuras de datos lineales, incluyendo listas, tuplas, y strings. Los diccionarios y los conjuntos también pueden ser recorridos secuencialmente a pesar de ser estructuras no lineales.

## Listas y Ciclos `for`

Las listas en Python son una estructura que contienen elementos ordenados. Podemos recorrer los elementos de una lista usando un ciclo `for`:

```python
lista = [1, 2, 3, 4, 5]
for elemento in lista:
    print(elemento)  # Imprime cada elemento de la lista
```

## Tuplas y Ciclos `for`

Las tuplas son similares a las listas, pero son inmutables. Al igual que las listas, podemos recorrer las tuplas usando un ciclo `for`:

```python
tupla = (1, 2, 3, 4, 5)
for elemento in tupla:
    print(elemento)  # Imprime cada elemento de la tupla
```

## Strings y Ciclos `for`

Los strings en Python son secuencias de caracteres y pueden ser recorridos usando un ciclo `for`:

```python
string = "Hola"
for caracter in string:
    print(caracter)  # Imprime cada caracter del string
```

## Diccionarios y Ciclos `for`

Los diccionarios en Python son una colección de pares clave-valor. Podemos recorrer las claves, los valores o ambos usando un ciclo `for`:

```python
diccionario = {"a": 1, "b": 2, "c": 3}
for clave in diccionario:
    print(clave)  # Imprime cada clave del diccionario

for valor in diccionario.values():
    print(valor)  # Imprime cada valor del diccionario

for clave, valor in diccionario.items():
    print(clave, valor)  # Imprime cada par clave-valor del diccionario
```

## Conjuntos y Ciclos `for`

Los conjuntos en Python son una colección de elementos únicos. Aunque no son lineales ni mantienen un orden, podemos recorrerlos usando un ciclo `for`:

```python
conjunto = {1, 2, 3, 4, 5}
for elemento in conjunto:
    print(elemento)  # Imprime cada elemento del conjunto
```

---

Los ciclos `for` son una herramienta esencial para trabajar con estructuras de datos en Python, ya que nos permiten recorrer los elementos de estas estructuras de manera eficiente y legible.