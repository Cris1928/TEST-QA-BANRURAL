# Test Strategy

## Proyecto

Juego "Adivina tu número"

---

## Objetivo

Realizar pruebas funcionales sobre el juego para detectar y corregir errores hasta cumplir los requisitos definidos en el README.

---

## Alcance

Se evaluará la interfaz y la lógica implementada en el archivo `index.html`.

---

## Estrategia de pruebas

1. Ejecutar la aplicación.
2. Revisar la consola del navegador.
3. Identificar errores de JavaScript.
4. Corregir únicamente los errores que impiden la ejecución.
5. Volver a ejecutar el sistema.
6. Documentar cada corrección.

---

## Ambiente de pruebas

- Windows
- Google Chrome
- HTML
- CSS
- JavaScript

---

# Errores encontrados

## BUG-001

**Descripción**

El elemento encargado de mostrar si el número es mayor o menor nunca es encontrado.

**Causa**

El selector utilizado en `querySelector()` no incluye el prefijo `.` para seleccionar una clase CSS.

**Solución**

Corregir:

```javascript
document.querySelector("lowOrHi")
```

por

```javascript
document.querySelector(".lowOrHi")
```

**Estado**

Corregido.

---

## BUG-002

**Descripción**

El botón para enviar un intento no responde al hacer clic.

**Causa**

Se utilizó incorrectamente el método `addeventListener()`.

**Solución**

Cambiar:

```javascript
addeventListener()
```

por

```javascript
addEventListener()
```

**Estado**

Corregido.

---

## BUG-003

**Descripción**

El botón para reiniciar el juego tampoco responde.

**Causa**

Se repite el mismo error tipográfico al registrar el evento.

**Solución**

Corregir el método `addEventListener()`.

**Estado**

Corregido.

---

## BUG-004

**Descripción**

Nunca es posible adivinar el número.

**Causa**

El número ingresado desde el formulario es un texto mientras que el número aleatorio es numérico.

**Solución**

Convertir el valor ingresado utilizando `Number()` antes de realizar la comparación.

**Estado**

Corregido.

---

# Casos pendientes

- Validación de números enteros.
- Generación correcta del número aleatorio.
- Límite de 10 intentos.
- Mensajes de éxito y error.
- Colores solicitados.
- Reinicio completo del juego.
- Cumplimiento de todas las reglas del README.

---

# Conclusión

Durante esta fase se corrigieron únicamente los errores que impedían la ejecución del juego. La aplicación ya puede ejecutarse sin errores de JavaScript en la consola y es posible interactuar con ella. Las reglas de negocio y los requisitos funcionales serán corregidos en los siguientes commits.