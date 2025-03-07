# Expansión en Fracciones Parciales con Raíces Reales Iguales

Este repositorio está dedicado al estudio de la **expansión en fracciones parciales** cuando el denominador tiene **raíces reales iguales** (factores repetidos). Esta técnica es fundamental en matemáticas aplicadas, ingeniería y ciencias, ya que permite descomponer fracciones algebraicas complejas en fracciones más simples.

---

## 1. Introducción

La expansión en fracciones parciales es una técnica que permite descomponer una fracción algebraica en una suma de fracciones más simples. Cuando el denominador tiene **factores repetidos**, la expansión incluye términos adicionales para cada potencia del factor repetido. Este método es especialmente útil en el análisis de sistemas dinámicos, control automático y procesamiento de señales.

---

## 2. Definiciones

>🔑 *Fracción Parcial:* Una fracción parcial es una fracción algebraica más simple que se obtiene al descomponer una fracción compleja en una suma de fracciones con denominadores más simples.

>🔑 *Raíces Reales Iguales:* Cuando un polinomio tiene factores repetidos, se dice que tiene raíces reales iguales. Por ejemplo, \( (s + 1)^2 \) tiene una raíz real igual en \( s = -1 \).

>🔑 *Expansión en Fracciones Parciales con Factores Repetidos:* Es el proceso de descomponer una fracción algebraica en una suma de fracciones parciales, incluyendo términos adicionales para cada potencia del factor repetido.

---

## 3. Métodos de Expansión

Cuando el denominador tiene factores repetidos, la expansión en fracciones parciales sigue la forma:
$$
\frac{P(s)}{(s - a)^m Q(s)} = \frac{A_1}{s - a} + \frac{A_2}{(s - a)^2} + \dots + \frac{A_m}{(s - a)^m} + \text{(términos para otros factores)}
$$

### 3.1. Pasos para la Expansión
1. **Identificar los factores repetidos** en el denominador.
2. **Escribir la expansión** incluyendo un término para cada potencia del factor repetido.
3. **Multiplicar ambos lados** por el denominador común para eliminar las fracciones.
4. **Resolver para las constantes** \( A_1, A_2, \dots, A_m \) utilizando valores convenientes de \( s \) o igualando coeficientes.

---

## 4. Ejemplo Resuelto

### 4.1. Problema
Descomponer la siguiente fracción en fracciones parciales:
$$
F(s) = \frac{3s^2 + 5s + 2}{(s + 1)^2 (s + 2)}
$$

### 4.2. Solución
1. **Expansión en fracciones parciales**:
   $$
   \frac{3s^2 + 5s + 2}{(s + 1)^2 (s + 2)} = \frac{A}{s + 1} + \frac{B}{(s + 1)^2} + \frac{C}{s + 2}
   $$

2. **Multiplicar ambos lados por el denominador común**:
   $$
   3s^2 + 5s + 2 = A(s + 1)(s + 2) + B(s + 2) + C(s + 1)^2
   $$

3. **Resolver para \( A \), \( B \) y \( C \)**:
   - Para \( s = -1 \):
     $$
     3(-1)^2 + 5(-1) + 2 = A(-1 + 1)(-1 + 2) + B(-1 + 2) + C(-1 + 1)^2 \\
     3 - 5 + 2 = A(0)(1) + B(1) + C(0) \\
     0 = B \\
     B = 0
     $$
   - Para \( s = -2 \):
     $$
     3(-2)^2 + 5(-2) + 2 = A(-2 + 1)(-2 + 2) + B(-2 + 2) + C(-2 + 1)^2 \\
     12 - 10 + 2 = A(-1)(0) + B(0) + C(1) \\
     4 = C \\
     C = 4
     $$
   - Para \( s = 0 \):
     $$
     3(0)^2 + 5(0) + 2 = A(0 + 1)(0 + 2) + B(0 + 2) + C(0 + 1)^2 \\
     2 = 2A + 2B + C \\
     Sustituyendo \( B = 0 \) y \( C = 4 \):
     2 = 2A + 0 + 4 \\
     2A = -2 \\
     A = -1
     $$

