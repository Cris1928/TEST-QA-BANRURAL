# Test Strategy

## Proyecto

**Juego "Adivina tu número"**

---

## Objetivo

Realizar pruebas funcionales sobre el juego para verificar el cumplimiento de los requisitos establecidos por el cliente y documentar las incidencias detectadas junto con las acciones correctivas aplicadas.

---

## Estrategia de pruebas

1. Ejecutar el proyecto en un navegador web.
2. Revisar la consola para identificar errores de JavaScript.
3. Validar el cumplimiento de cada requisito funcional.
4. Corregir las incidencias detectadas.
5. Repetir las pruebas después de cada corrección.
6. Documentar los resultados obtenidos.

---

## Ambiente de pruebas

- Sistema operativo: Windows
- Navegador: Google Chrome
- Tecnologías:
  - HTML
  - CSS
  - JavaScript

---

## Registro de errores

### BUG-001

**Descripción**

El selector del elemento `lowOrHi` era incorrecto.

**Estado**

Corregido.

---

### BUG-002

**Descripción**

Se utilizó incorrectamente el método `addEventListener()`.

**Estado**

Corregido.

---

### BUG-003

**Descripción**

El botón para reiniciar el juego utilizaba el mismo método incorrecto.

**Estado**

Corregido.

---

### BUG-004

**Descripción**

La comparación entre el número ingresado y el número generado nunca era verdadera debido a una diferencia de tipos de datos.

**Estado**

Corregido.

---

### BUG-005

**Descripción**

El número aleatorio se generaba utilizando números decimales entre 0 y 10.

**Resultado esperado**

Generar un número entero entre 1 y 100.

**Solución aplicada**

```javascript
Math.floor(Math.random() * 100) + 1
```

**Estado**

Corregido.

---

### BUG-006

**Descripción**

El juego permitía únicamente cinco intentos.

**Resultado esperado**

Permitir un máximo de diez intentos.

**Estado**

Corregido.

---

### BUG-007

**Descripción**

Las condiciones de victoria y derrota estaban invertidas.

**Resultado esperado**

- Mostrar un mensaje de éxito cuando el jugador adivine el número.
- Mostrar un mensaje de derrota al alcanzar el décimo intento sin acertar.

**Estado**

Corregido.

---

### BUG-008

**Descripción**

Los mensajes de ayuda mostraban una pista incorrecta respecto al número ingresado.

**Estado**

Corregido.

---

### BUG-009

**Descripción**

Los colores utilizados para los mensajes no coincidían con los requerimientos establecidos.

**Estado**

Corregido.

---

### BUG-010

**Descripción**

Al reiniciar el juego se generaba incorrectamente el nuevo número aleatorio.

**Estado**

Corregido.

---

### BUG-011

**Descripción**

El sistema aceptaba cualquier tipo de entrada, incluyendo texto y números decimales.

**Resultado esperado**

Aceptar únicamente números enteros. Cuando el usuario ingrese un valor inválido, se debe mostrar una alerta y el intento no debe contabilizarse.

**Solución aplicada**

Se implementó una validación utilizando `Number.isInteger()` antes de ejecutar la lógica del juego. Si la validación falla, se muestra un mensaje de alerta y la ejecución finaliza sin incrementar el contador de intentos.

**Estado**

Corregido.

---

## Casos de prueba ejecutados

| Caso de prueba | Estado |
|----------------|--------|
| La aplicación inicia correctamente | Aprobado |
| Se genera un número entero entre 1 y 100 | Aprobado |
| El jugador puede ganar antes del décimo intento | Aprobado |
| El jugador pierde después de diez intentos | Aprobado |
| Se muestran correctamente las pistas | Aprobado |
| El botón de reinicio funciona correctamente | Aprobado |
| Solo se aceptan números enteros | Aprobado |
| Una entrada inválida no consume un intento | Aprobado |

---

## Resultado final

Las pruebas funcionales fueron ejecutadas satisfactoriamente y todas las incidencias identificadas fueron corregidas.

Los casos de prueba definidos fueron validados con resultado **Aprobado**, confirmando que el juego cumple con los requisitos funcionales establecidos.

Durante la ejecución de las pruebas no se detectaron errores en la consola del navegador ni comportamientos distintos a los esperados.

El proyecto se considera listo para su entrega.