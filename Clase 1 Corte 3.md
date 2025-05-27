# Dinámica de Sistemas en Sistemas Hidráulicos

Los sistemas hidráulicos son fundamentales en aplicaciones industriales, donde el control de flujo y nivel de líquidos es esencial para garantizar operaciones eficientes y seguras. En esta clase, exploraremos los principios básicos de la dinámica de sistemas aplicados a tanques interconectados, modelando su comportamiento mediante ecuaciones diferenciales y analizando las relaciones entre flujos, resistencias y niveles de líquido.

---

## 1. Introducción a los Sistemas de Tanques

Los sistemas de tanques son comunes en la industria para almacenar y regular líquidos. El objetivo principal es mantener un flujo o nivel constante, lo que requiere un modelo matemático que describa las interacciones entre las variables del sistema.

>🔑 *Definición:* Un *sistema de tanques* es un conjunto de recipientes interconectados donde el flujo de líquido está influenciado por resistencias al flujo y las áreas transversales de los tanques.

---

## 2. Modelado de un Tanque Individual

### 2.1. Variables del Sistema
- \( $q_i$ \): Flujo de entrada al tanque.
- \( $q_1$ \): Flujo de salida del tanque.
- \( $R_1$ \): Resistencia al flujo.
- \( $A_1$ \): Área transversal del tanque.
- \( $h_1$ \): Nivel de líquido en el tanque.

### 2.2. Ecuaciones Fundamentales
El flujo de salida se relaciona con el nivel de líquido mediante:

$$q_1 = \frac{h_1}{R_1}$$

La dinámica del nivel del líquido se describe con:

$$A_1 \frac{dh_1}{dt} = q_i - q_1$$

💡**Ejemplo 1:** Si \( $q_i = 5\frac{m^3}{s}$) , \( $R_1 = 2 \frac{s}{m^2}$\) , y \($A_1 = 10{m}^2$\), el nivel en estado estacionario se calcula como:

$$h_1 = q_i \cdot R_1 = 10m$$

---

## 3. Tanques Interconectados

### 3.1. Modelo de Dos Tanques
En sistemas con dos tanques interconectados, las ecuaciones se extienden para incluir las interacciones entre ellos.

#### 3.1.1. Variables Adicionales
- \( $q_2$\): Flujo de salida del segundo tanque.
- \( $R_2$ \): Resistencia al flujo del segundo tanque.
- \( $A_2$ \): Área transversal del segundo tanque.
- \( $h_2$ \): Nivel de líquido en el segundo tanque.

#### 3.1.2. Ecuaciones del Sistema
Para el primer tanque:

$$A_1 \frac{dh_1}{dt} = q_i - q_1$$

Para el segundo tanque:

$$A_2 \frac{dh_2}{dt} = q_1 - q_2$$

Donde:

$$q_1 = \frac{h_1 - h_2}{R_1}$$

$$q_2 = \frac{h_2}{R_2}$$

### 3.2. Modelo Resultante
Combinando las ecuaciones, se obtiene un sistema de ecuaciones diferenciales acopladas:

$$A_1 R_1 R_2 A_2 \frac{d^2 q_2}{dt^2} + (A_1 R_1 + A_1 R_2 + R_2 A_2) \frac{d q_2}{dt} + q_2 = q_i$$

💡**Ejemplo 2:**  Si \( $A_1 = A_2 = 5{m}^2 $\),  \( $R_1 = R_2 = 1\frac{s}{m^2}$ \),  y  \( $q_i$ \)  es constante, el sistema alcanza un equilibrio donde:
\( $$q_2 = q_i$$ \).

---

## 4. Ejercicios

📚 **Ejercicio 1:**  
Para un tanque individual con \($A_1 = 8{m^2}$\) y \($R_1 = 4\frac{s}{m^2}$\), determine el nivel de líquido \( $h_1$ \) en estado estacionario si el flujo de entrada \( $q_i = 2\frac{m^3}{s}$\).

**Solución:**  
En estado estacionario, \($\frac{dh_1}{dt} = 0$\), por lo tanto:

$$q_i = q_1 = \frac{h_1}{R_1}$$

$$h_1 = q_i \cdot R_1 = 2 \cdot 4 = 8{m}. $$

📚 **Ejercicio 2:**  
Para dos tanques interconectados con \($A_1 = A_2 = 6{m}^2$\), \( $R_1 = 3\frac{s}{m^2}$\), y \( $R_2 = 2\frac{s}{m^2}$\), calcule el flujo \($q_2$\) en estado estacionario si \( $q_i = 4\frac{m^3}{s}$\).

**Solución:**  
En equilibrio, \( $q_2 = q_i = 4\frac{m^3}{s}$\).

---

## 5. Conclusiones

En esta clase, hemos modelado sistemas hidráulicos de tanques individuales e interconectados, utilizando ecuaciones diferenciales para describir su dinámica. Estos modelos son esenciales para diseñar sistemas de control que mantengan niveles y flujos deseados en aplicaciones industriales.

---

## 6. Referencias

- Presentación adjunta: "Sistemas hidráulicos", Sexto semestre – Sistemas Dinámicos.
