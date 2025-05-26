# Sistemas de primer orden

Los sistemas de primer orden son fundamentales en el estudio de sistemas dinámicos y control automático. Estos sistemas se caracterizan por tener una ecuación diferencial de primer orden y su respuesta temporal puede ser analizada mediante funciones de transferencia. En esta clase, se exploran los conceptos clave como la forma canónica, la constante de tiempo, la ganancia estática, y las respuestas a entradas escalón y rampa.

---

## 1. Ecuaciones diferenciales de primer orden

🔑 **Definición**: *Ecuación diferencial de primer orden*  
Una ecuación diferencial de primer orden tiene la forma general:  
$a\dot{y}(t) + by(t) = cu(t)$  
donde $\( y(t) \)$ es la salida, $\( u(t) \)$ es la entrada, y $\( a, b, c \)$ son parámetros constantes del sistema.

- Aplicando la transformada de Laplace, se obtiene la función de transferencia:  
$\frac{Y(s)}{U(s)} = \frac{c}{as + b}$

---

## 2. Forma canónica de los sistemas de primer orden

La forma canónica permite identificar parámetros temporales como la constante de tiempo $(\( \tau \)$ y la ganancia estática $(\( K \)$:  
$\frac{Y(s)}{U(s)}$ = $\frac{K}{\tau s + 1}$  
donde:  
- $\( \tau = \frac{a}{b} \)$ (constante de tiempo)  
- $\( K = \frac{c}{b} \)$ (ganancia estática).  

💡 **Ejemplo 1**:  
Para la función de transferencia:  
$\frac{Y(s)}{U(s)} = \frac{0.8}{s + 4}$  
Al convertirla a forma canónica:  
$\frac{Y(s)}{U(s)} = \frac{0.2}{0.25s + 1}$  
Se obtiene $\( \tau = 0.25 \)$ segundos y $\( K = 0.2 \)$.

---

## 3. Respuesta temporal de sistemas de primer orden

### 3.1. Respuesta a una entrada escalón

La salida $\( y(t) \)$ ante una entrada escalón de amplitud $\( A \)$ es:  
$y(t) = AK \left(1 - e^{-\frac{t}{\tau}}\right)$  

- **Estado transitorio**: Dominado por el término exponencial.  
- **Estado estacionario**: Valor final $\( AK \)$.

- *Figura 1*.

![Comparación entradas](https://github.com/JhonyCasas/Sistemas-Din-micos-/blob/main/Imagenes%20Apuntes/Grafica%207.png)
 

### 3.2. Respuesta a una entrada rampa

Para una entrada rampa, la salida es:  
$y(t) = AK \left(t - \tau + \tau e^{-\frac{t}{\tau}}\right)$  

- En estado estacionario, la salida sigue una rampa con pendiente $\( AK \)$.  

---

## 4. Ubicación de polos

Los sistemas de primer orden tienen un solo polo ubicado en:  
$s = -\frac{1}{\tau}$  

- Un polo negativo indica estabilidad.  
- La respuesta del sistema es más rápida cuanto más alejado esté el polo del eje imaginario.  

---

## 5. Ejercicios

📚 **Ejercicio 1**:  
Identificar $\( \tau \)$ y $\( K \)$ para la función de transferencia:  
$\frac{Y(s)}{U(s)}$ = $\frac{5}{2s + 16}$  

**Solución**:  
Convertir a forma canónica:  
$\frac{Y(s)}{U(s)}$ = $\frac{0.3125}{0.125s + 1}$  
Por lo tanto, $\( \tau = 0.125 \)$ segundos y $\( K = 0.3125 \)$.  

📚 **Ejercicio 2**:  
Calcular la salida $\( y(t) \)$ en $\( t = \tau \)$ para un sistema con $\( K = 2 \)$, $\( \tau = 3 \)$, y entrada escalón $\( A = 1 \)$.  

**Solución**:  
Usando la fórmula de respuesta a escalón:  
$y(\tau) = 2\left(1 - e^{-1}\right) \approx 1.264$  

---

## 6. Conclusiones

- Los sistemas de primer orden se modelan mediante ecuaciones diferenciales lineales y sus respuestas son exponenciales.  
- La forma canónica simplifica el análisis al destacar parámetros clave como $\( \tau \) y \( K \)$.  
- Las respuestas a escalón y rampa permiten evaluar el comportamiento transitorio y estacionario.  

## 7. Referencias

- Ogata, K. *Ingeniería de Control Moderna*. 4ª edición. Prentice Hall.  
- Presentación: "Función de transferencia" por Ing. Jorge Eduardo Cote Ballesteros (2025). 
