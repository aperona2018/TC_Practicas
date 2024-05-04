# Pregunta 1: 

**Descargue ProcesoX.mat a su disco duro y cárguelo en Matlab. La variable X contiene en cada fila una realización de un proceso discreto, por lo que cada columna se corresponde a un instante de tiempo discreto determinado.
Conteste a la siguiente pregunta indicando el resultado con una precisión de 4 decimales. Indique el valor de la potencia de la realización 10**

```Matlab
pot = mean((abs(X(10,:).^2));
```

La potencia es: 0.0809

# Pregunta 2:

**En la siguiente imagen se muestran cuatro figuras relacionadas con el filtrado de una señal de voz visto en el Hito 2 de la Práctica 2. 
Indique a qué se corresponde cada una de las cuatro figuras.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial2_2.png)

Figura A: DEP señal a la salida del filtro

Figura B: Señal original

Figura C: DEP filtro

Figra D: Dep señal a la entrada del filtro


# Pregunta 3:

**A continuación se muestra una imagen con cuatro figuras relacionadas con el Hito 3 de modulaciones analógicas vistas en la Práctica 2. 
Indique a qué tipo de señal se corresponde cada una de las cuatro figuras.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial2_3.png)

Figura A: Modulada FM

Figura B: Señal original

Figura C: Demodulada

Figura D: Modulada FM con ruido

# Pregunta 4:

**Sabiendo que la variable dep_x representa la densidad espectral de una señal de voz x cuya frecuencia de muestreo es Fs, 
indique cuál de los siguientes códigos proporciona una representación/visualización correcta de la densidad espectral de x.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial2_4.png)

Código D

**NOTA:** para visualizar bien usar ejes con linspace(-Fs/2, Fs/2, length(x));
o con linspace(-T, T, length(x));

# Pregunta 5:

**La variable X del ProcesoX.mat contiene en cada fila una realización de un proceso discreto, por lo que cada columna se corresponde a un instante de tiempo discreto determinado.
Escriba la línea de código Matlab para calcular la autocorrelación de la realización 14.
La línea no debe tener espacios y debe empezar con  rxx= y acabar con ; **

```Matlab
rxx=xcorr(X(14,:));
```
