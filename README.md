"""
Created on Thu Jun  5 16:53:15 2025

@author: valentian gonzalez cassola
"""

# Proyecto de Análisis de Datos - "Mi modulo"

## Descripción del Proyecto
"""
Este proyecto contiene  clases y funciones para facilitar el análisis estadístico de datos. 

Las funcionalidades son análisis descriptivo, análisis gráfico, generación de datos, modelado estadístico (regresión lineal y logística) e inferencia estadística mediante métodos clásicos y bootstrap.
"""



### Funcionalidades Principales

#### 1. **Resumen Estadístico**
Clases como `ResumenNumerico` y `ResumenGrafico` permiten:
- Calcular media, mediana, desviación estándar, cuartiles y varianza.
- Generar histogramas, QQ-plots y curvas de densidad mediante distintos núcleos (Gaussiano, Uniforme, Cuadrático, Triangular).

#### 2. **Generación de Datos**
Con `GeneradoraDeDatos` se pueden simular distribuciones:
- Normal, Bootstrap, T de Student, Uniforme y mezcla de distribuciones.

#### 3. **Modelos de Regresión**
- `RegresionLinealSimple` y `RegresionLinealMultiple`: permite entrenamiento, predicción, intervalos de confianza y visualización.
- `RegresionLogistica`: ajuste del modelo, predicción con umbral, matriz de confusión y curva ROC.

#### 4. **Inferencia Estadística**
La clase `Dados` permite realizar:
- Cálculo de intervalos de confianza.
- Bootstrap para proporciones.
- Test de hipótesis usando Chi-cuadrado para frecuencias observadas vs esperadas.

### 📈 Ejemplo de Uso

```python
# Generar datos normales
generador = GeneradoraDeDatos(tamaño=100)
datos = generador.generar_datos_dist_norm(media=0, varianza=1)

# Calcular estadísticos
resumen = ResumenNumerico(datos)
print(resumen.generacion_resumen_numerico())

# Ajustar modelo lineal
modelo = RegresionLinealSimple(x, y)
modelo.ajustar_modelo()
modelo.graficar_recta_ajustada()
```

