# Modelado de Sistemas Masa-Resorte-Amortiguador (MRA)

El modelamiento de sistemas mecánicos mediante el enfoque MRA (Modelado y Respuesta en la Amplitud) es fundamental para analizar el comportamiento dinámico de sistemas físicos, como vibraciones en estructuras, amortiguamiento y respuesta a excitaciones armónicas. Esta técnica permite representar sistemas complejos mediante ecuaciones diferenciales y funciones de transferencia, facilitando el diseño y la optimización de sistemas mecánicos. 

## 1. Descripción del Sistema

### 1.1 Fundamentos del Modelamiento MRA  

El modelamiento MRA se basa en describir sistemas mecánicos mediante ecuaciones que relacionan fuerzas, desplazamientos y propiedades del sistema (masa, rigidez, amortiguamiento).  

### 1.2 Definiciones 

>🔑 *Modelamiento MRA:* Proceso de representar un sistema mecánico mediante ecuaciones matemáticas para predecir su respuesta dinámica bajo diversas condiciones.  
>🔑 *Función de Transferencia:* Relación entre la salida y la entrada de un sistema en el dominio de la frecuencia, expresada como \( H(s) = \frac{X(s)}{F(s)} \).  
### 1.2 Componentes básicos
> - **Masa (m):** Representa la inercia del sistema (unidades: kg)
> - **Resorte (k):** Proporciona rigidez elástica (unidades: N/m)
> - **Amortiguador (c):** Modela la disipación viscosa (unidades: N·s/m)

![Diagrama MRA](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-07%20155735.png)  
*Figura 1: Sistema masa-resorte-amortiguador con notación estándar*

### 1.2 Configuraciones típicas
- **Sistema vertical:** Para análisis de suspensiones
- **Sistema horizontal:** Para estudios de vibraciones
- **Múltiples grados de libertad:** Sistemas acoplados


## 2. Introducción a los Diagramas de Cuerpo Libre (DCL)
Los diagramas de cuerpo libre son herramientas visuales fundamentales en el análisis de sistemas mecánicos. Permiten representar todas las fuerzas que actúan sobre un cuerpo, facilitando la aplicación de las leyes de Newton y la formulación correcta de las ecuaciones dinámicas del sistema.

>🔑 *Diagrama de Cuerpo Libre:* Representación gráfica que muestra todas las fuerzas externas actuando sobre un cuerpo o sistema, esencial para aplicar correctamente las leyes del movimiento.

## 2.1 Construcción de un DCL para Sistemas Mecánicos

### 2.1..1 Pasos para elaborar un DCL
1. **Aislar el sistema**: Seleccionar el cuerpo de interés
2. **Identificar fuerzas**:
   - Fuerzas externas aplicadas
   - Fuerzas de restricción (reacciones)
   - Fuerzas elásticas (resortes)
   - Fuerzas de amortiguamiento
3. **Establecer sistema de referencia**

### 2.2. Elementos clave en sistemas MRA
- **Masa (m)**: Representa la inercia del sistema
- **Resorte (k)**: Proporciona fuerza elástica
- **Amortiguador (c)**: Genera fuerza viscosa

## 2.2. Aplicación del DCL en Sistemas Mecánicos

### 2.2.1 Sistema Masa-Resorte-Amortiguador horizontal
![DCL Sistema Horizontal](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20231054.png)

*Figura 2: Diagrama de cuerpo libre para sistema horizontal*

**Ecuación resultante**:
$m\ddot{x} + c\dot{x} + kx = F(t)$

### 2.2.2 Sistema Masa-Resorte-Amortiguador vertical
![DCL Sistema Vertical](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20230620.png)

*Figura 3: Diagrama de cuerpo libre para sistema vertical*

**Ecuación resultante**:
$m\ddot{x} + c\dot{x} + kx = mg$

## 3. Beneficios del Uso de DCL en el Modelamiento

### 33.1. Ventajas principales
- Visualización clara de las interacciones físicas
- Identificación sistemática de todas las fuerzas relevantes
- Reducción de errores en la formulación de ecuaciones
- Facilita el análisis de sistemas complejos

