# Analizador Lógico – Comunicación UART

##  Descripción

Este repositorio contiene el desarrollo de la práctica de **Analizador Lógico**, realizada en la asignatura de **Comunicaciones Digitales** del programa de Ingeniería en Telecomunicaciones de la **Universidad Militar Nueva Granada**.

En la práctica se implementó una comunicación serial **UART** utilizando una **Raspberry Pi Pico 2W** y se utilizó un analizador lógico para visualizar y medir las señales transmitidas. Se trabajó con una configuración de **9600 baudios, 8 bits de datos, sin paridad y 1 bit de parada**, permitiendo analizar la estructura temporal de las tramas y verificar experimentalmente la duración de los bits.

Durante el desarrollo se realizaron diferentes pruebas:

* Carácter **U**
* Carácter **^**
* Transmisión repetida del carácter **^**
* Mensaje: `UMNG_2026_LIDER_EN_TELECOMUNICACIONES`
* Mensaje: `UMNG_2026_LIDER_EN_TELECOMUNICACIONES` con paridad impar

Para cada prueba se analizaron las tramas obtenidas mediante el analizador lógico y se realizaron mediciones del **tiempo de bit**, **tiempo de trama** y **tiempo total de transmisión**. Los resultados experimentales fueron comparados con los valores teóricos mediante el cálculo del error porcentual.

También se estudió el efecto de la **frecuencia de muestreo** sobre la representación de la señal UART, calculando la cantidad de muestras disponibles por bit para diferentes tasas de transmisión. Esto permitió establecer la importancia de seleccionar una frecuencia de muestreo adecuada para obtener mediciones confiables.

## Resultados principales

Las fórmulas utilizadas para el análisis de la comunicación UART fueron:

### Tiempo de bit

$$
T_b = \frac{1}{\text{Baudrate}}
$$

### Tiempo de trama

$$
T_{\text{trama}} = N_{\text{bits}} \cdot T_b
$$

### Tiempo total de transmisión

$$
T_{\text{total}} = N_{\text{tramas}} \cdot T_{\text{trama}}
$$

### Número de muestras por bit

$$
N_{\text{muestras/bit}} = \frac{f_s}{\text{Baudrate}}
$$

Los tiempos medidos para las diferentes pruebas presentaron errores inferiores al **0.2 %**, mostrando una buena concordancia entre los valores teóricos y experimentales.

##  Contenido del repositorio

[x]* **Código:** programas utilizados en la Raspberry Pi Pico 2W.
[]* **Datos:** archivos con los resultados de las mediciones y análisis de frecuencia de muestreo.
[]* **Capturas:** imágenes obtenidas durante las diferentes pruebas con el analizador lógico.
[]* **Informe:** documento final con el procedimiento, resultados, análisis y conclusiones.

## Autores

**Miguel Ángel Plazas**

**Daniel Mateo Alegría Bernate**

**Universidad Militar Nueva Granada**

**Ingeniería en Telecomunicaciones – 2026-2**

**Docente:** José de Jesús Rúgeles Uribe
