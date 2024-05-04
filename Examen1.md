# Pregunta 1:

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen1_1.png)

Figura A: Autocorrelacion del filtro

Figura B: Autocorrelacion del proceso al salir del filtro

Figura C: No existe

Figura D: Autocorrelacion del proceso

# Pregunta 2:

**a)**

```Matlab
Rx = mean(X(:, 10).*X(:, 20));
```

**b)**

```Matlab
media = mean(X(1,:));
```

**c)**

```Matlab
media = mean(X(:, 50));
```

**d)**

```Matlab
potencia = mean(abs(X.^2));
```

**e)**

Como la media estadistica no es igual a la media de la realizacion, no es ergodigo

# Pregunta 2

```Matlab
tau=linspace(-T, T, length(Rx));
```

# Pregunta 3

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen1_3.png)

Figura A: Mod AM

Figura B: Mod PM frec baja

Figura C: Mod FM

Figura D: demod + ruido

Figura E: Mod PM frec alta

Figura F: Señal original

# Pregunta 4: 

```Matlab
semilogy(Eb_No_dB, SER_Experimental);
```

# Pregunta 5:

BER = SER/K => SER = K * BER = 4 * 0.012 = 0.048

# Pregunta 6:

```Matlab
media = mean(X(:, 3));
```

# Pregunta 7:

![](https://github.com/aperona2018/TC_Practicas/blob/main/examen1_7.png)

Figura A: 10 dB

Figura B: 30 dB

Figura C: 20 dB

Figura D: 5 db

# Pregunta 8:

```Matlab
Nr = 100;
Nt = 1000;
X_1 = randn(Nr,Nt);
X_2 = 5*randn(Nr,Nt);

%% Media de realizaciones

media1 = zeros(1, Nr);

for nr = 1:Nr

    media1(1, nr) = mean(X_1(nr, :));

end

media2 = zeros(1, Nr);

for nr = 1:Nr
    media2(1, nr) = mean(X_2(nr, :));
end

figure
subplot(2,1,1);
plot(media1)
title("X_1 realizacion")
subplot(2, 1, 2);
plot(media2)
title("X_2 realizacion")

%% Media temporal estadística

est1 = zeros(1, Nt);

for nt = 1: Nt
    est1(1, nt) = mean(X_1(:, nt));
end

est2 = zeros(1, Nt);

for nt = 1:Nt
    est2(1, nt) = mean(X_2(:, nt));
end

figure
subplot(2, 1, 1)
plot(est1)
title("X_1 estadistica")
subplot(2, 1, 2)
plot(est2)
title("X_2 estadistica")
```

figura A: realizacion de X_2

figura B: realizacion de X_1

figura C: estadistica de X_1

figura D: estadistica de X_2

# Pregunta 9: 

```Matlab
Rxx = mean(X(:,10).*X(:, 200));
```
