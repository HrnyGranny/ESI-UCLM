# Ejercicios ARCO
 
## Fórmulas

* Energía consumida por 1 Transistor --> Edyn = k x CL x V^2 
* Poder consumido por 1 transistor -->  Pdyn = k x CL x V^2 x F (Si hay N transistores se multiplica por el num de transistores)
* Si hay N transistores el poder sera --> PdynIC = Pdyn x N
* Si el IC es activado en un tiempo t --> EdynIC = PdynIC x t     ----    t=CC/F (CC: cycle count)    --->    EdynIC = k x CL x V2 x CC x N
* Poder estático --> Pst ∝ Cst x V
* Execution time --> TCPU = CC x T = IC x CPI x T = IC x CPI / F

### Leyenda

* K = Constante de proporcionalidad
* CL = Carga capacitiva
* V = Voltage
* F = frecuencia
* N = Número de tanssitores

-------------------------------

## CPU performance

* Parallelism = P (%-->0.0)
* Number of cores = C
* Frecuenci = F
* Total number of clock cicles = CC

TCPU = CC x T = TCPU = CC / F
TCPU = (1-P + P/C) x CC / F

--------------
* Rendimiento realtivo de CPU1 respecto de CPU2 --> TCPU2 / TCPU1
* Comparar frecuencias --> TCPU1 = TCPU2 y despejas F

## Dynamic power

* K = Constante de proporcionalidad
* CL = Carga capacitiva
* V = Voltage
* F = frecuencia
* N = Número de tansistores (2 cores con el mismo num de transistores --> 2N)

Pdyn = k x CL x V^2 x F x N

---------
* Potencia dimanima de CPU1 respecto de CPU2 --> Pdyn2 / Pdyn1 || (V / F / N) ---> CAMBIA
* 
