**# Función de Transferencia

La función de transferencia es una herramienta fundamental en el análisis de sistemas dinámicos, permitiendo representar la relación entre la entrada y la salida de un sistema en el dominio de Laplace. Este enfoque simplifica el estudio de sistemas complejos al convertir ecuaciones diferenciales en expresiones algebraicas, facilitando el análisis de su comportamiento transitorio y estacionario.

## 1. Conceptos Básicos

1.1 Definición  
🔑 Función de transferencia: Relación entre la transformada de Laplace de la salida y la entrada de un sistema, asumiendo condiciones iniciales nulas.  
$G(s) = \frac{Y(s)}{U(s)} = \frac{N(s)}{D(s)}$

### 1.2. Clasificación  
- *Propia*: Grado del numerador \( n \) ≤ grado del denominador $\(m\)$.  
- *Impropia*: $\( n > m \)$.  
- *Bipropia*: $\( n = m \)$.

## 2. Polos y Ceros

🔑 Polos: Valores de \( s \) que hacen \( D(s) = 0 \). Representan las raíces del denominador y determinan la estabilidad del sistema.  
🔑 Ceros: Valores de \( s \) que hacen \( N(s) = 0 \). Afectan la respuesta transitoria pero no la estabilidad.

💡 *Ejemplo 1*: Para $$ G(s) = \frac{3s-1}{s^2 + 3s + 2} $$:  
- *Cero*: \( s = \frac{1}{3} \).  
- *Polos*: \( s = -1 \) y \( s = -2 \) (raíces de \( s^2 + 3s + 2 = 0 \)).

## 3. Teorema del Valor Final

Permite calcular el valor en estado estacionario de la salida:  
$$ \lim_{t \to \infty} f(t) = \lim_{s \to 0} sF(s) $$

💡 *Ejemplo 2*: Para \( G(s) = \frac{4}{5s+1} \) con entrada escalón unitario:  
$$ \lim_{s \to 0} s \cdot \frac{4}{s(5s+1)} = 4 $$

## 4. Entradas de Prueba en Sistemas de Control

🔑 Entradas de prueba: Señales estándar utilizadas para analizar el comportamiento dinámico de sistemas de control. Permiten evaluar características clave como estabilidad, rapidez de respuesta y error en estado estacionario.

### 4.1. Entrada Escalón

*Definición*:  
> Cambio abrupto en la entrada desde cero hasta un valor constante A en t=0. Modela perturbaciones súbitas o cambios de referencia.

*Expresión matemática*:  
$$ u(t) = \begin{cases} A & \text{para } t \geq 0 \\ 0 & \text{para } t < 0 \end{cases} \quad \mathcal{L}\{u(t)\} = \frac{A}{s} $$

*Caso de uso típico*:  
- Evaluar el tiempo de establecimiento (cuando la salida alcanza el 98% del valor final)
- Calcular el sobreimpulso máximo en sistemas subamortiguados

💡 *Ejemplo 3*: Para un sistema con \( G(s) = \frac{5}{s+2} \), la respuesta al escalón unitario (A=1) es:  
$$Y(s) = \frac{5}{s(s+2)} \quad \Rightarrow \quad y(t) = 2.5(1-e^{-2t}) $$

### 4.2. Entrada Rampa

*Definición*:  
> Señal que crece linealmente con el tiempo. Modela referencias que cambian a velocidad constante.

*Expresión matemática*:  
$$ r(t) = \begin{cases} At & \text{para } t \geq 0 \\ 0 & \text{para } t < 0 \end{cases} \quad \Rightarrow \quad \mathcal{L}\{r(t)\} = \frac{A}{s^2} $$

*Caso de uso típico*:  
- Evaluar la capacidad de seguimiento del sistema
- Determinar el error en estado estacionario para señales que varían continuamente

💡 *Ejemplo 4*: El mismo sistema \( G(s) = \frac{5}{s+2} \) con rampa A=3:  
$$ Y(s) = \frac{15}{s^2(s+2)} \quad \Rightarrow \quad y(t) = \frac{15}{4}(2t-1+e^{-2t}) $$

### 4.3. Entrada Parabólica

*Definición*:  
> Señal que varía cuadráticamente con el tiempo. Evalúa sistemas que deben seguir aceleraciones.

*Expresión matemática*:  
$$ p(t) = \begin{cases} At^2 & \text{para } t \geq 0 \\ 0 & \text{para } t < 0 \end{cases} \quad \Rightarrow \quad \mathcal{L}\{p(t)\} = \frac{2A}{s^3} $$

*Caso de uso típico*:  
- Sistemas de seguimiento de trayectorias (robótica, misiles)
- Análisis de error ante aceleraciones constantes

### 4.4. Comparación de Entradas

| Tipo       | Transformada | Aplicación típica                     | Error estacionario típico |
|------------|--------------|---------------------------------------|---------------------------|
| Escalón    | \( \frac{A}{s} \) | Cambios bruscos de referencia        | Posición                  |
| Rampa      | \( \frac{A}{s^2} \) | Sistemas de seguimiento continuo     | Velocidad                 |
| Parábola   | \( \frac{2A}{s^3} \) | Sistemas con aceleración constante   | Aceleración               |

*Figura 1*. Comparación gráfica de entradas de prueba

![Comparación entradas](images/entradas_prueba.png)  
Figura 1. Representación gráfica de las señales escalón (azul), rampa (rojo) y parábola (verde)

### 4.5. Selección de Entradas Adecuadas

1. *Sistemas de regulación*: Usar escalón para evaluar rechazo a perturbaciones  
2. *Sistemas de seguimiento*:  
   - Rampa para velocidades constantes (ej: telescopios)  
   - Parábola para sistemas con aceleración (ej: drones)  
3. *Validación de controladores*:  
   - Escalón para respuesta transitoria  
   - Rampa para error en estado estacionario  

💡 *Ejemplo 5*: En un motor DC controlado por posición:  
- Escalón evalúa el tiempo para alcanzar nueva posición  
- Rampa prueba el seguimiento al moverte entre puntos  
- Parábola verifica comportamiento ante movimientos curvos

## 5. Ejercicios

📚 *Ejercicio 1*: Para $\(G(s) = \frac{8}{s^3+6s^2+11s+6}\)$, determine:  
- Polos.  
- Valor final ante un escalón unitario.  

*Solución*:  
- Polos: Raíces de \( s^3 + 6s^2 + 11s + 6 = 0 \) (\( s = -1, -2, -3 \)).  
- Valor final: \( \lim_{s \to 0} s \cdot \frac{8}{s(s^3 + 6s^2 + 11s + 6)} = \frac{8}{6} \).

📚 *Ejercicio 2*: Para la ecuación diferencial \( \ddot{y} + 5\dot{y} + 13.5y = 7.5u \), obtenga:  
- Función de transferencia.  
- Polos y ceros.  

*Solución*:  
- \( G(s) = \frac{7.5}{s^2 + 5s + 13.5} \).  
- Polos: Raíces de \( s^2 + 5s + 13.5 = 0 \) (\( s = -2.5 \pm 2.5j \)).  
- No tiene ceros.

## 6. Conclusiones

La función de transferencia es una representación compacta que captura la dinámica de un sistema, permitiendo analizar su respuesta ante diferentes entradas. Los polos y ceros proporcionan información crítica sobre estabilidad y comportamiento transitorio, mientras que el teorema del valor final simplifica el cálculo de la respuesta en estado estacionario. Las entradas de prueba (escalón, rampa, parábola) son herramientas esenciales para evaluar el desempeño del sistema.**
