# PARCIAL 1 - 20%

Tema 1 - 2 - 3 (Punto 1 y 2)

## Tipo test

## Ejercicios de busqueda

| <!-- -->      | <!-- -->        | <!-- -->      |
|:-------------:|:---------------:|:-------------:|
| ID     |       | VALUE        |                             
|          | STATE       |        |
| DEPTH         | COST      | HEURISTIC       |

STATE : HEURISTIC : X

### Uninformed search alorithms
Just the info available in the problem dedinition. Heuristic don't care.

![SumUp](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/5a29d8b6-85fe-4092-8bb6-a1ad40224dd5)

#### Breath first search (BFS)
* Vas abriendo todo siguiendo el orden del DEPTH (En el nivel en el que estes de izq a derecha)
* CUT: Cuando tengas un nodo que ya has abierto con posterioridad
* VALUE = DEPTH

![BFS](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/199c8671-b79f-4527-a615-51fdf0e4deb1)

#### Uniform cost search
* Vas abriendo todo siguiendo el orden del COST (Abres el que tenga en el menor COST | Si el coste es igual abres de izq a derecha como en BFS)
* CUT: Cuando tengas un nodo que ya has abierto con posteriodidad
* VALUE = COST

#### Depth first search (DFS)
* Vas abriendo hasta el final de cada bifurcación, cuando terminas con esa pasas a la del nivel mas alto anterior 
* CUT: Cuando tengas un nodo que ya has abierto con posteriodidad, normalmente conforme vas acabando el ultimo nivel son todos CUT
* VALUE = Segun el nivel 1.00 - 0.50 - 0.33 - 0.25 - 0.20 - 0.17 - 0.14

![DFS](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/809a4d38-6fae-4a8c-810f-d2140d4c0e13)

#### Depth limited search
* Igual q DFS pero con limites por dnd no bajar mas
#### Interattive deepening search
* Vas haciendo DFS en los distintos niveles y bajas (Para no bajar hasta abajo del tiron)

### Informed search algorithms
Heuristic functions.

h(n) : Estimate a cost from n to the closest goal

#### Greedy best-first search
* Vas abriendo en funcion de la q menos heuristica tenga 
* CUT:
* VALUE = HEURISTICS

#### A*
* Vas abriendo en funcion del VALUE | Si el coste es igual abres de izq a derecha como en BFS
* CUT: 
* VALUE = COST + HEURISTICS

## Ejercicio de estados

* Variables: Factores relevantes a tener en cuenta q marcaran las caracteristicas de un estado (State = (Variable,variable,...))
* State Space (State + Sucessor function)
* Initial Space
* Goal function



