# Rúbrica de Evaluación del Curso de Programación con Python

## Caso Práctico: Sistema de Gestión de Biblioteca

A continuación, se presenta la rúbrica para evaluar el caso práctico del curso de programación con Python. El caso práctico consiste en desarrollar un sistema de gestión de biblioteca que permita a los usuarios buscar libros, realizar préstamos y devoluciones, y a los bibliotecarios agregar nuevos libros y gestionar préstamos.

### 1. Diseño y estructura del código (20%)

- **(0-5%)** El código está mal organizado, no sigue ninguna estructura lógica y es difícil de entender.
- **(6-10%)** El código sigue una estructura básica pero tiene margen de mejora en términos de organización y legibilidad.
- **(11-15%)** El código está bien organizado y sigue una estructura lógica, pero puede mejorarse en ciertos aspectos.
- **(16-20%)** El código está muy bien organizado, sigue una estructura lógica y es fácil de entender.

### 2. Funcionalidad y cumplimiento de requisitos (40%)

- **(0-10%)** El sistema no cumple con los requisitos básicos y presenta errores que impiden su correcto funcionamiento.
- **(11-20%)** El sistema cumple con algunos requisitos, pero presenta errores o falta de funcionalidades clave.
- **(21-30%)** El sistema cumple con la mayoría de los requisitos, pero presenta algunos errores o falta de funcionalidades menores.
- **(31-40%)** El sistema cumple con todos los requisitos y funciona correctamente.

### 3. Uso adecuado de conceptos aprendidos en el curso (30%)

- **(0-7%)** El código no utiliza los conceptos aprendidos en el curso o los utiliza de manera incorrecta.
- **(8-15%)** El código utiliza algunos conceptos aprendidos en el curso, pero no de manera óptima o eficiente.
- **(16-22%)** El código utiliza la mayoría de los conceptos aprendidos en el curso de manera adecuada y eficiente.
- **(23-30%)** El código demuestra un excelente uso de todos los conceptos aprendidos en el curso y emplea técnicas avanzadas.

### 4. Documentación y estilo del código (10%)

- **(0-2%)** El código no tiene comentarios ni documentación, y no sigue ninguna guía de estilo.
- **(3-5%)** El código tiene algunos comentarios y documentación, pero no es suficiente o no sigue una guía de estilo.
- **(6-8%)** El código está bien documentado y tiene comentarios claros, pero puede mejorarse en términos de estilo y coherencia.
- **(9-10%)** El código está excelentemente documentado, con comentarios claros y concisos, y sigue una guía de estilo coherente.

### Notas:

- Los porcentajes en cada categoría indican el rango de puntuación dentro de esa categoría.
- Para obtener una calificación final, se sumarán las puntuaciones de todas las categorías.
- La calificación máxima posible es 100%.

## Casos de prueba

A continuación, se presentan algunos casos de prueba para el proyecto del Sistema de Gestión de Biblioteca:

**Caso de prueba 1: Agregar un nuevo libro**

Entrada:
- Título: "Orgullo y Prejuicio"
- Autor: "Jane Austen"
- Año de publicación: 1813
- Cantidad de copias: 3

Salida esperada:
- Mensaje: "El libro 'Orgullo y Prejuicio' ha sido agregado exitosamente."
- El libro debe aparecer en la lista de libros disponibles.

**Caso de prueba 2: Buscar un libro existente**

Entrada:
- Título: "Orgullo y Prejuicio"

Salida esperada:
- Información del libro: Autor, Año de publicación, Cantidad de copias disponibles.

**Caso de prueba 3: Buscar un libro inexistente**

Entrada:
- Título: "Libro inexistente"

Salida esperada:
- Mensaje: "El libro 'Libro inexistente' no se encuentra en la biblioteca."

**Caso de prueba 4: Realizar un préstamo**

Entrada:
- Usuario: "Juan Pérez"
- Título: "Orgullo y Prejuicio"

Salida esperada:
- Mensaje: "El préstamo del libro 'Orgullo y Prejuicio' a Juan Pérez se ha realizado exitosamente."
- La cantidad de copias disponibles del libro debe disminuir en 1.

**Caso de prueba 5: Devolver un libro**

Entrada:
- Usuario: "Juan Pérez"
- Título: "Orgullo y Prejuicio"

Salida esperada:
- Mensaje: "La devolución del libro 'Orgullo y Prejuicio' por Juan Pérez se ha registrado exitosamente."
- La cantidad de copias disponibles del libro debe aumentar en 1.

**Caso de prueba 6: Realizar un préstamo sin copias disponibles**

Entrada:
- Usuario: "Ana Sánchez"
- Título: "Libro sin copias"

Salida esperada:
- Mensaje: "Lo sentimos, no hay copias disponibles del libro 'Libro sin copias'."

**Caso de prueba 7: Devolver un libro no prestado**

Entrada:
- Usuario: "Carlos López"
- Título: "Libro no prestado"

Salida esperada:
- Mensaje: "No se encuentra registrado un préstamo del libro 'Libro no prestado' a Carlos López."

Estos casos de prueba cubren diferentes escenarios del proyecto, incluyendo acciones válidas e inválidas. Al probar el sistema con estos casos de prueba, se puede evaluar si el proyecto cumple con los requisitos establecidos y si se manejan correctamente los errores y situaciones inesperadas.