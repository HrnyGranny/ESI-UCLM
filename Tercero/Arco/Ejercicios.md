# Ejercicios ARCO

## TEMA 1

### CPU performance

* Total number of clock cicles = CC
* Intrucciones per clicle = CPI
* Instructions executed = IC
* Frecuenci = F

TCPU = CC x T = TCPU = CC / F

TCPU = IC x CPI x T

### CPU performance with a program (% paralelized)

* Parallelism = P (%-->0.0)
* Number of cores = C
* Frecuenci = F
* Total number of clock cicles = CC

Tp = (1-P + P/C) x TCPU = (1-P + P/C) x CC / F

--------------
* Rendimiento realtivo de CPU1 respecto de CPU2 / Cuanto mas rapida --> TCPU2 / TCPU1
* Comparar frecuencias --> TCPU1 = TCPU2 y despejas F

### Dynamic power

* K = Constante de proporcionalidad
* CL = Carga capacitiva
* V = Voltage
* F = frecuencia
* N = Número de tansistores (2 cores con el mismo num de transistores --> 2N)

Pdyn = k x CL x V^2 x F x N

---------
* Potencia dimanima de CPU1 respecto de CPU2 --> Pdyn2 / Pdyn1 || (V / F / N) ---> CAMBIA

### Energy 

* K = Constante de proporcionalidad
* CL = Carga capacitiva
* V = Voltage
* IC = Instructions executed

Edyn = k x CL x V^2 

Si el IC es activado en un tiempo t --> EdynIC = PdynIC x t     ----    t=CC/F (CC: cycle count)    --->    EdynIC = k x CL x V2 x CC x N

### Speed / cost

Speedup = 1/(1-P + P/C)

Speedup/cost = Gx/Cx

## TEMA 2

### Inter / Intra-loop

* Intra loop / same interaction --> Los que son iguales y estan en distintos loops 
* loop carried / between interactions --> Se dan cuando ha acabado la interación (A la sig vuelta del bucle) entre i+1 y un i
* AMBOS TIENEN QUE ESTAR UNO DELANTE DEL = Y OTRO DESPUES
* RAW / WAR / WAW

![Screenshot_20240111_142702](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/4dbf686d-f950-482b-854a-be148770a4f9)

### AI

AI = Operations / Operations in memory x Bytes = Flops/Bytes

* Operations = + / - / x / %

* Operations in memory = Load / store

### Maximum performance value

* Maximum performance (GFLOP/s)
* Maximum performance (GFLOP)
* AI optimal point 
* AI
* Limit AI = Optimal point AI

#### Code

BW = Maximum performance (GFLOP/s) /  AI optimal point

BW = Maximum performance (GFLOP) x AI /  AI optimal point

Max Performance = BW x AI

#### Kernel

* AI optimal point = Limit AI / AI

Max Performance = Maximum performance (GFLOP/s) / AI optimal point

--------------------

* Memmory bound --> Max Performance far from current Max performance (Calculated)

### Roofline diagram

*  
* 

## TEMA 3

### DAG

### Warrens algorithm