### 3.2. Casos de aplicación
1. Sistemas vibratorios simples
2. Mecanismos articulados
3. Estructuras sometidas a cargas dinámicas

## 4. Ejemplos Prácticos

💡**Ejemplo 1: Sistema con excitación armónica**
Para un sistema con m=2 kg, c=5 Ns/m, k=100 N/m y F(t)=10sin(5t) N:

1. DCL muestra:
   - Fuerza aplicada: 10sin(5t) →
   - Fuerza del resorte: 100x ←
   - Fuerza amortiguadora: 5ẋ ←

2. Ecuación:
   $2\ddot{x} + 5\dot{x} + 100x = 10\sin(5t)$

## 5. Modelamiento Matemático

### 5.1 Ecuación diferencial del movimiento
Aplicando la segunda ley de Newton y la ley de Hooke:

$m\frac{d^2x}{dt^2} + c\frac{dx}{dt} + kx = F(t)$

Donde:
- $x(t)$: Desplazamiento desde la posición de equilibrio (m)
- $F(t)$: Fuerza externa aplicada (N)


## 6. Análisis Dinámico

### 3.1 Parámetros característicos
| **Parámetro** | **Símbolo** | **Unidad**  |  
|---------------|-------------|-------------|  
| Masa          | $\( m \)$     | kg          |  
| Rigidez       | $\( k \)$     | N/m         |  
| Amortiguamiento | $\( c \)$   | N·s/m       |  

*Tabla 1: Parámetros de un sistema mecánico.*

### 3.2 Parámetros característicos
| Parámetro | Fórmula | Significado Físico |
|-----------|---------|--------------------|
| Frecuencia natural | $\omega_n = \sqrt{\frac{k}{m}}$ | Frecuencia de oscilación libre |
| Factor de amortiguamiento | $\zeta = \frac{c}{2\sqrt{mk}}$ | Razón amortiguamiento/crítico |
| Frecuencia amortiguada | $\omega_d = \omega_n\sqrt{1-\zeta^2}$ | Frecuencia con amortiguamiento |

### 3.3 Tipos de respuesta
1. **Subamortiguado** ($\zeta < 1$): Oscilaciones decrecientes
2. **Críticamente amortiguado** ($\zeta = 1$): Retorno más rápido sin oscilar
3. **Sobreamortiguado** ($\zeta > 1$): Retorno lento sin oscilar


   

## 7. Simulación Numérica

### 4.1 Implementación en MATLAB
```matlab
%% Parámetros del sistema
m = 2;       % masa [kg]
k = 50;      % rigidez [N/m]
c = 5;       % amortiguamiento [N·s/m]
F0 = 10;     % amplitud fuerza [N]
w = 3;       % frecuencia fuerza [rad/s]

%% Modelo en espacio de estados
A = [0 1; -k/m -c/m];
B = [0; 1/m];
C = [1 0];
sys = ss(A, B, C, 0);

%% Simulación
t = 0:0.01:10;                  % Vector tiempo
u = F0*sin(w*t);                % Entrada forzante
x0 = [0.1; 0];                  % Condiciones iniciales
[y, t, x] = lsim(sys, u, t, x0);

%% Visualización
figure
subplot(2,1,1)
plot(t, y)
title('Respuesta temporal')
xlabel('Tiempo [s]')
ylabel('Desplazamiento [m]')
grid on

subplot(2,1,2)
plot(t, u)
xlabel('Tiempo [s]')
ylabel('Fuerza [N]')
grid on
````

## 8. Conclusiones
El modelamiento MRA permite analizar sistemas mecánicos mediante herramientas matemáticas y computacionales. La comprensión de sistemas 1DOF es la base para abordar problemas más complejos (MDOF).
## 9. Referencias
1. Ogata, K. (1978). DINAMICA DE SISTEMAS. Prentice.
2. Beer, F. P., & Johnston, E. R. (2019). Mecánica Vectorial para Ingenieros: Dinámica. McGraw-Hill.
