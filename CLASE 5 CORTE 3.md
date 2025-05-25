# Diagramas de Flujo de Señales

Los diagramas de flujo de señales son una herramienta gráfica utilizada en el análisis de sistemas dinámicos para representar relaciones entre variables y simplificar la obtención de funciones de transferencia en sistemas complejos. Esta técnica, complementaria a los diagramas de bloques, se basa en la aplicación de la fórmula de Mason, que permite calcular la función de transferencia total de manera sistemática. A continuación, se presenta un resumen estructurado de los conceptos clave.

---

## 1. Elementos de los Diagramas de Flujo de Señales

### 1.1. Nodos
🔑 *Definición:* Los nodos representan señales de entrada o salida del sistema. Se ilustran como círculos con una etiqueta que identifica la señal.  
Ejemplo:  
$V(s) \quad T(s)$

### 1.2. Flechas
🔑 *Definición:* Las flechas indican la relación entre variables, mostrando el sentido de la señal y la función de transferencia asociada.  
Ejemplo:  
$X(s)\{G(s)} Y(s)$

*Figura 1*.

![Comparación entradas](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/Grafica%206.png)

## 2. Definiciones Clave

### 2.1. Trayectorias y Lazos
🔑 *Trayectoria directa:* Camino desde un nodo de entrada a uno de salida sin repetir nodos.  
🔑 *Lazo:* Trayectoria cerrada que comienza y termina en el mismo nodo.  
🔑 *Ganancia de lazo:* Producto de las funciones de transferencia en un lazo.  

### 2.2. Fórmula de Mason
La función de transferencia total \( P \) se calcula como:  
$P = \frac{1}{\Delta} \sum_k P_k \Delta_k$  
Donde:  
- $\( P_k \)$: Ganancia de la trayectoria directa $\( k \)$.  
- $\( \Delta \)$: Determinante del sistema.  
- $\( \Delta_k \)$: Cofactor asociado a $\( P_k \)$.  

---

## 3. Ejemplos Aplicados

### 3.1. Ejemplo 1: Sistema con Retroalimentación
💡 **Ejemplo 1:**  
- Trayectoria directa: $\( P_1 = G_1 G_2 G_3 \)$.
- Lazos: $\( L_1 = G_1 G_2 H_1 \), \( L_2 = -G_2 G_3 H_2 \)$.  
- Función de transferencia:  
  $\frac{C(s)}{R(s)} = \frac{G_1 G_2 G_3}{1 - G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}$

### 3.2. Ejemplo 2: Sistema Múltiple
💡 **Ejemplo 2:**  
- Trayectorias: $\( P_1 = G_1 G_2 G_3 G_4 G_5 \)$, $\( P_2 = G_1 G_6 G_4 G_5 \)$.  
- Lazos: $\( L_1 = -G_4 H_1 \)$, $\( L_2 = -G_2 G_7 H_2 \)$.  
- Determinantes: $\( \Delta = 1 - (L_1 + L_2) \)$.

---

## 4. Comparación con Diagramas de Bloques

- **Ventaja:** Los diagramas de flujo simplifican sistemas complejos mediante la fórmula de Mason, evitando manipulaciones algebraicas tediosas.  
- **Ejemplo:** Conversión de un diagrama de bloques a flujo de señales para aplicar Mason.  

---

## 5. Ejercicios

📚 **Ejercicio 1:**  
Dado el siguiente diagrama de flujo, calcule $\( \frac{Y(s)}{R(s)} \)$:  
- Trayectorias: $\( P_1 = 30/s \)$, $\( P_2 = 0.05 \)$.  
- Lazos: $\( L_1 = -1/s \)$.  

**Solución:**  
Aplicar la fórmula de Mason considerando $\( \Delta = 1 - L_1 \)$.

📚 **Ejercicio 2:**  
Convierta el siguiente diagrama de bloques a flujo de señales y calcule la función de transferencia:  
$R(s) \rightarrow \boxed{G_1} \rightarrow \boxed{G_2} \rightarrow Y(s)$  

**Solución:**  
Identificar nodos y flechas equivalentes, luego aplicar Mason.

---

## 6. Conclusiones

- Los diagramas de flujo de señales ofrecen un método sistemático para analizar sistemas dinámicos complejos.  
- La fórmula de Mason automatiza el cálculo de funciones de transferencia, reduciendo errores en manipulaciones algebraicas.  
- Su aplicación es especialmente útil en sistemas con múltiples lazos y retroalimentaciones.  

## 7. Referencias

- Presentación: *Diagramas de flujo de señales*, Ing. Jorge Eduardo Cote Ballesteros, 2025.  
- Ogata, K. (2010). *Ingeniería de Control Moderna* (5ª ed.). Pearson. 
