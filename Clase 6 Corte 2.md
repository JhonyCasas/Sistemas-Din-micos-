# Dinámica de Sistemas Eléctricos con Amplificadores Operacionales

Los amplificadores operacionales (op-amps) son componentes fundamentales en sistemas eléctricos y electrónicos, especialmente en computadoras analógicas. Estos dispositivos permiten realizar operaciones matemáticas como integración, suma e inversión de signo, gracias a su alta ganancia y características específicas. En esta clase, exploraremos su funcionamiento, aplicaciones y configuraciones básicas.

## 1. Fundamentos de Amplificadores Operacionales
### 1.1. Características ideales vs. reales
### 1.2. Configuraciones básicas: inversor, no inversor y seguidor de voltaje

## 2. Definiciones

>🔑*Definición:* Un *amplificador operacional* es un dispositivo electrónico de alta ganancia utilizado para realizar operaciones matemáticas en señales analógicas, como suma, integración e inversión de signo.

>🔑 *Slew rate:* Tasa máxima de cambio del voltaje de salida de un op-amp, medida en V/µs. Limita la respuesta dinámica en señales de alta frecuencia.

## 3. Modelado Dinámico de Op-Amps
### 3.1. Función de transferencia
$H(s) = \frac{A_0}{1 + \frac{s}{\omega_c}}$
Donde $\( A_0 \)$ es la ganancia DC y $\( \omega_c \)$ la frecuencia de corte.

### 3.2. Diagramas de Bode
![Diagrama de Bode de un op-amp](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/2025-04-13%20192522.png)  
Figura 1. Respuesta en frecuencia típica de un amplificador operacional

## 4. Ejemplos

💡**Ejemplo 1:** Calcular la frecuencia de corte de un circuito inversor con $\( R_1 = 1k\Omega \) , \( R_2 = 10k\Omega \)$ y op-amp con $\( GBW = 1MHz \)$:
$f_c = \frac{GBW}{1 + \frac{R_2}{R_1}} = \frac{1MHz}{11} \approx 90.9kHz$

💡**Ejemplo 2:**  
Con $R_o = 1 \text{MΩ}$, $R_1 = 0.25 \text{MΩ}$, $R_2 = 1 \text{MΩ}$:  
$e_o = -(4e_1 + 1e_2)$


## 5. Ejercicios
📚 **Ejercicio 1:**  
Calcule $e_o$ en un inversor con $R_i = 0.1 \text{MΩ}$, $R_o = 1 \text{MΩ}$ y $e_i = 3 \text{V}$.  
*Solución:*  
$e_o = -\left(\frac{1}{0.1}\right) \times 3 = -30 \text{V}$

📚 **Ejercicio 2:**  
Diseñe un sumador que calcule $e_o = -(2e_1 + 5e_2)$. Use $R_o = 10 \text{MΩ}$.  
*Solución:*  
- $R_1 = \frac{10}{2} = 5 \text{MΩ}$  
- $R_2 = \frac{10}{5} = 2 \text{MΩ}$  



## 6. Aplicaciones Dinámicas
### 6.1. Filtros activos

| **Tipo**       | **Función de Transferencia**          | **Aplicación**         |
|----------------|---------------------------------------|------------------------|
| Pasa-bajas     | $\( \frac{1}{1 + sRC} \)$               | Eliminar ruido         |
| Pasa-altas     | $\( \frac{sRC}{1 + sRC} \)$             | Acoplamiento AC        |
| Pasa-banda     | $\( \frac{sRC}{1 + 2sRC + (sRC)^2} \)$  | Comunicaciones         |

Tabla 1. Comparación de filtros activos básicos

### 7.2. Osciladores
```matlab
% Simulación de oscilador Wien en MATLAB
R = 10e3; C = 10e-9; 
f = 1/(2*pi*R*C); % Frecuencia de oscilación
disp(['Frecuencia: ', num2str(f), ' Hz']);

````
## 8. Conclusiones
Los amplificadores operacionales permiten implementar sistemas dinámicos complejos mediante configuraciones adecuadas. El análisis de su respuesta en frecuencia y criterios de estabilidad es esencial para diseños prácticos.

9. Referencias
García Z., J. (2018). Electrónica Analógica: Amplificadores Operacionales y Aplicaciones. Editorial Limusa.

Martínez López, R. (2020). Diseño de Circuitos con Amplificadores Operacionales. McGraw-Hill Interamericana.
