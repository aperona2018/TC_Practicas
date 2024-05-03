# Preparación Examen de Prácticas de Teoría de la Comunicación

## Práctica 1: Procesos Estocásticos

* PE con distribución uniforme:

-> Declaración:
```Matlab
% Nr = numero de realizaciones
% Nt = numero de tiradas por realización
% V = valor max
X_A = randi(V, Nr, Nt);  
```

-> Graficarlo:
```Matlab
figure
stem(X_A(1,:)); % PRIMERA REALIZACION
```

* Ruido Gaussiano:

-> Declaración:

```Matlab
Nr = 1000; %  Numero de realizaciones
Ts = 0.001; % Tiempo de muestreo
T = 10; % Tiempo de medición


t = 0:Ts:T; % Vector de tiempos
Nm = length(t); % Numero de medidas por medicion

% Var = varianza que queremos
ruido = sqrt(Var) * randn(Nr, Nm);
```

-> PROBLEMA EXAMEN:

```Matlab
ruido = sqrt(No/2)*randn(1, L);
```

* Histograma

-> Histograma de la realización N:

```Matlab
hist(X(N,:));
```

* Calculo de Medias

-> Media de cada realización

![Media_realizacion](https://github.com/aperona2018/TC_Practicas/blob/main/media_realizacion.png)


```Matlab
Media = zeros(1, Nr);

for nr = 1:Nr
  Media(1, nr) = mean(X(nr,:));
end

figure
subplot(1, 1, 1);
plot(Media);
```

-> Media estadística de cada instante de tiempo

![Media_instante](https://github.com/aperona2018/TC_Practicas/blob/main/media_estadistica_instantes_tiempo.png)

```Matlab
Media_estadistica = zeros(1, Nm);

for nm = 1:Nm
  Media_estadistica(1, nm) = mean(X(nm,:));
end

figure
subplot(1, 1, 1);
plot(Media_estadistica);
```

-> Media en una realizacion:

```Matlab
media_realizacion_N = mean(X(N, :));
```

-> Media en un instante de tiempo:

```Matlab
media_instante_N = mean(X(:, N));
```

* Correlacion entre dos instantes de tiempo -- DUDA: ¿Como consigo saber instantes dado un tiempo en segundos?

```Matlab
x = mean(X1(:, N1));
y = mean(X1(:, N2));

Rxy = x*y;
```

DUDA: Por que antes no me da bien pero asi si?:

```Matlab
y_n1 = Y(:, n1); % Valores en el instante n1
y_n2 = Y(:, n2); % Valores en el instante n2

% Calcular la autocorrelación entre y_n1 y y_n2
Ryy = sum(y_n1 .* y_n2) / length(y_n1);
```

## Práctica 2: PROCESOS ESTOCASTICOS Y SISTEMAS LINEALES MODULACIONES ANALOGICAS

* Autocorrelación de un proceso
```Matlab
% Nr = numero realizacion
% Nt = numero instante tiempo

rxx = xcorr(X(Nr, Nt));
```

* EXAMEN: Imágenes correlacion

-> Correlación proceso estocástico original:

![Corr_original](https://github.com/aperona2018/TC_Practicas/blob/main/corr_pe_original.png)

-> Correlación filtro:

![Corr_filtro](https://github.com/aperona2018/TC_Practicas/blob/main/corr_filtro.png)

-> Correlación proceso estocástico filtrado:

![Corr_salida](https://github.com/aperona2018/TC_Practicas/blob/main/corr_pe_filtrada.png)

* Para visualizar bien los ejes:

```Matlab
eje = linspace(-Fs/2, Fs/2, length(H));
```

* EXAMEN: Sea un proceso estacionario de duración T segundos. Se ha calculado su autocorrelación y almacenado en una variable denominada Rx. Se desea representar dicha autocorrelación usando la expresión plot(tau, Rx).
Indique la línea de código para generar el vector tau:

```Matlab
tau=linspace(T, -T, length(Rx));
```

* DEP de un filtro:

```Matlab
dep_h = H.^2;
```

* Modulaciones:

-> Modulación AM:

![Modulación AM](https://github.com/aperona2018/TC_Practicas/blob/main/mod_AM.png)

-> Modulación PM 

- Frecuencia baja
  
![PM_Frec_baja](https://github.com/aperona2018/TC_Practicas/blob/main/mod_PM_frec_peque%C3%B1a.png)

- Frecuencia alta
  
![PM_Frec_alta](https://github.com/aperona2018/TC_Practicas/blob/main/mod_PM_frec_grande.png)

-> Modulación FM

![Mod_FM](https://github.com/aperona2018/TC_Practicas/blob/main/mod_FM.png)

* EXAMEN MODULACIONES:

-> Señal original:

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_original.png)

-> Señal modulada AM

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_AM.png)

-> Señal modulada PM frecuencia baja

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_PM_frec_baja.png)

-> Señal modulada PM frecuencia alta

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_PM_frec_alta.png)

-> Señal modulada FM

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_FM.png)

-> Señal demodulada

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_Demod.png)


* DEP Y FILTROS:

-> Señal original

![](https://github.com/aperona2018/TC_Practicas/blob/main/se%C3%B1al_original.png)

-> DEP Original

![](https://github.com/aperona2018/TC_Practicas/blob/main/dep_original.png)

-> DEP Filtro

![](https://github.com/aperona2018/TC_Practicas/blob/main/dep_filtro.png)

-> DEP Filtrada

![](https://github.com/aperona2018/TC_Practicas/blob/main/dep_filtrada.png)


* EXAMEN FILTROS:

-> DEP Original

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_dep_original.png)

-> DEP Filtro

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen_dep_filtro.png)

-> DEP Filtrada

![](https://github.com/aperona2018/TC_Practicas/blob/main/dep_filtrada.png)

## Práctica 3: TRANSMISIÓN DIGITAL EN BANDA BASE

* DIAGRAMA DE OJO:

  -> Diagrama con SNR = 5 dB

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjo1.png)

  -> Diagrama con SNR = 15 dB

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjo4.png)

  -> Diagrama con SNR = 25 dB

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjo2.png)

  -> Diagrama con SNR = 35 dB

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjo3.png)

  -> Diagrama con r = 0

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjor_0.png)

  -> Diagrama con r = 1

  ![](https://github.com/aperona2018/TC_Practicas/blob/main/diagOjor_1.png)

  **¡A MAYOR R, MENOS LINEAS DISPERSAS!**

* ENERGIA DE SIMBOLO Y DE BIT

-> Energía de simbolo:

```Matlab
An = [-7, -5, -3, -1, 1, 3, 5, 7];

Es = mean(An.^2);
```

-> Energía de bit:

```Matlab
Eb = Es/k
```

* RUIDO

```Matlab
ruido=sqrt(No/2)*randn(1,L);
```

* SIMBOLOS:

```
simbolos_Tx = pammod(indices_simbolos_Tx, M);

simbolos_Rx = simbolos_Tx + ruido;

simbolos_decision = decisor_8PAM(simbolos_Rx);
```

* SER EXPERIMENTAL:

```Matlab
SER_Experimental(count)=sum((simbolos_decision ~= simbolos_Tx))/L
```

* CURVA

```Matlab
semilogy(Eb_No_dB,SER_Experimental);
```

**¡!** Con 10.000 simbolos, la curva de la SER experimental se aproxima más a la curva de la SER teórica


## EXTRAS:

* Frecuencia de muestreo: frec_muestreo = 2*frec_portadora
