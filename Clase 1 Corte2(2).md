# Solución de Ecuaciones Diferenciales por el Método de Laplace

El método de Laplace es una técnica poderosa para resolver ecuaciones diferenciales lineales. Transforma ecuaciones diferenciales en ecuaciones algebraicas en el dominio de Laplace, simplificando su resolución. Este repositorio explica la metodología paso a paso, con ejemplos y ejercicios prácticos.

---

## 1. Introducción al Método de Laplace

>🔑 *Transformada de Laplace:* Una transformada integral que convierte una función del tiempo $\( f(t) \)$ en una función de una variable compleja $\( s \)$, definida como:
$F(s) = {L}\{f(t)\} = \int_0^\infty f(t)e^{-st}dt$

El método de Laplace es especialmente útil para resolver ecuaciones diferenciales con condiciones iniciales.

---

## 2. Metodología de Solución

### 2.1. Pasos Básicos
1. **Aplicar la Transformada de Laplace** a ambos lados de la ecuación diferencial.
2. **Despejar la variable de salida** en el dominio de Laplace.
3. **Aplicar la Transformada Inversa de Laplace** para obtener la solución en el dominio del tiempo.

### 2.2. Detalle de Cada Paso

#### 2.2.1. Aplicar la Transformada de Laplace
Transformamos cada término de la ecuación diferencial usando las propiedades de la Transformada de Laplace.

💡**Ejemplo 1:** Para la ecuación $\( \frac{dy}{dt} + 2y = e^{-t} \)$ con $\( y(0) = 1 \)$:

${L}{\frac{dy}{dt}} + 2{L}\{y\} = {L}\{e^{-t}\} $

$sY(s) - y(0) + 2Y(s) = \frac{1}{s+1}$

#### 2.2.2. Despejar la Variable de Salida
Resolvemos la ecuación algebraica resultante para \( Y(s) \).

Continuando con el ejemplo:
$Y(s)(s + 2) = \frac{1}{s+1} + 1$

$Y(s) = \frac{s + 2}{(s+1)(s+2)} = \frac{1}{s+1}$

#### 2.2.3. Aplicar la Transformada Inversa
Finalmente, aplicamos la transformada inversa para obtener $\( y(t) \).$

Para el ejemplo:
$y(t) = {L}^{-1}{\frac{1}{s+1}} = e^{-t}$

---

## 3. Ejemplos Resueltos

