# Pregunta 1:

**Tenemos una modulación 8-PAM (con constelación An = [-7,-5,-3,-1,1,3,5,7];). Suponiendo que los símbolos transmitidos y los recibidos (antes del decisor en ausencia de ruido) tienen la anterior constelación)
¿Cuál es el valor de la energía media de símbolo Es?**

```Matlab
An = [-7, -5, -3, -1, 1, 3, 5, 7];

Es = mean(An.^2);
```

La energía media de símbolo es: 21

# Pregunta 2:

**Dados:
Un vector Eb_No_dB (de longitud M y que contiene distintos valores de energía de bit (Eb) entre potencia de ruido (No), en dBs).
Un vector SER_Experimental (de longitud M y que contiene los valores de probabilidad de error de simbolo (SER) experimental calculados para los correspondientes valores de Eb/No).
Escriba la instrucción (línea en MATLAB) para representar, con una correcta visualización, la SER_Experimental (en el eje y) frente a la Eb_No_dB (en el eje x).
Nota: debe expresar la instrucción sin espacios y acabando en punto y coma.**

```Matlab
semilogy(Eb_No_dB, SER_Experimental);
```

# Pregunta 3:

**Para una modulación 8-PAM, con codificación Gray, que tiene una BER (probabilidad de error de bit) de 0,012, ¿cuál es el valor de su SER (probabilidad de error de símbolo)?**

BER = SER/K

SER = BER * K = 0.012 * 3 = 0.036

# Pregunta 4:

**En la siguiente gráfica se muestran 4 diagramas de ojo se una señal PAM polar (con símbolos 1 y -1) obtenidos para un coeficiente de roll-off del filtro de coseno alzado fijo 
y varios valores de SNR. Relacione cada una de las figuras con su descripción correspondiente.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial3_4.png)

Figura A: SNR = 5 dB

Figura B: SNR = 25 dB

Figura C: SNR = 35 dB

Figura D: SNR = 15 dB

# Pregunta 5:

**En la siguiente gráfica se muestran 4 diagramas de ojo se una señal PAM polar (con símbolos 1 y -1) obtenidos para varios valores del coeficiente de roll-off del filtro de coseno alzado. 
Relacione cada una de las figuras con su descripción correspondiente**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial3_5.png)

Figura A: r = 0.75

Figura B: r = 0

Figura C: r = 0.5

Figura D: r = 1

**NOTA:** A menor roll off mas lineas finas
