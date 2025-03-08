# Solución de Fracciones Parciales por Anuladores

Este repositorio está dedicado al estudio de la **solución de fracciones parciales utilizando anuladores**. Los anuladores son operadores que permiten eliminar términos específicos en una ecuación diferencial, facilitando la descomposición en fracciones parciales. Esta técnica es fundamental en matemáticas aplicadas, ingeniería y ciencias, ya que permite resolver ecuaciones diferenciales lineales de manera eficiente.

---

## 1. Introducción

La **solución de fracciones parciales por anuladores** es una técnica avanzada que combina el uso de operadores diferenciales (anuladores) con la expansión en fracciones parciales. Este método es especialmente útil para resolver ecuaciones diferenciales lineales no homogéneas con coeficientes constantes.

---

## 2. Definiciones

>🔑 *Anulador:* Un anulador es un operador diferencial que, cuando se aplica a una función, produce cero. Por ejemplo, el anulador de \( e^{at} \) es \( D - a \), donde \( D \) es el operador derivada.

>🔑 *Fracción Parcial:* Una fracción parcial es una fracción algebraica más simple que se obtiene al descomponer una fracción compleja en una suma de fracciones con denominadores más simples.

>🔑 *Expansión en Fracciones Parciales:* Es el proceso de descomponer una fracción algebraica en una suma de fracciones parciales.

---

## 3. Métodos de Expansión con Anuladores

El método de anuladores se utiliza para resolver ecuaciones diferenciales lineales no homogéneas. Los pasos son los siguientes:

1. **Identificar el término no homogéneo** en la ecuación diferencial.
2. **Aplicar el anulador** correspondiente al término no homogéneo para convertir la ecuación en una ecuación diferencial homogénea de orden superior.
3. **Resolver la ecuación homogénea** resultante.
4. **Descomponer la solución** en fracciones parciales si es necesario.
5. **Aplicar la transformada inversa de Laplace** para obtener la solución en el dominio del tiempo.

---

## 4. Ejemplo Resuelto

### 4.1. Problema
Resolver la siguiente ecuación diferencial utilizando anuladores y fracciones parciales:
$$
\frac{d^2y}{dt^2} + 3\frac{dy}{dt} + 2y = e^{-t}
$$

### 4.2. Solución
1. **Identificar el término no homogéneo**:
   El término no homogéneo es \( e^{-t} \).

2. **Aplicar el anulador**:
   El anulador de \( e^{-t} \) es \( D + 1 \), donde \( D \) es el operador derivada. Aplicamos el anulador a ambos lados de la ecuación:
   $$
   (D + 1)\left(\frac{d^2y}{dt^2} + 3\frac{dy}{dt} + 2y\right) = (D + 1)e^{-t}
   $$
   Simplificando:
   $$
   (D + 1)(D^2 + 3D + 2)y = 0
   $$

3. **Resolver la ecuación homogénea**:
   La ecuación característica es:
   $$
   (r + 1)(r^2 + 3r + 2) = 0
   $$
   Las raíces son \( r = -1 \), \( r = -1 \), y \( r = -2 \). Por lo tanto, la solución general es:
   $$
   y(t) = C_1 e^{-t} + C_2 t e^{-t} + C_3 e^{-2t}
   $$

4. **Descomponer en fracciones parciales**:
   Si aplicamos la transformada de Laplace a la ecuación original, obtenemos:
   $$
   Y(s) = \frac{1}{(s + 1)(s^2 + 3s + 2)}
   $$
   Descomponemos en fracciones parciales:
   $$
   Y(s) = \frac{A}{s + 1} + \frac{B}{s + 2}
   $$
   Resolviendo para \( A \) y \( B \):
   - Para \( s = -1 \):
     $$
     A = \frac{1}{1} = 1
     $$
   - Para \( s = -2 \):
     $$
     B = \frac{1}{-1} = -1
     $$
   Por lo tanto:
   $$
   Y(s) = \frac{1}{s + 1} - \frac{1}{s + 2}
   $$

5. **Aplicar la transformada inversa de Laplace**:
   $$
   y(t) = e^{-t} - e^{-2t}
   $$

---

## 5. Ejercicios

📚**Ejercicio 1:** 

$$\frac{d^2y}{dt^2} + 4\frac{dy}{dt} + 4y = e^{-2t}$$

**Solución:**
1. Identificar el término no homogéneo:
   El término no homogéneo es \( e^{-2t} \).

2. Aplicar el anulador:
   El anulador de \( e^{-2t} \) es \( D + 2 \). Aplicamos el anulador a ambos lados de la ecuación:
   $$
   (D + 2)\left(\frac{d^2y}{dt^2} + 4\frac{dy}{dt} + 4y\right) = (D + 2)e^{-2t}
   $$
   Simplificando:
   $$
   (D + 2)(D^2 + 4D + 4)y = 0
   $$

3. Resolver la ecuación homogénea:
   La ecuación característica es:
   $$
   (r + 2)(r^2 + 4r + 4) = 0
   $$
   Las raíces son \( r = -2 \), \( r = -2 \), y \( r = -2 \). Por lo tanto, la solución general es:
   $$
   y(t) = C_1 e^{-2t} + C_2 t e^{-2t} + C_3 t^2 e^{-2t}
   $$

4. Descomponer en fracciones parciales:
   Si aplicamos la transformada de Laplace a la ecuación original, obtenemos:
   $$
   Y(s) = \frac{1}{(s + 2)^3}
   $$
   La transformada inversa de Laplace es:
   $$
   y(t) = \frac{t^2}{2} e^{-2t}
   $$

---

## 6. Conclusiones

La **solución de fracciones parciales por anuladores** es una técnica poderosa para resolver ecuaciones diferenciales lineales no homogéneas. A través de este repositorio, hemos explorado:
- Los **métodos de expansión** utilizando anuladores.
- **Ejemplos prácticos** que ilustran cómo aplicar la técnica.
- **Ejercicios resueltos** que refuerzan el aprendizaje.

Esta herramienta es fundamental en áreas como el control automático, el procesamiento de señales y la resolución de ecuaciones diferenciales. Dominar la expansión de fracciones parciales es clave para avanzar en el estudio de sistemas dinámicos y otras disciplinas técnicas.

---

## 7. Referencias

- [1] **"Matemáticas para Ingeniería"**, Autor: James Stewart.  
