# Test Strategy

## Proyecto

**Juego "Adivina tu número"**

---

## Objetivo

Realizar pruebas funcionales sobre la aplicación para identificar incidencias, aplicar las correcciones necesarias y verificar el cumplimiento de los requisitos definidos para el proyecto.

---

## Alcance

Las pruebas se ejecutaron sobre la aplicación implementada en el archivo `index.html`, incluyendo la interfaz de usuario y la lógica desarrollada con HTML, CSS y JavaScript.

---

## Ambiente de pruebas

- Sistema operativo: Windows
- Navegador: Google Chrome
- Tecnologías:
  - HTML
  - CSS
  - JavaScript

---

## Estrategia de pruebas

El proceso de validación se desarrolló en las siguientes etapas:

1. Análisis de los requisitos funcionales.
2. Ejecución inicial de la aplicación.
3. Revisión de errores en la consola del navegador.
4. Corrección de errores de ejecución.
5. Corrección de la lógica del juego.
6. Implementación de validaciones de entrada.
7. Reejecución de los casos de prueba.
8. Documentación de las incidencias y las soluciones aplicadas.

---

## Registro de incidencias

| Identificador | Incidencia | Acción correctiva | Estado |
|----------------|------------|-------------------|--------|
| BUG-001 | Selector incorrecto para `lowOrHi`. | Corrección del selector CSS. | Corregido |
| BUG-002 | Uso incorrecto de `addEventListener()`. | Actualización del método utilizado. | Corregido |
| BUG-003 | Comparación incorrecta por diferencia de tipos de datos. | Conversión de la entrada mediante `Number()`. | Corregido |
| BUG-004 | Generación incorrecta del número aleatorio. | Implementación de `Math.floor(Math.random() * 100) + 1`. | Corregido |
| BUG-005 | Límite incorrecto de intentos. | Ajuste del máximo a diez intentos. | Corregido |
| BUG-006 | Lógica de victoria y derrota invertida. | Corrección de las condiciones del juego. | Corregido |
| BUG-007 | Pistas mostradas de forma incorrecta. | Ajuste de la lógica de mensajes de ayuda. | Corregido |
| BUG-008 | Error al reiniciar la partida. | Corrección de la generación del nuevo número. | Corregido |
| BUG-009 | Falta de validación para números enteros. | Implementación mediante `Number.isInteger()`. | Corregido |
| BUG-010 | Se aceptaban valores fuera del rango permitido. | Validación del rango entre 1 y 100. | Corregido |
| BUG-011 | Entradas inválidas afectaban el flujo del juego. | Finalización anticipada de la ejecución mediante `return`. | Corregido |

---

## Casos de prueba ejecutados

| Caso de prueba | Estado |
|----------------|--------|
| Inicio de la aplicación | Aprobado |
| Generación del número aleatorio | Aprobado |
| Condición de victoria | Aprobado |
| Condición de derrota | Aprobado |
| Mensajes de ayuda | Aprobado |
| Validación de números enteros | Aprobado |
| Validación del rango permitido | Aprobado |
| Entradas inválidas sin consumir intentos | Aprobado |
| Reinicio de la partida | Aprobado |

---

## Resultado final

Las pruebas funcionales fueron ejecutadas nuevamente después de cada corrección para verificar la estabilidad del sistema.

Los resultados obtenidos confirman que:

- Todas las incidencias identificadas fueron corregidas.
- Todos los casos de prueba finalizaron con estado **Aprobado**.
- No se detectaron errores de ejecución en la consola del navegador.
- La lógica del juego cumple con los requisitos funcionales establecidos.
- La validación de datos evita entradas inválidas y preserva el flujo correcto de la aplicación.

---

## Historial de cambios

El trabajo se desarrolló de forma incremental mediante los siguientes commits:

1. `docs: crear estrategia inicial de pruebas`
2. `fix: corregir errores de ejecución`
3. `fix: corregir lógica del juego`
4. `feat: agregar validación de números enteros`
5. `refactor: mejorar interfaz y experiencia de usuario`
6. `docs: documentar incidencias y soluciones`

---

## Conclusión

La aplicación presenta un comportamiento estable, cumple con los requisitos funcionales definidos para la prueba técnica y mantiene un historial de cambios organizado que facilita la trazabilidad de las correcciones realizadas.