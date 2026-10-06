# Retroalimentación — Taller evaluativo 01

**Estudiante:** Juan Sebastián Gómez Vargas · **Taller:** Taller evaluativo 01 — Python y estructuras de datos
**Fecha límite:** 2026-10-06 23:59 · **Versión revisada:** commit `de4d8f7`

## Nota

| Criterio | Puntos |
|---|---|
| Variables, tipos y operadores (Ej. 1 a 4) | 9 / 20 |
| Condicionales y clasificación (Ej. 5) | 15 / 15 |
| Bucles, acumuladores y control de flujo (Ej. 6 a 8) | 21 / 30 |
| Estructuras de datos nativas (Ej. 9) | 14 / 15 |
| Ejecución sin errores | 5 / 10 |
| Documentación en celdas de texto | 4 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **69 / 100** |
| **Nota (0–5)** | **3.45** |

Este taller aporta **10.4 %** de los 15 % del momento evaluativo.

## 1. Variables, tipos y operadores (9 / 20)
**Lo que hizo bien:**
- Las siete variables del Ejercicio 1 tienen el tipo correcto y las verificó con `type()`.
- La conversión de unidades del Ejercicio 2 sale de multiplicar por `factor_conversion`.
- El Ejercicio 3 usa solo `//` y `%`, y los resultados son correctos (25 horas, 1 día, 1 hora sobrante).

**Lo que puede mejorar:**
- En el Ejercicio 1 la variable se llama `altitud_mar` y no `altitud_m`, como pedía la guía.
- En el Ejercicio 2 el error absoluto está al revés: se debe restar el patrón a la lectura (lectura menos patrón), no al contrario. Por eso los errores salen con el signo contrario.
- En el Ejercicio 4 `es_dato_faltante` no es una comparación: es una resta entre dos números y da -1499.0. Debía ser `lectura == codigo_dato_faltante`, que da `False`.
- Además creó una variable extra, `es_dato_faltante2`, escrita a mano como `True`. Los resultados deben calcularse, no escribirse.
- El rango usa `>` y `<` en lugar de `>=` y `<=`, y por el error anterior `lectura_valida` da `False` cuando la lectura de 41.8 sí es válida.

## 2. Condicionales y clasificación (15 / 15)
**Lo que hizo bien:**
- La cadena `if` / `elif` / `else` está ordenada de menor a mayor y clasifica bien las cuatro categorías.
- Para 41.8 da "Dañina para grupos sensibles".

## 3. Bucles, acumuladores y control de flujo (21 / 30)
**Lo que hizo bien:**
- El Ejercicio 6 da 10 lecturas válidas, 2 descartadas y promedio 22.55.
- El Ejercicio 7 encuentra máximo 58.3 y mínimo 7.5 con dos recorridos y sin `max()`, `min()` ni `sum()`.
- El Ejercicio 8 usa `while`, actualiza `concentracion` dentro del bloque y termina (10 horas).

**Lo que puede mejorar:**
- En el Ejercicio 6 se pedía saltar el dato faltante con `continue`; usted usó un `else`. El resultado es correcto, pero no cumple esa instrucción. Tampoco recorre los valores directamente, sino por índice.
- En el Ejercicio 7 dividió entre (n - 1) en la desviación estándar; la guía pedía dividir entre la cantidad de lecturas válidas. Por eso obtuvo 17.17 en lugar de 16.29.
- Dejó dudas escritas en el código para el profesor: es mejor llevarlas a clase.

## 4. Estructuras de datos nativas (14 / 15)
**Lo que hizo bien:**
- Accede a los datos por clave, desempaqueta la tupla en `latitud` y `longitud`, y usa `get` con "no disponible", sin errores.

**Lo que puede mejorar:**
- Se pedía una línea por estación; usted imprimió varias líneas por estación. Es un detalle menor.

## 5. Ejecución sin errores (5 / 10)
**Lo que hizo bien:**
- Todas las celdas corren de principio a fin sin errores y sin bucles que no terminan.

**Lo que puede mejorar:**
- Falta la celda de verificación final, así que no aparece el mensaje "Verificación completada sin errores.". Además, con esa celda el resultado de `lectura_valida` habría fallado.

## 6. Documentación en celdas de texto (4 / 5)
**Lo que hizo bien:**
- Cada ejercicio tiene su celda de texto previa y los nombres de variables son claros y en `snake_case`.

**Lo que puede mejorar:**
- La celda inicial no incluye el título del taller, y las celdas previas solo repiten el nombre del ejercicio, sin explicar qué hace.

## 7. Entrega correcta (1 / 5)
**No siguió la estructura acordada:** el notebook debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-01-calidad-del-aire.ipynb`. Usted lo subió a la raíz del repositorio como `taller_evaluativo_01_calidad_del_aire.ipynb` (con guiones bajos). Sí llegó antes del plazo y está en `main`.

## ¿El notebook funciona?
Corre completo sin errores y la mayoría de resultados coinciden con los esperados. No tiene la celda de verificación, y los errores del Ejercicio 2 y los booleanos del Ejercicio 4 no coinciden con lo pedido.

## Para el próximo taller
- Copie la celda de verificación al final y ejecútela antes de entregar.
- Guarde el archivo en `ejercicios/` con el nombre exacto de la guía.
- Lea cada instrucción con calma (`continue`, orden de la resta, comparar con `==`) y haga lo que dice.
- Calcule los resultados con operadores y evite escribir valores a mano.
- Suba también los talleres de variables y de condicionales a `ejercicios/`.
