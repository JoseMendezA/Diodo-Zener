# Diodo-Zener
Obtención de la curva característica del diodo zener

# Práctica 4: Obtención de la Curva Característica del Diodo Zener

## 1. Objetivos

- Obtener experimentalmente la curva característica de operación del diodo Zener.
- Identificar experimentalmente las diferentes zonas de operación del diodo Zener.

## 2. Metodología

### a. Análisis del Circuito Electrónico

![image](https://github.com/user-attachments/assets/db5f87dc-2097-4593-b9c3-6340ca2a6e33)


Para el circuito electrónico dado, donde:

- $\( R = 1 \, \text{k}\Omega \)$
- $\( R_L = 10 \, \text{k}\Omega \)$
- $\( V_z = 10 \, \text{V} \)$
- $\( P_{Zmax} = 0.5 \, \text{W} \)$

Realizaremos los siguientes cálculos para determinar el valor de $\( V_i \)$ y la corriente $\( I_{Zmn} \)$:

### Paso 1: Análisis del Circuito

El circuito incluye una fuente de voltaje $\( V_i \)$, una resistencia en serie $\( R \)$, una carga $\( R_L \)$, y un diodo Zener con voltaje de ruptura $\( V_z \)$ y potencia máxima $\( P_{Zmax} \)$.

### Paso 2: Cálculo del Voltaje de Entrada $\( V_i \)$ Mínimo para Operación Zener

1. **Condición para la Operación Zener**: Para que el diodo Zener opere en la zona de regulación, el voltaje a través del diodo debe ser igual a $\( V_z \)$. Esto implica que el voltaje a través de la carga también debe ser $\( V_z \)$ (ya que el diodo está en paralelo con $\( R_L \))$.

2. **Ley de Ohm en la Resistencia**: La corriente a través de la resistencia $\( R \)$ es:
   
```math
I_R = \frac{V_i - V_z}{R}
```

3. **Corriente a través de \( R_L \)**: La corriente a través de la carga $\( R_L \)$ es:
  ```math
   I_L = \frac{V_z}{R_L}
   ```

4. **Corriente del Diodo Zener $\( I_Z \)$**: Usando la ley de corriente de Kirchhoff en el nodo del diodo Zener:
  ```math
   I_Z = I_R - I_L
   ```

5. **Condición de Potencia Máxima**: La potencia disipada en el diodo Zener no debe exceder $\( P_{Zmax} \)$:

      $$P_Z = V_Z \cdot I_Z \leq P_{Zmax}$$

   
   Despejando $\( I_Z \)$:
   $$I_Z \leq \frac{P_{Zmax}}{V_z}$$

7. **Cálculo del $\( V_i \)$ Mínimo**: Sustituyendo $\( I_Z \)$ en términos de $\( I_R \)$ y $\( I_L \)$:
  
   $$\frac{V_i - V_z}{R} - \frac{V_z}{R_L} \leq \frac{P_{Zmax}}{V_z}$$
  
   Simplificando para $\( V_i \)$:
  
   $$V_i \geq V_z + R \left( \frac{P_{Zmax}}{V_z} + \frac{V_z}{R_L} \right)$$
   

### Paso 3: Cálculo de la Corriente $\( I_{Zmn} \)$

1. La corriente $\( I_{Zmn} \)$ es la corriente mínima requerida por el diodo Zener para entrar en la zona de regulación:
   
   $$I_{Zmn} = I_Z \text{ (mínima)}$$
   

2. Dado que la corriente a través del Zener debe ser suficiente para que el diodo empiece a regular el voltaje, podemos tomar el caso límite cuando $\( I_Z \)$ es igual a:
  ```math
   I_{Zmn} = \frac{P_{Zmax}}{V_z}
  ```

### Paso 4: Ejemplo con Valores Dados

1. **Valores Específicos**:
   - $\( R = 1 \, \text{k}\Omega \)$
   - $\( R_L = 10 \, \text{k}\Omega \)$
   - $\( V_z = 10 \, \text{V} \)$
   - $\( P_{Zmax} = 0.5 \, \text{W} \)$

2. **Cálculo de $\( V_i \)$**:
- $$V_i \geq 10 \ \text{V} + 1000 \ \Omega \left( \frac{0.5 \, \text{W}}{10 \ \text{V}} + \frac{10 \ \text{V}}{10000 \ \Omega} \right)$$
   
- $$V_i \geq 10 \, \text{V} + 1000 \, \Omega \left( 0.05 \, \text{A} + 0.001 \, \text{A} \right)$$
  
- $$V_i \geq 10 \, \text{V} + 51 \, \text{V}$$
   
- $$V_i \geq 15.1 \, \text{V}$$
   

3. **Cálculo de $\( I_{Zmn} \)$**:
  - $$I_{Zmn} = \frac{0.5 \, \text{W}}{10 \, \text{V}} = 0.05 \, \text{A}$$

Este análisis provee los pasos para determinar experimentalmente la curva característica del diodo Zener y establecer los valores de operación segura dentro del circuito.
```
