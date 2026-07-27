# Test Strategy

## Proyecto

**Juego "Adivina tu número"**

---

## Objetivo

Verificar el correcto funcionamiento del juego y documentar las actividades realizadas durante las fases de pruebas, corrección y mejora del proyecto.

---

## Resumen del proceso

El trabajo se desarrolló en las siguientes etapas:

1. Definición de la estrategia de pruebas.
2. Corrección de errores de ejecución.
3. Corrección de la lógica del negocio.
4. Implementación de validaciones de entrada.
5. Refactorización y mejoras de la experiencia de usuario.

---

## Ambiente de pruebas

- Sistema operativo: Windows
- Navegador: Google Chrome
- Tecnologías:
  - HTML
  - CSS
  - JavaScript

---

## Registro de incidencias

Durante el proceso de pruebas se identificaron once incidencias funcionales, todas corregidas satisfactoriamente.

| Identificador | Estado |
|----------------|--------|
| BUG-001 | Corregido |
| BUG-002 | Corregido |
| BUG-003 | Corregido |
| BUG-004 | Corregido |
| BUG-005 | Corregido |
| BUG-006 | Corregido |
| BUG-007 | Corregido |
| BUG-008 | Corregido |
| BUG-009 | Corregido |
| BUG-010 | Corregido |
| BUG-011 | Corregido |

---

## Mejoras implementadas

Una vez completadas las correcciones funcionales, se realizaron mejoras enfocadas en la mantenibilidad del código y la experiencia del usuario:

- Se cambió el tipo del campo de entrada a `type="number"` para facilitar el ingreso de datos.
- Se agregaron los atributos `min`, `max` y `step` al campo de entrada para restringir los valores permitidos.
- Se incorporó un `placeholder` indicando el rango válido de números.
- Se mejoró la apariencia visual de los controles mediante estilos CSS.
- Se simplificó el texto del botón principal para hacerlo más intuitivo.
- Se eliminaron espacios en blanco antes de validar la entrada del usuario.
- Se añadieron comentarios descriptivos al código JavaScript para facilitar su mantenimiento.
- Se reorganizó el código con el objetivo de mejorar su legibilidad sin modificar el comportamiento funcional.

---

## Casos de prueba ejecutados

| Caso de prueba | Estado |
|----------------|--------|
| Inicio del juego | Aprobado |
| Generación correcta del número aleatorio | Aprobado |
| Validación de números enteros | Aprobado |
| Control del número máximo de intentos | Aprobado |
| Visualización de mensajes de ayuda | Aprobado |
| Condición de victoria | Aprobado |
| Condición de derrota | Aprobado |
| Reinicio del juego | Aprobado |
| Manejo de entradas inválidas | Aprobado |

---

## Resultado final

Se ejecutaron nuevamente todas las pruebas funcionales después de aplicar las correcciones y mejoras correspondientes.

Los resultados obtenidos confirman que:

- Todas las incidencias identificadas fueron corregidas.
- Todos los casos de prueba finalizaron con estado **Aprobado**.
- No se detectaron errores de ejecución durante las pruebas.
- La refactorización realizada mejoró la organización del código y la experiencia del usuario sin modificar el comportamiento esperado de la aplicación.

En consecuencia, el proyecto cumple con los requisitos funcionales establecidos y se considera listo para su entrega.