### 3.1. Ecuación de Primer Orden
💡**Ejemplo 2:** Resolver $\( y' + 3y = 0 \)$ con $\( y(0) = 2 \).$

**Solución:**
1. Aplicar Laplace:
$sY(s) - 2 + 3Y(s) = 0$
2. Despejar \( Y(s) \):
$Y(s) = \frac{2}{s+3}$
3. Transformada inversa:
$y(t) = 2e^{-3t}$

### 3.2. Ecuación de Segundo Orden
💡**Ejemplo 3:** Resolver $\( y'' + 4y' + 4y = 0 \)$ con $\( y(0) = 1, y'(0) = 0 \).$

**Solución:**
1. Aplicar Laplace:
$s^2Y(s) - s + 4sY(s) - 4 + 4Y(s) = 0$
2. Despejar $\( Y(s) \):$
$Y(s) = \frac{s + 4}{s^2 + 4s + 4} = \frac{s + 4}{(s + 2)^2} $
3. Transformada inversa:
$y(t) = e^{-2t}(1 + 2t)$

---

## 4. Ejercicios

📚 **Ejercicio 1:** Resolver la ecuación diferencial $\( y' + 5y = 3 \)$ con $\( y(0) = 0 \)$.

**Solución:** $y(t) = \frac{3}{5}(1 - e^{-5t})$


$\[\mathcal{L}\{y' + 5y\} = \mathcal{L}\{3\}\]$

$sY(s) - y(0) + 5Y(s) = \frac{3}{s}$
  
$sY(s) + 5Y(s) = \frac{3}{s}$

$Y(s)(s + 5) = \frac{3}{s}$
   
$Y(s) = \frac{3}{s(s + 5)}$


$\frac{3}{s(s + 5)} = \frac{A}{s} + \frac{B}{s + 5}$

$3 = A(s + 5) + Bs$
  
$Y(s) = \frac{3/5}{s} - \frac{3/5}{s + 5}$

$y(t) = \frac{3}{5}\mathcal{L}^{-1}{\frac{1}{s}} - \frac{3}{5}\mathcal{L}^{-1}{\frac{1}{s + 5}}$

$y(t) = \frac{3}{5}(1 - e^{-5t})$

📚 **Ejercicio 2:** Resolver $\( y'' + y = \sin(t) \)$ con $\( y(0) = 0, y'(0) = 1$.

**Solución:**   $y(t) = \frac{3\sin(t) - t\cos(t)}{2}$

   
   $\mathcal{L}\{y'' + y\} = \mathcal{L}\{\sin(t)\}$
   
   $s^2Y(s) - sy(0) - y'(0) + Y(s) = \frac{1}{s^2 + 1}$
   
   $y(0) = 0 \) y \( y'(0) = 1 \)$:
   
   $s^2Y(s) - 1 + Y(s) = \frac{1}{s^2 + 1}$
  
   $Y(s)(s^2 + 1) = 1 + \frac{1}{s^2 + 1}$
   
   $Y(s) = \frac{1}{s^2 + 1} + \frac{1}{(s^2 + 1)^2}$

   $Y(s) = \frac{s^2 + 2}{(s^2 + 1)^2}$

   $\mathcal{L}^{-1}{\frac{1}{s^2 + 1}} = \sin(t)$
     
   $\mathcal{L}^{-1}{\frac{1}{(s^2 + 1)^2}} = \frac{\sin(t) - t\cos(t)}{2}$
   
   $y(t) = \sin(t) + \frac{\sin(t) - t\cos(t)}{2}$
     
   $y(t) = \frac{2\sin(t) + \sin(t) - t\cos(t)}{2}$
     
   $y(t) = \frac{3\sin(t) - t\cos(t)}{2}\$


 📚 **Ejercicio 3:** Resolver la ecuación diferencial $\( x'' + 2x' + 5x = 3 \)$ con $\( x(0) = a \)$ y $\( x'(0) = b \)$.

**Solucion**  $x(t) = \frac{3}{5} - \frac{3}{5}e^{-t}\cos(2t) - \frac{3}{10}e^{-t}\sin(2t)\$

$\[{L}\{x''\} + 2{L}\{x'\} + 5{L}\{x\} = {L}\{3\}\]$

$[s^2 X(s) - s x(0) - x'(0)] + 2[s X(s) - x(0)] + 5X(s) = \frac{3}{s}\

$s^2 X(s) - s a - b + 2s X(s) - 2a + 5X(s) = \frac{3}{s}$

$X(s)(s^2 + 2s + 5) = \frac{3}{s}$

$X(s) = \frac{A}{s} + \frac{B s + C}{s^2 + 2s +5}$

$s^2 + 2s + 5 = 0 \implies s = \frac{-2 \pm \sqrt{4 - 20}}{2} = -1 \pm 2i$

$\\frac{3}{s(s^2 + 2s + 5)} = \frac{A}{s} + \frac{Bs + C}{s^2 + 2s + 5}\$

$3 = A(s^2 + 2s + 5) + (Bs + C)s\$

$3 = A(s^2 + 2s + 5) + Bs^2 + Cs\$

$3 = As^2 + 2As + 5A + Bs^2 + Cs\$

$3 = (A + B)s^2 + (2A + C)s + 5A\$

$A = \frac{3}{5}, \quad B = -A = -\frac{3}{5}, \quad C = -2A = -\frac{6}{5}\$

$\\frac{3}{s(s^2 + 2s + 5)} = \frac{3}{5s} + \frac{-\frac{3}{5}s - \frac{6}{5}}{s^2 + 2s + 5}\$

$\\mathcal{L}^{-1}{ \frac{3}{5s}} = \frac{3}{5}\$

$\\frac{-\frac{3}{5}s - \frac{6}{5}}{s^2 + 2s + 5} = \frac{-\frac{3}{5}(s + 1) - \frac{3}{5}}{(s + 1)^2 + 2^2}\$

$\= \frac{-\frac{3}{5}(s + 1)}{(s + 1)^2 + 4} - \frac{3}{10} \cdot \frac{2}{(s + 1)^2 + 4}\$

$\\mathcal{L}^{-1}{ \frac{s + a}{(s + a)^2 + b^2}} = e^{-at}\cos(bt)\$

$\\mathcal{L}^{-1}{ \frac{b}{(s + a)^2 + b^2}} = e^{-at}\sin(bt)\$

$\\mathcal{L}^{-1}{ \frac{-\frac{3}{5}(s + 1)}{(s + 1)^2 + 4}} = -\frac{3}{5}e^{-t}\cos(2t)\$

$\\mathcal{L}^{-1}{ \frac{-\frac{3}{10} \cdot 2}{(s + 1)^2 + 4}} = -\frac{3}{10}e^{-t}\sin(2t)$

$x(t) = \frac{3}{5} - \frac{3}{5}e^{-t}\cos(2t) - \frac{3}{10}e^{-t}\sin(2t)\$

---

## 5. Tablas

### 5.1. Tabla de Transformadas Comunes

| **Función \( f(t) \)** | **Transformada \( F(s) \)** |
|------------------------|-----------------------------|
| $\( 1 \)$                | $\( \frac{1}{s} \)$           |
| $\( e^{at} \)$           | $\( \frac{1}{s - a} \)$       |
| $\( \sin(at) \)$         | $\( \frac{a}{s^2 + a^2} \)$   |
| $\( \cos(at) \)$         | $\( \frac{s}{s^2 + a^2} \)$   |

Tabla 1. Transformadas de Laplace comunes.

## 5.2 Tabla de Transformadas de Derivadas

| **Derivada en el tiempo**       | **Transformada en $\( s \)$**                     | **Condiciones iniciales**              |
|----------------------------------|-----------------------------------------------|----------------------------------------|
| $\( \mathcal{L}\{x(t)\} \)$        | $\( X(s) \)$                                    | -                                      |
| $\( \mathcal{L}\{\dot{x}(t)\} \)$  | $\( sX(s) - x(0) \)$                            | $\( x(0) = \text{valor inicial} \)$      |
| $\( \mathcal{L}\{\ddot{x}(t)\} \)$ | $\( s^2X(s) - sx(0) - \dot{x}(0) \)$            | $\( x(0), \dot{x}(0) \)$                 |
| $\( \mathcal{L}\{x^{(n)}(t)\} \)$  | $\( s^nX(s) - \sum_{k=1}^{n} s^{n-k}x^{(k-1)}(0) \)$ | $\( x(0), \dot{x}(0), \dots, x^{(n-1)}(0) \)$ |

Tabla 2. Trasformadas de Laplace en las derivadas.

### 5.2.1 Notas:
1. $\( \dot{x}(t)$ = $\frac{dx}{dt} \)$, $\( \ddot{x}(t) = \frac{d^2x}{dt^2} \),$ etc.
2. Las condiciones iniciales se aplican en $\( t = 0 \)$.
3. Para derivadas de orden superior, se restan términos con las derivadas evaluadas en $\( t=0 \)$.

💡 **Ejemplo:**  
Para $\( \dddot{x} + 2\ddot{x} + 3\dot{x} = e^{-t} \)$, la transformada sería:  
$$
$s^3X(s) - s^2x(0) - s\dot{x}(0) - \ddot{x}(0) + 2[s^2X(s) - sx(0) - \dot{x}(0)] + 3[sX(s) - x(0)] = \frac{1}{s+1}
$

### 5.2. Código MATLAB para Transformada de Laplace

```matlab
syms t s
f = exp(-2*t);
F = laplace(f, t, s);
disp(F);

```

## 6. Conclusiones

- El método de Laplace transforma ecuaciones diferenciales en ecuaciones algebraicas, facilitando su resolución.
- Es especialmente útil para ecuaciones lineales con coeficientes constantes y condiciones iniciales.
- La transformada inversa permite recuperar la solución en el dominio del tiempo.

----
## 7. Referencias

Ogata, K. (1978). DINAMICA DE SISTEMAS. Prentice.

Zill, D. (2018). Ecuaciones Diferenciales con Aplicaciones. Cengage.
