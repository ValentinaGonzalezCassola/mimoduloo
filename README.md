
"""

Created on Thu Jun  5 16:53:15 2025

@author: valentina gonzalez cassola

"""

Este proyecto contiene  clases y funciones para facilitar el análisis estadístico de datos.

Las funcionalidades son análisis descriptivo, análisis gráfico, generación de datos, modelado estadístico (regresión lineal y logística) e inferencia estadística mediante métodos clásicos y bootstrap.

"""


\# Proyecto de Análisis de Datos - "Mi modulo"

\## Descripción del Proyecto

\## Estructura del Código

\### `Resumen`

Realiza cálculos estadísticos básicos:

- Media, Mediana
- Desvío estándar, Varianza
- Cuartiles, Mínimo y Máximo

\---

\### `Histograma`

Permite:

- Generar histogramas normalizados
- Estimar densidades con distintos \*\*kernels\*\*: gaussiano, uniforme, cuadrático, triangular
- Graficar estimaciones y QQ plot


\---

\### `GeneradoraDeDatos`

Genera muestras simuladas desde distribuciones:

- Normal
- Uniforme
- T de Student
- Distribución mixta tipo BS

Incluye funciones para calcular curvas teóricas de densidad.

\---

\### `Regresion` (y subclases)

Modelos ajustables:

- `RegresionLinealSimple`
- `RegresionLinealMultiple`
- `RegresionLogistica`

Funciones destacadas:

- Ajuste del modelo (`ajustar\_modelo`)
- Predicción e intervalos
- Visualización de residuos
- Evaluación de supuestos
- Cálculo de R², p-valores, t-tests

\---

\### `Estadistica`

Herramientas auxiliares como:

- Análisis de varianza (ANOVA)

\---


\##  Ejemplo de uso

\```python

datos = GeneradoraDeDatos(1000).generar\_datos\_dist\_norm(0, 1)

resumen = Resumen(datos)

resumen.muestra\_resumen()

hist = Histograma(datos)

hist.grafico\_histograma(0.2)

hist.grafico\_densidad\_nucleo(0.2, 'gaussiano')

\```

\---
