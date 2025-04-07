# Solución de Ecuaciones Diferenciales por Método de Laplace  
El método de Laplace es una herramienta fundamental en ingeniería y matemáticas para resolver ecuaciones diferenciales lineales. Transforma ecuaciones diferenciales en ecuaciones algebraicas en el dominio de Laplace, simplificando su resolución. Esta clase cubre los conceptos básicos, aplicaciones y ejemplos prácticos.  

---

## 1. Introducción al Método de Laplace  
>🔑 *Transformada de Laplace:* Operación que convierte una función temporal  $$\( f(t) \)$$  en una función compleja  $$\( F(s) \)$$ , donde $$\( s = \sigma + j\omega \)$$ Se define como:

$$
{L}\{f(t)\} = \int_0^\infty f(t)e^{-st}dt
$$

### 1.1. Propiedades Clave  

- Linealidad: $$\( \mathcal{L}\{a f(t) + b g(t)\} = a F(s) + b G(s) \)$$.  
- Derivada: $$\( {L}\{f'(t)\} = sF(s) - f(0) \).$$  

---

## 2. Aplicación a Ecuaciones Diferenciales  
### 2.1. Pasos Básicos  
1. Aplicar Laplace a ambos lados de la ecuación.  
2. Resolver la ecuación algebraica resultante para $$\( F(s) \).$$  
3. Antitransformar para obtener $$\( f(t) \). $$ 

💡**Ejemplo 1:** Resolver $$\( \frac{dy}{dt} + 2y = e^{-t} \)$$ con $$\( y(0) = 1 \):$$  
1. Transformada: $$\( sY(s) - 1 + 2Y(s) = \frac{1}{s+1} \).$$  
2. Despejar $\( Y(s) \): Y(s) = \frac{s+2}{(s+1)(s+2)} = \frac{1}{s+1} $
 
5. Solución: $$\( y(t) = e^{-t} \)$$.  

---

## 3. Casos Especiales  
### 3.1. Funciones Discontinuas  
Para $$\( f(t) = u(t-a) \)$$ (escalón unitario):  
$$ \mathcal{L}\{u(t-a)\} = \frac{e^{-as}}{s} $$  

### 3.2. Convolución  
$$ {L}\{f(t) * g(t)\} = F(s) \cdot G(s) $$  

---

## 4. Ejercicios  
📚 **Ejercicio 1:** Resolver $$\( y'' + 3y' + 2y = 0 \)$$ con $$\( y(0) = 1, y'(0) = 0 \)$$.  
**Solución:**  
1. Transformada: $$\( s^2Y(s) - s + 3sY(s) - 3 + 2Y(s) = 0 \).$$  
2. $$\( Y(s) = \frac{s+3}{s^2 + 3s + 2} \).$$  
3. Antitransformada: $$\( y(t) = 2e^{-t} - e^{-2t} \).$$  

📚 **Ejercicio 2:** Resolver $$\( y' + y = \sin(t) \) $$ con $$ \( y(0) = 0 \).$$  
**Solución:**  
1. $$\( Y(s) = \frac{1}{(s+1)(s^2 + 1)} \).$$  
2. Descomposición: $$ \( Y(s) = \frac{A}{s+1} + \frac{Bs + C}{s^2 + 1} \) $$.
3. Solución: $$\( y(t) = \frac{e^{-t}}{2} - \frac{\cos(t) + \sin(t)}{2} \). $$ 

---

## 5. Conclusiones  
- El método de Laplace simplifica la resolución de ecuaciones diferenciales lineales.  
- Es especialmente útil para sistemas con condiciones iniciales y entradas discontinuas.  

## 6. Referencias  
1. Ogata, K. (1978). *DINAMICA DE SISTEMAS*. Prentice.  
2. Zill, D. (2018). *Ecuaciones Diferenciales con Aplicaciones*. Cengage.  
