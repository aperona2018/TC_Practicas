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
