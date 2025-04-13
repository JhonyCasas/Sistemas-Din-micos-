# Dinámica Rotacional: Conceptos Fundamentales y Aplicaciones

## 1. Conceptos Básicos y Definiciones

>🔑 **Inercia rotacional (J):** Propiedad de un cuerpo que cuantifica su resistencia a cambios en su movimiento de rotación. Depende de la distribución de masa respecto al eje:
$J = \int r^2 dm$
*Ejemplo:* Para un disco sólido: $J = \frac{1}{2}MR^2$

>🔑 **Par torsional (τ):** Medida de la tendencia de una fuerza a causar rotación:
$\tau = r \times F = rF\sinθ$ 
*Unidad:* N·m (Newton-metro)

## 2. Segunda Ley de Newton para Rotación

### Formulación Básica:
$\sum \tau = J\alpha $
donde:
- $\sum \tau$ = Suma de pares
- $J$ = Momento de inercia
- $\alpha$ = Aceleración angular ($rad/s^2$)

### Analogía Traslacional-Rotacional:
| Traslación       | Rotación          |
|------------------|-------------------|
| Fuerza (F)       | Par (τ)           |
| Masa (m)         | Inercia (J)       |
| Aceleración (a)  | Aceleración (α)   |

## 3. Ejemplos de Aplicación

### 💡3.1 Sistema Básico: Volante
**Configuración:**
- Disco de acero (M = 50 kg, R = 0.2 m)
- Par aplicado: 10 N·m

**Cálculos:**
1. Momento de inercia:
   $J = \frac{1}{2}MR^2 = \frac{1}{2}(50)(0.2)^2 = 1\,kg\cdot m^2$

3. Aceleración angular:
$\alpha = \frac{\tau}{J} = \frac{10}{1} = 10\,rad/s^2$

### 💡3.2 Sistema Motor-Engranaje
**Componentes:**
- Motor: $τₘ = 2 N·m, Jₘ = 0.05 kg·m²$
- Engranaje: relación 4:1
- Carga: J_c = 0.8 kg·m²

**Análisis:**
1. Inercia equivalente en eje motor:
   
   $J_{eq} = J_m + (\frac{1}{4})^2 J_c = 0.05 + 0.05 = 0.1\,kg\cdot m^2$

3. Aceleración del sistema:
$\alpha = \frac{\tau_m}{J_{eq}} = \frac{2}{0.1} = 20\,rad/s^2$

## 4. Casos de Estudio Avanzados

### 4.1 Péndulo Físico
$\tau = -mgL\sinθ$
$J\ddot{θ} + mgLθ = 0 \quad (\text{para pequeñas oscilaciones})$

**Frecuencia natural:**
$ω_n = \sqrt{\frac{mgL}{J}}$

### 4.2 Sistema Masa-Resorte Rotacional
![Sistema rotacional](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20151731.png)

**Ecuación diferencial:**
$J\ddot{θ} + b\dot{θ} + kθ = \tau(t)$

## 5. Tabla de Momentos de Inercia Comunes

| Cuerpo          | Eje           | Momento de Inercia       |
|-----------------|---------------|--------------------------|
| Varilla delgada | Por centro    | $\frac{1}{12}ML^2$      |
| Disco sólido    | Perpendicular | $\frac{1}{2}MR^2$        |
| Esfera sólida   | Diámetro      | $\frac{2}{5}MR^2$        |
| Cilindro hueco  | Longitudinal  | $M(R_1^2 + R_2^2)$       |

## 6. Ejercicios Resueltos

📚 **Ejercicio 1:** Calcular el par necesario para acelerar un volante (J = 2 kg·m²) desde reposo hasta 100 rpm en 5 segundos.

**Solución:**
1. Convertir rpm a rad/s:
   
$ω = 100\times\frac{2π}{60} = 10.47\,rad/s$

3. Calcular α:
$α = \frac{Δω}{Δt} = \frac{10.47}{5} = 2.094\,rad/s^2$

4. Calcular τ:
$τ = Jα = 2\times2.094 = 4.19\,N\cdot m$

📚 **Ejercicio 2:** Sistema con J = 0.5 kg·m², b = 0.1 N·m·s/rad, k = 20 N·m/rad. Determinar tipo de amortiguamiento cuando se aplica un par de 5 N·m.

**Solución:**
1. Amortiguamiento crítico:
$b_c = 2\sqrt{Jk} = 2\sqrt{0.5\times20} = 6.32\,N\cdot m\cdot s/rad$

2. Comparación:
   $b = 0.1 < b_c \Rightarrow \text{Sistema subamortiguado}$

   ## 7. Conclusión

La dinámica rotacional provee herramientas fundamentales para analizar sistemas mecánicos en rotación mediante:

1. **Conceptos clave**:
   - Segunda Ley de Newton rotacional: ∑τ = Jα
   - Momentos de inercia (J) y pares torsionales (τ)
   
2. **Aplicaciones**:
   - Diseño de motores y transmisiones
   - Análisis de sistemas oscilatorios
   - Optimización de componentes rotativos

## 8.Referencias

1. Beer, F. P., & Johnston, E. R. (2019). *Mecánica Vectorial para Ingenieros: Dinámica*. McGraw-Hill.  
2. Norton, R. L. (2020). *Diseño de Maquinaria*. McGraw-Hill.  
3. Ogata, K. (1978). DINAMICA DE SISTEMAS. Prentice.
