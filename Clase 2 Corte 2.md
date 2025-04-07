# Modelado de Sistemas Masa-Resorte-Amortiguador

El análisis de sistemas mecánicos mediante el modelo masa-resorte-amortiguador es fundamental para entender comportamientos dinámicos en ingeniería. Este repositorio se enfoca en el modelamiento matemático de estos sistemas utilizando las Leyes de Newton y la Ley de Hooke.

## 1. Descripción del Sistema

### 1.1 Componentes básicos
> 🔑 *Sistema MRA:* Configuración mecánica compuesta por:
> - **Masa (m):** Elemento inercial (kg)
> - **Resorte (k):** Elemento elástico (N/m)
> - **Amortiguador (c):** Elemento disipativo (N·s/m)

* Primero escribimos ![](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/Captura%20de%20pantalla%202025-04-07%20160251.png).
*Figura 1: Sistema masa-resorte-amortiguador (adaptado de Fig. 2-23)*

## 2. Modelamiento Matemático

### 2.1 Ecuación diferencial del movimiento
Aplicando la segunda ley de Newton:

$$m\ddot{x} + c\dot{x} + kx = F(t)$$

💡**Ejemplo 1:** Para el sistema mostrado en la Figura 1:
- Si m=2 kg, c=4 N·s/m, k=10 N/m
- Con fuerza externa F(t)=5sin(2t) N
- La ecuación queda:
$$2\ddot{x} + 4\dot{x} + 10x = 5\sin(2t)$$

### 2.2 Representación en espacio de estados
Se puede expresar como:

$$
\begin{cases}
\dot{x}_1 = x_2 \\
\dot{x}_2 = -\frac{c}{m}x_2 - \frac{k}{m}x_1 + \frac{1}{m}F(t)
\end{cases}
$$

## 3. Simulación en MATLAB

### 3.1 Implementación básica
```matlab
% Parámetros del sistema
m = 2;     % kg
k = 10;    % N/m
c = 4;     % N·s/m

% Función para resolver la EDO
function dx = mra_system(t,x)
    F = 5*sin(2*t);  % Fuerza externa
    dx = zeros(2,1);
    dx(1) = x(2);
    dx(2) = (-c*x(2) - k*x(1) + F)/m;
end

% Condiciones iniciales y tiempo
x0 = [0.1; 0];  % x(0)=0.1m, v(0)=0m/s
tspan = [0 10];

% Solución
[t,x] = ode45(@mra_system, tspan, x0);

% Gráfica
plot(t, x(:,1))
xlabel('Tiempo (s)')
ylabel('Desplazamiento (m)')
grid on