4. **Expresión en fracciones parciales**:
   $$
   F(s) = \frac{-1}{s + 1} + \frac{0}{(s + 1)^2} + \frac{4}{s + 2}
   $$

5. **Transformada inversa de Laplace**:
   $$
   f(t) = -e^{-t} + 4e^{-2t}
   $$

---

## 5. Ejercicios

📚**Ejercicio 1:** Descomponer la siguiente fracción en fracciones parciales y encontrar su transformada inversa de Laplace:
$$
F(s) = \frac{2s^2 + 3s + 1}{(s + 2)^2 (s + 3)}
$$

**Solución:**
1. Expansión en fracciones parciales:
   $$
   \frac{2s^2 + 3s + 1}{(s + 2)^2 (s + 3)} = \frac{A}{s + 2} + \frac{B}{(s + 2)^2} + \frac{C}{s + 3}
   $$
2. Multiplicar ambos lados por el denominador común:
   $$
   2s^2 + 3s + 1 = A(s + 2)(s + 3) + B(s + 3) + C(s + 2)^2
   $$
3. Resolver para \( A \), \( B \) y \( C \):
   - Para \( s = -2 \):
     $$
     2(-2)^2 + 3(-2) + 1 = A(-2 + 2)(-2 + 3) + B(-2 + 3) + C(-2 + 2)^2 \\
     8 - 6 + 1 = A(0)(1) + B(1) + C(0) \\
     3 = B \\
     B = 3
     $$
   - Para \( s = -3 \):
     $$
     2(-3)^2 + 3(-3) + 1 = A(-3 + 2)(-3 + 3) + B(-3 + 3) + C(-3 + 2)^2 \\
     18 - 9 + 1 = A(-1)(0) + B(0) + C(1) \\
     10 = C \\
     C = 10
     $$
   - Para \( s = 0 \):
     $$
     2(0)^2 + 3(0) + 1 = A(0 + 2)(0 + 3) + B(0 + 3) + C(0 + 2)^2 \\
     1 = 6A + 3B + 4C \\
     Sustituyendo \( B = 3 \) y \( C = 10 \):
     1 = 6A + 9 + 40 \\
     6A = -48 \\
     A = -8
     $$
4. Expresión en fracciones parciales:
   $$
   F(s) = \frac{-8}{s + 2} + \frac{3}{(s + 2)^2} + \frac{10}{s + 3}
   $$
5. Transformada inversa de Laplace:
   $$
   f(t) = -8e^{-2t} + 3te^{-2t} + 10e^{-3t}
   $$

---

## 6. Conclusiones

La **expansión en fracciones parciales con raíces reales iguales** es una técnica esencial en matemáticas aplicadas, ingeniería y ciencias. Permite descomponer fracciones algebraicas complejas en fracciones más simples, lo que facilita su manipulación, integración y análisis. A través de este repositorio, hemos explorado:
- Los **métodos de expansión** para factores repetidos.
- **Ejemplos prácticos** que ilustran cómo aplicar la técnica.
- **Ejercicios resueltos** que refuerzan el aprendizaje.

Esta herramienta es fundamental en áreas como el control automático, el procesamiento de señales y la resolución de ecuaciones diferenciales. Dominar la expansión de fracciones parciales es clave para avanzar en el estudio de sistemas dinámicos y otras disciplinas técnicas.

---

## 7. Referencias

- [1] **"Matemáticas para Ingeniería"**, Autor: James Stewart.  
- [2] **MATLAB Documentation**: [https://www.mathworks.com/help/symbolic/partial-fraction-decomposition.html](https://www.mathworks.com/help/symbolic/partial-fraction-decomposition.html)  

---

Este repositorio proporciona una guía completa para entender y aplicar la expansión de fracciones parciales con raíces reales iguales. ¡Esperamos que sea de gran ayuda en tu aprendizaje! 😊
