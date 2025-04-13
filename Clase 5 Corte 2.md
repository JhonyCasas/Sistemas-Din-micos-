# Trabajo, Energía y Potencia en Sistemas Mecánicos

El estudio del trabajo, energía y potencia en sistemas mecanicos traslacionales y rotacionales permite analizar la transferencia y transformación de energía en componentes mecánicos. Estos conceptos son esenciales para diseñar máquinas eficientes y predecir su comportamiento dinámico.

## 1. Definiciones Fundamentales

>🔑 *Trabajo (W):*
**Traslacional:** $W = \int \vec{F} \cdot d\vec{x}$  
**Rotacional:** $W = \int \tau \, d\theta$  
*Unidad: Joule (J)*

>🔑 *Energía Cinética (T):*  
**Traslacional:** $T = \frac{1}{2}mv^2$  
**Rotacional:** $T = \frac{1}{2}J\omega^2$

>🔑 *Potencia (P):*  
**Traslacional:** $P = \vec{F} \cdot \vec{v}$  
**Rotacional:** $P = \tau \cdot \omega$  
*Unidad: Watt (W)*


### 2.2 Potencia Rotacional
>🔑 *Potencia instantánea:* Tasa de transferencia de energía:
$P = \tau \cdot ω \quad [W]$

💡**Ejemplo 1:** Motor que genera 50 N·m a 300 rpm:
$P = 50 \times (300 \times \frac{2π}{60}) = 1570.8\,W$



## 3. Analogías entre Sistemas

| Concepto          | Traslacional               | Rotacional                  |
|-------------------|----------------------------|-----------------------------|
| **Fuerza/Par**    | F [N]                      | τ [N·m]                     |
| **Desplazamiento**| x [m]                      | θ [rad]                     |
| **Inercia**       | m [kg]                     | J [kg·m²]                   |
| **Rigidez**       | k [N/m]                    | k [N·m/rad]                 |
| **Amortiguamiento**| b [N·s/m]                 | b [N·m·s/rad]               |

*Tabla 1: Correspondencia entre variables traslacionales y rotacionales*


## 4. Principios Energéticos

### 4.1 Teorema Trabajo-Energía
**Para ambos sistemas:**
$W_{neto} = \Delta T$

### 4.2 Conservación de Energía
**Sistema conservativo:**  
$T_1 + U_1 = T_2 + U_2$

### 4.2 Conversión Traslacional-Rotacional
![Sistema polea-masa](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20160440.png)  
*Figura 1: Equivalencia energética en sistemas combinados*

## 5. Aplicaciones Prácticas

### 5.1 Mecanismo Polea-Masa

**Descripción:**  
Sistema que combina movimiento lineal (masa) y rotacional (polea) mediante una cuerda inextensible.

**Relaciones fundamentales:**
- Cinemática:  
  $v = r\omega$  
  $a = r\alpha$
- Energética:  
  $E_{total} = \frac{1}{2}mv^2 + \frac{1}{2}J\omega^2 + mgh$

**Aplicaciones:**  
Sistemas de izado, ascensores simples, contrapesos.

---

### 5.2 Sistema Cremallera-Piñón

**Principio de funcionamiento:**  
Convierte rotación del piñón en traslación lineal de la cremallera.

**Ecuaciones clave:**
- Desplazamiento:  
  $x = r\theta $
- Fuerza/Par:  
  $F = \frac{\tau}{r}$
- Potencia:  
  $P = \tau\omega = Fv$

**Usos típicos:**  
Dirección automotriz, posicionadores lineales en CNC.

---

### 5.3 Tornillo Sin Fin

**Características:**  
Transformación movimiento rotacional-lineal mediante paso helicoidal.

**Relación velocidad:**
$v = \frac{p}{2\pi}\omega$

**Ventajas:**  
Alta reducción de velocidad en espacio reducido.

**Aplicaciones:**  
Prensas, gatos mecánicos, sistemas de posicionamiento vertical.

---

### 5.4 Sistema Banda-Polea con Masa

**Dinámica del sistema:**
$a = \frac{\tau/r}{m + J/r^2}$

**Componentes críticos:**
- Inercia equivalente del sistema
- Tensión en la banda/cuerda
- Rozamiento en cojinetes

