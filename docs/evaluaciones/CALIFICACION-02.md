# Retroalimentación — Funciones y POO

**Estudiante:** Juan Sebastián Gómez Vargas · **Taller:** Taller evaluativo 02 — Funciones y POO
**Fecha límite:** 2026-10-21 00:00 · **Versión revisada:** commit `e1e9550`

Muy buen trabajo con las clases: funcionan y dan los resultados esperados.

## Nota

| Criterio | Puntos |
|---|---|
| Funciones: parámetros, valores por defecto y retorno (Ej. 1 a 3) | 14 / 20 |
| `map`, `filter` y `lambda` (Ej. 4) | 10 / 10 |
| Clases, atributos y métodos (Ej. 5 y 7) | 15 / 15 |
| Encapsulamiento y validación (Ej. 6) | 15 / 15 |
| `__repr__` y `__str__` (Ej. 6 a 8) | 10 / 10 |
| Integración de funciones y clases (Ej. 8) | 7 / 10 |
| Ejecución sin errores | 5 / 10 |
| Documentación | 2 / 5 |
| Entrega correcta | 2 / 5 |
| **Total** | **80 / 100** |
| **Nota (0–5)** | **4.00** |

Este taller aporta **12.0 %** de los 15 % del momento evaluativo.

## 1. Funciones (14 / 20)
**Lo que hizo bien:**
- `calibrar_lectura` tiene los valores por defecto en la firma y usa `return`; da 11.5 y 12.0 como se espera.
- `es_lectura_valida` clasifica bien -999.0, 600.0, 25.0 y 0.0.
- `promedio_valido` reutiliza `es_lectura_valida` y da 27.0.

**Lo que puede mejorar:**
- En `promedio_valido`, la revisión "si no hay lecturas válidas, devolver None" quedó dentro del `for`. Si la primera lectura de la lista no es válida, la función devuelve `None` de inmediato aunque más adelante haya lecturas buenas (por ejemplo con `[-999.0, 10.0]`). Esa revisión debe ir después del `for`.
- La lista se llamó `lecturas_sbs_a` y la guía pide `lecturas_sbc_a`.
- Las funciones no tienen docstring (la frase entre triples comillas); usted escribió comentarios con `#`.

## 2. `map`, `filter` y `lambda` (10 / 10)
**Lo que hizo bien:**
- Obtuvo las 5 lecturas calibradas (de 11.5 a 61.9) y 2 excedencias, sin bucles ni comprensiones.

## 3. Clases, atributos y métodos (15 / 15)
**Lo que hizo bien:**
- `Lectura` guarda sus tres datos con valores por defecto, y `a_microgramos` y `es_dato_faltante` funcionan.
- `Estacion` guarda objetos `Lectura` y `valores()` entrega los ocho valores usando `a_microgramos()`.

## 4. Encapsulamiento y validación (15 / 15)
**Lo que hizo bien:**
- `Sensor` lanza `ValueError` para código vacío y pendiente menor o igual a cero, antes de guardar datos.
- Usa `_pendiente` e `_intercepto` y `calibrar` reutiliza `calibrar_lectura`.
- No dejó celdas de prueba que fallen.

## 5. `__repr__` y `__str__` (10 / 10)
**Lo que hizo bien:**
- Los textos de `Sensor`, `Estacion` e `InformeEstacion` salen exactamente como se pedía.

## 6. Integración (7 / 10)
**Lo que hizo bien:**
- `InformeEstacion` da promedio 31.9 y categoría "Moderada", reutilizando las funciones y el método `calibrar`.
- `categoria_pm25` usa una sola cadena `if` / `elif` / `else`.

**Lo que puede mejorar:**
- Los nombres de las dos últimas categorías están mal escritos: salen "Dañada para grupos sensibles" y "Dañada para la salud", y debían ser "Dañina para grupos sensibles" y "Dañina para la salud". Los textos deben coincidir carácter por carácter.

## 7. Ejecución sin errores (5 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin ningún error.

**Lo que puede mejorar:**
- Falta la celda de verificación final, así que no aparece el mensaje "Verificación completada sin errores.". Debía copiarla al final tal como está en la guía.

## 8. Documentación (2 / 5)
**Lo que hizo bien:**
- Cada ejercicio tiene una celda de texto previa y los nombres siguen `snake_case` y `PascalCase`.

**Lo que puede mejorar:**
- Ninguna función, clase o método tiene docstring de una línea.

## 9. Entrega correcta (2 / 5)
**Lo que hizo bien:**
- El notebook está en la carpeta `ejercicios/` y se subió antes del plazo.

**Lo que puede mejorar:**
- No siguió la estructura acordada: el nombre del archivo debe ser exactamente `taller-evaluativo-02-funciones-y-poo.ipynb` (con guiones), y el suyo usa guiones bajos.

## ¿El notebook funciona?
Corre completo sin errores y los resultados coinciden con los esperados (27.0, 5 lecturas calibradas, 31.9 y "Moderada"). Falta la celda de verificación, y hay dos textos de categoría mal escritos.

## Para el próximo taller
- Copie la celda de verificación al final y confirme que imprime el mensaje final.
- Escriba un docstring de una línea en cada función, clase y método.
- Use el nombre de archivo exacto que pide la guía.
- Ponga la revisión de "sin datos" después del bucle, no dentro.
- Compare los textos de salida con la guía antes de entregar.
