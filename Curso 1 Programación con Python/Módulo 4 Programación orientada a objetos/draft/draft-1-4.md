
# Programación orientada a objetos: clases, objetos, atributos, métodos

## 1. Introducción a la programación orientada a objetos (POO)

La Programación Orientada a Objetos (POO) es un paradigma de programación que utiliza objetos y sus interacciones para diseñar y desarrollar aplicaciones. Algunas ventajas de utilizar la POO incluyen la modularidad, reusabilidad de código y facilidad para realizar mantenimiento y depuración.

## 2. Clases y objetos

### Clases

Una clase es una plantilla que define la estructura y comportamiento de un objeto. Contiene atributos y métodos que serán compartidos por todos los objetos de esa clase.

**Ejemplo de definición de una clase en Python:**

```python
class Persona:
    pass
```

### Objetos

Un objeto es una instancia de una clase, que representa a una entidad individual con su propio conjunto de atributos y comportamientos.

**Ejemplo de creación de objetos en Python:**

```python
persona1 = Persona()
persona2 = Persona()
```

## 3. Atributos y métodos

### Atributos

Los atributos son variables asociadas a un objeto. Cada objeto de una clase puede tener diferentes valores para sus atributos.

**Ejemplo de atributos en Python:**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
```

### Métodos

Los métodos son funciones asociadas a un objeto que pueden acceder y modificar sus atributos.

**Ejemplo de métodos en Python:**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def presentarse(self):
        print(f"Hola, mi nombre es {self.nombre} y tengo {self.edad} años.")
```

### La función `__init__`

El método `__init__` es un método especial en las clases de Python. Se llama automáticamente cuando se crea un objeto de la clase. Usualmente, se utiliza para inicializar los atributos del objeto.

### El parámetro `self`

El parámetro `self` es una referencia al objeto que llama al método. Se utiliza para acceder a los atributos y métodos del objeto desde dentro de la clase.

## 4. Ejemplo práctico

Vamos a crear una clase `Persona` con atributos y métodos, y luego crearemos objetos de esa clase.

**Ejemplo de clase Persona:**

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def presentarse(self):
        print(f"Hola, mi nombre es {self.nombre} y tengo {self.edad} años.")
```

**Creación de objetos `Persona`:**

```python
persona1 = Persona("Ana", 28)
persona2 = Persona("Carlos", 35)

persona1.presentarse()
persona2.presentarse()
```

**Salida:**

```
Hola, mi nombre es Ana y tengo 28 años.
Hola, mi nombre es Carlos y tengo 35 años.
```
# Programación orientada a objetos: herencia y polimorfismo

## 1. Herencia

La herencia es un mecanismo que permite a una clase heredar atributos y métodos de otra clase. Facilita la reutilización de código y la creación de clases más específicas.

### Herencia simple en Python

**Ejemplo de herencia simple en Python:**

```python
class Empleado(Persona):
    pass
```

### La función `super()`

**Ejemplo de uso de `super()` en Python:**

```python
class Empleado(Persona):
    def __init__(self, nombre, edad, puesto):
        super().__init__(nombre, edad)
        self.puesto = puesto
```

### Herencia múltiple en Python

**Ejemplo de herencia múltiple en Python:**

```python
class EmpleadoAdministrativo(Persona, Administrativo):
    pass
```

## 2. Polimorfismo

El polimorfismo se refiere a la capacidad de una clase hija de sobrescribir o modificar el comportamiento de métodos de la clase padre.

**Ejemplo de polimorfismo en Python:**

```python
class Empleado(Persona):
    def __init__(self, nombre, edad, puesto):
        super().__init__(nombre, edad)
        self.puesto = puesto

    def presentarse(self):
        print(f"Hola, mi nombre es {self.nombre}, tengo {self.edad} años y trabajo como {self.puesto}.")
```

## 3. Ejemplo práctico

Vamos a crear una clase `Empleado` que herede de la clase `Persona` y utilice polimorfismo para modificar el método `presentarse()`.

**Creación de la clase `Empleado`:**

```python
class Empleado(Persona):
    def __init__(self, nombre, edad, puesto):
        super().__init__(nombre, edad)
        self.puesto = puesto

    def presentarse(self):
        print(f"Hola, mi nombre es {self.nombre}, tengo {self.edad} años y trabajo como {self.puesto}.")
```

**Creación de objetos `Empleado`:**

```python
empleado1 = Empleado("Laura", 30, "desarrolladora")
empleado2 = Empleado("Pedro", 40, "gerente")

empleado1.presentarse()
empleado2.presentarse()
```

**Salida:**

```
Hola, mi nombre es Laura, tengo 30 años y trabajo como desarrolladora.
Hola, mi nombre es Pedro, tengo 40 años y trabajo como gerente.
```

```
# Aplicación de herencia y polimorfismo en un ejemplo más completo

Vamos a utilizar la herencia y el polimorfismo para modelar una jerarquía de clases que representen diferentes tipos de vehículos.

## 1. Creación de la clase base `Vehiculo`