**Ejemplo industrial:**  
Transmisión de potencia en maquinaria de fabricación.

---

### 5.5 Tren de Engranajes con Carga Lineal

**Concepto:**  
Combinación de reducción angular y conversión a movimiento lineal.

**Inercia equivalente:**
$J_{eq} = J_1 + \left(\frac{N_1}{N_2}\right)^2 J_2$

**Implementaciones:**  
Robots articulados, sistemas de apertura automática.

---

## 6. Ejercicios

📚**Ejercicio 1:**  Se aplica un par T a la flecha 1 en el sistema de tren de engranes. Obténgase la ecuación de movimiento del sistema. Supóngase que los 
momentos de inercia de los engranes son J1 y J, como se muestra en el diagrama y que 
el par de carga es TL

![Sistema polea-masa](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20160440.png)  

**Para la flecha 1:**

$\[ J_1 \ddot{\theta}_1 = -k\theta_1 - T_1 + T \]$

**Para la flecha 2:**

$\[ J_2 \ddot{\theta}_2 = -b \dot{\theta}_2 - T_L + T_2 $\]

. **Relación cinemática:**

$\[ r_1 \theta_1 = r_2 \theta_2 \]$

2. **Equilibrio de potencia (trabajo):**
   
$\[ T_1 \dot{\theta}_1 = T_2 \dot{\theta}_2 \]$

4. **Relación de pares:**
   
$\[ \frac{T_1}{T_2} = \frac{\theta_2}{\theta_1} = \frac{r_1}{r_2} \]$ 

---

### Ecuación Combinada

Sustituyendo $\( T_2 \)$:

$\[ J_2 \ddot{\theta}_2 + b \dot{\theta}_2 + T_L = T_1 \frac{r_2}{r_1} \]$

**Solución:**
$ω = 1200 \times \frac{2π}{60} = 125.66\,rad/s$
$T = \frac{1}{2} \times 2 \times (125.66)^2 = 15,796\,J$

📚**Ejercicio 2:** Determinar la potencia disipada en un amortiguador rotacional (b = 0.1 N·m·s/rad) a 100 rad/s.
$P = bω^2 = 0.1 \times (100)^2 = 1000\,W$

📚 **Ejercicio 3 (Rotacional):**  
Motor (J=0.8 kg·m²) acelera de 0 a 1800 rpm en 5 s. Calcular potencia media.  
**Solución:**  
$\omega = 1800 \times \frac{2\pi}{60} = 188.5\,rad/s$  
$P_{med} = \frac{\Delta T}{\Delta t} = \frac{\frac{1}{2} \times 0.8 \times (188.5)^2}{5} = 2.84\,kW$

📚 **Ejercicio 4 (Rotacional-Traslacional):**  
Un piñón (J = 0.05 kg·m², r = 0.08 m) acciona una cremallera con masa de 4 kg. Si se aplica un par constante de 3 N·m:  
a) Determinar la aceleración lineal de la cremallera  
b) Calcular la potencia transmitida a t = 1.5 s

**Solución:**  
a) $a = \frac{\tau/r}{m + J/r^2} = \frac{3/0.08}{4 + 0.05/(0.08)^2} = 4.29\,m/s^2$  
b) $v = at = 4.29 \times 1.5 = 6.44\,m/s$  
$P = \tau \cdot \omega = 3 \times (6.44/0.08) = 241.5\,W$

Una palanca de 0.7 m (masa despreciable) conectada a una rueda dentada (J = 0.15 kg·m², r = 0.1 m) soporta una fuerza de 40 N en su extremo. Calcular:  
a) La aceleración angular inicial  
b) La velocidad después de 90° de giro


---


## 7. Conclusiones
1. El trabajo y energía rotacional siguen principios análogos a los sistemas traslacionales
2. Las conversiones entre movimiento lineal y angular siguen relaciones geométricas
3. Los modelos energéticos permiten analizar sistemas complejos combinados  
4. Los momentos de inercia determinan la respuesta dinámica del sistema

## 8. Referencias
1. Ogata, K. (1987). DINAMICA DE SISTEMAS. Prentice.
2. Kuo, B. (1996). SISTEMAS DE CONTROL AUTOMATICO. 
