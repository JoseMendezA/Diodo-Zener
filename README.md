# Diodo-Zener
Obtención de la curva característica del diodo zener

Para desarrollar el taller sobre la obtención de la curva característica del diodo Zener, realizaremos los cálculos analíticos necesarios para determinar el valor de \( V_i \) y la corriente \( I_{Zmn} \) siguiendo estos pasos:

### Paso 1: Análisis del circuito
El circuito dado incluye una fuente de voltaje \( V_i \), una resistencia en serie \( R \), una carga \( R_L \), y un diodo Zener con voltaje de ruptura \( V_z \) y potencia máxima \( P_{Zmax} \).

### Paso 2: Cálculo del voltaje de entrada \( V_i \) mínimo para operación Zener
1. **Condición para la operación Zener**: Para que el diodo Zener opere en la zona de regulación, el voltaje a través del diodo debe ser igual a \( V_z \). Esto implica que el voltaje a través de la carga debe ser también \( V_z \) (ya que el diodo está en paralelo con \( R_L \)).

2. **Ley de Ohm en la resistencia**: La corriente a través de la resistencia \( R \) es:
   \[ I_R = \frac{V_i - V_z}{R} \]

3. **Corriente a través de \( R_L \)**: La corriente a través de la carga \( R_L \) es:
   \[ I_L = \frac{V_z}{R_L} \]

4. **Corriente del diodo Zener \( I_Z \)**: Usando la ley de corriente de Kirchhoff en el nodo del diodo Zener:
   \[ I_Z = I_R - I_L \]

5. **Condición de potencia máxima**: La potencia disipada en el diodo Zener no debe exceder \( P_{Zmax} \):
   \[ P_Z = V_z \times I_Z \leq P_{Zmax} \]
   Despejando \( I_Z \), tenemos:
   \[ I_Z \leq \frac{P_{Zmax}}{V_z} \]

6. **Cálculo del \( V_i \) mínimo**: Sustituyendo \( I_Z \) en términos de \( I_R \) y \( I_L \):
   \[ \frac{V_i - V_z}{R} - \frac{V_z}{R_L} \leq \frac{P_{Zmax}}{V_z} \]
   Simplificando para \( V_i \):
   \[ V_i \geq V_z + R \left( \frac{P_{Zmax}}{V_z} + \frac{V_z}{R_L} \right) \]

### Paso 3: Cálculo de la corriente \( I_{Zmn} \)
1. La corriente \( I_{Zmn} \) es la corriente mínima requerida por el diodo Zener para entrar en la zona de regulación:
   \[ I_{Zmn} = I_Z \text{ (mínima)} \]

2. Dado que la corriente a través del Zener debe ser suficiente para que el diodo empiece a regular el voltaje, podemos tomar el caso límite cuando \( I_Z \) es igual a:
   \[ I_{Zmn} = \frac{P_{Zmax}}{V_z} \]

### Paso 4: Ejemplo con valores dados
1. **Valores específicos**: 
   - \( R = 1 \, \text{k}\Omega \)
   - \( R_L = 10 \, \text{k}\Omega \)
   - \( V_z = 10 \, \text{V} \)
   - \( P_{Zmax} = 0.5 \, \text{W} \)

2. **Cálculo de \( V_i \)**:
   \[ V_i \geq 10 \, \text{V} + 1000 \, \Omega \left( \frac{0.5 \, \text{W}}{10 \, \text{V}} + \frac{10 \, \text{V}}{10000 \, \Omega} \right) \]
   \[ V_i \geq 10 \, \text{V} + 1000 \, \Omega \left( 0.05 \, \text{A} + 0.001 \, \text{A} \right) \]
   \[ V_i \geq 10 \, \text{V} + 1000 \, \Omega \times 0.051 \, \text{A} \]
   \[ V_i \geq 10 \, \text{V} + 51 \, \text{V} \]
   \[ V_i \geq 15.1 \, \text{V} \]

3. **Cálculo de \( I_{Zmn} \)**:
   \[ I_{Zmn} = \frac{0.5 \, \text{W}}{10 \, \text{V}} = 0.05 \, \text{A} \]

Este análisis provee los pasos para determinar experimentalmente la curva característica del diodo Zener y establecer los valores de operación segura dentro del circuito.
