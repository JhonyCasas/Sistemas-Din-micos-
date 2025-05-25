# Modelamiento de sistemas con diagramas de bloques

Esta clase aborda el modelamiento de sistemas dinámicos utilizando diagramas de bloques, una herramienta fundamental en ingeniería de control para representar y analizar sistemas complejos. Se exploran componentes como solenoides, motores DC, engranajes, y sensores, junto con sus respectivas funciones de transferencia y ecuaciones diferenciales. El enfoque integra aspectos eléctricos, mecánicos y térmicos para construir modelos completos.

---

## 1. Componentes y modelos básicos

### 1.1. Solenoide
- Modelado como un sistema electromecánico que combina un circuito eléctrico, un transductor y un sistema mecánico de traslación.
- **Parte eléctrica**:  
  $$L \frac{di}{dt} + R i = v(t) \quad I(s) = V(s) \frac{1}{L s + R}$$  
- **Transductor**: Fuerza proporcional a la corriente:  
  $$f_s = K_s i \quad F_s(s) = K_s I(s)$$  
- **Parte mecánica**: Sistema masa-resorte-amortiguador:  
  $$m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + kx = f(t) \quad X(s) = F(s) \frac{1}{ms^2 + bs + k}$$  

🔑 *Definición*: Un *solenoide* es un dispositivo que convierte energía eléctrica en movimiento mecánico lineal mediante un campo electromagnético.

### 1.2. Motor DC
- **Corriente de campo**:  
  - Modelo eléctrico:  
    $$L_c \frac{di_c}{dt} + R_c i_c = v_c(t) \quad I_c(s) = V_c(s) \frac{1}{(sL_c + R_c)}$$  
  - Torque generado:  
    $$T_m(s) = K_m I_c(s)$$  
  - Parte mecánica:  
    $$\Theta(s) = T_c(s) \frac{1}{(s^2 J + b s)}$$  

- **Corriente de armadura**:  
  - Voltaje inducido:  
    $$V_b(s) = K_b \omega(s)$$  
  - Ecuación combinada:  
    $$I_a(s) = \frac{V_a(s) - K_b \omega(s)}{sL_a + R_a}$$  

💡 **Ejemplo 1**: Para un motor DC con corriente de campo constante, la función de transferencia entre el ángulo $\Theta(s)$ y el voltaje $V_a(s)$ es:  
$$\frac{\Theta(s)}{V_a(s)} = \frac{K_m}{(sL_a + R_a)(Js^2 + bs)}$$  

---

## 2. Elementos transmisores de energía

### 2.1. Engranajes y poleas
- Relación de torque y velocidad angular:  
  $$\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1} \quad \frac{\theta_1}{\theta_2} = -\frac{N_2}{N_1}$$  
- Inercia equivalente:  
  $$J_{\text{equiv}} = J_{N1} + \left(\frac{N_1}{N_2}\right)^2 (J + J_{N2})$$  

### 2.2. Palancas
- Relación de fuerzas y desplazamientos:  
  $$\frac{f_2}{f_1} = \frac{d_1}{d_2} \quad \frac{x_1}{x_2} = -\frac{d_1}{d_2}$$  

---

## 3. Sensores y transductores

### 3.1. Potenciómetros
- **Rotación**:  
  $$V_o = \frac{\theta}{\theta_{\text{max}}} V_{ac}$$  
- **Translación**:  
  $$V_o = \frac{x}{x_{\text{max}}} V_{ac}$$  

### 3.2. Tacómetros
- Dispositivos que convierten velocidad angular en voltaje.  

🔑 *Definición*: Un *tacómetro* es un sensor que mide la velocidad rotacional y la traduce a una señal eléctrica proporcional.

---

## 4. Modelos de procesos industriales

### 4.1. Mezcla de sustancias
- Función de transferencia para un tanque de mezcla:  
  $$G(s) = \frac{Q(s)}{Q_i(s)} = \frac{\rho_{\text{inicial}}s + \rho_{\text{in}}v_{\text{in}}}{s + v_{\text{out}}}$$  

