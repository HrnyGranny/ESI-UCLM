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

![Screenshot_20240123_185012](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/82efb864-d7c0-42f3-8e6e-60b3b949c9aa)



### Dynamic power

* K = Constante de proporcionalidad
* CL = Carga capacitiva
* V = Voltage
* F = frecuencia
* N = Número de tansistores (2 cores con el mismo num de transistores --> 2N)

Pdyn = k x CL x V^2 x F x N

---------

![Screenshot_20240123_185035](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/8992b51d-1c15-472f-8cf4-f00c68d6eee2)

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
* TIENES QUE ESTAR EN DIFF INTERACIONES NO VALE EN LA MISMA
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

![Screenshot_20240115_162446](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/d5dc70db-6d29-4fe1-8e66-b0ede0bb8281)


### Warrens algorithm

CUIDAO con el ETT q no deja usar hasta q pase X time si hay q dejar huecos se dejan

![Screenshot_20240115_162600](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/eca92a56-6a9d-43e3-b075-383b9496d6f8)
![Screenshot_20240115_162640](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/f866e81b-b8c8-485f-934a-9b8c7f4f6917)


### Tomasulo

![Screenshot_20240115_193759](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/aea9e13c-c3d1-46a2-9cf3-bbc0e027248a)
![Screenshot_20240115_194106](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/874a1251-8dc2-4971-bdbc-27df12290255)

## TEMA 4

* El flush --> se realiza cuando una caché tiene el bloque modificado y otra solicita leer o escribir ese mismo dato. Como la memoria no tiene el dato (para no generar tráfico en el bus) se envía el dato a memoria y se actualiza el bloque.

    * I I M I ---> I M I I
    * I I M I ---> I I S S
    * I I S I ---> I M I I
    * I I S I ---> I I S S
      

* BusUPG --> Cuando modificas un cache Shared (es decir haces un hit)
