# Modelado de Sistemas Dinámicos Hidráulicos: Tanques de Agua  

Este repositorio está enfocado en el modelado matemático de sistemas dinámicos hidráulicos, específicamente en tanques de agua interconectados, flujos de entrada/salida e intercambio de energía. Se abordarán conceptos fundamentales como balances de masa, ecuaciones de Bernoulli, y modelado en espacio de estados, aplicados a sistemas reales como redes de distribución de agua o sistemas de refrigeración.  

### 1.1. Balance de Masa en Tanques  
>🔑 *Definición:* La *ley de conservación de masa* para un tanque establece:  
> $$\frac{dV}{dt} = Q_{in} - Q_{out}$$  
> donde $V$ es volumen ($V = A \cdot h$) y $Q$ flujo volumétrico.  

### 1.2. Ecuación de Torricelli  
Para flujo por gravedad:  
$$Q_{out} = k\sqrt{h}, \quad k = C_d A_{orificio}\sqrt{2g}$$  

## 2. Modelado de Sistemas Acoplados  
### 2.1. Dos Tanques Interconectados  
![Diagrama tanques](images/two_tanks.png)  
*Figura 1: Tanques con acoplamiento hidráulico.*  

💡**Ejemplo 1:** Dinámica no lineal para tanques con áreas $A_1$, $A_2$:  
$$
\begin{cases}
\frac{dh_1}{dt} = \frac{Q_{in} - k_1\sqrt{h_1 - h_2}}{A_1} \\
\frac{dh_2}{dt} = \frac{k_1\sqrt{h_1 - h_2} - k_2\sqrt{h_2}}{A_2}
\end{cases}
$$

## 3. Simulación Numérica  
### 3.1. Método de Euler  

def simulate_tanks(h1_0, h2_0, k1, k2, A1, A2, Qin, dt, steps):
    h1, h2 = h1_0, h2_0
    for _ in range(steps):
        dh1 = (Qin - k1*np.sqrt(max(h1-h2,0)))/A1 * dt
        dh2 = (k1*np.sqrt(max(h1-h2,0)) - k2*np.sqrt(h2))/A2 * dt
        h1 += dh1; h2 += dh2
    return h1, h2

# Modelado de Sistemas Dinámicos Hidráulicos: Tanques de Agua

Repositorio para análisis de sistemas de tanques interconectados, flujos y transferencia de energía.

# Modelado de Sistemas Dinámicos Hidráulicos: Tanques de Agua  
**Repositorio académico** | [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Introducción  
Estudio de modelos matemáticos para sistemas hidráulicos con:  
- Tanques interconectados  
- Flujos turbulentos/laminares  
- Transferencia de energía térmica  

## 📚 Contenido
1. [Fundamentos Teóricos](#1-fundamentos-teóricos)  
2. [Modelado Matemático](#2-modelado-matemático)  
3. [Simulación Numérica](#3-simulación-numérica)  
4. [Ejercicios Resueltos](#4-ejercicios-resueltos)  

---

## 1. Fundamentos Teóricos  
### 1.1. Ecuaciones Básicas  
> 🔑 *Ley de Conservación de Masa*:  
> $$\frac{d(ρAh)}{dt} = ρQ_{in} - ρQ_{out}$$  
> Para líquidos incompresibles ($ρ$ constante):  
> $$A\frac{dh}{dt} = Q_{in} - Q_{out}$$

### 1.2. Tipos de Flujos  
| Tipo        | Ecuación               | Rango Reynolds |
|-------------|------------------------|----------------|
| Laminar     | $Q = k_1Δh$            | Re < 2000      |
| Turbulento  | $Q = k_2\sqrt{Δh}$     | Re > 4000      |

*Tabla 1: Clasificación de regímenes de flujo*

---

## 2. Modelado Matemático  
### 2.1. Sistema de Dos Tanques  
```mermaid
graph LR
    A[Tanque 1] -->|Q₁₂| B[Tanque 2]
    B -->|Q₂ₑ| C[Entorno]
