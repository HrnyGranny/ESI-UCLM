# PART 2

## Genetic algorithm

## Restrictions

* Variables 
* Dominio asociado a cada variable de posibles valores
* Restricciones entre variables (Unary, Binary, higher order >= 3)
* Solucion de un valor a cada variable que satisface todas las restricciones --> Mundos posibles

### Solucion

* Generate and test algorithm --> generas y testeas
* Backtracking --> Vas para atrás
* Forward Checking --> Hacer un seguimiento de los valores legales restantes para variables no asignadas. Terminar la búsqueda cuando alguna variable tiene valores no legales

#### get before to the solution

* MRV = Variable que menos valores pueda tener
* Degree = Variable con el mayor numero de restricciones (EMPATE --> MRV)
* Least constraing value = Variable que menos restriccione tiene

### Constraint graph

![Screenshot_20240605_195725](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/28f9d12b-b188-4189-aaa9-238a557c4138)

## MinMax


![Screenshot_20240605_204422](https://github.com/HrnyGranny/ESI-UCLM/assets/91948162/b3995602-b9fb-41a0-96be-1fb646d728a6)



