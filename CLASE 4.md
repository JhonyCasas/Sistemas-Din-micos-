# Expansión en Fracciones Parciales con Factores Cuadráticos Irreducibles

Este repositorio está dedicado al estudio de la **expansión en fracciones parciales** cuando el denominador tiene **factores cuadráticos irreducibles** (que no se pueden factorizar en factores lineales reales). Estos factores requieren el uso de la **fórmula cuadrática** para determinar si son irreducibles. Esta técnica es fundamental en matemáticas aplicadas, ingeniería y ciencias, ya que permite descomponer fracciones algebraicas complejas en fracciones más simples, facilitando su integración, diferenciación o análisis.

---

## 1. Introducción

La expansión en fracciones parciales es una técnica que permite descomponer una fracción algebraica en una suma de fracciones más simples. Cuando el denominador tiene **factores cuadráticos irreducibles**, la expansión incluye términos con numeradores lineales. Este método es especialmente útil en el análisis de sistemas dinámicos, control automático y procesamiento de señales.

---

## 2. Definiciones

>🔑 *Fracción Parcial:* Una fracción parcial es una fracción algebraica más simple que se obtiene al descomponer una fracción compleja en una suma de fracciones con denominadores más simples.

>🔑 *Factor Cuadrático Irreducible:* Un polinomio cuadrático que no se puede factorizar en factores lineales reales. Por ejemplo, \( s^2 + 4s + 5 \) es irreducible porque su discriminante es negativo (\( b^2 - 4ac = 16 - 20 = -4 \)).

>🔑 *Fórmula Cuadrática:* La fórmula general para resolver una ecuación cuadrática \( as^2 + bs + c = 0 \) es:
$$
s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$
Si el discriminante \( b^2 - 4ac \) es negativo, el polinomio es irreducible en los números reales.

---

## 3. Uso de la Fórmula Cuadrática

La **fórmula cuadrática** se utiliza para determinar si un polinomio cuadrático es irreducible. Si el discriminante \( b^2 - 4ac \) es negativo, el polinomio no se puede factorizar en factores lineales reales y se considera irreducible.

### 3.1. Pasos para Aplicar la Fórmula Cuadrática
1. Identificar los coeficientes \( a \), \( b \) y \( c \) en el polinomio cuadrático \( as^2 + bs + c \).
2. Calcular el discriminante \( \Delta = b^2 - 4ac \).
3. Evaluar el discriminante:
   - Si \( \Delta > 0 \): El polinomio tiene dos raíces reales distintas y se puede factorizar.
   - Si \( \Delta = 0 \): El polinomio tiene una raíz real repetida y se puede factorizar.
   - Si \( \Delta < 0 \): El polinomio es irreducible en los números reales.

### 3.2. Ejemplo de Aplicación
Consideremos el polinomio cuadrático \( s^2 + 4s + 5 \):
1. Identificamos los coeficientes:
   - \( a = 1 \)
   - \( b = 4 \)
   - \( c = 5 \)
2. Calculamos el discriminante:

   $$\Delta = b^2 - 4ac = 4^2 - 4(1)(5) = 16 - 20 = -4$$
   
4. Como \( \Delta < 0 \), el polinomio es irreducible.

---

## 4. Métodos de Expansión

Cuando el denominador tiene factores cuadráticos irreducibles, la expansión en fracciones parciales sigue la forma:

$$\frac{P(s)}{(s^2 + as + b) Q(s)} = \frac{As + B}{s^2 + as + b} + \text{(términos para otros factores)}$$

### 4.1. Pasos para la Expansión
1. **Identificar los factores cuadráticos irreducibles** en el denominador.
2. **Escribir la expansión** incluyendo un término con numerador lineal para cada factor cuadrático.
3. **Multiplicar ambos lados** por el denominador común para eliminar las fracciones.
4. **Resolver para las constantes** \( A \) y \( B \) utilizando valores convenientes de \( s \) o igualando coeficientes.

---

## 5. Ejemplo Resuelto

### 5.1. Problema
Descomponer la siguiente fracción en fracciones parciales:

$$F(s) = \frac{2s^2 + 3s + 4}{(s^2 + 2s + 5)(s + 1)}$$

### 5.2. Solución
1. **Identificar el factor cuadrático irreducible**:
   El denominador \( s^2 + 2s + 5 \) es irreducible porque su discriminante es negativo (\( b^2 - 4ac = 4 - 20 = -16 \)).

2. **Expansión en fracciones parciales**:
3. 
   $$\frac{2s^2 + 3s + 4}{(s^2 + 2s + 5)(s + 1)} = \frac{As + B}{s^2 + 2s + 5} + \frac{C}{s + 1}$$

4. **Multiplicar ambos lados por el denominador común**:

   $$2s^2 + 3s + 4 = (As + B)(s + 1) + C(s^2 + 2s + 5)$$