```python
class Vehiculo:
    def __init__(self, marca, modelo, color):
        self.marca = marca
        self.modelo = modelo
        self.color = color

    def encender(self):
        print("El vehículo está encendido.")

    def apagar(self):
        print("El vehículo está apagado.")
```

## 2. Creación de clases derivadas

### Clase `Automovil`

```python
class Automovil(Vehiculo):
    def __init__(self, marca, modelo, color, num_puertas):
        super().__init__(marca, modelo, color)
        self.num_puertas = num_puertas

    def abrir_puertas(self, num_puertas_abiertas):
        print(f"Se han abierto {num_puertas_abiertas} puertas.")
```

### Clase `Motocicleta`

```python
class Motocicleta(Vehiculo):
    def __init__(self, marca, modelo, color, tipo):
        super().__init__(marca, modelo, color)
        self.tipo = tipo

    def encender(self):
        print("La motocicleta está encendida y lista para conducir.")
```

## 3. Creación de objetos y demostración de polimorfismo

```python
auto = Automovil("Toyota", "Corolla", "Rojo", 4)
moto = Motocicleta("Honda", "CBR 600", "Azul", "Deportiva")

auto.encender()
auto.abrir_puertas(2)
auto.apagar()

moto.encender()
moto.apagar()
```

**Salida:**

```
El vehículo está encendido.
Se han abierto 2 puertas.
El vehículo está apagado.
La motocicleta está encendida y lista para conducir.
El vehículo está apagado.
```

En este ejemplo, hemos creado una clase base `Vehiculo` y dos clases derivadas, `Automovil` y `Motocicleta`. La clase `Automovil` hereda todos los métodos y atributos de la clase `Vehiculo` y agrega un atributo adicional (`num_puertas`) y un nuevo método (`abrir_puertas`). La clase `Motocicleta` hereda también todos los métodos y atributos de la clase `Vehiculo`, pero sobrescribe el método `encender()` para mostrar un mensaje específico para las motocicletas.

Este ejemplo demuestra cómo la herencia permite reutilizar y extender código de una clase base en clases derivadas, y cómo el polimorfismo permite modificar el comportamiento de un método heredado en una clase derivada.

En este caso práctico, vamos a modelar un sistema de gestión de empleados para una empresa utilizando la programación orientada a objetos en Python.

## 1. Creación de la clase base `Empleado`

```python
class Empleado:
    def __init__(self, nombre, identificacion, salario):
        self.nombre = nombre
        self.identificacion = identificacion
        self.salario = salario

    def mostrar_informacion(self):
        print(f"Empleado: {self.nombre}\nID: {self.identificacion}\nSalario: {self.salario}")
```

## 2. Creación de clases derivadas

### Clase `Gerente`

```python
class Gerente(Empleado):
    def __init__(self, nombre, identificacion, salario, departamento):
        super().__init__(nombre, identificacion, salario)
        self.departamento = departamento

    def mostrar_informacion(self):
        super().mostrar_informacion()
        print(f"Departamento: {self.departamento}")
```

### Clase `Vendedor`

```python
class Vendedor(Empleado):
    def __init__(self, nombre, identificacion, salario, ventas):
        super().__init__(nombre, identificacion, salario)
        self.ventas = ventas

    def mostrar_informacion(self):
        super().mostrar_informacion()
        print(f"Ventas: {self.ventas}")

    def calcular_comision(self, porcentaje_comision):
        comision = self.ventas * porcentaje_comision
        print(f"Comisión: {comision}")
```

## 3. Creación de objetos y demostración de polimorfismo

```python
gerente = Gerente("Laura", "G123", 5000, "Marketing")
vendedor = Vendedor("Carlos", "V456", 3000, 15000)

print("Información del gerente:")
gerente.mostrar_informacion()
print("\nInformación del vendedor:")
vendedor.mostrar_informacion()
print("\nCálculo de comisión del vendedor:")
vendedor.calcular_comision(0.10)
```

**Salida:**

```
Información del gerente:
Empleado: Laura
ID: G123
Salario: 5000
Departamento: Marketing

Información del vendedor:
Empleado: Carlos
ID: V456
Salario: 3000
Ventas: 15000

Cálculo de comisión del vendedor:
Comisión: 1500.0
```

En este ejemplo, hemos creado una clase base `Empleado` y dos clases derivadas, `Gerente` y `Vendedor`. La clase `Gerente` hereda todos los métodos y atributos de la clase `Empleado` y agrega un atributo adicional (`departamento`). La clase `Vendedor` hereda también todos los métodos y atributos de la clase `Empleado`, pero agrega un atributo adicional (`ventas`) y un nuevo método (`calcular_comision`).

Este ejemplo demuestra cómo la programación orientada a objetos en Python puede ser utilizada para modelar un sistema de gestión de empleados en un negocio. La herencia y el polimorfismo permiten reutilizar y extender código de una clase base en clases derivadas, lo que facilita la creación de un sistema modular y fácil de mantener.