# Sistemas de Segundo Orden

Los sistemas de segundo orden son fundamentales en el estudio de sistemas dinámicos y control automático. Estos sistemas se modelan mediante ecuaciones diferenciales de segundo orden y su comportamiento se caracteriza por parámetros como la frecuencia natural, el factor de amortiguamiento y la ganancia estática. En esta clase, se exploran las formas canónicas, las respuestas temporales y los efectos de los ceros y el tiempo muerto en estos sistemas.

---

## 1. Ecuaciones Diferenciales de Segundo Orden

La estructura general de una ecuación de segundo orden es:

$$
j(t) + a_1y(t) + a_0y(t) = b_0u(t)
$$

Aplicando la transformada de Laplace, se obtiene la función de transferencia:

$$
\frac{Y(s)}{U(s)} = \frac{b_0}{s^2 + a_1s + a_0}
$$

🔑 *Definición*: La *función de transferencia* relaciona la salida \( Y(s) \) con la entrada \( U(s) \) en el dominio de Laplace, proporcionando una representación algebraica del sistema.

---

## 2. Forma Canónica de los Sistemas de Segundo Orden

La forma canónica permite identificar parámetros temporales clave:

$$
G(s) = \frac{K \cdot \omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
$$

Donde:
- \( K \): Ganancia estática.
- \( \omega_n \): Frecuencia natural.
- \( \zeta \): Factor de amortiguamiento.

🔑 *Definición*: El *factor de amortiguamiento* $\( \zeta \)$ determina si el sistema está sub-amortiguado $(\( \zeta < 1 \)$, críticamente amortiguado $(\( \zeta = 1 \)$ o sobre-amortiguado $(\( \zeta > 1 \)$.

---

## 3. Respuesta Temporal a un Escalón

La respuesta del sistema varía según el valor de $\( \zeta \)$:

- **Sub-amortiguado $(\( \zeta < 1 \))**: y(t) = K \cdot A \cdot \left(1 - e^{-\zeta \omega_n t} \left(\cos(\omega_d t) + \frac{\zeta}{\sqrt{1-\zeta^2}} \sin(\omega_d t)\right)\right)$
  Donde $\( \omega_d = \omega_n \sqrt{1-\zeta^2} \)$.

- **Críticamente amortiguado $(\( \zeta = 1 \))**: y(t) = K \cdot A \cdot (1 - e^{-\omega_n t} (1 + \omega_n t)$

- **Sobre-amortiguado (\( \zeta > 1 \))**:y(t) = K \cdot A \cdot \left(1 - e^{-\left(\zeta - \sqrt{\zeta^2 - 1}\right)\omega_n t}\right)$

---

## 4. Parámetros Temporales en Sistemas Sub-amortiguados

- **Tiempo de pico $(\( t_p \))$

  t_p = \frac{\pi}{\omega_n \sqrt{1-\zeta^2}}$
  
- **Tiempo de establecimiento $(\( t_s \))**:$
  - Para 2%: $\( t_s \approx \frac{4}{\zeta \omega_n} \)$
  - Para 5%: $\( t_s \approx \frac{3}{\zeta \omega_n} \)$

💡 **Ejemplo 1**: Para $\( G(s) = \frac{36}{s^2 + 4.2s + 36} \)$, se tiene $\( \omega_n = 6 \)$ y $\( \zeta = 0.35 \)$. El sistema es sub-amortiguado.

---

## 5. Efecto de los Ceros

Los ceros afectan el estado transitorio pero no el estado estacionario. Por ejemplo:

$$
Y_1(s) = \frac{2}{s(s+5)} \quad \text{y} \quad Y_2(s) = \frac{s+2}{s(s+5)}
$$

Las respuestas son:
- \( y_1(t) = 0.4(1 - e^{-5t}) \)
- \( y_2(t) = 0.4 + 0.6e^{-5t} \)

---

## 6. Tiempo Muerto

El tiempo muerto \( t_0 \) se representa en el dominio de Laplace como:

$$
G(s) = \frac{K \cdot e^{-s t_0}}{\tau s + 1}
$$

🔑 *Definición*: El *tiempo muerto* es un retardo en la respuesta del sistema, representado por una exponencial en el dominio de Laplace.

---

## 7. Ejercicios

📚 **Ejercicio 1**: Determine los parámetros \( \omega_n \) y \( \zeta \) para el sistema con función de transferencia \( G(s) = \frac{20}{s^2 + 6s + 20} \).

**Solución**:
- $\( \omega_n = \sqrt{20} \approx 4.47 \)$
- $\( \zeta = \frac{6}{2 \cdot 4.47} \approx 0.67 \)$

📚 **Ejercicio 2**: Calcule el tiempo de pico $\( t_p \)$ para el sistema del Ejercicio 1.

**Solución**:
- $\( t_p = \frac{\pi}{4.47 \sqrt{1 - 0.67^2}} \approx 0.93 \)$ segundos.

---

## 8. Conclusiones

Los sistemas de segundo orden son esenciales para entender el comportamiento dinámico de muchos sistemas físicos. Sus parámetros $(\( \omega_n \), \( \zeta \)$, $\( K \)$ permiten predecir respuestas temporales y diseñar estrategias de control efectivas. Además, el efecto de los ceros y el tiempo muerto son consideraciones importantes en el análisis y diseño de sistemas.

---

## 9. Referencias

- Ogata, K. *Ingeniería de Control Moderna*. 5ª edición. Prentice Hall.
- Nise, N. *Control Systems Engineering*. 6ª edición. 2011.
- Hernández, R. *Introducción a los sistemas de control*. Pearson, 2010.
