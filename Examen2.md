# Pregunta 1:

figura A: autocorrelacion del filtro

figura B: autocorrelacion del proceso a la salida del filtro

figura C: no puede ser

figura D: autocorrelacion del proceso

# Pregunta 2:

**a)**

```Matlab
Rxx = mean(X(:, 10) .* X(:, 20));
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
pot = mean(abs(X.^2));
```

**e)**

Al no coincidir las medias, no es ergodico

# Pregunta 2:

f_muestreo = 10 KHz

f_muestreo = 2 * fc => fc = f_muestreo/2 = 10/2 = 5 KHz

# Pregunta 3:

¿Que modulacion es mas sensible a la hora de muestear en los instantes de tiempo adecuados?

Figura B (Tiene mas lineas)

¿Que modulacion tiene mas margen frente al ruido?

Ambas igual (Están igual de espaciadas)

¿ Que modulacion usa un coseno alzado con roll off = 0?

Figura B (Tiene mas lineas)

# Pregunta 4:

```Matlab
An = [-7, -5, -3, -1, 1, 3, 5, 7];

Es = mean(An.^2);

Eb = Es/3
```

Eb = 7 

# Pregunta 5:

```Matlab
simbolosTx = pammod(indices_simbolos_Tx, M);
```

# Pregunta 6:

```Matlab
ruido = sqrt(No/2)*randn(1, L);
```

# Pregunta 7:

```Matlab
SER_experimental(count)=sum((simbolos_decision ~= simbolos_Tx))/L;
```
