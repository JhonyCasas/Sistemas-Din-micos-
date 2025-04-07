Dinámica de Sistemas Mecánicos - Sistemas Masa-Resorte-Amortiguador

La dinámica de sistemas mecánicos permite comprender el comportamiento de cuerpos en movimiento bajo la acción de fuerzas. En esta clase se abordará un modelo clásico: el sistema masa-resorte-amortiguador, el cual es fundamental en ingeniería para representar oscilaciones, vibraciones y amortiguación en estructuras, vehículos, maquinaria y más. Se estudiarán los principios físicos que rigen su funcionamiento como la ley de Hooke, la fricción viscosa y las leyes de Newton. Este análisis permite construir modelos matemáticos que describen con precisión su comportamiento.

## 1. Introducción a los Sistemas Masa-Resorte-Amortiguador

En esta sección se presenta el concepto general del sistema masa-resorte-amortiguador y se discute su utilidad en el modelado de fenómenos físicos como vibraciones y amortiguación.

## 2. Definiciones

>🔑 *Ley de Hooke:* principio físico que establece que la fuerza ejercida por un resorte es proporcional a su elongación, es decir, \( F = -kx \), donde \( k \) es la constante del resorte y \( x \) el desplazamiento respecto a la posición de equilibrio.

>🔑 *Fricción viscosa:* tipo de fricción que se opone al movimiento y es proporcional a la velocidad. Se modela como $\( F = -b \dot{x} \)$, donde \( b \) es el coeficiente de amortiguamiento y \( \dot{x} \) la velocidad.

>🔑 *Segunda Ley de Newton:* ley fundamental de la dinámica que indica que la fuerza neta aplicada a un cuerpo es igual al producto de su masa por su aceleración: \( F = ma \).

## 3. Modelado de Sistemas Dinámicos

### 3.1. Sistema de un solo grado de libertad (1DOF)

Un sistema masa-resorte-amortiguador de un grado de libertad se representa con una sola masa unida a un resorte y un amortiguador.

### 3.2. Sistema de dos grados de libertad (2DOF)

En este caso se modela un sistema con dos masas conectadas mediante resortes y amortiguadores, como se muestra a continuación.

## 4. Ejemplos

💡**Ejemplo 1:** Modelado de un sistema masa-resorte-amortiguador de dos grados de libertad

Se tiene el siguiente sistema:

- \( m_1, m_2 \): masas
- \( k_1, k_2 \): constantes de los resortes
- \( b \): coeficiente de fricción viscosa
- \( x_1(t), x_2(t) \): desplazamientos verticales de las masas

Aplicando la segunda ley de Newton:

**Para \( m_1 \):**

$$
m_1 \ddot{x}_1 = -k_1 x_1 - b \dot{x}_1 - k_2(x_1 - x_2)
$$

**Para \( m_2 \):**

$$
m_2 \ddot{x}_2 = -k_2(x_2 - x_1)
$$

## 5. Ecuaciones

El sistema de ecuaciones diferenciales que rige el comportamiento es:

$$
\begin{cases}
m_1 \ddot{x}_1 + b \dot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0 \\
m_2 \ddot{x}_2 + k_2 x_2 - k_2 x_1 = 0
\end{cases}
$$

# 📚Ejercicio: Absorbedor de vibraciones dinámico

**Descripción:**  
Se tiene un sistema mecánico con un absorbedor de vibraciones dinámico, como se muestra en la figura. El sistema está compuesto por una masa principal $m$ unida a un resorte $k$ y un amortiguador $b$, y una masa secundaria $m_a$ unida mediante un resorte $k_a$. El sistema es excitado por una fuerza armónica $P \sin(\omega t)$.

**Ecuaciones del sistema:**

\[
m \ddot{x}_1 + b \dot{x}_1 + k x_1 + k_a (x_1 - x_2) = P \sin(\omega t)
\]
\[
m_a \ddot{x}_2 + k_a (x_2 - x_1) = 0
\]

**Valores numéricos:**

- $m = 1\,kg$, $m_a = 0.5\,kg$
- $b = 5\,\text{N·s/m}$
- $k = 500\,\text{N/m}$, $k_a = 200\,\text{N/m}$
- $P = 20\,\text{N}$, $\omega = 20\,\text{rad/s}$

**Ecuaciones con valores sustituidos:**

\[
\ddot{x}_1 + 5\dot{x}_1 + 500x_1 + 200(x_1 - x_2) = 20 \sin(20t)
\]
\[
0.5 \ddot{x}_2 + 200(x_2 - x_1) = 0
\]

**Cambio de escala de tiempo:**  
Usando $\tau = 10t$

\[
\frac{d^2x_1}{d\tau^2} + 0.5\frac{dx_1}{d\tau} + 5x_1 + 2(x_1 - x_2) = 0.2 \sin(2\tau)
\]
\[
\frac{d^2x_2}{d\tau^2} + 4(x_2 - x_1) = 0
\]

**Cambio de variables:**  
$y_1 = 100x_1$, $y_2 = 100x_2$

\[
\frac{d^2y_1}{d\tau^2} + 0.5\frac{dy_1}{d\tau} + 5y_1 + 2(y_1 - y_2) = 20 \sin(2\tau)
\]
\[
\frac{d^2y_2}{d\tau^2} + 4(y_2 - y_1) = 0
\]

**Objetivo:**  
Simular este sistema y observar el efecto del absorbedor de vibraciones sobre la masa principal cuando la fuerza externa actúa a la frecuencia de resonancia.

![Sistema con absorbedor de vibraciones](images/absorbedor_vibraciones.png)

## 6. Figuras

💡**Ejemplo 2:**

![Sistema masa-resorte-amortiguador 2DOF](images/sistema_2dof.png)

Figura 1. Sistema masa-resorte-amortiguador con dos grados de libertad

## 7. Tablas

💡**Ejemplo 3:** Parámetros de un sistema masa-resorte

| Parámetro | Símbolo | Unidades | Descripción                      |
|-----------|---------|----------|----------------------------------|
| Masa 1    | \( m_1 \) | kg       | Masa superior del sistema        |
| Masa 2    | \( m_2 \) | kg       | Masa inferior del sistema        |
| Resorte 1 | \( k_1 \) | N/m      | Resorte entre techo y \( m_1 \)  |
| Resorte 2 | \( k_2 \) | N/m      | Resorte entre \( m_1 \) y \( m_2 \) |
| Amortiguador | \( b \) | Ns/m    | Amortiguador viscoso             |

Tabla 1. Parámetros del sistema masa-resorte-amortiguador

## 8. Código

💡**Ejemplo 4:**
```matlab
% Resolución de sistema 2DOF en MATLAB
syms x1(t) x2(t) m1 m2 k1 k2 b

eq1 = m1*diff(x1,2) + b*diff(x1) + (k1 + k2)*x1 - k2*x2 == 0;
eq2 = m2*diff(x2,2) + k2*x2 - k2*x1 == 0;

odes = [eq1; eq2];
