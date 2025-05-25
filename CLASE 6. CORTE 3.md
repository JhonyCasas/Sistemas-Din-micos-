# Álgebra de Diagramas de Flujo de Señal, Transformación a Diagramas de Bloques y Fórmula de Mason

Los diagramas de flujo de señal (SFG) son herramientas gráficas para representar sistemas de ecuaciones lineales, comúnmente utilizados en el análisis de sistemas de control. Esta clase cubre las reglas del álgebra de SFG, su transformación a diagramas de bloques y la aplicación de la fórmula de ganancia de Mason para simplificar cálculos en sistemas complejos.

## 1. Álgebra de Diagramas de Flujo de Señal

🔑 *Definición*: Un *diagrama de flujo de señal* es una red de nodos (variables) conectados por ramas (ganancias) que representan relaciones matemáticas entre variables.

### 1.1 Reglas Básicas
- **Nodos**: Representan variables del sistema (suma de señales entrantes).
- **Ramas**: Muestran la relación causal entre nodos (dirección + ganancia).
- **Nodo fuente**: Solo tiene ramas salientes (entrada).
- **Nodo sumidero**: Solo tiene ramas entrantes (salida).

### 1.2 Operaciones
- **Serie**: Multiplicar ganancias en cascada.
- **Paralelo**: Sumar ganancias de ramas paralelas.
- **Lazos**: Realimentaciones que requieren reducción.

## 2. Transformación a Diagrama de Bloques

🔑 *Definición*: La *transformación a diagrama de bloques* convierte un SFG en una representación con bloques funcionales y operadores de suma.

### 2.1 Pasos para la Conversión
1. Identificar nodos de entrada/salida.
2. Reemplazar nodos intermedios por bloques.
3. Agrupar lazos de realimentación.

💡 **Ejemplo 1**: Conversión de SFG a diagrama de bloques
SFG: X1 →[G1]→ X2 →[G2]→ X3
Diagrama equivalente:
[G1] -> [G2] (en cascada)


## 3. Fórmula de Ganancia de Mason

🔑 *Definición*: La *fórmula de Mason* calcula la ganancia total \( T \) entre un nodo fuente y un sumidero:

$$
T = $\frac{\sum_{k} P_k \Delta_k}{\Delta}$

Donde:
- $\( P_k \)$: Ganancia del k-ésimo camino directo.
- $\( \Delta \)$: Determinante del grafo $(\( 1 - \sum L_n + \sum L_mL_p - \dots \)$.
- $\( \Delta_k \)$: Cofactor del k-ésimo camino.

### 3.1 Aplicación
1. Identificar caminos directos $(\( P_k \)$.
2. Encontrar lazos individuales $(\( L_n \)$.
3. Calcular lazos no tocados y productos.

💡 **Ejemplo 2**: Sistema con realimentación simple
Camino: $P1 = G1G2$

Lazo: $L1 = -G1G2H1$

$Δ = 1 - L1$


$T = \frac{G1G2}{(1 + G1G2H1)}$


## 📚 Ejercicios

### Ejercicio 1
**Enunciado**: Simplifique el siguiente SFG usando álgebra:
X1 →[2]→ X2 →[3]→ X3
X1 →[4]→ X3

**Solución**:  
Ganancia total = $\( 2 \times 3 + 4 = 10 \)$

### Ejercicio 2
**Enunciado**: Calcule la ganancia usando Mason:
X1 →[G1]→ X2 →[G2]→ X3
X3 →[-H]→ X2

**Solución**:  
$\( \Delta = 1 + G2H \)$, $\( P1 = G1G2 \)$, $\( T = \frac{G1G2}{1 + G2H} \)$

## 4. Conclusiones
- Los SFG permiten visualizar relaciones algebraicas en sistemas dinámicos.
- La fórmula de Mason automatiza el cálculo de ganancias en sistemas complejos.
- La conversión a diagramas de bloques facilita la implementación práctica.

## 5. Referencias
- Ogata, K. (2010). *Ingeniería de Control Moderno*. Pearson.
- Apuntes de clase: Sistemas de Control (2023).
