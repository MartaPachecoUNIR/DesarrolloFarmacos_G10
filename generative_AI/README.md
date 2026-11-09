# Optimización estructural mediante inteligencia artificial generativa
El módulo se compone de 3 ficheros principales:

## 1. Análisis estructural (analisis_estructural.py)

Se encargará de evaluar los modelos tridimensionales obtenidos mediante AlphaFold, identificando posibles regiones de baja confianza o imperfecciones estructurales.

Para ello, analizará parámetros como la confianza local (pLDDT), la disposición relativa de los dominios (PAE), la geometría molecular y la presencia de posibles regiones desordenadas. Esta información permitirá identificar aquellas zonas de la proteína que podrían beneficiarse de un análisis estructural adicional.

## 2. Generación conformacional (generacion_conformacional.py)

Se encargará de utilizar modelos de inteligencia artificial generativa para explorar el espacio conformacional de las proteínas diana.

A partir de los modelos estructurales iniciales, generará diferentes conformaciones alternativas mediante la modificación controlada de determinadas regiones estructurales, prestando especial atención a aquellas zonas con mayor flexibilidad o incertidumbre.

El objetivo será obtener diferentes representaciones tridimensionales de una misma proteína que permitan contemplar su posible variabilidad estructural durante el posterior proceso de docking molecular.

## 3. Validación y selección (validacion_y_seleccion.py)

Se encargará de evaluar la calidad de las estructuras generadas y seleccionar aquellas más adecuadas para su utilización en el siguiente módulo.

Para ello, tendrá en cuenta parámetros como la geometría de los enlaces, los ángulos de torsión, los posibles impedimentos estéricos y la conservación de los dominios funcionales de la proteína. También comprobará que las conformaciones generadas mantengan la compatibilidad con la secuencia aminoacídica original.

Finalmente, seleccionará los modelos estructurales que superen los criterios de calidad establecidos y los almacenará para su posterior utilización en el cribado y docking molecular.

