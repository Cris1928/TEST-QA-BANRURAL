# Test Strategy

## Proyecto

**Juego "Adivina tu número"**

---

## Objetivo

Verificar que la lógica del juego cumpla con las reglas funcionales definidas por el cliente y documentar las correcciones realizadas.

---

## Estrategia de pruebas

1. Ejecutar el juego.
2. Validar cada regla de negocio.
3. Comparar el comportamiento con los requisitos establecidos.
4. Corregir la lógica cuando sea necesario.
5. Ejecutar nuevamente todas las pruebas.

---

## Ambiente de pruebas

- Sistema operativo: Windows
- Navegador: Google Chrome
- Tecnologías:
  - HTML
  - CSS
  - JavaScript

---

## Errores corregidos

### BUG-001

**Descripción**

El selector del elemento `lowOrHi` era incorrecto.

**Estado**

Corregido.

---

### BUG-002

**Descripción**

Se utilizó incorrectamente `addEventListener()`.

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

La comparación entre el número ingresado y el número aleatorio nunca era verdadera debido a una diferencia de tipos de datos.

**Estado**

Corregido.

---

### BUG-005

**Descripción**

El número aleatorio se generaba entre 0 y 10 utilizando valores decimales.

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

El juego únicamente permitía cinco intentos.

**Resultado esperado**

Permitir diez intentos.

**Estado**

Corregido.

---

### BUG-007

**Descripción**

La condición de victoria y derrota estaba invertida.

**Resultado esperado**

- Si el usuario adivina el número, mostrar mensaje de éxito.
- Si alcanza el décimo intento sin acertar, mostrar mensaje de derrota.

**Estado**

Corregido.

---

### BUG-008

**Descripción**

Los mensajes "El número es mayor" y "El número es menor" se mostraban de forma inversa.

**Estado**

Corregido.

---

### BUG-009

**Descripción**

El color del mensaje para intentos incorrectos no coincidía con el solicitado.

**Estado**

Corregido.

---

### BUG-010

**Descripción**

Al reiniciar el juego se volvía a generar un número entre 1 y 1 debido a una fórmula incorrecta.

**Estado**

Corregido.

---

## Casos de prueba

| Caso de prueba | Estado |
|----------------|--------|
| El juego inicia correctamente | Aprobado |
| Se genera un número entre 1 y 100 | Aprobado |
| El usuario gana al adivinar | Aprobado |
| El usuario pierde después de 10 intentos | Aprobado |
| Se muestran las pistas correctas | Aprobado |
| Reinicio del juego | Aprobado |
| Validación de números enteros | Pendiente |

---

## Trabajo pendiente

Implementar la validación de entradas para aceptar únicamente números enteros y evitar consumir intentos cuando el usuario ingrese valores inválidos.

Esta funcionalidad será desarrollada en el siguiente commit.

---

## Conclusión

La lógica principal del juego cumple con los requisitos funcionales definidos para esta fase del proyecto. La única funcionalidad pendiente corresponde a la validación de la entrada del usuario, la cual se implementará en una siguiente iteración para mantener una separación clara entre la corrección de la lógica del negocio y la validación de datos.