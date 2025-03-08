# Expansión de Fracciones Parciales
La expansión de fracciones parciales es una técnica matemática utilizada para descomponer una fracción algebraica en una suma de fracciones más simples. Este método es especialmente útil en cálculo, ingeniería y otras áreas donde se requiere simplificar expresiones complejas.

## 1. Introducción
La expansión de fracciones parciales permite descomponer una fracción compleja en fracciones más simples, lo que facilita su integración, diferenciación o análisis. Esta técnica es fundamental en el estudio de sistemas dinámicos, control automático y procesamiento de señales.

## 2. Definiciones
>🔑 *Fracción Parcial:* Una fracción parcial es una fracción algebraica más simple que se obtiene al descomponer una fracción compleja en una suma de fracciones con denominadores más simples.

>🔑 *Expansión de Fracciones Parciales:* Es el proceso de descomponer una fracción algebraica en una suma de fracciones parciales.

## 3. Métodos de Expansión
Existen diferentes métodos para realizar la expansión de fracciones parciales, dependiendo de la forma del denominador.

### 3.1. Factores Lineales No Repetidos
Cuando el denominador tiene factores lineales no repetidos, la expansión se realiza de la siguiente manera:

$$\frac{P(s)}{(s - a)(s - b)} = \frac{A}{s - a} + \frac{B}{s - b}$$

### 3.2. Factores Lineales Repetidos
Cuando el denominador tiene factores lineales repetidos, la expansión incluye términos adicionales:

$$\frac{P(s)}{(s - a)^2} = \frac{A}{s - a} + \frac{B}{(s - a)^2}$$

### 3.3. Factores Cuadráticos Irreducibles
Cuando el denominador tiene factores cuadráticos irreducibles, la expansión incluye términos con numeradores lineales:

$$\frac{P(s)}{(s^2 + as + b)} = \frac{As + B}{s^2 + as + b}$$

## 4. Ejemplos
💡**Ejemplo 1:** Descomponer la fracción:

$$\frac{3s + 5}{(s + 1)(s + 2)}$$
Solución:

$$\frac{3s + 5}{(s + 1)(s + 2)} = \frac{A}{s + 1} + \frac{B}{s + 2}$$

Resolviendo, obtenemos \( A = 2 \) y \( B = 1 \), por lo tanto:

$$\frac{3s + 5}{(s + 1)(s + 2)} = \frac{2}{s + 1} + \frac{1}{s + 2}$$

💡**Ejemplo 2:** Descomponer la fracción:

$$\frac{2s^2 + 6s + 5}{(s + 1)(s + 2)^2}$$
Solución:

$$\frac{2s^2 + 6s + 5}{(s + 1)(s + 2)^2} = \frac{A}{s + 1} + \frac{B}{s + 2} + \frac{C}{(s + 2)^2}$$

Resolviendo, obtenemos \( A = 1 \), \( B = 1 \) y \( C = -1 \), por lo tanto:

$$\frac{2s^2 + 6s + 5}{(s + 1)(s + 2)^2} = \frac{1}{s + 1} + \frac{1}{s + 2} - \frac{1}{(s + 2)^2}$$

## 5. Ecuaciones
Las ecuaciones son fundamentales para describir la expansión de fracciones parciales.

### 5.1. Expansión de Fracciones Parciales
$$
\frac{P(s)}{Q(s)} = \sum_{i=1}^{n} \frac{A_i}{(s - a_i)}
$$

### 5.2. Expansión con Factores Repetidos
$$
\frac{P(s)}{(s - a)^m} = \sum_{i=1}^{m} \frac{A_i}{(s - a)^i}
$$

## 6. Figuras

Figura 1. Diagrama de expansión de fracciones parciales.

## 7. Tablas
| **Tipo de Factor** | **Forma de la Expansión** |
|---------------------|---------------------------|
| Lineal No Repetido  | $$\(\frac{A}{s - a}\)$$       |
| Lineal Repetido     | $$\(\frac{A}{(s - a)^2}\)$$   |
| Cuadrático          | $$\(\frac{As + B}{s^2 + as + b}\)$$ |

Tabla 1. Tipos de factores y sus formas de expansión.

## 9. Ejercicios


📚**Ejercicio 1:**

$$\frac{5s + 10}{(s + 1)(s + 2)}$$

**Solucion:** $f(t) = 5e^{-t}$

$$=\frac{5s + 10}{(s + 1)(s + 2)} = \frac{A}{s + 1} + \frac{B}{s + 2}$$

$$=5s + 10 = A(s + 2) + B(s + 1)$$

$$5(-1) + 10 = A(-1 + 2) + B(-1 + 1) \\
-5 + 10 = A(1) + B(0) \\
A = 5$$

$$5(-2) + 10 = A(-2 + 2) + B(-2 + 1) \\
-10 + 10 = A(0) + B(-1) \\
B = 0$$