💡 **Ejemplo 2**: Tanque con 8 L de agua y 2 kg de sal, entrada de 4 L/min (3 kg/L):  
$$G(s) = \frac{2s + 12}{s + 4}$$  

### 4.2. Sistema térmico
- Modelo de transferencia de calor:  
  $$G(s) = \frac{T(s)}{Q_{\text{in}}(s)} = \frac{1/C}{s + 1/RC}$$  

---

## 📚 Ejercicios

### Ejercicio 1
**Enunciado**: Calcule la función de transferencia $X(s)/V(s)$ para un solenoide con $L = 0.1\,H$, $R = 2\,\Omega$, $m = 0.5\,kg$, $b = 1\,N\cdot s/m$, $k = 10\,N/m$, y $K_s = 0.3\,N/A$.  

**Solución**:  
$$\frac{X(s)}{V(s)} = \frac{K_s}{(Ls + R)(ms^2 + bs + k)} = \frac{0.3}{(0.1s + 2)(0.5s^2 + s + 10)}$$  

### Ejercicio 2
**Enunciado**: Determine la inercia equivalente $J_{\text{equiv}}$ para un sistema con engranajes donde $J_{N1} = 0.2\,kg\cdot m^2$, $J_{N2} = 0.5\,kg\cdot m^2$, $J = 1\,kg\cdot m^2$, y relación $N_1/N_2 = 0.5$.  

**Solución**:  
$$J_{\text{equiv}} = 0.2 + (0.5)^2 (1 + 0.5) = 0.2 + 0.25 \times 1.5 = 0.575\,kg\cdot m^2$$

###  Ejercicio 3

*Figura 1*.
![Comparación entradas](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/Grafica%204.png)

*Figura 2*.
![Comparación entradas](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/Grafica%203%20.png)

- $\overline{\Theta}_i$ = temperatura en estado estable del líquido que entra, °C  
- $\overline{\Theta}_o$ = temperatura en estado estable del líquido que sale, °C  
- $G$ = velocidad de flujo del líquido en estado estable, kg/seg  
- $M$ = masa del líquido en el tanque, kg  
- $c$ = calor específico del líquido, kcal/kg°C  
- $R$ = resistencia térmica, °C·seg/kcal  
- $C$ = capacitancia térmica, kcal/°C  
- $H$ = entrada del flujo de calor en estado estable, kcal/seg


Se tiene:

- $h_o = G c \theta$
- $C = M c$
- $R = \dfrac{\theta}{h_o} = \dfrac{1}{G c}$

La ecuación diferencial para este sistema es:

$$
C \, d\theta = (h_i - h_o) \, dt
$$

o bien:

$$
C \, \dfrac{d\theta}{dt} = h_i - h_o
$$

$\[RC \frac{d\theta}{dt} + \theta = Rh_i\]$

$\[\frac{\Theta(s)}{H_i(s)} = \frac{R}{RCs + 1}\]$

$\[C \, d\theta = (Gc\theta_i - h_o) \, dt\]$

$\[C \frac{d\theta}{dt} = Gc\theta_i - h_o\]$

$\[RC \frac{d\theta}{dt} + \theta = \theta_i\]$

$\[\frac{\Theta(s)}{\Theta_i(s)} = \frac{1}{RCs + 1}\]$

$\[RC \frac{d\theta}{dt} + \theta = \theta_i + Rh_i\]$


---

## Conclusiones
El modelamiento con diagramas de bloques permite integrar múltiples subsistemas (eléctricos, mecánicos, térmicos) en un marco unificado. A través de funciones de transferencia y relaciones físicas, se simplifica el análisis y diseño de sistemas complejos. Los ejemplos y ejercicios ilustran la aplicabilidad en problemas reales, desde actuadores hasta procesos industriales.

---

## Referencias
- Hernández, R. (2010). *Introducción a los sistemas de control*. Pearson.  
- Chen, C. *Analog and digital control system design*. Saunders College Publishing.  
