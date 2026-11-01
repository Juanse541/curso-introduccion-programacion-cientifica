# Retroalimentación — Taller evaluativo 03 NumPy

**Estudiante:** Juan Sebastián Gómez Vargas · **Taller:** Taller evaluativo 03 — NumPy
**Fecha límite:** 2026-11-01 23:59 · **Versión revisada:** commit `76eac4a`

Excelente trabajo: los resultados de todos los ejercicios coinciden con los esperados.

## Nota

| Criterio | Puntos |
|---|---|
| Creación y atributos de arreglos (Ej. 1) | 10 / 10 |
| Indexación y slicing (Ej. 2) | 10 / 10 |
| Máscaras booleanas (Ej. 3) | 15 / 15 |
| Vectorización y broadcasting (Ej. 4) | 11 / 15 |
| Estadística por eje y funciones universales (Ej. 5 y 6) | 20 / 20 |
| Integración (Ej. 7) | 10 / 10 |
| Ejecución sin errores | 10 / 10 |
| Documentación | 3 / 5 |
| Entrega correcta | 2 / 5 |
| **Total** | **91 / 100** |
| **Nota (0–5)** | **4.55** |

Este taller aporta **13.7 %** de los 15 % del momento evaluativo.

## 1. Creación y atributos de arreglos (10 / 10)
**Lo que hizo bien:** creó `lecturas_crudas` con `np.array`, leyó sus atributos en vez de escribirlos a mano, y `dias`, `pendientes` e `interceptos` son correctos.

## 2. Indexación y slicing (10 / 10)
**Lo que hizo bien:** cada resultado sale de una sola expresión, con índice negativo en `ultimo_primer` y un `bloque` de forma (3, 4).

## 3. Máscaras booleanas (15 / 15)
**Lo que hizo bien:** `es_util` une dos comparaciones con `&`, quedan 5 lecturas útiles, 2 faltantes y el promedio es 27.0, sin bucles.

## 4. Vectorización y broadcasting (11 / 15)
**Lo que hizo bien:** convirtió `pendientes` e `interceptos` en columnas, `calibradas` tiene la forma y los valores correctos, y el promedio de SBC-A es 31.9.
**Lo que puede mejorar:**
- Falta la explicación escrita de por qué multiplicar `lecturas_crudas * pendientes` daba error al comparar las formas (5, 7) y (5,).
**Cómo corregirlo:**
- En la celda de texto del Ejercicio 4 escriba dos o tres frases: NumPy compara las formas de derecha a izquierda, el 7 no coincide con el 5, y por eso el vector debe volverse columna (5, 1).

## 5. Estadística por eje y funciones universales (20 / 20)
**Lo que hizo bien:** promedios por sensor y por día, máximos y media sobre el límite son correctos; usó `np.maximum`, `np.abs`, `np.round` y trabajó `en_alerta` sobre una copia, con 8 celdas mayores que 0.

## 6. Integración (10 / 10)
**Lo que hizo bien:** los conteos son 9, 18, 7 y 1 (suman 35), `dia_pico` es 5 y las dos líneas de salida coinciden con lo pedido.

## 7. Ejecución sin errores (10 / 10)
**Lo que hizo bien:** el notebook corre completo sin errores y la celda de verificación quedó intacta.

## 8. Documentación (3 / 5)
**Lo que hizo bien:** hay una celda de texto antes de cada ejercicio y los nombres siguen `snake_case` sin tildes.
**Lo que puede mejorar:**
- Las celdas de texto solo repiten el título del ejercicio; no explican qué hace cada uno.
**Cómo corregirlo:**
- Agregue a cada celda de texto una o dos frases sobre qué se hace y con qué herramienta de NumPy.

## 9. Entrega correcta (2 / 5)
**Lo que hizo bien:** el notebook está en `ejercicios/` en la rama `main`, antes del plazo.
**Lo que puede mejorar:**
- No siguió la estructura acordada: el nombre del archivo debe ser exacto y el suyo es `taller_evaluativo_03_numpy.ipynb`.
**Cómo corregirlo:**
- Renombre el archivo a `taller-evaluativo-03-numpy.ipynb` (con guiones) dentro de `ejercicios/` y súbalo de nuevo.

## ¿El notebook funciona?
Sí. Corre completo sin errores, la celda de verificación imprime "Verificación completada sin errores." y los resultados coinciden con los esperados.

## Para el próximo taller
- Use el nombre de archivo exacto que pide la guía.
- Explique en cada celda de texto qué hace el ejercicio.
- Incluya siempre la explicación escrita cuando la guía la pida.
- Siga ejecutando "Reiniciar y ejecutar todas" antes de entregar.