$$\frac{5s + 10}{(s + 1)(s + 2)} = \frac{5}{s + 1}$$

$$\mathcal{L}^{-1}{\frac{5}{s + 1}} = 5e^{-t}$$

$$f(t) = 5e^{-t}$$

📚**Ejercicio 2:** 

$$\frac{3s^2 + 7s + 2}{(s + 1)^2 (s + 2)}$$

**Solucion:** $\boxed{f(t) = 3e^{-t} - 2te^{-t}}$

$$3s^2 + 7s + 2 = A(s + 1)(s + 2) + B(s + 2) + C(s + 1)^2$$

$$3(-1)^2 + 7(-1) + 2 = A(-1 + 1)(-1 + 2) + B(-1 + 2) + C(-1 + 1)^2 \\
3 - 7 + 2 = A(0) + B(1) + C(0) \\
B = -2$$
$$3(-2)^2 + 7(-2) + 2 = A(-2 + 1)(-2 + 2) + B(-2 + 2) + C(-2 + 1)^2 \\
12 - 14 + 2 = A(0) + B(0) + C(1) \\
C = 0$$}

$$3(0)^2 + 7(0) + 2 = A(0 + 1)(0 + 2) + B(0 + 2) + C(0 + 1)^2 \\
2 = 2A + 2B + C \\
 \( B = -2 \) y \( C = 0 \):
2 = 2A + 2(-2) + 0 \\
2 = 2A - 4 \\
2A = 6 \\
A = 3$$
$$\frac{3s^2 + 7s + 2}{(s + 1)^2 (s + 2)} = \frac{3}{s + 1} - \frac{2}{(s + 1)^2}$$


$$\mathcal{L}^{-1}{\frac{3s^2 + 7s + 2}{(s + 1)^2 (s + 2)}} = 3e^{-t} - 2te^{-t}$$

$$\boxed{f(t) = 3e^{-t} - 2te^{-t}}$$

📚**Ejercicio 3:** 

$$\frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)}$$

**Solucion:** $\boxed{f(t) = -\frac{1}{6}e^{-t} - \frac{4}{3}e^{2t} + \frac{7}{2}e^{3t}}$

$$\frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = \frac{A}{s + 1} + \frac{B}{s - 2} + \frac{C}{s - 3}$$

$$2s^2 - 4 = A(s - 2)(s - 3) + B(s + 1)(s - 3) + C(s + 1)(s - 2)$$
$$A(s^2 - 5s + 6)$$
$$B(s^2 - 2s - 3)$$
$$C(s^2 - s - 2)$$
$$2s^2 - 4 = (A + B + C)s^2 + (-5A - 2B - C)s + (6A - 3B - 2C)$$

$$A + B + C = 2$$
$$-5A - 2B - C = 0$$
$$6A - 3B - 2C = -4$$
$$ C = 2 - A - B$$

$$-4A - B = 2$$

$$ 8A - B = 0 $$

$$A = -\frac{1}{6}, \quad B = -\frac{4}{3}, \quad C = \frac{7}{2} $$

$$\frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = -\frac{1}{6(s + 1)} - \frac{4}{3(s - 2)} + \frac{7}{2(s - 3)}$$

$$-\frac{1}{6}e^{-t} $$

 $$-\frac{4}{3}e^{2t}$$

$$\frac{7}{2}e^{3t}$$

$$\boxed{f(t) = -\frac{1}{6}e^{-t} - \frac{4}{3}e^{2t} + \frac{7}{2}e^{3t}}$$

## 10. Conclusiones

La **expansión de fracciones parciales** es una técnica esencial en matemáticas aplicadas, ingeniería y ciencias. Permite descomponer fracciones algebraicas complejas en fracciones más simples, lo que facilita su manipulación, integración y análisis. A través de este repositorio, hemos explorado:

1. **Métodos de Expansión**:
   - Para factores lineales no repetidos:
     
    $$ \frac{P(s)}{(s - a)(s - b$$

   - Para factores lineales repetidos:

     $$\frac{P(s)}{(s - a)^2} = \frac{A}{s - a} + \frac{B}{(s - a)^2}$$

   - Para factores cuadráticos irreducibles:

    $$\frac{P(s)}{(s^2 + as + b)} = \frac{As + B}{s^2 + as + b}$$


   ## 11. Referencias

1. **Stewart, J. (2015). *Cálculo: Trascendentes tempranas.* Cengage Learning.**  
   - Técnicas de integración (Sección 7.4).  
   - Enlace: [Cengage](https://www.cengage.com)

2. **Zill, D. G. (2014). *Matemáticas avanzadas para ingeniería.* Cengage Learning.**  
   - Transformada de Laplace (Sección 7.2).  
   - Enlace: [Cengage](https://www.cengage.com)

3. **Khan Academy. *Expansion en Fracciones parciales.***  
   - Enlace: [Khan Academy](https://www.youtube.com/results?search_query=expansion+en+fracciones+parciales)