5. **Resolver para \( A \), \( B \) y \( C \)**:
   - Para \( s = -1 \):
   - 
     $$2(-1)^2 + 3(-1) + 4 = (A(-1) + B)(-1 + 1) + C((-1)^2 + 2(-1) + 5) \\
     2 - 3 + 4 = ( -A + B )(0) + C(1 - 2 + 5) \\
     3 = 4C \\
     C = \frac{3}{4}$$
   - Para \( s = 0 \):
   - 
     $$2(0)^2 + 3(0) + 4 = (A(0) + B)(0 + 1) + C(0^2 + 2(0) + 5) \\
     4 = B + 5C \\
     Sustituyendo \( C = \frac{3}{4} \):
     4 = B + 5\left(\frac{3}{4}\right) \\
     4 = B + \frac{15}{4} \\
     B = 4 - \frac{15}{4} = \frac{1}{4}$$
     
   - Para \( s = 1 \):

     $$2(1)^2 + 3(1) + 4 = (A(1) + B)(1 + 1) + C(1^2 + 2(1) + 5) \\
     2 + 3 + 4 = (A + B)(2) + C(8) \\
     9 = 2A + 2B + 8C \\
     Sustituyendo \( B = \frac{1}{4} \) y \( C = \frac{3}{4} \):
     9 = 2A + 2\left(\frac{1}{4}\right) + 8\left(\frac{3}{4}\right) \\
     9 = 2A + \frac{1}{2} + 6 \\
     2A = 9 - 6 - \frac{1}{2} = \frac{5}{2} \\
     A = \frac{5}{4}$$

6. **Expresión en fracciones parciales**:
   $$
   F(s) = \frac{\frac{5}{4}s + \frac{1}{4}}{s^2 + 2s + 5} + \frac{\frac{3}{4}}{s + 1}
   $$

7. **Transformada inversa de Laplace**:
   - Para \( \frac{\frac{5}{4}s + \frac{1}{4}}{s^2 + 2s + 5} \):
     Completamos el cuadrado en el denominador:
     $$
     s^2 + 2s + 5 = (s + 1)^2 + 4
     $$
     Luego, aplicamos la transformada inversa:
     $$
     \mathcal{L}^{-1}\left\{\frac{\frac{5}{4}s + \frac{1}{4}}{(s + 1)^2 + 4}\right\} = \frac{5}{4}e^{-t}\cos(2t) + \frac{1}{4}e^{-t}\sin(2t)
     $$
   - Para \( \frac{\frac{3}{4}}{s + 1} \):
     $$
     \mathcal{L}^{-1}\left\{\frac{\frac{3}{4}}{s + 1}\right\} = \frac{3}{4}e^{-t}
     $$

8. **Solución final**:

   $$f(t) = \frac{5}{4}e^{-t}\cos(2t) + \frac{1}{4}e^{-t}\sin(2t) + \frac{3}{4}e^{-t}$$

---

## 9. Ejercicios

📚**Ejercicio 1:** 
$$F(s) = \frac{3s^2 + 4s + 5}{(s^2 + 4s + 13)(s + 2)}$$

**Solución:** $$\[f(t) = e^{-2t}\left(2\cos(3t) - \frac{8}{3}\sin(3t) + 1\right)\]$$

   $$
   \frac{3s^2 + 4s + 5}{(s^2 + 4s + 13)(s + 2)} = \frac{As + B}{s^2 + 4s + 13} + \frac{C}{s + 2}
   $$

   $$
   3s^2 + 4s + 5 = (As + B)(s + 2) + C(s^2 + 4s + 13)
   $$

   - Para \( s = -2 \):
     $$
     3(-2)^2 + 4(-2) + 5 = (A(-2) + B)(-2 + 2) + C((-2)^2 + 4(-2) + 13) \\
     12 - 8 + 5 = ( -2A + B )(0) + C(4 - 8 + 13) \\
     9 = 9C \\
     C = 1
     $$
   - Para \( s = 0 \):
     $$
     3(0)^2 + 4(0) + 5 = (A(0) + B)(0 + 2) + C(0^2 + 4(0) + 13) \\
     5 = 2B + 13C \\
     Sustituyendo \( C = 1 \):
     5 = 2B + 13 \\
     2B = -8 \\
     B = -4
     $$
   - Para \( s = 1 \):
   - $$3(1)^2 + 4(1) + 5 = (A(1) + B)(1 + 2) + C(1^2 + 4(1) + 13) \\3 + 4 + 5 = (A + B)(3) + C(18) \\12 = 3A + 3B + 18C \\ Sustituyendo \( B = -4 \) y \( C = 1 \):12 = 3A + 3(-4) + 18(1) \\12 = 3A - 12 + 18 \\3A = 12 + 12 - 18 = 6 \\A = 2$$

## 10.Conclusiones
La fórmula cuadrática es una herramienta fundamental en matemáticas y ciencias aplicadas debido a su capacidad para resolver ecuaciones de segundo grado
