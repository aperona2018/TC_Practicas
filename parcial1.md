# Pregunta 1: 
**Descargue Procesos.mat a su disco duro y cárguelo en Matlab. La variable X contiene en cada fila una realización de un proceso discreto, por lo que cada columna se corresponde a un instante de tiempo discreto determinado.
Conteste a la siguiente pregunta indicando el resultado con una precisión de 4 decimales. Indique la media de la realización 20.**

```Matlab
media = mean(X(20,:));
media
```

La media es: -0.3770

# Pregunta 2:
**Descargue Procesos.mat a su disco duro y cárguelo en Matlab. La variable Y contiene en cada fila una realización de un proceso discreto, por lo que cada columna se corresponde a un instante de tiempo discreto determinado.
Conteste a la siguiente pregunta indicando el resultado con una precisión de 4 decimales. Indique el valor de la autocorrelación Ryy[n1; n2] entre los instantes temporales n1=40 y n2=60.**

```Matlab
Ryy = mean(Y(:,40).*Y(:,60));
```

La autocorrelación es: 39.7371

# Pregunta 3:
**Indique que instrucción de MATLAB se ha utilizado para generar el histograma de una realización con Nm = 10.000 muestras de cada uno de los procesos que se muestran en las siguientes figuras.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial1_3.png)

Figura A: histogram(2+0.5*rand(1,Nm),Normalization="pdf")

Figura B: histogram(2+0.5*randn(1,Nm)),

Figura C:  histogram(2+0.5*rand(1,Nm))

Figura D: No hay una instrucción correcta para generar esta figura

**NOTA:** rand es para distribucion uniforme y randn es para distribución normal

# Pregunta 4:

**Indique cuál de las siguientes figuras se corresponde a la media temporal y media estadística del proceso con 1000 realizaciones y 1000 instantes temporales donde n(t) es un ruido Gaussiano estacionario de media cero y varianza unidad.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial1_4.png)

Media temporal: Figura B

Media estadística: Figura A

**NOTA:** La media temporal siempre es "fea"

# Pregunta 5:

**Indique que instrucción de MATLAB se ha utilizado para generar una realización con 200 muestras de cada uno de los procesos que se muestran en las siguientes figuras.**

![](https://github.com/aperona2018/TC_Practicas/blob/main/parcial1_5.png)

Figura A: 1+ 0.5*rand(1,200)

Figura B: randi(6,1,200)

Figura C: 1+ 0.5*randn(1,200)

Figura D: No hay una instrucción correcta para generar esta figura

**NOTA**: Siempre que sea discreto, es randi
